## cljs.core/IList



 <table border="1">
<tr>
<td>protocol</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1211"><img valign="middle" alt="[+] 0.0-1211" title="Added in 0.0-1211" src="https://img.shields.io/badge/+-0.0--1211-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.lang/IPersistentList</samp>](https://github.com/clojure/clojure/blob//src/jvm/clojure/lang/IPersistentList.java)
</td>
</tr>
</table>







Source docstring:

```
Marker interface indicating a persistent list
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r1450/src/cljs/cljs/core.cljs#L223-L224):

```clj
(defprotocol IList
  "Marker interface indicating a persistent list")
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1450
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:223-224](https://github.com/clojure/clojurescript/blob/r1450/src/cljs/cljs/core.cljs#L223-L224)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.lang/IPersistentList` @ clojuredocs](http://clojuredocs.org/clojure.lang/IPersistentList)<br>
[`clojure.lang/IPersistentList` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.lang/IPersistentList/)<br>
[`clojure.lang/IPersistentList` @ crossclj](http://crossclj.info/fun/clojure.lang/IPersistentList.html)<br>
[`cljs.core/IList` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/IList.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_IList.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "IList",
 :history [["+" "0.0-1211"]],
 :type "protocol",
 :full-name-encode "cljs.core_IList",
 :source {:code "(defprotocol IList\n  \"Marker interface indicating a persistent list\")",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1450",
          :filename "src/cljs/cljs/core.cljs",
          :lines [223 224]},
 :full-name "cljs.core/IList",
 :clj-symbol "clojure.lang/IPersistentList",
 :docstring "Marker interface indicating a persistent list"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/IList"]))
```

-->
