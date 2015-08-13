## cljs.analyzer.api/resolve



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-2496"><img valign="middle" alt="[+] 0.0-2496" title="Added in 0.0-2496" src="https://img.shields.io/badge/+-0.0--2496-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/resolve</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/resolve)
</td>
</tr>
</table>


 <samp>
(__resolve__ env sym)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r2498/src/clj/cljs/analyzer/api.clj#L14-L15):

```clj
(defn resolve [env sym]
  (ana/resolve-var env sym))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2498
└── src
    └── clj
        └── cljs
            └── analyzer
                └── <ins>[api.clj:14-15](https://github.com/clojure/clojurescript/blob/r2498/src/clj/cljs/analyzer/api.clj#L14-L15)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/resolve` @ clojuredocs](http://clojuredocs.org/clojure.core/resolve)<br>
[`clojure.core/resolve` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/resolve/)<br>
[`clojure.core/resolve` @ crossclj](http://crossclj.info/fun/clojure.core/resolve.html)<br>
[`cljs.analyzer.api/resolve` @ crossclj](http://crossclj.info/fun/cljs.analyzer.api/resolve.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.analyzer.api_resolve.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.analyzer.api",
 :name "resolve",
 :signature ["[env sym]"],
 :history [["+" "0.0-2496"]],
 :type "function",
 :full-name-encode "cljs.analyzer.api_resolve",
 :source {:code "(defn resolve [env sym]\n  (ana/resolve-var env sym))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2498",
          :filename "src/clj/cljs/analyzer/api.clj",
          :lines [14 15]},
 :full-name "cljs.analyzer.api/resolve",
 :clj-symbol "clojure.core/resolve"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.analyzer.api/resolve"]))
```

-->
