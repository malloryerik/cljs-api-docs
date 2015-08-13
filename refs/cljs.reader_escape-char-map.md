## cljs.reader/escape-char-map



 <table border="1">
<tr>
<td>var</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>









Source code @ [github](https://github.com/clojure/clojurescript/blob/r927/src/cljs/cljs/reader.cljs#L137-L143):

```clj
(def escape-char-map {\t "\t"
                      \r "\r"
                      \n "\n"
                      \\ \\
                      \" \"
                      \b "\b"
                      \f "\f"})
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r927
└── src
    └── cljs
        └── cljs
            └── <ins>[reader.cljs:137-143](https://github.com/clojure/clojurescript/blob/r927/src/cljs/cljs/reader.cljs#L137-L143)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.reader/escape-char-map` @ crossclj](http://crossclj.info/fun/cljs.reader.cljs/escape-char-map.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.reader_escape-char-map.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.reader",
 :name "escape-char-map",
 :type "var",
 :source {:code "(def escape-char-map {\\t \"\\t\"\n                      \\r \"\\r\"\n                      \\n \"\\n\"\n                      \\\\ \\\\\n                      \\\" \\\"\n                      \\b \"\\b\"\n                      \\f \"\\f\"})",
          :title "Source code",
          :repo "clojurescript",
          :tag "r927",
          :filename "src/cljs/cljs/reader.cljs",
          :lines [137 143]},
 :full-name "cljs.reader/escape-char-map",
 :full-name-encode "cljs.reader_escape-char-map",
 :history [["+" "0.0-927"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.reader/escape-char-map"]))
```

-->
