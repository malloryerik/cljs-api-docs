## cljs.pprint/\*print-miser-width\*



 <table border="1">
<tr>
<td>dynamic var</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-3255"><img valign="middle" alt="[+] 0.0-3255" title="Added in 0.0-3255" src="https://img.shields.io/badge/+-0.0--3255-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.pprint/\*print-miser-width\*</samp>](http://clojure.github.io/clojure/branch-master/clojure.pprint-api.html#clojure.pprint/*print-miser-width*)
</td>
</tr>
</table>







Source docstring:

```
The column at which to enter miser style. Depending on the dispatch table,
miser style add newlines in more places to try to keep lines short allowing for further
levels of nesting.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r3308/src/main/cljs/cljs/pprint.cljs#L634-L639):

```clj
(def ^:dynamic
 ^{:doc "The column at which to enter miser style. Depending on the dispatch table,
miser style add newlines in more places to try to keep lines short allowing for further
levels of nesting.",
   :added "1.2"}
 *print-miser-width* 40)
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3308
└── src
    └── main
        └── cljs
            └── cljs
                └── <ins>[pprint.cljs:634-639](https://github.com/clojure/clojurescript/blob/r3308/src/main/cljs/cljs/pprint.cljs#L634-L639)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.pprint/*print-miser-width*` @ clojuredocs](http://clojuredocs.org/clojure.pprint/*print-miser-width*)<br>
[`clojure.pprint/*print-miser-width*` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.pprint/*print-miser-width*/)<br>
[`clojure.pprint/*print-miser-width*` @ crossclj](http://crossclj.info/fun/clojure.pprint/*print-miser-width*.html)<br>
[`cljs.pprint/*print-miser-width*` @ crossclj](http://crossclj.info/fun/cljs.pprint.cljs/*print-miser-width*.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.pprint_STARprint-miser-widthSTAR.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.pprint",
 :name "*print-miser-width*",
 :history [["+" "0.0-3255"]],
 :type "dynamic var",
 :full-name-encode "cljs.pprint_STARprint-miser-widthSTAR",
 :source {:code "(def ^:dynamic\n ^{:doc \"The column at which to enter miser style. Depending on the dispatch table,\nmiser style add newlines in more places to try to keep lines short allowing for further\nlevels of nesting.\",\n   :added \"1.2\"}\n *print-miser-width* 40)",
          :title "Source code",
          :repo "clojurescript",
          :tag "r3308",
          :filename "src/main/cljs/cljs/pprint.cljs",
          :lines [634 639]},
 :full-name "cljs.pprint/*print-miser-width*",
 :clj-symbol "clojure.pprint/*print-miser-width*",
 :docstring "The column at which to enter miser style. Depending on the dispatch table,\nmiser style add newlines in more places to try to keep lines short allowing for further\nlevels of nesting."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.pprint/*print-miser-width*"]))
```

-->
