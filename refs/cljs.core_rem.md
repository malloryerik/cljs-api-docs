## cljs.core/rem



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/rem</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/rem)
</td>
</tr>
</table>


 <samp>
(__rem__ n d)<br>
</samp>

---

Returns the remainder of dividing numerator `n` by denominator `d`.

Returns `NaN` when `d` is 0 (divide by 0 error).

---


###### See Also:

[`cljs.core/quot`](cljs.core_quot.md)<br>
[`cljs.core/mod`](cljs.core_mod.md)<br>

---


Source docstring:

```
remainder of dividing numerator by denominator.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r2814/src/cljs/cljs/core.cljs#L2081-L2085):

```clj
(defn rem
  [n d]
  (let [q (quot n d)]
    (- n (* d q))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2814
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:2081-2085](https://github.com/clojure/clojurescript/blob/r2814/src/cljs/cljs/core.cljs#L2081-L2085)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/rem` @ clojuredocs](http://clojuredocs.org/clojure.core/rem)<br>
[`clojure.core/rem` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/rem/)<br>
[`clojure.core/rem` @ crossclj](http://crossclj.info/fun/clojure.core/rem.html)<br>
[`cljs.core/rem` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/rem.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_rem.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Returns the remainder of dividing numerator `n` by denominator `d`.\n\nReturns `NaN` when `d` is 0 (divide by 0 error).",
 :ns "cljs.core",
 :name "rem",
 :signature ["[n d]"],
 :history [["+" "0.0-927"]],
 :type "function",
 :related ["cljs.core/quot" "cljs.core/mod"],
 :full-name-encode "cljs.core_rem",
 :source {:code "(defn rem\n  [n d]\n  (let [q (quot n d)]\n    (- n (* d q))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2814",
          :filename "src/cljs/cljs/core.cljs",
          :lines [2081 2085]},
 :full-name "cljs.core/rem",
 :clj-symbol "clojure.core/rem",
 :docstring "remainder of dividing numerator by denominator."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/rem"]))
```

-->
