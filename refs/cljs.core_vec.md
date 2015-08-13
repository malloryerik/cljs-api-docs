## cljs.core/vec



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/vec</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/vec)
</td>
</tr>
</table>


 <samp>
(__vec__ coll)<br>
</samp>

---

Creates a new vector containing the contents of `coll`

---


###### See Also:

[`cljs.core/vector`](cljs.core_vector.md)<br>
[`cljs.core/vector?`](cljs.core_vectorQMARK.md)<br>

---




Source code @ [github](https://github.com/clojure/clojurescript/blob/r2985/src/cljs/cljs/core.cljs#L4481-L4487):

```clj
(defn vec [coll]
  (if (array? coll)
    (.fromArray PersistentVector coll true)
    (-persistent!
      (reduce -conj!
        (-as-transient (.-EMPTY PersistentVector))
        coll))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2985
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:4481-4487](https://github.com/clojure/clojurescript/blob/r2985/src/cljs/cljs/core.cljs#L4481-L4487)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/vec` @ clojuredocs](http://clojuredocs.org/clojure.core/vec)<br>
[`clojure.core/vec` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/vec/)<br>
[`clojure.core/vec` @ crossclj](http://crossclj.info/fun/clojure.core/vec.html)<br>
[`cljs.core/vec` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/vec.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_vec.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Creates a new vector containing the contents of `coll`",
 :ns "cljs.core",
 :name "vec",
 :signature ["[coll]"],
 :history [["+" "0.0-927"]],
 :type "function",
 :related ["cljs.core/vector" "cljs.core/vector?"],
 :full-name-encode "cljs.core_vec",
 :source {:code "(defn vec [coll]\n  (if (array? coll)\n    (.fromArray PersistentVector coll true)\n    (-persistent!\n      (reduce -conj!\n        (-as-transient (.-EMPTY PersistentVector))\n        coll))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2985",
          :filename "src/cljs/cljs/core.cljs",
          :lines [4481 4487]},
 :full-name "cljs.core/vec",
 :clj-symbol "clojure.core/vec"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/vec"]))
```

-->
