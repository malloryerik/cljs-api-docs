## cljs.reader/read-2-chars



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1424"><img valign="middle" alt="[+] 0.0-1424" title="Added in 0.0-1424" src="https://img.shields.io/badge/+-0.0--1424-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__read-2-chars__ reader)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r2199/src/cljs/cljs/reader.cljs#L173-L177):

```clj
(defn read-2-chars [reader]
  (.toString
    (gstring/StringBuffer.
      (read-char reader)
      (read-char reader))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2199
└── src
    └── cljs
        └── cljs
            └── <ins>[reader.cljs:173-177](https://github.com/clojure/clojurescript/blob/r2199/src/cljs/cljs/reader.cljs#L173-L177)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.reader/read-2-chars` @ crossclj](http://crossclj.info/fun/cljs.reader.cljs/read-2-chars.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.reader_read-2-chars.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.reader",
 :name "read-2-chars",
 :type "function",
 :signature ["[reader]"],
 :source {:code "(defn read-2-chars [reader]\n  (.toString\n    (gstring/StringBuffer.\n      (read-char reader)\n      (read-char reader))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2199",
          :filename "src/cljs/cljs/reader.cljs",
          :lines [173 177]},
 :full-name "cljs.reader/read-2-chars",
 :full-name-encode "cljs.reader_read-2-chars",
 :history [["+" "0.0-1424"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.reader/read-2-chars"]))
```

-->
