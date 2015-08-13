## cljs.reader/desugar-meta



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__desugar-meta__ f)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r3030/src/cljs/cljs/reader.cljs#L353-L359):

```clj
(defn desugar-meta
  [f]
  (cond
   (symbol? f) {:tag f}
   (string? f) {:tag f}
   (keyword? f) {f true}
   :else f))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3030
└── src
    └── cljs
        └── cljs
            └── <ins>[reader.cljs:353-359](https://github.com/clojure/clojurescript/blob/r3030/src/cljs/cljs/reader.cljs#L353-L359)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.reader/desugar-meta` @ crossclj](http://crossclj.info/fun/cljs.reader.cljs/desugar-meta.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.reader_desugar-meta.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.reader",
 :name "desugar-meta",
 :type "function",
 :signature ["[f]"],
 :source {:code "(defn desugar-meta\n  [f]\n  (cond\n   (symbol? f) {:tag f}\n   (string? f) {:tag f}\n   (keyword? f) {f true}\n   :else f))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r3030",
          :filename "src/cljs/cljs/reader.cljs",
          :lines [353 359]},
 :full-name "cljs.reader/desugar-meta",
 :full-name-encode "cljs.reader_desugar-meta",
 :history [["+" "0.0-927"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.reader/desugar-meta"]))
```

-->
