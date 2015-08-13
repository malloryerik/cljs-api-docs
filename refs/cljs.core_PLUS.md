## cljs.core/+



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/+</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/+)
</td>
</tr>
</table>


 <samp>
(__+__)<br>
</samp>
 <samp>
(__+__ x)<br>
</samp>
 <samp>
(__+__ x y)<br>
</samp>
 <samp>
(__+__ x y & more)<br>
</samp>

---

Returns the sum of nums.

`(+)` returns 0.

---

###### Examples:

```clj
(+)
;;=> 0

(+ 1)
;;=> 1

(+ -10)
;;=> -10

(+ 1 2)
;;=> 3

(+ 1 2 3)
;;=> 6
```

---

###### See Also:

[`cljs.core/*`](cljs.core_STAR.md)<br>
[`cljs.core/-`](cljs.core_-.md)<br>

---


Source docstring:

```
Returns the sum of nums. (+) returns 0.
```


Function code @ [github](https://github.com/clojure/clojurescript/blob/r3255/src/main/cljs/cljs/core.cljs#L2111-L2117):

```clj
(defn ^number +
  ([] 0)
  ([x] x)
  ([x y] (cljs.core/+ x y))
  ([x y & more]
    (reduce + (cljs.core/+ x y) more)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3255
└── src
    └── main
        └── cljs
            └── cljs
                └── <ins>[core.cljs:2111-2117](https://github.com/clojure/clojurescript/blob/r3255/src/main/cljs/cljs/core.cljs#L2111-L2117)</ins>
</pre>

-->

---

Macro code @ [github](https://github.com/clojure/clojurescript/blob/r3255/src/main/clojure/cljs/core.clj#L422-L426):

```clj
(defmacro ^::ana/numeric +
  ([] 0)
  ([x] x)
  ([x y] (core/list 'js* "(~{} + ~{})" x y))
  ([x y & more] `(+ (+ ~x ~y) ~@more)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3255
└── src
    └── main
        └── clojure
            └── cljs
                └── <ins>[core.clj:422-426](https://github.com/clojure/clojurescript/blob/r3255/src/main/clojure/cljs/core.clj#L422-L426)</ins>
</pre>
-->

---


###### External doc links:

[`clojure.core/+` @ clojuredocs](http://clojuredocs.org/clojure.core/+)<br>
[`clojure.core/+` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/%2B/)<br>
[`clojure.core/+` @ crossclj](http://crossclj.info/fun/clojure.core/%2B.html)<br>
[`cljs.core/+` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/%2B.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_PLUS.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Returns the sum of nums.\n\n`(+)` returns 0.",
 :return-type number,
 :ns "cljs.core",
 :name "+",
 :signature ["[]" "[x]" "[x y]" "[x y & more]"],
 :history [["+" "0.0-927"]],
 :type "function",
 :related ["cljs.core/*" "cljs.core/-"],
 :full-name-encode "cljs.core_PLUS",
 :source {:code "(defn ^number +\n  ([] 0)\n  ([x] x)\n  ([x y] (cljs.core/+ x y))\n  ([x y & more]\n    (reduce + (cljs.core/+ x y) more)))",
          :title "Function code",
          :repo "clojurescript",
          :tag "r3255",
          :filename "src/main/cljs/cljs/core.cljs",
          :lines [2111 2117]},
 :extra-sources [{:code "(defmacro ^::ana/numeric +\n  ([] 0)\n  ([x] x)\n  ([x y] (core/list 'js* \"(~{} + ~{})\" x y))\n  ([x y & more] `(+ (+ ~x ~y) ~@more)))",
                  :title "Macro code",
                  :repo "clojurescript",
                  :tag "r3255",
                  :filename "src/main/clojure/cljs/core.clj",
                  :lines [422 426]}],
 :examples [{:id "650668",
             :content "```clj\n(+)\n;;=> 0\n\n(+ 1)\n;;=> 1\n\n(+ -10)\n;;=> -10\n\n(+ 1 2)\n;;=> 3\n\n(+ 1 2 3)\n;;=> 6\n```"}],
 :full-name "cljs.core/+",
 :clj-symbol "clojure.core/+",
 :docstring "Returns the sum of nums. (+) returns 0."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/+"]))
```

-->
