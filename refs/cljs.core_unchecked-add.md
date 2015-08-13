## cljs.core/unchecked-add



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1798"><img valign="middle" alt="[+] 0.0-1798" title="Added in 0.0-1798" src="https://img.shields.io/badge/+-0.0--1798-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/unchecked-add</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/unchecked-add)
</td>
</tr>
</table>


 <samp>
(__unchecked-add__)<br>
</samp>
 <samp>
(__unchecked-add__ x)<br>
</samp>
 <samp>
(__unchecked-add__ x y)<br>
</samp>
 <samp>
(__unchecked-add__ x y & more)<br>
</samp>

---





Source docstring:

```
Returns the sum of nums. (+) returns 0.
```


Function code @ [github](https://github.com/clojure/clojurescript/blob/r3165/src/cljs/cljs/core.cljs#L2217-L2222):

```clj
(defn ^number unchecked-add
  ([] 0)
  ([x] x)
  ([x y] (cljs.core/unchecked-add x y))
  ([x y & more] (reduce unchecked-add (cljs.core/unchecked-add x y) more)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3165
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:2217-2222](https://github.com/clojure/clojurescript/blob/r3165/src/cljs/cljs/core.cljs#L2217-L2222)</ins>
</pre>

-->

---

Macro code @ [github](https://github.com/clojure/clojurescript/blob/r3165/src/clj/cljs/core.clj#L390-L391):

```clj
(defmacro ^::ana/numeric unchecked-add
  ([& xs] `(+ ~@xs)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3165
└── src
    └── clj
        └── cljs
            └── <ins>[core.clj:390-391](https://github.com/clojure/clojurescript/blob/r3165/src/clj/cljs/core.clj#L390-L391)</ins>
</pre>
-->

---


###### External doc links:

[`clojure.core/unchecked-add` @ clojuredocs](http://clojuredocs.org/clojure.core/unchecked-add)<br>
[`clojure.core/unchecked-add` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/unchecked-add/)<br>
[`clojure.core/unchecked-add` @ crossclj](http://crossclj.info/fun/clojure.core/unchecked-add.html)<br>
[`cljs.core/unchecked-add` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/unchecked-add.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_unchecked-add.cljsdoc
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
 :name "unchecked-add",
 :signature ["[]" "[x]" "[x y]" "[x y & more]"],
 :history [["+" "0.0-1798"]],
 :type "function",
 :full-name-encode "cljs.core_unchecked-add",
 :source {:code "(defn ^number unchecked-add\n  ([] 0)\n  ([x] x)\n  ([x y] (cljs.core/unchecked-add x y))\n  ([x y & more] (reduce unchecked-add (cljs.core/unchecked-add x y) more)))",
          :title "Function code",
          :repo "clojurescript",
          :tag "r3165",
          :filename "src/cljs/cljs/core.cljs",
          :lines [2217 2222]},
 :extra-sources [{:code "(defmacro ^::ana/numeric unchecked-add\n  ([& xs] `(+ ~@xs)))",
                  :title "Macro code",
                  :repo "clojurescript",
                  :tag "r3165",
                  :filename "src/clj/cljs/core.clj",
                  :lines [390 391]}],
 :full-name "cljs.core/unchecked-add",
 :clj-symbol "clojure.core/unchecked-add",
 :docstring "Returns the sum of nums. (+) returns 0."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/unchecked-add"]))
```

-->
