## cljs.core/List.EMPTY



 <table border="1">
<tr>
<td>var</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.lang/PersistentList.EMPTY</samp>](https://github.com/clojure/clojure/blob//src/jvm/clojure/lang/PersistentList.java)
</td>
</tr>
</table>









Source code @ [github](https://github.com/clojure/clojurescript/blob/r1586/src/cljs/cljs/core.cljs#L1677):

```clj
(set! cljs.core.List/EMPTY (EmptyList. nil))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1586
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:1677](https://github.com/clojure/clojurescript/blob/r1586/src/cljs/cljs/core.cljs#L1677)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.lang/PersistentList.EMPTY` @ clojuredocs](http://clojuredocs.org/clojure.lang/PersistentList.EMPTY)<br>
[`clojure.lang/PersistentList.EMPTY` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.lang/PersistentList.EMPTY/)<br>
[`clojure.lang/PersistentList.EMPTY` @ crossclj](http://crossclj.info/fun/clojure.lang/PersistentList.EMPTY.html)<br>
[`cljs.core/List.EMPTY` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/List.EMPTY.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_ListDOTEMPTY.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "List.EMPTY",
 :history [["+" "0.0-927"]],
 :parent-type "List",
 :type "var",
 :full-name-encode "cljs.core_ListDOTEMPTY",
 :source {:code "(set! cljs.core.List/EMPTY (EmptyList. nil))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1586",
          :filename "src/cljs/cljs/core.cljs",
          :lines [1677]},
 :full-name "cljs.core/List.EMPTY",
 :clj-symbol "clojure.lang/PersistentList.EMPTY"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/List.EMPTY"]))
```

-->
