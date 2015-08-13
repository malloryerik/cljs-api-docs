## cljs.core/unchecked-add-int



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1798"><img valign="middle" alt="[+] 0.0-1798" title="Added in 0.0-1798" src="https://img.shields.io/badge/+-0.0--1798-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/unchecked-add-int</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/unchecked-add-int)
</td>
</tr>
</table>


 <samp>
(__unchecked-add-int__)<br>
</samp>
 <samp>
(__unchecked-add-int__ x)<br>
</samp>
 <samp>
(__unchecked-add-int__ x y)<br>
</samp>
 <samp>
(__unchecked-add-int__ x y & more)<br>
</samp>

---





Source docstring:

```
Returns the sum of nums. (+) returns 0.
```


Function code @ [github](https://github.com/clojure/clojurescript/blob/r3030/src/cljs/cljs/core.cljs#L2028-L2033):

```clj
(defn ^number unchecked-add-int
  ([] 0)
  ([x] x)
  ([x y] (cljs.core/unchecked-add-int x y))
  ([x y & more] (reduce unchecked-add-int (cljs.core/unchecked-add-int x y) more)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3030
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:2028-2033](https://github.com/clojure/clojurescript/blob/r3030/src/cljs/cljs/core.cljs#L2028-L2033)</ins>
</pre>

-->

---

Macro code @ [github](https://github.com/clojure/clojurescript/blob/r3030/src/clj/cljs/core.clj#L382-L383):

```clj
(defmacro ^::ana/numeric unchecked-add-int
  ([& xs] `(+ ~@xs)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3030
└── src
    └── clj
        └── cljs
            └── <ins>[core.clj:382-383](https://github.com/clojure/clojurescript/blob/r3030/src/clj/cljs/core.clj#L382-L383)</ins>
</pre>
-->

---


###### External doc links:

[`clojure.core/unchecked-add-int` @ clojuredocs](http://clojuredocs.org/clojure.core/unchecked-add-int)<br>
[`clojure.core/unchecked-add-int` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/unchecked-add-int/)<br>
[`clojure.core/unchecked-add-int` @ crossclj](http://crossclj.info/fun/clojure.core/unchecked-add-int.html)<br>
[`cljs.core/unchecked-add-int` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/unchecked-add-int.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_unchecked-add-int.cljsdoc
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
 :name "unchecked-add-int",
 :signature ["[]" "[x]" "[x y]" "[x y & more]"],
 :history [["+" "0.0-1798"]],
 :type "function",
 :full-name-encode "cljs.core_unchecked-add-int",
 :source {:code "(defn ^number unchecked-add-int\n  ([] 0)\n  ([x] x)\n  ([x y] (cljs.core/unchecked-add-int x y))\n  ([x y & more] (reduce unchecked-add-int (cljs.core/unchecked-add-int x y) more)))",
          :title "Function code",
          :repo "clojurescript",
          :tag "r3030",
          :filename "src/cljs/cljs/core.cljs",
          :lines [2028 2033]},
 :extra-sources [{:code "(defmacro ^::ana/numeric unchecked-add-int\n  ([& xs] `(+ ~@xs)))",
                  :title "Macro code",
                  :repo "clojurescript",
                  :tag "r3030",
                  :filename "src/clj/cljs/core.clj",
                  :lines [382 383]}],
 :full-name "cljs.core/unchecked-add-int",
 :clj-symbol "clojure.core/unchecked-add-int",
 :docstring "Returns the sum of nums. (+) returns 0."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/unchecked-add-int"]))
```

-->
