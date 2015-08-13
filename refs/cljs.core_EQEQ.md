## cljs.core/==



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/==</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/==)
</td>
</tr>
</table>


 <samp>
(__==__ x)<br>
</samp>
 <samp>
(__==__ x y)<br>
</samp>
 <samp>
(__==__ x y & more)<br>
</samp>

---

This is an equality check for numbers of different types that was carried over from Clojure,
to allow compatibility when converting code to ClojureScript.

Since there is only a single number type in JavaScript, 64-bit floating point, there is no
reason to use the `==` operator in ClojureScript.

Behavior on non-number arguments is undefined.

---

###### Examples:

```clj
(== 1 1)
;;=> true

(== 1 2)
;;=> false
```

---

###### See Also:

[`cljs.core/=`](cljs.core_EQ.md)<br>
[`cljs.core/identical?`](cljs.core_identicalQMARK.md)<br>

---


Source docstring:

```
Returns non-nil if nums all have the equivalent
value, otherwise false. Behavior on non nums is
undefined.
```


Function code @ [github](https://github.com/clojure/clojurescript/blob/r2629/src/cljs/cljs/core.cljs#L2081-L2092):

```clj
(defn ^boolean ==
  ([x] true)
  ([x y] (-equiv x y))
  ([x y & more]
   (if (== x y)
     (if (next more)
       (recur y (first more) (next more))
       (== y (first more)))
     false)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2629
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:2081-2092](https://github.com/clojure/clojurescript/blob/r2629/src/cljs/cljs/core.cljs#L2081-L2092)</ins>
</pre>

-->

---

Macro code @ [github](https://github.com/clojure/clojurescript/blob/r2629/src/clj/cljs/core.clj#L454-L457):

```clj
(defmacro ^::ana/numeric ==
  ([x] true)
  ([x y] (bool-expr (core/list 'js* "(~{} === ~{})" x y)))
  ([x y & more] `(and (== ~x ~y) (== ~y ~@more))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2629
└── src
    └── clj
        └── cljs
            └── <ins>[core.clj:454-457](https://github.com/clojure/clojurescript/blob/r2629/src/clj/cljs/core.clj#L454-L457)</ins>
</pre>
-->

---


###### External doc links:

[`clojure.core/==` @ clojuredocs](http://clojuredocs.org/clojure.core/==)<br>
[`clojure.core/==` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/%3D%3D/)<br>
[`clojure.core/==` @ crossclj](http://crossclj.info/fun/clojure.core/%3D%3D.html)<br>
[`cljs.core/==` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/%3D%3D.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_EQEQ.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "This is an equality check for numbers of different types that was carried over from Clojure,\nto allow compatibility when converting code to ClojureScript.\n\nSince there is only a single number type in JavaScript, 64-bit floating point, there is no\nreason to use the `==` operator in ClojureScript.\n\nBehavior on non-number arguments is undefined.",
 :return-type boolean,
 :ns "cljs.core",
 :name "==",
 :signature ["[x]" "[x y]" "[x y & more]"],
 :history [["+" "0.0-927"]],
 :type "function",
 :related ["cljs.core/=" "cljs.core/identical?"],
 :full-name-encode "cljs.core_EQEQ",
 :source {:code "(defn ^boolean ==\n  ([x] true)\n  ([x y] (-equiv x y))\n  ([x y & more]\n   (if (== x y)\n     (if (next more)\n       (recur y (first more) (next more))\n       (== y (first more)))\n     false)))",
          :title "Function code",
          :repo "clojurescript",
          :tag "r2629",
          :filename "src/cljs/cljs/core.cljs",
          :lines [2081 2092]},
 :extra-sources [{:code "(defmacro ^::ana/numeric ==\n  ([x] true)\n  ([x y] (bool-expr (core/list 'js* \"(~{} === ~{})\" x y)))\n  ([x y & more] `(and (== ~x ~y) (== ~y ~@more))))",
                  :title "Macro code",
                  :repo "clojurescript",
                  :tag "r2629",
                  :filename "src/clj/cljs/core.clj",
                  :lines [454 457]}],
 :examples [{:id "5ac342",
             :content "```clj\n(== 1 1)\n;;=> true\n\n(== 1 2)\n;;=> false\n```"}],
 :full-name "cljs.core/==",
 :clj-symbol "clojure.core/==",
 :docstring "Returns non-nil if nums all have the equivalent\nvalue, otherwise false. Behavior on non nums is\nundefined."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/=="]))
```

-->
