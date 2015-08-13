## cljs.core/js-obj



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__js-obj__ & keyvals)<br>
</samp>

---

Returns a new JavaScript object using the supplied mappings.

`keyvals` must be an even number of forms.

---

###### Examples:

```clj
(js-obj "foo" 1 "bar" 2)
;;=> #js {:foo 1, :bar 2}
```

---

###### See Also:

[`#js literal`](syntax_js-literal.md)<br>
[`cljs.core/array`](cljs.core_array.md)<br>
[`cljs.core/clj->js`](cljs.core_clj-GTjs.md)<br>

---


Source docstring:

```
Create JavaSript object from an even number arguments representing
interleaved keys and values.
```


Function code @ [github](https://github.com/clojure/clojurescript/blob/r1.7.107/src/main/cljs/cljs/core.cljs#L1924-L1930):

```clj
(defn js-obj
  ([]
     (cljs.core/js-obj))
  ([& keyvals]
     (apply gobject/create keyvals)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1.7.107
└── src
    └── main
        └── cljs
            └── cljs
                └── <ins>[core.cljs:1924-1930](https://github.com/clojure/clojurescript/blob/r1.7.107/src/main/cljs/cljs/core.cljs#L1924-L1930)</ins>
</pre>

-->

---

Macro code @ [github](https://github.com/clojure/clojurescript/blob/r1.7.107/src/main/clojure/cljs/core.cljc#L2379-L2397):

```clj
(core/defmacro js-obj [& rest]
  (core/let [sym-or-str? (core/fn [x] (core/or (core/symbol? x) (core/string? x)))
             filter-on-keys (core/fn [f coll]
                              (core/->> coll
                                (filter (core/fn [[k _]] (f k)))
                                (into {})))
             kvs (into {} (map vec (partition 2 rest)))
             sym-pairs (filter-on-keys core/symbol? kvs)
             expr->local (zipmap
                           (filter (complement sym-or-str?) (keys kvs))
                           (repeatedly gensym))
             obj (gensym "obj")]
    (if (empty? rest)
      (js-obj* '())
      `(let [~@(apply concat (clojure.set/map-invert expr->local))
            ~obj ~(js-obj* (filter-on-keys core/string? kvs))]
        ~@(map (core/fn [[k v]] `(aset ~obj ~k ~v)) sym-pairs)
        ~@(map (core/fn [[k v]] `(aset ~obj ~v ~(core/get kvs k))) expr->local)
        ~obj))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1.7.107
└── src
    └── main
        └── clojure
            └── cljs
                └── <ins>[core.cljc:2379-2397](https://github.com/clojure/clojurescript/blob/r1.7.107/src/main/clojure/cljs/core.cljc#L2379-L2397)</ins>
</pre>
-->

---


###### External doc links:

[`cljs.core/js-obj` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/js-obj.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_js-obj.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Returns a new JavaScript object using the supplied mappings.\n\n`keyvals` must be an even number of forms.",
 :ns "cljs.core",
 :name "js-obj",
 :signature ["[& keyvals]"],
 :history [["+" "0.0-927"]],
 :type "function",
 :related ["syntax/js-literal" "cljs.core/array" "cljs.core/clj->js"],
 :full-name-encode "cljs.core_js-obj",
 :source {:code "(defn js-obj\n  ([]\n     (cljs.core/js-obj))\n  ([& keyvals]\n     (apply gobject/create keyvals)))",
          :title "Function code",
          :repo "clojurescript",
          :tag "r1.7.107",
          :filename "src/main/cljs/cljs/core.cljs",
          :lines [1924 1930]},
 :extra-sources [{:code "(core/defmacro js-obj [& rest]\n  (core/let [sym-or-str? (core/fn [x] (core/or (core/symbol? x) (core/string? x)))\n             filter-on-keys (core/fn [f coll]\n                              (core/->> coll\n                                (filter (core/fn [[k _]] (f k)))\n                                (into {})))\n             kvs (into {} (map vec (partition 2 rest)))\n             sym-pairs (filter-on-keys core/symbol? kvs)\n             expr->local (zipmap\n                           (filter (complement sym-or-str?) (keys kvs))\n                           (repeatedly gensym))\n             obj (gensym \"obj\")]\n    (if (empty? rest)\n      (js-obj* '())\n      `(let [~@(apply concat (clojure.set/map-invert expr->local))\n            ~obj ~(js-obj* (filter-on-keys core/string? kvs))]\n        ~@(map (core/fn [[k v]] `(aset ~obj ~k ~v)) sym-pairs)\n        ~@(map (core/fn [[k v]] `(aset ~obj ~v ~(core/get kvs k))) expr->local)\n        ~obj))))",
                  :title "Macro code",
                  :repo "clojurescript",
                  :tag "r1.7.107",
                  :filename "src/main/clojure/cljs/core.cljc",
                  :lines [2379 2397]}],
 :examples [{:id "657cd7",
             :content "```clj\n(js-obj \"foo\" 1 \"bar\" 2)\n;;=> #js {:foo 1, :bar 2}\n```"}],
 :full-name "cljs.core/js-obj",
 :docstring "Create JavaSript object from an even number arguments representing\ninterleaved keys and values."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/js-obj"]))
```

-->
