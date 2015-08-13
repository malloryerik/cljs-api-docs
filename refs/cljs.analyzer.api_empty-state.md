## cljs.analyzer.api/empty-state



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/1.7.10"><img valign="middle" alt="[+] 1.7.10" title="Added in 1.7.10" src="https://img.shields.io/badge/+-1.7.10-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__empty-state__)<br>
</samp>

---





Source docstring:

```
Creates an empty compilation state Atom<Map>.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r1.7.107/src/main/clojure/cljs/analyzer/api.clj#L20-L23):

```clj
(defn empty-state
  []
  (env/default-compiler-env))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1.7.107
└── src
    └── main
        └── clojure
            └── cljs
                └── analyzer
                    └── <ins>[api.clj:20-23](https://github.com/clojure/clojurescript/blob/r1.7.107/src/main/clojure/cljs/analyzer/api.clj#L20-L23)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.analyzer.api/empty-state` @ crossclj](http://crossclj.info/fun/cljs.analyzer.api/empty-state.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.analyzer.api_empty-state.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.analyzer.api",
 :name "empty-state",
 :signature ["[]"],
 :history [["+" "1.7.10"]],
 :type "function",
 :full-name-encode "cljs.analyzer.api_empty-state",
 :source {:code "(defn empty-state\n  []\n  (env/default-compiler-env))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1.7.107",
          :filename "src/main/clojure/cljs/analyzer/api.clj",
          :lines [20 23]},
 :full-name "cljs.analyzer.api/empty-state",
 :docstring "Creates an empty compilation state Atom<Map>."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.analyzer.api/empty-state"]))
```

-->
