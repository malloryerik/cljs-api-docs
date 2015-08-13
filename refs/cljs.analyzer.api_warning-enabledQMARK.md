## cljs.analyzer.api/warning-enabled?



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/1.7.10"><img valign="middle" alt="[+] 1.7.10" title="Added in 1.7.10" src="https://img.shields.io/badge/+-1.7.10-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__warning-enabled?__ warning-type)<br>
</samp>

---





Source docstring:

```
Test if the given warning-type is enabled.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r1.7.58/src/main/clojure/cljs/analyzer/api.clj#L43-L46):

```clj
(defn warning-enabled?
  [warning-type]
  (ana/*cljs-warnings* warning-type))
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
                    └── <ins>[api.clj:43-46](https://github.com/clojure/clojurescript/blob/r1.7.58/src/main/clojure/cljs/analyzer/api.clj#L43-L46)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.analyzer.api/warning-enabled?` @ crossclj](http://crossclj.info/fun/cljs.analyzer.api/warning-enabled%3F.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.analyzer.api_warning-enabledQMARK.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.analyzer.api",
 :name "warning-enabled?",
 :signature ["[warning-type]"],
 :history [["+" "1.7.10"]],
 :type "function",
 :full-name-encode "cljs.analyzer.api_warning-enabledQMARK",
 :source {:code "(defn warning-enabled?\n  [warning-type]\n  (ana/*cljs-warnings* warning-type))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1.7.58",
          :filename "src/main/clojure/cljs/analyzer/api.clj",
          :lines [43 46]},
 :full-name "cljs.analyzer.api/warning-enabled?",
 :docstring "Test if the given warning-type is enabled."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.analyzer.api/warning-enabled?"]))
```

-->
