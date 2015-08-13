## cljs.core/unchecked-inc



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1798"><img valign="middle" alt="[+] 0.0-1798" title="Added in 0.0-1798" src="https://img.shields.io/badge/+-0.0--1798-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/unchecked-inc</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/unchecked-inc)
</td>
</tr>
</table>


 <samp>
(__unchecked-inc__ x)<br>
</samp>

---







Function code @ [github](https://github.com/clojure/clojurescript/blob/r1.7.10/src/main/cljs/cljs/core.cljs#L2383-L2384):

```clj
(defn unchecked-inc [x]
  (cljs.core/unchecked-inc x))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1.7.10
└── src
    └── main
        └── cljs
            └── cljs
                └── <ins>[core.cljs:2383-2384](https://github.com/clojure/clojurescript/blob/r1.7.10/src/main/cljs/cljs/core.cljs#L2383-L2384)</ins>
</pre>

-->

---

Macro code @ [github](https://github.com/clojure/clojurescript/blob/r1.7.10/src/main/clojure/cljs/core.cljc#L930-L931):

```clj
(core/defmacro ^::ana/numeric unchecked-inc
  ([x] `(inc ~x)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1.7.10
└── src
    └── main
        └── clojure
            └── cljs
                └── <ins>[core.cljc:930-931](https://github.com/clojure/clojurescript/blob/r1.7.10/src/main/clojure/cljs/core.cljc#L930-L931)</ins>
</pre>
-->

---


###### External doc links:

[`clojure.core/unchecked-inc` @ clojuredocs](http://clojuredocs.org/clojure.core/unchecked-inc)<br>
[`clojure.core/unchecked-inc` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/unchecked-inc/)<br>
[`clojure.core/unchecked-inc` @ crossclj](http://crossclj.info/fun/clojure.core/unchecked-inc.html)<br>
[`cljs.core/unchecked-inc` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/unchecked-inc.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_unchecked-inc.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "unchecked-inc",
 :signature ["[x]"],
 :history [["+" "0.0-1798"]],
 :type "function",
 :full-name-encode "cljs.core_unchecked-inc",
 :source {:code "(defn unchecked-inc [x]\n  (cljs.core/unchecked-inc x))",
          :title "Function code",
          :repo "clojurescript",
          :tag "r1.7.10",
          :filename "src/main/cljs/cljs/core.cljs",
          :lines [2383 2384]},
 :extra-sources [{:code "(core/defmacro ^::ana/numeric unchecked-inc\n  ([x] `(inc ~x)))",
                  :title "Macro code",
                  :repo "clojurescript",
                  :tag "r1.7.10",
                  :filename "src/main/clojure/cljs/core.cljc",
                  :lines [930 931]}],
 :full-name "cljs.core/unchecked-inc",
 :clj-symbol "clojure.core/unchecked-inc"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/unchecked-inc"]))
```

-->
