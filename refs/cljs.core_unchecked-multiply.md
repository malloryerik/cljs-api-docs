## cljs.core/unchecked-multiply



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1798"><img valign="middle" alt="[+] 0.0-1798" title="Added in 0.0-1798" src="https://img.shields.io/badge/+-0.0--1798-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/unchecked-multiply</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/unchecked-multiply)
</td>
</tr>
</table>


 <samp>
(__unchecked-multiply__)<br>
</samp>
 <samp>
(__unchecked-multiply__ x)<br>
</samp>
 <samp>
(__unchecked-multiply__ x y)<br>
</samp>
 <samp>
(__unchecked-multiply__ x y & more)<br>
</samp>

---





Source docstring:

```
Returns the product of nums. (*) returns 1.
```


Function code @ [github](https://github.com/clojure/clojurescript/blob/r2060/src/cljs/cljs/core.cljs#L1578-L1583):

```clj
(defn unchecked-multiply
  ([] 1)
  ([x] x)
  ([x y] (cljs.core/unchecked-multiply x y))
  ([x y & more] (reduce unchecked-multiply (cljs.core/unchecked-multiply x y) more)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2060
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:1578-1583](https://github.com/clojure/clojurescript/blob/r2060/src/cljs/cljs/core.cljs#L1578-L1583)</ins>
</pre>

-->

---

Macro code @ [github](https://github.com/clojure/clojurescript/blob/r2060/src/clj/cljs/core.clj#L367-L368):

```clj
(defmacro unchecked-multiply
  ([& xs] `(* ~@xs)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2060
└── src
    └── clj
        └── cljs
            └── <ins>[core.clj:367-368](https://github.com/clojure/clojurescript/blob/r2060/src/clj/cljs/core.clj#L367-L368)</ins>
</pre>
-->

---


###### External doc links:

[`clojure.core/unchecked-multiply` @ clojuredocs](http://clojuredocs.org/clojure.core/unchecked-multiply)<br>
[`clojure.core/unchecked-multiply` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/unchecked-multiply/)<br>
[`clojure.core/unchecked-multiply` @ crossclj](http://crossclj.info/fun/clojure.core/unchecked-multiply.html)<br>
[`cljs.core/unchecked-multiply` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/unchecked-multiply.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_unchecked-multiply.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "unchecked-multiply",
 :signature ["[]" "[x]" "[x y]" "[x y & more]"],
 :history [["+" "0.0-1798"]],
 :type "function",
 :full-name-encode "cljs.core_unchecked-multiply",
 :source {:code "(defn unchecked-multiply\n  ([] 1)\n  ([x] x)\n  ([x y] (cljs.core/unchecked-multiply x y))\n  ([x y & more] (reduce unchecked-multiply (cljs.core/unchecked-multiply x y) more)))",
          :title "Function code",
          :repo "clojurescript",
          :tag "r2060",
          :filename "src/cljs/cljs/core.cljs",
          :lines [1578 1583]},
 :extra-sources [{:code "(defmacro unchecked-multiply\n  ([& xs] `(* ~@xs)))",
                  :title "Macro code",
                  :repo "clojurescript",
                  :tag "r2060",
                  :filename "src/clj/cljs/core.clj",
                  :lines [367 368]}],
 :full-name "cljs.core/unchecked-multiply",
 :clj-symbol "clojure.core/unchecked-multiply",
 :docstring "Returns the product of nums. (*) returns 1."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/unchecked-multiply"]))
```

-->
