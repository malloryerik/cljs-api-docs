## cljs.core/int-array



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1798"><img valign="middle" alt="[+] 0.0-1798" title="Added in 0.0-1798" src="https://img.shields.io/badge/+-0.0--1798-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/int-array</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/int-array)
</td>
</tr>
</table>


 <samp>
(__int-array__ size-or-seq)<br>
</samp>
 <samp>
(__int-array__ size init-val-or-seq)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r2725/src/cljs/cljs/core.cljs#L2777-L2795):

```clj
(defn int-array
  ([size-or-seq]
     (if (number? size-or-seq)
       (int-array size-or-seq nil)
       (into-array size-or-seq)))
  ([size init-val-or-seq]
     (let [a (make-array size)]
       (if (seq? init-val-or-seq)
         (let [s (seq init-val-or-seq)]
           (loop [i 0 s s]
             (if (and s (< i size))
               (do
                 (aset a i (first s))
                 (recur (inc i) (next s)))
               a)))
         (do
           (dotimes [i size]
             (aset a i init-val-or-seq))
           a)))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2725
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:2777-2795](https://github.com/clojure/clojurescript/blob/r2725/src/cljs/cljs/core.cljs#L2777-L2795)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/int-array` @ clojuredocs](http://clojuredocs.org/clojure.core/int-array)<br>
[`clojure.core/int-array` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/int-array/)<br>
[`clojure.core/int-array` @ crossclj](http://crossclj.info/fun/clojure.core/int-array.html)<br>
[`cljs.core/int-array` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/int-array.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_int-array.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "int-array",
 :signature ["[size-or-seq]" "[size init-val-or-seq]"],
 :history [["+" "0.0-1798"]],
 :type "function",
 :full-name-encode "cljs.core_int-array",
 :source {:code "(defn int-array\n  ([size-or-seq]\n     (if (number? size-or-seq)\n       (int-array size-or-seq nil)\n       (into-array size-or-seq)))\n  ([size init-val-or-seq]\n     (let [a (make-array size)]\n       (if (seq? init-val-or-seq)\n         (let [s (seq init-val-or-seq)]\n           (loop [i 0 s s]\n             (if (and s (< i size))\n               (do\n                 (aset a i (first s))\n                 (recur (inc i) (next s)))\n               a)))\n         (do\n           (dotimes [i size]\n             (aset a i init-val-or-seq))\n           a)))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2725",
          :filename "src/cljs/cljs/core.cljs",
          :lines [2777 2795]},
 :full-name "cljs.core/int-array",
 :clj-symbol "clojure.core/int-array"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/int-array"]))
```

-->
