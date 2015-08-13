## cljs.core/nfirst



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/nfirst</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/nfirst)
</td>
</tr>
</table>


 <samp>
(__nfirst__ coll)<br>
</samp>

---

Same as `(next (first coll))`.

---

###### Examples:

```clj
(nfirst [[1 2 3] [4 5]])
;;=> (2 3)

(nfirst [[1 2] [3 4]])
;;=> (2)

(nfirst [[1] [2 3]])
;;=> nil

(nfirst [[] [1 2]])
;;=> nil
```

---

###### See Also:

[`cljs.core/next`](cljs.core_next.md)<br>

---


Source docstring:

```
Same as (next (first x))
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r2138/src/cljs/cljs/core.cljs#L803-L806):

```clj
(defn nfirst
  [coll]
  (next (first coll)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2138
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:803-806](https://github.com/clojure/clojurescript/blob/r2138/src/cljs/cljs/core.cljs#L803-L806)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/nfirst` @ clojuredocs](http://clojuredocs.org/clojure.core/nfirst)<br>
[`clojure.core/nfirst` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/nfirst/)<br>
[`clojure.core/nfirst` @ crossclj](http://crossclj.info/fun/clojure.core/nfirst.html)<br>
[`cljs.core/nfirst` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/nfirst.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_nfirst.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Same as `(next (first coll))`.",
 :ns "cljs.core",
 :name "nfirst",
 :signature ["[coll]"],
 :history [["+" "0.0-927"]],
 :type "function",
 :related ["cljs.core/next"],
 :full-name-encode "cljs.core_nfirst",
 :source {:code "(defn nfirst\n  [coll]\n  (next (first coll)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2138",
          :filename "src/cljs/cljs/core.cljs",
          :lines [803 806]},
 :examples [{:id "60b8a4",
             :content "```clj\n(nfirst [[1 2 3] [4 5]])\n;;=> (2 3)\n\n(nfirst [[1 2] [3 4]])\n;;=> (2)\n\n(nfirst [[1] [2 3]])\n;;=> nil\n\n(nfirst [[] [1 2]])\n;;=> nil\n```"}],
 :full-name "cljs.core/nfirst",
 :clj-symbol "clojure.core/nfirst",
 :docstring "Same as (next (first x))"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/nfirst"]))
```

-->
