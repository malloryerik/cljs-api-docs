## cljs.core/hash-map



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/hash-map</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/hash-map)
</td>
</tr>
</table>


 <samp>
(__hash-map__ & keyvals)<br>
</samp>

---

Returns a new hash map with supplied mappings.

`keyvals` must be an even number of forms.

---


###### See Also:

[`cljs.core/array-map`](cljs.core_array-map.md)<br>
[`cljs.core/sorted-map`](cljs.core_sorted-map.md)<br>

---


Source docstring:

```
keyval => key val
Returns a new hash map with supplied mappings.
```


Function code @ [github](https://github.com/clojure/clojurescript/blob/r2307/src/cljs/cljs/core.cljs#L6752-L6759):

```clj
(defn hash-map
  [& keyvals]
  (loop [in (seq keyvals), out (transient (.-EMPTY PersistentHashMap))]
    (if in
      (recur (nnext in) (assoc! out (first in) (second in)))
      (persistent! out))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2307
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:6752-6759](https://github.com/clojure/clojurescript/blob/r2307/src/cljs/cljs/core.cljs#L6752-L6759)</ins>
</pre>

-->

---

Macro code @ [github](https://github.com/clojure/clojurescript/blob/r2307/src/clj/cljs/core.clj#L1419-L1427):

```clj
(defmacro hash-map
  ([] `(.-EMPTY cljs.core/PersistentHashMap))
  ([& kvs]
    (let [pairs (partition 2 kvs)
          ks    (map first pairs)
          vs    (map second pairs)]
      (vary-meta
        `(.fromArrays cljs.core/PersistentHashMap (array ~@ks) (array ~@vs))
        assoc :tag 'cljs.core/PersistentHashMap))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2307
└── src
    └── clj
        └── cljs
            └── <ins>[core.clj:1419-1427](https://github.com/clojure/clojurescript/blob/r2307/src/clj/cljs/core.clj#L1419-L1427)</ins>
</pre>
-->

---


###### External doc links:

[`clojure.core/hash-map` @ clojuredocs](http://clojuredocs.org/clojure.core/hash-map)<br>
[`clojure.core/hash-map` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/hash-map/)<br>
[`clojure.core/hash-map` @ crossclj](http://crossclj.info/fun/clojure.core/hash-map.html)<br>
[`cljs.core/hash-map` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/hash-map.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_hash-map.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Returns a new hash map with supplied mappings.\n\n`keyvals` must be an even number of forms.",
 :ns "cljs.core",
 :name "hash-map",
 :signature ["[& keyvals]"],
 :history [["+" "0.0-927"]],
 :type "function",
 :related ["cljs.core/array-map" "cljs.core/sorted-map"],
 :full-name-encode "cljs.core_hash-map",
 :source {:code "(defn hash-map\n  [& keyvals]\n  (loop [in (seq keyvals), out (transient (.-EMPTY PersistentHashMap))]\n    (if in\n      (recur (nnext in) (assoc! out (first in) (second in)))\n      (persistent! out))))",
          :title "Function code",
          :repo "clojurescript",
          :tag "r2307",
          :filename "src/cljs/cljs/core.cljs",
          :lines [6752 6759]},
 :extra-sources [{:code "(defmacro hash-map\n  ([] `(.-EMPTY cljs.core/PersistentHashMap))\n  ([& kvs]\n    (let [pairs (partition 2 kvs)\n          ks    (map first pairs)\n          vs    (map second pairs)]\n      (vary-meta\n        `(.fromArrays cljs.core/PersistentHashMap (array ~@ks) (array ~@vs))\n        assoc :tag 'cljs.core/PersistentHashMap))))",
                  :title "Macro code",
                  :repo "clojurescript",
                  :tag "r2307",
                  :filename "src/clj/cljs/core.clj",
                  :lines [1419 1427]}],
 :full-name "cljs.core/hash-map",
 :clj-symbol "clojure.core/hash-map",
 :docstring "keyval => key val\nReturns a new hash map with supplied mappings."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/hash-map"]))
```

-->
