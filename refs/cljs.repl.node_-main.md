## cljs.repl.node/-main



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-3165"><img valign="middle" alt="[+] 0.0-3165" title="Added in 0.0-3165" src="https://img.shields.io/badge/+-0.0--3165-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__-main__)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r3297/src/main/clojure/cljs/repl/node.clj#L221-L222):

```clj
(defn -main []
  (repl/repl (repl-env)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3297
└── src
    └── main
        └── clojure
            └── cljs
                └── repl
                    └── <ins>[node.clj:221-222](https://github.com/clojure/clojurescript/blob/r3297/src/main/clojure/cljs/repl/node.clj#L221-L222)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.repl.node/-main` @ crossclj](http://crossclj.info/fun/cljs.repl.node/-main.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.repl.node_-main.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.repl.node",
 :name "-main",
 :type "function",
 :signature ["[]"],
 :source {:code "(defn -main []\n  (repl/repl (repl-env)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r3297",
          :filename "src/main/clojure/cljs/repl/node.clj",
          :lines [221 222]},
 :full-name "cljs.repl.node/-main",
 :full-name-encode "cljs.repl.node_-main",
 :history [["+" "0.0-3165"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.repl.node/-main"]))
```

-->
