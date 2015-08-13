## cljs.core/unchecked-short



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1798"><img valign="middle" alt="[+] 0.0-1798" title="Added in 0.0-1798" src="https://img.shields.io/badge/+-0.0--1798-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/unchecked-short</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/unchecked-short)
</td>
</tr>
</table>


 <samp>
(__unchecked-short__ x)<br>
</samp>

---







Function code @ [github](https://github.com/clojure/clojurescript/blob/r2024/src/cljs/cljs/core.cljs#L1512):

```clj
(defn unchecked-short [x] x)
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2024
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:1512](https://github.com/clojure/clojurescript/blob/r2024/src/cljs/cljs/core.cljs#L1512)</ins>
</pre>

-->

---

Macro code @ [github](https://github.com/clojure/clojurescript/blob/r2024/src/clj/cljs/core.clj#L341):

```clj
(defmacro unchecked-short [x] x)
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2024
└── src
    └── clj
        └── cljs
            └── <ins>[core.clj:341](https://github.com/clojure/clojurescript/blob/r2024/src/clj/cljs/core.clj#L341)</ins>
</pre>
-->

---


###### External doc links:

[`clojure.core/unchecked-short` @ clojuredocs](http://clojuredocs.org/clojure.core/unchecked-short)<br>
[`clojure.core/unchecked-short` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/unchecked-short/)<br>
[`clojure.core/unchecked-short` @ crossclj](http://crossclj.info/fun/clojure.core/unchecked-short.html)<br>
[`cljs.core/unchecked-short` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/unchecked-short.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_unchecked-short.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "unchecked-short",
 :signature ["[x]"],
 :history [["+" "0.0-1798"]],
 :type "function",
 :full-name-encode "cljs.core_unchecked-short",
 :source {:code "(defn unchecked-short [x] x)",
          :title "Function code",
          :repo "clojurescript",
          :tag "r2024",
          :filename "src/cljs/cljs/core.cljs",
          :lines [1512]},
 :extra-sources [{:code "(defmacro unchecked-short [x] x)",
                  :title "Macro code",
                  :repo "clojurescript",
                  :tag "r2024",
                  :filename "src/clj/cljs/core.clj",
                  :lines [341]}],
 :full-name "cljs.core/unchecked-short",
 :clj-symbol "clojure.core/unchecked-short"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/unchecked-short"]))
```

-->
