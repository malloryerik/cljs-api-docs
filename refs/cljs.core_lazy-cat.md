## cljs.core/lazy-cat



 <table border="1">
<tr>
<td>macro</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1803"><img valign="middle" alt="[+] 0.0-1803" title="Added in 0.0-1803" src="https://img.shields.io/badge/+-0.0--1803-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/lazy-cat</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/lazy-cat)
</td>
</tr>
</table>


 <samp>
(__lazy-cat__ & colls)<br>
</samp>

---

Expands to code which yields a lazy sequence of the concatenation of the
supplied collections. Each collections expression is not evaluated until it is
needed.

<table class="code-tbl-9bef6">
  <thead>
    <tr>
      <th>Code</th>
      <th>Expands To</th></tr></thead>
  <tbody>
    <tr>
      <td><code>(lazy-cat x y z)</code>
      <td><pre>
(concat (lazy-seq x)
        (lazy-seq y)
        (lazy-seq z))</pre></td></tr></tbody></table>

---


###### See Also:

[`cljs.core/lazy-seq`](cljs.core_lazy-seq.md)<br>
[`cljs.core/concat`](cljs.core_concat.md)<br>

---


Source docstring:

```
Expands to code which yields a lazy sequence of the concatenation
of the supplied colls.  Each coll expr is not evaluated until it is
needed. 

(lazy-cat xs ys zs) === (concat (lazy-seq xs) (lazy-seq ys) (lazy-seq zs))
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r2173/src/clj/cljs/core.clj#L1576-L1583):

```clj
(defmacro lazy-cat
  [& colls]
  `(concat ~@(map #(core/list `lazy-seq %) colls)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2173
└── src
    └── clj
        └── cljs
            └── <ins>[core.clj:1576-1583](https://github.com/clojure/clojurescript/blob/r2173/src/clj/cljs/core.clj#L1576-L1583)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/lazy-cat` @ clojuredocs](http://clojuredocs.org/clojure.core/lazy-cat)<br>
[`clojure.core/lazy-cat` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/lazy-cat/)<br>
[`clojure.core/lazy-cat` @ crossclj](http://crossclj.info/fun/clojure.core/lazy-cat.html)<br>
[`cljs.core/lazy-cat` @ crossclj](http://crossclj.info/fun/cljs.core/lazy-cat.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_lazy-cat.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Expands to code which yields a lazy sequence of the concatenation of the\nsupplied collections. Each collections expression is not evaluated until it is\nneeded.\n\n<table class=\"code-tbl-9bef6\">\n  <thead>\n    <tr>\n      <th>Code</th>\n      <th>Expands To</th></tr></thead>\n  <tbody>\n    <tr>\n      <td><code>(lazy-cat x y z)</code>\n      <td><pre>\n(concat (lazy-seq x)\n        (lazy-seq y)\n        (lazy-seq z))</pre></td></tr></tbody></table>",
 :ns "cljs.core",
 :name "lazy-cat",
 :signature ["[& colls]"],
 :history [["+" "0.0-1803"]],
 :type "macro",
 :related ["cljs.core/lazy-seq" "cljs.core/concat"],
 :full-name-encode "cljs.core_lazy-cat",
 :source {:code "(defmacro lazy-cat\n  [& colls]\n  `(concat ~@(map #(core/list `lazy-seq %) colls)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2173",
          :filename "src/clj/cljs/core.clj",
          :lines [1576 1583]},
 :full-name "cljs.core/lazy-cat",
 :clj-symbol "clojure.core/lazy-cat",
 :docstring "Expands to code which yields a lazy sequence of the concatenation\nof the supplied colls.  Each coll expr is not evaluated until it is\nneeded. \n\n(lazy-cat xs ys zs) === (concat (lazy-seq xs) (lazy-seq ys) (lazy-seq zs))"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/lazy-cat"]))
```

-->
