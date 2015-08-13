## cljs.core/PersistentHashMap



 <table border="1">
<tr>
<td>type</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1211"><img valign="middle" alt="[+] 0.0-1211" title="Added in 0.0-1211" src="https://img.shields.io/badge/+-0.0--1211-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.lang/PersistentHashMap</samp>](https://github.com/clojure/clojure/blob//src/jvm/clojure/lang/PersistentHashMap.java)
</td>
</tr>
</table>


 <samp>
(__PersistentHashMap.__ meta cnt root has-nil? nil-val __hash)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r1933/src/cljs/cljs/core.cljs#L4927-L5025):

```clj
(deftype PersistentHashMap [meta cnt root ^boolean has-nil? nil-val ^:mutable __hash]
  Object
  (toString [coll]
    (pr-str* coll))

  IWithMeta
  (-with-meta [coll meta] (PersistentHashMap. meta cnt root has-nil? nil-val __hash))

  IMeta
  (-meta [coll] meta)

  ICollection
  (-conj [coll entry]
    (if (vector? entry)
      (-assoc coll (-nth entry 0) (-nth entry 1))
      (reduce -conj coll entry)))

  IEmptyableCollection
  (-empty [coll] (-with-meta cljs.core.PersistentHashMap.EMPTY meta))

  IEquiv
  (-equiv [coll other] (equiv-map coll other))

  IHash
  (-hash [coll] (caching-hash coll hash-imap __hash))

  ISeqable
  (-seq [coll]
    (when (pos? cnt)
      (let [s (if-not (nil? root) (.inode-seq root))]
        (if has-nil?
          (cons [nil nil-val] s)
          s))))

  ICounted
  (-count [coll] cnt)

  ILookup
  (-lookup [coll k]
    (-lookup coll k nil))

  (-lookup [coll k not-found]
    (cond (nil? k)    (if has-nil?
                        nil-val
                        not-found)
          (nil? root) not-found
          :else       (.inode-lookup root 0 (hash k) k not-found)))

  IAssociative
  (-assoc [coll k v]
    (if (nil? k)
      (if (and has-nil? (identical? v nil-val))
        coll
        (PersistentHashMap. meta (if has-nil? cnt (inc cnt)) root true v nil))
      (let [added-leaf? (Box. false)
            new-root    (-> (if (nil? root)
                              cljs.core.BitmapIndexedNode.EMPTY
                              root)
                            (.inode-assoc 0 (hash k) k v added-leaf?))]
        (if (identical? new-root root)
          coll
          (PersistentHashMap. meta (if ^boolean (.-val added-leaf?) (inc cnt) cnt) new-root has-nil? nil-val nil)))))

  (-contains-key? [coll k]
    (cond (nil? k)    has-nil?
          (nil? root) false
          :else       (not (identical? (.inode-lookup root 0 (hash k) k lookup-sentinel)
                                       lookup-sentinel))))

  IMap
  (-dissoc [coll k]
    (cond (nil? k)    (if has-nil?
                        (PersistentHashMap. meta (dec cnt) root false nil nil)
                        coll)
          (nil? root) coll
          :else
          (let [new-root (.inode-without root 0 (hash k) k)]
            (if (identical? new-root root)
              coll
              (PersistentHashMap. meta (dec cnt) new-root has-nil? nil-val nil)))))

  IKVReduce
  (-kv-reduce [coll f init]
    (let [init (if has-nil? (f init nil nil-val) init)]
      (cond
        (reduced? init)          @init
        (not (nil? root)) (.kv-reduce root f init)
        :else                    init)))

  IFn
  (-invoke [coll k]
    (-lookup coll k))

  (-invoke [coll k not-found]
    (-lookup coll k not-found))

  IEditableCollection
  (-as-transient [coll]
    (TransientHashMap. (js-obj) root cnt has-nil? nil-val)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1933
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:4927-5025](https://github.com/clojure/clojurescript/blob/r1933/src/cljs/cljs/core.cljs#L4927-L5025)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.lang/PersistentHashMap` @ clojuredocs](http://clojuredocs.org/clojure.lang/PersistentHashMap)<br>
[`clojure.lang/PersistentHashMap` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.lang/PersistentHashMap/)<br>
[`clojure.lang/PersistentHashMap` @ crossclj](http://crossclj.info/fun/clojure.lang/PersistentHashMap.html)<br>
[`cljs.core/PersistentHashMap` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/PersistentHashMap.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_PersistentHashMap.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "PersistentHashMap",
 :signature ["[meta cnt root has-nil? nil-val __hash]"],
 :history [["+" "0.0-1211"]],
 :type "type",
 :full-name-encode "cljs.core_PersistentHashMap",
 :source {:code "(deftype PersistentHashMap [meta cnt root ^boolean has-nil? nil-val ^:mutable __hash]\n  Object\n  (toString [coll]\n    (pr-str* coll))\n\n  IWithMeta\n  (-with-meta [coll meta] (PersistentHashMap. meta cnt root has-nil? nil-val __hash))\n\n  IMeta\n  (-meta [coll] meta)\n\n  ICollection\n  (-conj [coll entry]\n    (if (vector? entry)\n      (-assoc coll (-nth entry 0) (-nth entry 1))\n      (reduce -conj coll entry)))\n\n  IEmptyableCollection\n  (-empty [coll] (-with-meta cljs.core.PersistentHashMap.EMPTY meta))\n\n  IEquiv\n  (-equiv [coll other] (equiv-map coll other))\n\n  IHash\n  (-hash [coll] (caching-hash coll hash-imap __hash))\n\n  ISeqable\n  (-seq [coll]\n    (when (pos? cnt)\n      (let [s (if-not (nil? root) (.inode-seq root))]\n        (if has-nil?\n          (cons [nil nil-val] s)\n          s))))\n\n  ICounted\n  (-count [coll] cnt)\n\n  ILookup\n  (-lookup [coll k]\n    (-lookup coll k nil))\n\n  (-lookup [coll k not-found]\n    (cond (nil? k)    (if has-nil?\n                        nil-val\n                        not-found)\n          (nil? root) not-found\n          :else       (.inode-lookup root 0 (hash k) k not-found)))\n\n  IAssociative\n  (-assoc [coll k v]\n    (if (nil? k)\n      (if (and has-nil? (identical? v nil-val))\n        coll\n        (PersistentHashMap. meta (if has-nil? cnt (inc cnt)) root true v nil))\n      (let [added-leaf? (Box. false)\n            new-root    (-> (if (nil? root)\n                              cljs.core.BitmapIndexedNode.EMPTY\n                              root)\n                            (.inode-assoc 0 (hash k) k v added-leaf?))]\n        (if (identical? new-root root)\n          coll\n          (PersistentHashMap. meta (if ^boolean (.-val added-leaf?) (inc cnt) cnt) new-root has-nil? nil-val nil)))))\n\n  (-contains-key? [coll k]\n    (cond (nil? k)    has-nil?\n          (nil? root) false\n          :else       (not (identical? (.inode-lookup root 0 (hash k) k lookup-sentinel)\n                                       lookup-sentinel))))\n\n  IMap\n  (-dissoc [coll k]\n    (cond (nil? k)    (if has-nil?\n                        (PersistentHashMap. meta (dec cnt) root false nil nil)\n                        coll)\n          (nil? root) coll\n          :else\n          (let [new-root (.inode-without root 0 (hash k) k)]\n            (if (identical? new-root root)\n              coll\n              (PersistentHashMap. meta (dec cnt) new-root has-nil? nil-val nil)))))\n\n  IKVReduce\n  (-kv-reduce [coll f init]\n    (let [init (if has-nil? (f init nil nil-val) init)]\n      (cond\n        (reduced? init)          @init\n        (not (nil? root)) (.kv-reduce root f init)\n        :else                    init)))\n\n  IFn\n  (-invoke [coll k]\n    (-lookup coll k))\n\n  (-invoke [coll k not-found]\n    (-lookup coll k not-found))\n\n  IEditableCollection\n  (-as-transient [coll]\n    (TransientHashMap. (js-obj) root cnt has-nil? nil-val)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1933",
          :filename "src/cljs/cljs/core.cljs",
          :lines [4927 5025]},
 :full-name "cljs.core/PersistentHashMap",
 :clj-symbol "clojure.lang/PersistentHashMap"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/PersistentHashMap"]))
```

-->
