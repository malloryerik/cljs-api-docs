## cljs.core/PersistentVector.fromArray



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1006"><img valign="middle" alt="[+] 0.0-1006" title="Added in 0.0-1006" src="https://img.shields.io/badge/+-0.0--1006-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__PersistentVector.fromArray__ xs)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r1236/src/cljs/cljs/core.cljs#L2676-L2681):

```clj
(set! cljs.core.PersistentVector/fromArray
      (fn [xs]
        (loop [xs (seq xs) out (transient cljs.core.PersistentVector/EMPTY)]
          (if xs
            (recur (next xs) (conj! out (first xs)))
            (persistent! out)))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1236
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:2676-2681](https://github.com/clojure/clojurescript/blob/r1236/src/cljs/cljs/core.cljs#L2676-L2681)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/PersistentVector.fromArray` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/PersistentVector.fromArray.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_PersistentVectorDOTfromArray.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "PersistentVector.fromArray",
 :signature ["[xs]"],
 :history [["+" "0.0-1006"]],
 :parent-type "PersistentVector",
 :type "function",
 :full-name-encode "cljs.core_PersistentVectorDOTfromArray",
 :source {:code "(set! cljs.core.PersistentVector/fromArray\n      (fn [xs]\n        (loop [xs (seq xs) out (transient cljs.core.PersistentVector/EMPTY)]\n          (if xs\n            (recur (next xs) (conj! out (first xs)))\n            (persistent! out)))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1236",
          :filename "src/cljs/cljs/core.cljs",
          :lines [2676 2681]},
 :full-name "cljs.core/PersistentVector.fromArray"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/PersistentVector.fromArray"]))
```

-->
