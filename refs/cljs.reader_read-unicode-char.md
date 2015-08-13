## ~~cljs.reader/read-unicode-char~~



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> <a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1424"><img valign="middle" alt="[×] 0.0-1424" title="Removed in 0.0-1424" src="https://img.shields.io/badge/×-0.0--1424-red.svg"></a> </td>
</tr>
</table>


 <samp>
(__read-unicode-char__ reader initch)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r1236/src/cljs/cljs/reader.cljs#L171-L173):

```clj
(defn read-unicode-char
  [reader initch]
  (reader-error reader "Unicode characters not supported by reader (yet)"))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1236
└── src
    └── cljs
        └── cljs
            └── <ins>[reader.cljs:171-173](https://github.com/clojure/clojurescript/blob/r1236/src/cljs/cljs/reader.cljs#L171-L173)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.reader/read-unicode-char` @ crossclj](http://crossclj.info/fun/cljs.reader.cljs/read-unicode-char.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.reader_read-unicode-char.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.reader",
 :name "read-unicode-char",
 :signature ["[reader initch]"],
 :history [["+" "0.0-927"] ["-" "0.0-1424"]],
 :type "function",
 :full-name-encode "cljs.reader_read-unicode-char",
 :source {:code "(defn read-unicode-char\n  [reader initch]\n  (reader-error reader \"Unicode characters not supported by reader (yet)\"))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1236",
          :filename "src/cljs/cljs/reader.cljs",
          :lines [171 173]},
 :full-name "cljs.reader/read-unicode-char",
 :removed {:in "0.0-1424", :last-seen "0.0-1236"}}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.reader/read-unicode-char"]))
```

-->