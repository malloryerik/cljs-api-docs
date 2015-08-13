## cljs.repl.node/platform-path



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-2814"><img valign="middle" alt="[+] 0.0-2814" title="Added in 0.0-2814" src="https://img.shields.io/badge/+-0.0--2814-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__platform-path__ v)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r3030/src/clj/cljs/repl/node.clj#L77-L78):

```clj
(defn platform-path [v]
  (str "path.join.apply(null, " (seq->js-array v) ")"))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3030
└── src
    └── clj
        └── cljs
            └── repl
                └── <ins>[node.clj:77-78](https://github.com/clojure/clojurescript/blob/r3030/src/clj/cljs/repl/node.clj#L77-L78)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.repl.node/platform-path` @ crossclj](http://crossclj.info/fun/cljs.repl.node/platform-path.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.repl.node_platform-path.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.repl.node",
 :name "platform-path",
 :type "function",
 :signature ["[v]"],
 :source {:code "(defn platform-path [v]\n  (str \"path.join.apply(null, \" (seq->js-array v) \")\"))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r3030",
          :filename "src/clj/cljs/repl/node.clj",
          :lines [77 78]},
 :full-name "cljs.repl.node/platform-path",
 :full-name-encode "cljs.repl.node_platform-path",
 :history [["+" "0.0-2814"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.repl.node/platform-path"]))
```

-->
