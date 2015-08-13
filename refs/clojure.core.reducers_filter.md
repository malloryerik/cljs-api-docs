## clojure.core.reducers/filter



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1236"><img valign="middle" alt="[+] 0.0-1236" title="Added in 0.0-1236" src="https://img.shields.io/badge/+-0.0--1236-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core.reducers/filter</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core.reducers/filter)
</td>
</tr>
</table>


 <samp>
(__filter__ pred)<br>
</samp>
 <samp>
(__filter__ pred coll)<br>
</samp>

---





Source docstring:

```
Retains values in the reduction of coll for which (pred val)
  returns logical true. Foldable.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r2496/src/cljs/clojure/core/reducers.cljs#L117-L128):

```clj
(defcurried filter
  "Retains values in the reduction of coll for which (pred val)
  returns logical true. Foldable."
  {}
  [pred coll]
  (folder coll
   (fn [f1]
     (rfn [f1 k]
          ([ret k v]
             (if (pred k v)
               (f1 ret k v)
               ret))))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2496
└── src
    └── cljs
        └── clojure
            └── core
                └── <ins>[reducers.cljs:117-128](https://github.com/clojure/clojurescript/blob/r2496/src/cljs/clojure/core/reducers.cljs#L117-L128)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core.reducers/filter` @ clojuredocs](http://clojuredocs.org/clojure.core.reducers/filter)<br>
[`clojure.core.reducers/filter` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core.reducers/filter/)<br>
[`clojure.core.reducers/filter` @ crossclj](http://crossclj.info/fun/clojure.core.reducers/filter.html)<br>
[`clojure.core.reducers/filter` @ crossclj](http://crossclj.info/fun/clojure.core.reducers.cljs/filter.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/clojure.core.reducers_filter.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "clojure.core.reducers",
 :name "filter",
 :signature ["[pred]" "[pred coll]"],
 :history [["+" "0.0-1236"]],
 :type "function",
 :full-name-encode "clojure.core.reducers_filter",
 :source {:code "(defcurried filter\n  \"Retains values in the reduction of coll for which (pred val)\n  returns logical true. Foldable.\"\n  {}\n  [pred coll]\n  (folder coll\n   (fn [f1]\n     (rfn [f1 k]\n          ([ret k v]\n             (if (pred k v)\n               (f1 ret k v)\n               ret))))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2496",
          :filename "src/cljs/clojure/core/reducers.cljs",
          :lines [117 128]},
 :full-name "clojure.core.reducers/filter",
 :clj-symbol "clojure.core.reducers/filter",
 :docstring "Retains values in the reduction of coll for which (pred val)\n  returns logical true. Foldable."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "clojure.core.reducers/filter"]))
```

-->
