## cljs.core/assoc!



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1211"><img valign="middle" alt="[+] 0.0-1211" title="Added in 0.0-1211" src="https://img.shields.io/badge/+-0.0--1211-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/assoc!</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/assoc!)
</td>
</tr>
</table>


 <samp>
(__assoc!__ tcoll key val)<br>
</samp>
 <samp>
(__assoc!__ tcoll key val & kvs)<br>
</samp>

---

assoc(iate) on transient collection

When applied to a transient map, adds mapping of key(s) to val(s).

When applied to a transient vector, sets the val at index.  Note - index must
be <= (count vector).

Returns coll.

---

###### Examples:

```clj
(def tcoll (transient! {}))
(assoc! tcoll :a 1)
(assoc! tcoll :b 2)

tcoll
;;=> #<[object Object]> 

(:a tcoll)
;;=> 1

(:b tcoll)
;;=> 2

(def a (persistent! tcoll))
;;=> {:a 1 :b 2}
```

---

###### See Also:

[`cljs.core/transient`](cljs.core_transient.md)<br>
[`cljs.core/persistent!`](cljs.core_persistentBANG.md)<br>

---


Source docstring:

```
When applied to a transient map, adds mapping of key(s) to
val(s). When applied to a transient vector, sets the val at index.
Note - index must be <= (count vector). Returns coll.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r3115/src/cljs/cljs/core.cljs#L3225-L3235):

```clj
(defn assoc!
  ([tcoll key val]
    (-assoc! tcoll key val))
  ([tcoll key val & kvs]
    (let [ntcoll (-assoc! tcoll key val)]
      (if kvs
        (recur ntcoll (first kvs) (second kvs) (nnext kvs))
        ntcoll))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3115
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:3225-3235](https://github.com/clojure/clojurescript/blob/r3115/src/cljs/cljs/core.cljs#L3225-L3235)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/assoc!` @ clojuredocs](http://clojuredocs.org/clojure.core/assoc!)<br>
[`clojure.core/assoc!` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/assoc%21/)<br>
[`clojure.core/assoc!` @ crossclj](http://crossclj.info/fun/clojure.core/assoc%21.html)<br>
[`cljs.core/assoc!` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/assoc%21.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_assocBANG.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "assoc(iate) on transient collection\n\nWhen applied to a transient map, adds mapping of key(s) to val(s).\n\nWhen applied to a transient vector, sets the val at index.  Note - index must\nbe <= (count vector).\n\nReturns coll.",
 :ns "cljs.core",
 :name "assoc!",
 :signature ["[tcoll key val]" "[tcoll key val & kvs]"],
 :history [["+" "0.0-1211"]],
 :type "function",
 :related ["cljs.core/transient" "cljs.core/persistent!"],
 :full-name-encode "cljs.core_assocBANG",
 :source {:code "(defn assoc!\n  ([tcoll key val]\n    (-assoc! tcoll key val))\n  ([tcoll key val & kvs]\n    (let [ntcoll (-assoc! tcoll key val)]\n      (if kvs\n        (recur ntcoll (first kvs) (second kvs) (nnext kvs))\n        ntcoll))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r3115",
          :filename "src/cljs/cljs/core.cljs",
          :lines [3225 3235]},
 :examples [{:id "7d1e6b",
             :content "```clj\n(def tcoll (transient! {}))\n(assoc! tcoll :a 1)\n(assoc! tcoll :b 2)\n\ntcoll\n;;=> #<[object Object]> \n\n(:a tcoll)\n;;=> 1\n\n(:b tcoll)\n;;=> 2\n\n(def a (persistent! tcoll))\n;;=> {:a 1 :b 2}\n```"}],
 :full-name "cljs.core/assoc!",
 :clj-symbol "clojure.core/assoc!",
 :docstring "When applied to a transient map, adds mapping of key(s) to\nval(s). When applied to a transient vector, sets the val at index.\nNote - index must be <= (count vector). Returns coll."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/assoc!"]))
```

-->
