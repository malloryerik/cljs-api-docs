## def

_known as "define"_


 <table border="1">
<tr>
<td>special form</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/def</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/def)
</td>
</tr>
</table>


 <samp>
(__def__ symbol)<br>
</samp>
 <samp>
(__def__ symbol init)<br>
</samp>
 <samp>
(__def__ symbol doc-string init)<br>
</samp>

---

Creates a global variable with the name of `symbol` and a namespace of the
current namespace.

If `init` is supplied, it is evaluated and the result is assigned to `symbol`.

`doc-string` is an optional documentation string.

`def` is one of ClojureScript's [special forms](http://clojure.org/special_forms)
and is used by many macros to define common elements (ie: `defn`, `defmacro`,
etc).

Supported metadata:

- `^:private boolean` - make non-accessible from other namespaces
- `^:dynamic boolean` - make [dynamically bindable](cljs.core_binding.md) (usually named with [`*earmuffs*`](syntax_earmuffs.md))
- `^:const boolean` - prevents redef and allows it to be used in [`case`](cljs.core_case.md).
- `^:jsdoc [""]` - vector of JSDoc Tags for [Google Closure][closure-jsdoc] or [standard][other-jsdoc].
- `^:test (fn [] (assert ...))` - allows function to be tested with [cljs.core/test].
- `^:doc ""` - doc-string (prefer the use of the `(def symbol doc-string init)`)

[closure-jsdoc]:https://developers.google.com/closure/compiler/docs/js-for-compiler?hl=en#tags
[other-jsdoc]:http://usejsdoc.org/#block-tags

Compiler will also add metadata:

- `:ns`
- `:name`
- `:file`
- `:line`, `:end-line`
- `:column`, `:end-column`
- `:source`
- `:arglists`

---

###### Examples:

```clj
(def a)
a
;;=> nil

(def b 42)
b
;;=> 42

(def c "an optional docstring" 42)
c
;;=> 42
```

---

###### See Also:

[`cljs.core/defn`](cljs.core_defn.md)<br>
[`cljs.core/fn`](cljs.core_fn.md)<br>
[`cljs.core/defmacro`](cljs.core_defmacro.md)<br>
[`cljs.core/defmulti`](cljs.core_defmulti.md)<br>

---




Parser code @ [github](https://github.com/clojure/clojurescript/blob/r1586/src/clj/cljs/analyzer.clj#L281-L348):

```clj
(defmethod parse 'def
  [op env form name]
  (let [pfn (fn
              ([_ sym] {:sym sym})
              ([_ sym init] {:sym sym :init init})
              ([_ sym doc init] {:sym sym :doc doc :init init}))
        args (apply pfn form)
        sym (:sym args)
        sym-meta (meta sym)
        tag (-> sym meta :tag)
        protocol (-> sym meta :protocol)
        dynamic (-> sym meta :dynamic)
        ns-name (-> env :ns :name)]
    (assert (not (namespace sym)) "Can't def ns-qualified name")
    (let [env (if (or (and (not= ns-name 'cljs.core)
                           (core-name? env sym))
                      (get-in @namespaces [ns-name :uses sym]))
                (let [ev (resolve-existing-var (dissoc env :locals) sym)]
                  (when *cljs-warn-on-redef*
                    (warning env
                      (str "WARNING: " sym " already refers to: " (symbol (str (:ns ev)) (str sym))
                           " being replaced by: " (symbol (str ns-name) (str sym)))))
                  (swap! namespaces update-in [ns-name :excludes] conj sym)
                  (update-in env [:ns :excludes] conj sym))
                env)
          name (:name (resolve-var (dissoc env :locals) sym))
          init-expr (when (contains? args :init)
                      (disallowing-recur
                       (analyze (assoc env :context :expr) (:init args) sym)))
          fn-var? (and init-expr (= (:op init-expr) :fn))
          export-as (when-let [export-val (-> sym meta :export)]
                      (if (= true export-val) name export-val))
          doc (or (:doc args) (-> sym meta :doc))]
      (when-let [v (get-in @namespaces [ns-name :defs sym])]
        (when (and *cljs-warn-on-fn-var*
                   (not (-> sym meta :declared))
                   (and (:fn-var v) (not fn-var?)))
          (warning env
            (str "WARNING: " (symbol (str ns-name) (str sym))
                 " no longer fn, references are stale"))))
      (swap! namespaces assoc-in [ns-name :defs sym]
                 (merge 
                   {:name name}
                   sym-meta
                   (when doc {:doc doc})
                   (when dynamic {:dynamic true})
                   (source-info env)
                   ;; the protocol a protocol fn belongs to
                   (when protocol
                     {:protocol protocol})
                   ;; symbol for reified protocol
                   (when-let [protocol-symbol (-> sym meta :protocol-symbol)]
                     {:protocol-symbol protocol-symbol})
                   (when fn-var?
                     {:fn-var true
                      ;; protocol implementation context
                      :protocol-impl (:protocol-impl init-expr)
                      ;; inline protocol implementation context
                      :protocol-inline (:protocol-inline init-expr)
                      :variadic (:variadic init-expr)
                      :max-fixed-arity (:max-fixed-arity init-expr)
                      :method-params (map :params (:methods init-expr))})))
      (merge {:env env :op :def :form form
              :name name :doc doc :init init-expr}
             (when tag {:tag tag})
             (when dynamic {:dynamic true})
             (when export-as {:export export-as})
             (when init-expr {:children [init-expr]})))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1586
└── src
    └── clj
        └── cljs
            └── <ins>[analyzer.clj:281-348](https://github.com/clojure/clojurescript/blob/r1586/src/clj/cljs/analyzer.clj#L281-L348)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/def` @ clojuredocs](http://clojuredocs.org/clojure.core/def)<br>
[`clojure.core/def` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/def/)<br>
[`clojure.core/def` @ crossclj](http://crossclj.info/fun/clojure.core/def.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/special_def.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Creates a global variable with the name of `symbol` and a namespace of the\ncurrent namespace.\n\nIf `init` is supplied, it is evaluated and the result is assigned to `symbol`.\n\n`doc-string` is an optional documentation string.\n\n`def` is one of ClojureScript's [special forms](http://clojure.org/special_forms)\nand is used by many macros to define common elements (ie: `defn`, `defmacro`,\netc).\n\nSupported metadata:\n\n- `^:private boolean` - make non-accessible from other namespaces\n- `^:dynamic boolean` - make [dynamically bindable](cljs.core/binding) (usually named with [syntax/earmuffs])\n- `^:const boolean` - prevents redef and allows it to be used in [cljs.core/case].\n- `^:jsdoc [\"\"]` - vector of JSDoc Tags for [Google Closure][closure-jsdoc] or [standard][other-jsdoc].\n- `^:test (fn [] (assert ...))` - allows function to be tested with [cljs.core/test].\n- `^:doc \"\"` - doc-string (prefer the use of the `(def symbol doc-string init)`)\n\n[closure-jsdoc]:https://developers.google.com/closure/compiler/docs/js-for-compiler?hl=en#tags\n[other-jsdoc]:http://usejsdoc.org/#block-tags\n\nCompiler will also add metadata:\n\n- `:ns`\n- `:name`\n- `:file`\n- `:line`, `:end-line`\n- `:column`, `:end-column`\n- `:source`\n- `:arglists`",
 :ns "special",
 :name "def",
 :signature ["[symbol]" "[symbol init]" "[symbol doc-string init]"],
 :history [["+" "0.0-927"]],
 :type "special form",
 :related ["cljs.core/defn"
           "cljs.core/fn"
           "cljs.core/defmacro"
           "cljs.core/defmulti"],
 :full-name-encode "special_def",
 :source {:code "(defmethod parse 'def\n  [op env form name]\n  (let [pfn (fn\n              ([_ sym] {:sym sym})\n              ([_ sym init] {:sym sym :init init})\n              ([_ sym doc init] {:sym sym :doc doc :init init}))\n        args (apply pfn form)\n        sym (:sym args)\n        sym-meta (meta sym)\n        tag (-> sym meta :tag)\n        protocol (-> sym meta :protocol)\n        dynamic (-> sym meta :dynamic)\n        ns-name (-> env :ns :name)]\n    (assert (not (namespace sym)) \"Can't def ns-qualified name\")\n    (let [env (if (or (and (not= ns-name 'cljs.core)\n                           (core-name? env sym))\n                      (get-in @namespaces [ns-name :uses sym]))\n                (let [ev (resolve-existing-var (dissoc env :locals) sym)]\n                  (when *cljs-warn-on-redef*\n                    (warning env\n                      (str \"WARNING: \" sym \" already refers to: \" (symbol (str (:ns ev)) (str sym))\n                           \" being replaced by: \" (symbol (str ns-name) (str sym)))))\n                  (swap! namespaces update-in [ns-name :excludes] conj sym)\n                  (update-in env [:ns :excludes] conj sym))\n                env)\n          name (:name (resolve-var (dissoc env :locals) sym))\n          init-expr (when (contains? args :init)\n                      (disallowing-recur\n                       (analyze (assoc env :context :expr) (:init args) sym)))\n          fn-var? (and init-expr (= (:op init-expr) :fn))\n          export-as (when-let [export-val (-> sym meta :export)]\n                      (if (= true export-val) name export-val))\n          doc (or (:doc args) (-> sym meta :doc))]\n      (when-let [v (get-in @namespaces [ns-name :defs sym])]\n        (when (and *cljs-warn-on-fn-var*\n                   (not (-> sym meta :declared))\n                   (and (:fn-var v) (not fn-var?)))\n          (warning env\n            (str \"WARNING: \" (symbol (str ns-name) (str sym))\n                 \" no longer fn, references are stale\"))))\n      (swap! namespaces assoc-in [ns-name :defs sym]\n                 (merge \n                   {:name name}\n                   sym-meta\n                   (when doc {:doc doc})\n                   (when dynamic {:dynamic true})\n                   (source-info env)\n                   ;; the protocol a protocol fn belongs to\n                   (when protocol\n                     {:protocol protocol})\n                   ;; symbol for reified protocol\n                   (when-let [protocol-symbol (-> sym meta :protocol-symbol)]\n                     {:protocol-symbol protocol-symbol})\n                   (when fn-var?\n                     {:fn-var true\n                      ;; protocol implementation context\n                      :protocol-impl (:protocol-impl init-expr)\n                      ;; inline protocol implementation context\n                      :protocol-inline (:protocol-inline init-expr)\n                      :variadic (:variadic init-expr)\n                      :max-fixed-arity (:max-fixed-arity init-expr)\n                      :method-params (map :params (:methods init-expr))})))\n      (merge {:env env :op :def :form form\n              :name name :doc doc :init init-expr}\n             (when tag {:tag tag})\n             (when dynamic {:dynamic true})\n             (when export-as {:export export-as})\n             (when init-expr {:children [init-expr]})))))",
          :title "Parser code",
          :repo "clojurescript",
          :tag "r1586",
          :filename "src/clj/cljs/analyzer.clj",
          :lines [281 348]},
 :examples [{:id "a5f898",
             :content "```clj\n(def a)\na\n;;=> nil\n\n(def b 42)\nb\n;;=> 42\n\n(def c \"an optional docstring\" 42)\nc\n;;=> 42\n```"}],
 :known-as "define",
 :full-name "special/def",
 :clj-symbol "clojure.core/def"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "special/def"]))
```

-->