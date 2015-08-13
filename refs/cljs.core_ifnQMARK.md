## cljs.core/ifn?



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1211"><img valign="middle" alt="[+] 0.0-1211" title="Added in 0.0-1211" src="https://img.shields.io/badge/+-0.0--1211-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/ifn?</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/ifn?)
</td>
</tr>
</table>


 <samp>
(__ifn?__ f)<br>
</samp>

---

Returns true if `f` implements the `IFn` protocol, false otherwise.

Functions, keywords, map, sets, and vectors can be called as functions.

---


###### See Also:

[`cljs.core/fn?`](cljs.core_fnQMARK.md)<br>

---




Source code @ [github](https://github.com/clojure/clojurescript/blob/r2322/src/cljs/cljs/core.cljs#L1446-L1447):

```clj
(defn ^boolean ifn? [f]
  (or (fn? f) (satisfies? IFn f)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2322
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:1446-1447](https://github.com/clojure/clojurescript/blob/r2322/src/cljs/cljs/core.cljs#L1446-L1447)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/ifn?` @ clojuredocs](http://clojuredocs.org/clojure.core/ifn_q)<br>
[`clojure.core/ifn?` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/ifn%3F/)<br>
[`clojure.core/ifn?` @ crossclj](http://crossclj.info/fun/clojure.core/ifn%3F.html)<br>
[`cljs.core/ifn?` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/ifn%3F.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_ifnQMARK.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Returns true if `f` implements the `IFn` protocol, false otherwise.\n\nFunctions, keywords, map, sets, and vectors can be called as functions.",
 :return-type boolean,
 :ns "cljs.core",
 :name "ifn?",
 :signature ["[f]"],
 :history [["+" "0.0-1211"]],
 :type "function",
 :related ["cljs.core/fn?"],
 :full-name-encode "cljs.core_ifnQMARK",
 :source {:code "(defn ^boolean ifn? [f]\n  (or (fn? f) (satisfies? IFn f)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2322",
          :filename "src/cljs/cljs/core.cljs",
          :lines [1446 1447]},
 :full-name "cljs.core/ifn?",
 :clj-symbol "clojure.core/ifn?"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/ifn?"]))
```

-->
