## cljs.core/unchecked-substract



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1798"><img valign="middle" alt="[+] 0.0-1798" title="Added in 0.0-1798" src="https://img.shields.io/badge/+-0.0--1798-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__unchecked-substract__ x)<br>
</samp>
 <samp>
(__unchecked-substract__ x y)<br>
</samp>
 <samp>
(__unchecked-substract__ x y & more)<br>
</samp>

---





Source docstring:

```
If no ys are supplied, returns the negation of x, else subtracts
the ys from x and returns the result.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r2227/src/cljs/cljs/core.cljs#L1633-L1638):

```clj
(defn ^number unchecked-substract
  ([x] (cljs.core/unchecked-subtract x))
  ([x y] (cljs.core/unchecked-subtract x y))
  ([x y & more] (reduce unchecked-substract (cljs.core/unchecked-subtract x y) more)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2227
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:1633-1638](https://github.com/clojure/clojurescript/blob/r2227/src/cljs/cljs/core.cljs#L1633-L1638)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/unchecked-substract` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/unchecked-substract.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_unchecked-substract.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:return-type number,
 :ns "cljs.core",
 :name "unchecked-substract",
 :signature ["[x]" "[x y]" "[x y & more]"],
 :history [["+" "0.0-1798"]],
 :type "function",
 :full-name-encode "cljs.core_unchecked-substract",
 :source {:code "(defn ^number unchecked-substract\n  ([x] (cljs.core/unchecked-subtract x))\n  ([x y] (cljs.core/unchecked-subtract x y))\n  ([x y & more] (reduce unchecked-substract (cljs.core/unchecked-subtract x y) more)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2227",
          :filename "src/cljs/cljs/core.cljs",
          :lines [1633 1638]},
 :full-name "cljs.core/unchecked-substract",
 :docstring "If no ys are supplied, returns the negation of x, else subtracts\nthe ys from x and returns the result."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/unchecked-substract"]))
```

-->
