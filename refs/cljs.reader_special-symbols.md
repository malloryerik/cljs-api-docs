## cljs.reader/special-symbols



 <table border="1">
<tr>
<td>var</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>









Source code @ [github](https://github.com/clojure/clojurescript/blob/r1011/src/cljs/cljs/reader.cljs#L243-L246):

```clj
(def special-symbols
  {"nil" nil
   "true" true
   "false" false})
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1011
└── src
    └── cljs
        └── cljs
            └── <ins>[reader.cljs:243-246](https://github.com/clojure/clojurescript/blob/r1011/src/cljs/cljs/reader.cljs#L243-L246)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.reader/special-symbols` @ crossclj](http://crossclj.info/fun/cljs.reader.cljs/special-symbols.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.reader_special-symbols.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.reader",
 :name "special-symbols",
 :type "var",
 :source {:code "(def special-symbols\n  {\"nil\" nil\n   \"true\" true\n   \"false\" false})",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1011",
          :filename "src/cljs/cljs/reader.cljs",
          :lines [243 246]},
 :full-name "cljs.reader/special-symbols",
 :full-name-encode "cljs.reader_special-symbols",
 :history [["+" "0.0-927"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.reader/special-symbols"]))
```

-->
