## cljs.analyzer.api/find-ns



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-2496"><img valign="middle" alt="[+] 0.0-2496" title="Added in 0.0-2496" src="https://img.shields.io/badge/+-0.0--2496-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/find-ns</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/find-ns)
</td>
</tr>
</table>


 <samp>
(__find-ns__ sym)<br>
</samp>
 <samp>
(__find-ns__ state sym)<br>
</samp>

---





Source docstring:

```
Given a namespace return the corresponding namespace analysis map. Analagous
to clojure.core/find-ns.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r1.7.48/src/main/clojure/cljs/analyzer/api.clj#L153-L160):

```clj
(defn find-ns
  ([sym]
   (find-ns env/*compiler* sym))
  ([state sym]
   {:pre [(symbol? sym)]}
   (get-in @state [::ana/namespaces sym])))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1.7.48
└── src
    └── main
        └── clojure
            └── cljs
                └── analyzer
                    └── <ins>[api.clj:153-160](https://github.com/clojure/clojurescript/blob/r1.7.48/src/main/clojure/cljs/analyzer/api.clj#L153-L160)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/find-ns` @ clojuredocs](http://clojuredocs.org/clojure.core/find-ns)<br>
[`clojure.core/find-ns` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/find-ns/)<br>
[`clojure.core/find-ns` @ crossclj](http://crossclj.info/fun/clojure.core/find-ns.html)<br>
[`cljs.analyzer.api/find-ns` @ crossclj](http://crossclj.info/fun/cljs.analyzer.api/find-ns.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.analyzer.api_find-ns.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.analyzer.api",
 :name "find-ns",
 :signature ["[sym]" "[state sym]"],
 :history [["+" "0.0-2496"]],
 :type "function",
 :full-name-encode "cljs.analyzer.api_find-ns",
 :source {:code "(defn find-ns\n  ([sym]\n   (find-ns env/*compiler* sym))\n  ([state sym]\n   {:pre [(symbol? sym)]}\n   (get-in @state [::ana/namespaces sym])))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1.7.48",
          :filename "src/main/clojure/cljs/analyzer/api.clj",
          :lines [153 160]},
 :full-name "cljs.analyzer.api/find-ns",
 :clj-symbol "clojure.core/find-ns",
 :docstring "Given a namespace return the corresponding namespace analysis map. Analagous\nto clojure.core/find-ns."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.analyzer.api/find-ns"]))
```

-->
