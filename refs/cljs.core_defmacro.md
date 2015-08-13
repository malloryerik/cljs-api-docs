## cljs.core/defmacro



 <table border="1">
<tr>
<td>macro</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/defmacro</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/defmacro)
</td>
</tr>
</table>


 <samp>
(__defmacro__ &form &env name & args)<br>
</samp>

---





Source docstring:

```
Like defn, but the resulting function name is declared as a
macro and will be used as a macro by the compiler when it is
called.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r1.7.10/src/main/clojure/cljs/core.cljc#L2788-L2829):

```clj
(core/defn defmacro
  [&form &env name & args]
  (core/let [prefix (core/loop [p (core/list (vary-meta name assoc :macro true)) args args]
                      (core/let [f (first args)]
                        (if (core/string? f)
                          (recur (cons f p) (next args))
                          (if (map? f)
                            (recur (cons f p) (next args))
                            p))))
             fdecl (core/loop [fd args]
                     (if (core/string? (first fd))
                       (recur (next fd))
                       (if (map? (first fd))
                         (recur (next fd))
                         fd)))
             fdecl (if (vector? (first fdecl))
                     (core/list fdecl)
                     fdecl)
             add-implicit-args (core/fn [fd]
                                 (core/let [args (first fd)]
                                   (cons (vec (cons '&form (cons '&env args))) (next fd))))
             add-args (core/fn [acc ds]
                        (if (core/nil? ds)
                          acc
                          (core/let [d (first ds)]
                            (if (map? d)
                              (conj acc d)
                              (recur (conj acc (add-implicit-args d)) (next ds))))))
             fdecl (seq (add-args [] fdecl))
             decl (core/loop [p prefix d fdecl]
                    (if p
                      (recur (next p) (cons (first p) d))
                      d))]
    (core/list 'do
      (cons `defn decl)
      (core/list 'set! `(. ~name ~'-cljs$lang$macro) true))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1.7.10
└── src
    └── main
        └── clojure
            └── cljs
                └── <ins>[core.cljc:2788-2829](https://github.com/clojure/clojurescript/blob/r1.7.10/src/main/clojure/cljs/core.cljc#L2788-L2829)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/defmacro` @ clojuredocs](http://clojuredocs.org/clojure.core/defmacro)<br>
[`clojure.core/defmacro` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/defmacro/)<br>
[`clojure.core/defmacro` @ crossclj](http://crossclj.info/fun/clojure.core/defmacro.html)<br>
[`cljs.core/defmacro` @ crossclj](http://crossclj.info/fun/cljs.core/defmacro.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_defmacro.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "defmacro",
 :signature ["[&form &env name & args]"],
 :history [["+" "0.0-927"]],
 :type "macro",
 :full-name-encode "cljs.core_defmacro",
 :source {:code "(core/defn defmacro\n  [&form &env name & args]\n  (core/let [prefix (core/loop [p (core/list (vary-meta name assoc :macro true)) args args]\n                      (core/let [f (first args)]\n                        (if (core/string? f)\n                          (recur (cons f p) (next args))\n                          (if (map? f)\n                            (recur (cons f p) (next args))\n                            p))))\n             fdecl (core/loop [fd args]\n                     (if (core/string? (first fd))\n                       (recur (next fd))\n                       (if (map? (first fd))\n                         (recur (next fd))\n                         fd)))\n             fdecl (if (vector? (first fdecl))\n                     (core/list fdecl)\n                     fdecl)\n             add-implicit-args (core/fn [fd]\n                                 (core/let [args (first fd)]\n                                   (cons (vec (cons '&form (cons '&env args))) (next fd))))\n             add-args (core/fn [acc ds]\n                        (if (core/nil? ds)\n                          acc\n                          (core/let [d (first ds)]\n                            (if (map? d)\n                              (conj acc d)\n                              (recur (conj acc (add-implicit-args d)) (next ds))))))\n             fdecl (seq (add-args [] fdecl))\n             decl (core/loop [p prefix d fdecl]\n                    (if p\n                      (recur (next p) (cons (first p) d))\n                      d))]\n    (core/list 'do\n      (cons `defn decl)\n      (core/list 'set! `(. ~name ~'-cljs$lang$macro) true))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1.7.10",
          :filename "src/main/clojure/cljs/core.cljc",
          :lines [2788 2829]},
 :full-name "cljs.core/defmacro",
 :clj-symbol "clojure.core/defmacro",
 :docstring "Like defn, but the resulting function name is declared as a\nmacro and will be used as a macro by the compiler when it is\ncalled."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/defmacro"]))
```

-->
