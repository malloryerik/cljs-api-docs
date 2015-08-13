## cljs.reader/make-unicode-char



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1424"><img valign="middle" alt="[+] 0.0-1424" title="Added in 0.0-1424" src="https://img.shields.io/badge/+-0.0--1424-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__make-unicode-char__ code-str)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r3297/src/main/cljs/cljs/reader.cljs#L189-L191):

```clj
(defn make-unicode-char [code-str]
    (let [code (js/parseInt code-str 16)]
      (.fromCharCode js/String code)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3297
└── src
    └── main
        └── cljs
            └── cljs
                └── <ins>[reader.cljs:189-191](https://github.com/clojure/clojurescript/blob/r3297/src/main/cljs/cljs/reader.cljs#L189-L191)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.reader/make-unicode-char` @ crossclj](http://crossclj.info/fun/cljs.reader.cljs/make-unicode-char.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.reader_make-unicode-char.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.reader",
 :name "make-unicode-char",
 :type "function",
 :signature ["[code-str]"],
 :source {:code "(defn make-unicode-char [code-str]\n    (let [code (js/parseInt code-str 16)]\n      (.fromCharCode js/String code)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r3297",
          :filename "src/main/cljs/cljs/reader.cljs",
          :lines [189 191]},
 :full-name "cljs.reader/make-unicode-char",
 :full-name-encode "cljs.reader_make-unicode-char",
 :history [["+" "0.0-1424"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.reader/make-unicode-char"]))
```

-->
