## cljs.core/inc



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/inc</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/inc)
</td>
</tr>
</table>


 <samp>
(__inc__ x)<br>
</samp>

---

Returns a number one greater than `x`.

---


###### See Also:

[`cljs.core/dec`](cljs.core_dec.md)<br>

---


Source docstring:

```
Returns a number one greater than num.
```


Function code @ [github](https://github.com/clojure/clojurescript/blob/r2341/src/cljs/cljs/core.cljs#L759-L761):

```clj
(defn inc
  [x] (cljs.core/+ x 1))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2341
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:759-761](https://github.com/clojure/clojurescript/blob/r2341/src/cljs/cljs/core.cljs#L759-L761)</ins>
</pre>

-->

---

Macro code @ [github](https://github.com/clojure/clojurescript/blob/r2341/src/clj/cljs/core.clj#L477-L478):

```clj
(defmacro ^::ana/numeric inc [x]
  `(+ ~x 1))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2341
└── src
    └── clj
        └── cljs
            └── <ins>[core.clj:477-478](https://github.com/clojure/clojurescript/blob/r2341/src/clj/cljs/core.clj#L477-L478)</ins>
</pre>
-->

---


###### External doc links:

[`clojure.core/inc` @ clojuredocs](http://clojuredocs.org/clojure.core/inc)<br>
[`clojure.core/inc` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/inc/)<br>
[`clojure.core/inc` @ crossclj](http://crossclj.info/fun/clojure.core/inc.html)<br>
[`cljs.core/inc` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/inc.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_inc.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Returns a number one greater than `x`.",
 :ns "cljs.core",
 :name "inc",
 :signature ["[x]"],
 :history [["+" "0.0-927"]],
 :type "function",
 :related ["cljs.core/dec"],
 :full-name-encode "cljs.core_inc",
 :source {:code "(defn inc\n  [x] (cljs.core/+ x 1))",
          :title "Function code",
          :repo "clojurescript",
          :tag "r2341",
          :filename "src/cljs/cljs/core.cljs",
          :lines [759 761]},
 :extra-sources [{:code "(defmacro ^::ana/numeric inc [x]\n  `(+ ~x 1))",
                  :title "Macro code",
                  :repo "clojurescript",
                  :tag "r2341",
                  :filename "src/clj/cljs/core.clj",
                  :lines [477 478]}],
 :full-name "cljs.core/inc",
 :clj-symbol "clojure.core/inc",
 :docstring "Returns a number one greater than num."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/inc"]))
```

-->
