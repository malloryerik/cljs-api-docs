## cljs.core/List



 <table border="1">
<tr>
<td>type</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.lang/PersistentList</samp>](https://github.com/clojure/clojure/blob//src/jvm/clojure/lang/PersistentList.java)
</td>
</tr>
</table>


 <samp>
(__List.__ meta first rest count)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r1006/src/cljs/cljs/core.cljs#L1123-L1155):

```clj
(deftype List [meta first rest count]
  IWithMeta
  (-with-meta [coll meta] (List. meta first rest count))

  IMeta
  (-meta [coll] meta)

  ISeq
  (-first [coll] first)
  (-rest [coll] rest)

  IStack
  (-peek [coll] first)
  (-pop [coll] (-rest coll))

  ICollection
  (-conj [coll o] (List. meta o coll (inc count)))

  IEmptyableCollection
  (-empty [coll] cljs.core.List/EMPTY)

  ISequential
  IEquiv
  (-equiv [coll other] (equiv-sequential coll other))

  IHash
  (-hash [coll] (hash-coll coll))

  ISeqable
  (-seq [coll] coll)

  ICounted
  (-count [coll] count))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1006
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:1123-1155](https://github.com/clojure/clojurescript/blob/r1006/src/cljs/cljs/core.cljs#L1123-L1155)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.lang/PersistentList` @ clojuredocs](http://clojuredocs.org/clojure.lang/PersistentList)<br>
[`clojure.lang/PersistentList` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.lang/PersistentList/)<br>
[`clojure.lang/PersistentList` @ crossclj](http://crossclj.info/fun/clojure.lang/PersistentList.html)<br>
[`cljs.core/List` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/List.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_List.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "List",
 :signature ["[meta first rest count]"],
 :history [["+" "0.0-927"]],
 :type "type",
 :full-name-encode "cljs.core_List",
 :source {:code "(deftype List [meta first rest count]\n  IWithMeta\n  (-with-meta [coll meta] (List. meta first rest count))\n\n  IMeta\n  (-meta [coll] meta)\n\n  ISeq\n  (-first [coll] first)\n  (-rest [coll] rest)\n\n  IStack\n  (-peek [coll] first)\n  (-pop [coll] (-rest coll))\n\n  ICollection\n  (-conj [coll o] (List. meta o coll (inc count)))\n\n  IEmptyableCollection\n  (-empty [coll] cljs.core.List/EMPTY)\n\n  ISequential\n  IEquiv\n  (-equiv [coll other] (equiv-sequential coll other))\n\n  IHash\n  (-hash [coll] (hash-coll coll))\n\n  ISeqable\n  (-seq [coll] coll)\n\n  ICounted\n  (-count [coll] count))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1006",
          :filename "src/cljs/cljs/core.cljs",
          :lines [1123 1155]},
 :full-name "cljs.core/List",
 :clj-symbol "clojure.lang/PersistentList"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/List"]))
```

-->
