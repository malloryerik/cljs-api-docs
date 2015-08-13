## cljs.core/LazySeq



 <table border="1">
<tr>
<td>type</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.lang/LazySeq</samp>](https://github.com/clojure/clojure/blob//src/jvm/clojure/lang/LazySeq.java)
</td>
</tr>
</table>


 <samp>
(__LazySeq.__ meta realized x __hash)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r1503/src/cljs/cljs/core.cljs#L1795-L1827):

```clj
(deftype LazySeq [meta realized x ^:mutable __hash]
  Object
  (toString [this]
    (pr-str this))

  IWithMeta
  (-with-meta [coll meta] (LazySeq. meta realized x __hash))

  IMeta
  (-meta [coll] meta)

  ISeq
  (-first [coll] (first (lazy-seq-value coll)))
  (-rest [coll] (rest (lazy-seq-value coll)))

  INext
  (-next [coll] (-seq (-rest coll)))

  ICollection
  (-conj [coll o] (cons o coll))

  IEmptyableCollection
  (-empty [coll] (with-meta cljs.core.List/EMPTY meta))

  ISequential
  IEquiv
  (-equiv [coll other] (equiv-sequential coll other))

  IHash
  (-hash [coll] (caching-hash coll hash-coll __hash))

  ISeqable
  (-seq [coll] (seq (lazy-seq-value coll))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1503
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:1795-1827](https://github.com/clojure/clojurescript/blob/r1503/src/cljs/cljs/core.cljs#L1795-L1827)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.lang/LazySeq` @ clojuredocs](http://clojuredocs.org/clojure.lang/LazySeq)<br>
[`clojure.lang/LazySeq` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.lang/LazySeq/)<br>
[`clojure.lang/LazySeq` @ crossclj](http://crossclj.info/fun/clojure.lang/LazySeq.html)<br>
[`cljs.core/LazySeq` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/LazySeq.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_LazySeq.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "LazySeq",
 :signature ["[meta realized x __hash]"],
 :history [["+" "0.0-927"]],
 :type "type",
 :full-name-encode "cljs.core_LazySeq",
 :source {:code "(deftype LazySeq [meta realized x ^:mutable __hash]\n  Object\n  (toString [this]\n    (pr-str this))\n\n  IWithMeta\n  (-with-meta [coll meta] (LazySeq. meta realized x __hash))\n\n  IMeta\n  (-meta [coll] meta)\n\n  ISeq\n  (-first [coll] (first (lazy-seq-value coll)))\n  (-rest [coll] (rest (lazy-seq-value coll)))\n\n  INext\n  (-next [coll] (-seq (-rest coll)))\n\n  ICollection\n  (-conj [coll o] (cons o coll))\n\n  IEmptyableCollection\n  (-empty [coll] (with-meta cljs.core.List/EMPTY meta))\n\n  ISequential\n  IEquiv\n  (-equiv [coll other] (equiv-sequential coll other))\n\n  IHash\n  (-hash [coll] (caching-hash coll hash-coll __hash))\n\n  ISeqable\n  (-seq [coll] (seq (lazy-seq-value coll))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1503",
          :filename "src/cljs/cljs/core.cljs",
          :lines [1795 1827]},
 :full-name "cljs.core/LazySeq",
 :clj-symbol "clojure.lang/LazySeq"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/LazySeq"]))
```

-->
