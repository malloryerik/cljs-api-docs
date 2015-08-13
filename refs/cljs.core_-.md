## cljs.core/-



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/-</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/-)
</td>
</tr>
</table>


 <samp>
(__-__ x)<br>
</samp>
 <samp>
(__-__ x y)<br>
</samp>
 <samp>
(__-__ x y & more)<br>
</samp>

---

If no `y`s are supplied, returns the negation of `x`, else subtracts the `y`s
from `x` and returns the result.

---

###### Examples:

```clj
(- 1)
;;=> -1

(- 6 3)
;;=> 3

(- 10 3 2)
;;=> 5
```

---

###### See Also:

[`cljs.core/+`](cljs.core_PLUS.md)<br>

---


Source docstring:

```
If no ys are supplied, returns the negation of x, else subtracts
the ys from x and returns the result.
```


Function code @ [github](https://github.com/clojure/clojurescript/blob/r1835/src/cljs/cljs/core.cljs#L1379-L1384):

```clj
(defn -
  ([x] (cljs.core/- x))
  ([x y] (cljs.core/- x y))
  ([x y & more] (reduce - (cljs.core/- x y) more)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1835
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:1379-1384](https://github.com/clojure/clojurescript/blob/r1835/src/cljs/cljs/core.cljs#L1379-L1384)</ins>
</pre>

-->

---

Macro code @ [github](https://github.com/clojure/clojurescript/blob/r1835/src/clj/cljs/core.clj#L328-L331):

```clj
(defmacro -
  ([x] (list 'js* "(- ~{})" x))
  ([x y] (list 'js* "(~{} - ~{})" x y))
  ([x y & more] `(- (- ~x ~y) ~@more)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1835
└── src
    └── clj
        └── cljs
            └── <ins>[core.clj:328-331](https://github.com/clojure/clojurescript/blob/r1835/src/clj/cljs/core.clj#L328-L331)</ins>
</pre>
-->

---


###### External doc links:

[`clojure.core/-` @ clojuredocs](http://clojuredocs.org/clojure.core/-)<br>
[`clojure.core/-` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/-/)<br>
[`clojure.core/-` @ crossclj](http://crossclj.info/fun/clojure.core/-.html)<br>
[`cljs.core/-` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/-.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_-.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "If no `y`s are supplied, returns the negation of `x`, else subtracts the `y`s\nfrom `x` and returns the result.",
 :ns "cljs.core",
 :name "-",
 :signature ["[x]" "[x y]" "[x y & more]"],
 :history [["+" "0.0-927"]],
 :type "function",
 :related ["cljs.core/+"],
 :full-name-encode "cljs.core_-",
 :source {:code "(defn -\n  ([x] (cljs.core/- x))\n  ([x y] (cljs.core/- x y))\n  ([x y & more] (reduce - (cljs.core/- x y) more)))",
          :title "Function code",
          :repo "clojurescript",
          :tag "r1835",
          :filename "src/cljs/cljs/core.cljs",
          :lines [1379 1384]},
 :extra-sources [{:code "(defmacro -\n  ([x] (list 'js* \"(- ~{})\" x))\n  ([x y] (list 'js* \"(~{} - ~{})\" x y))\n  ([x y & more] `(- (- ~x ~y) ~@more)))",
                  :title "Macro code",
                  :repo "clojurescript",
                  :tag "r1835",
                  :filename "src/clj/cljs/core.clj",
                  :lines [328 331]}],
 :examples [{:id "0a974e",
             :content "```clj\n(- 1)\n;;=> -1\n\n(- 6 3)\n;;=> 3\n\n(- 10 3 2)\n;;=> 5\n```"}],
 :full-name "cljs.core/-",
 :clj-symbol "clojure.core/-",
 :docstring "If no ys are supplied, returns the negation of x, else subtracts\nthe ys from x and returns the result."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/-"]))
```

-->
