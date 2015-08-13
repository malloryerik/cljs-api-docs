## cljs.core/number?



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/number?</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/number?)
</td>
</tr>
</table>


 <samp>
(__number?__ n)<br>
</samp>

---

Returns true if `n` is a number, false otherwise.

---


###### See Also:

[`cljs.core/integer?`](cljs.core_integerQMARK.md)<br>

---




Function code @ [github](https://github.com/clojure/clojurescript/blob/r1885/src/cljs/cljs/core.cljs#L74-L75):

```clj
(defn ^boolean number? [n]
  (cljs.core/number? n))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1885
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:74-75](https://github.com/clojure/clojurescript/blob/r1885/src/cljs/cljs/core.cljs#L74-L75)</ins>
</pre>

-->

---

Macro code @ [github](https://github.com/clojure/clojurescript/blob/r1885/src/clj/cljs/core.clj#L258-L259):

```clj
(defmacro number? [x]
  (bool-expr (list 'js* "typeof ~{} === 'number'" x)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1885
└── src
    └── clj
        └── cljs
            └── <ins>[core.clj:258-259](https://github.com/clojure/clojurescript/blob/r1885/src/clj/cljs/core.clj#L258-L259)</ins>
</pre>
-->

---


###### External doc links:

[`clojure.core/number?` @ clojuredocs](http://clojuredocs.org/clojure.core/number_q)<br>
[`clojure.core/number?` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/number%3F/)<br>
[`clojure.core/number?` @ crossclj](http://crossclj.info/fun/clojure.core/number%3F.html)<br>
[`cljs.core/number?` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/number%3F.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_numberQMARK.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Returns true if `n` is a number, false otherwise.",
 :return-type boolean,
 :ns "cljs.core",
 :name "number?",
 :signature ["[n]"],
 :history [["+" "0.0-927"]],
 :type "function",
 :related ["cljs.core/integer?"],
 :full-name-encode "cljs.core_numberQMARK",
 :source {:code "(defn ^boolean number? [n]\n  (cljs.core/number? n))",
          :title "Function code",
          :repo "clojurescript",
          :tag "r1885",
          :filename "src/cljs/cljs/core.cljs",
          :lines [74 75]},
 :extra-sources [{:code "(defmacro number? [x]\n  (bool-expr (list 'js* \"typeof ~{} === 'number'\" x)))",
                  :title "Macro code",
                  :repo "clojurescript",
                  :tag "r1885",
                  :filename "src/clj/cljs/core.clj",
                  :lines [258 259]}],
 :full-name "cljs.core/number?",
 :clj-symbol "clojure.core/number?"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/number?"]))
```

-->
