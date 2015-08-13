## cljs.core/unchecked-char



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1798"><img valign="middle" alt="[+] 0.0-1798" title="Added in 0.0-1798" src="https://img.shields.io/badge/+-0.0--1798-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/unchecked-char</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/unchecked-char)
</td>
</tr>
</table>


 <samp>
(__unchecked-char__ x)<br>
</samp>

---







Function code @ [github](https://github.com/clojure/clojurescript/blob/r2127/src/cljs/cljs/core.cljs#L1540):

```clj
(defn ^number unchecked-char [x] x)
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2127
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:1540](https://github.com/clojure/clojurescript/blob/r2127/src/cljs/cljs/core.cljs#L1540)</ins>
</pre>

-->

---

Macro code @ [github](https://github.com/clojure/clojurescript/blob/r2127/src/clj/cljs/core.clj#L345):

```clj
(defmacro unchecked-char [x] x)
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2127
└── src
    └── clj
        └── cljs
            └── <ins>[core.clj:345](https://github.com/clojure/clojurescript/blob/r2127/src/clj/cljs/core.clj#L345)</ins>
</pre>
-->

---


###### External doc links:

[`clojure.core/unchecked-char` @ clojuredocs](http://clojuredocs.org/clojure.core/unchecked-char)<br>
[`clojure.core/unchecked-char` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/unchecked-char/)<br>
[`clojure.core/unchecked-char` @ crossclj](http://crossclj.info/fun/clojure.core/unchecked-char.html)<br>
[`cljs.core/unchecked-char` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/unchecked-char.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_unchecked-char.cljsdoc
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
 :name "unchecked-char",
 :signature ["[x]"],
 :history [["+" "0.0-1798"]],
 :type "function",
 :full-name-encode "cljs.core_unchecked-char",
 :source {:code "(defn ^number unchecked-char [x] x)",
          :title "Function code",
          :repo "clojurescript",
          :tag "r2127",
          :filename "src/cljs/cljs/core.cljs",
          :lines [1540]},
 :extra-sources [{:code "(defmacro unchecked-char [x] x)",
                  :title "Macro code",
                  :repo "clojurescript",
                  :tag "r2127",
                  :filename "src/clj/cljs/core.clj",
                  :lines [345]}],
 :full-name "cljs.core/unchecked-char",
 :clj-symbol "clojure.core/unchecked-char"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/unchecked-char"]))
```

-->
