## cljs.core/IVector



 <table border="1">
<tr>
<td>protocol</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.lang/IPersistentVector</samp>](https://github.com/clojure/clojure/blob//src/jvm/clojure/lang/IPersistentVector.java)
</td>
</tr>
</table>









Source code @ [github](https://github.com/clojure/clojurescript/blob/r2280/src/cljs/cljs/core.cljs#L280-L281):

```clj
(defprotocol IVector
  (^clj -assoc-n [coll n val]))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2280
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:280-281](https://github.com/clojure/clojurescript/blob/r2280/src/cljs/cljs/core.cljs#L280-L281)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.lang/IPersistentVector` @ clojuredocs](http://clojuredocs.org/clojure.lang/IPersistentVector)<br>
[`clojure.lang/IPersistentVector` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.lang/IPersistentVector/)<br>
[`clojure.lang/IPersistentVector` @ crossclj](http://crossclj.info/fun/clojure.lang/IPersistentVector.html)<br>
[`cljs.core/IVector` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/IVector.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_IVector.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "IVector",
 :history [["+" "0.0-927"]],
 :type "protocol",
 :full-name-encode "cljs.core_IVector",
 :source {:code "(defprotocol IVector\n  (^clj -assoc-n [coll n val]))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2280",
          :filename "src/cljs/cljs/core.cljs",
          :lines [280 281]},
 :methods [{:name "-assoc-n",
            :signature ["[coll n val]"],
            :docstring nil}],
 :full-name "cljs.core/IVector",
 :clj-symbol "clojure.lang/IPersistentVector"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/IVector"]))
```

-->
