## cljs.analyzer.api/with-state



 <table border="1">
<tr>
<td>macro</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/1.7.10"><img valign="middle" alt="[+] 1.7.10" title="Added in 1.7.10" src="https://img.shields.io/badge/+-1.7.10-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__with-state__ state body)<br>
</samp>

---





Source docstring:

```
Run the body with the given compilation state Atom<Map>.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r1.7.58/src/main/clojure/cljs/analyzer/api.clj#L25-L29):

```clj
(defmacro with-state
  [state body]
  `(env/with-compiler-env ~state
     ~@body))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1.7.58
└── src
    └── main
        └── clojure
            └── cljs
                └── analyzer
                    └── <ins>[api.clj:25-29](https://github.com/clojure/clojurescript/blob/r1.7.58/src/main/clojure/cljs/analyzer/api.clj#L25-L29)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.analyzer.api/with-state` @ crossclj](http://crossclj.info/fun/cljs.analyzer.api/with-state.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.analyzer.api_with-state.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.analyzer.api",
 :name "with-state",
 :signature ["[state body]"],
 :history [["+" "1.7.10"]],
 :type "macro",
 :full-name-encode "cljs.analyzer.api_with-state",
 :source {:code "(defmacro with-state\n  [state body]\n  `(env/with-compiler-env ~state\n     ~@body))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1.7.58",
          :filename "src/main/clojure/cljs/analyzer/api.clj",
          :lines [25 29]},
 :full-name "cljs.analyzer.api/with-state",
 :docstring "Run the body with the given compilation state Atom<Map>."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.analyzer.api/with-state"]))
```

-->
