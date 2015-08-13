## cljs.core/import-macros



 <table border="1">
<tr>
<td>macro</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__import-macros__ ns \[& vars\])<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r2134/src/clj/cljs/core.clj#L43-L50):

```clj
(defmacro import-macros [ns [& vars]]
  (core/let [ns (find-ns ns)
             vars (map #(ns-resolve ns %) vars)
             syms (map (core/fn [^clojure.lang.Var v] (core/-> v .sym (with-meta {:macro true}))) vars)
             defs (map (core/fn [sym var]
                                `(def ~sym (deref ~var))) syms vars)]
            `(do ~@defs
                 :imported)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2134
└── src
    └── clj
        └── cljs
            └── <ins>[core.clj:43-50](https://github.com/clojure/clojurescript/blob/r2134/src/clj/cljs/core.clj#L43-L50)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/import-macros` @ crossclj](http://crossclj.info/fun/cljs.core/import-macros.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_import-macros.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "import-macros",
 :type "macro",
 :signature ["[ns [& vars]]"],
 :source {:code "(defmacro import-macros [ns [& vars]]\n  (core/let [ns (find-ns ns)\n             vars (map #(ns-resolve ns %) vars)\n             syms (map (core/fn [^clojure.lang.Var v] (core/-> v .sym (with-meta {:macro true}))) vars)\n             defs (map (core/fn [sym var]\n                                `(def ~sym (deref ~var))) syms vars)]\n            `(do ~@defs\n                 :imported)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2134",
          :filename "src/clj/cljs/core.clj",
          :lines [43 50]},
 :full-name "cljs.core/import-macros",
 :full-name-encode "cljs.core_import-macros",
 :history [["+" "0.0-927"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/import-macros"]))
```

-->
