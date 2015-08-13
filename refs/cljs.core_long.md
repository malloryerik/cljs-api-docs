## cljs.core/long



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1211"><img valign="middle" alt="[+] 0.0-1211" title="Added in 0.0-1211" src="https://img.shields.io/badge/+-0.0--1211-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/long</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/long)
</td>
</tr>
</table>


 <samp>
(__long__ x)<br>
</samp>

---





Source docstring:

```
Coerce to long by stripping decimal places. Identical to `int'.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r1586/src/cljs/cljs/core.cljs#L1330-L1333):

```clj
(defn long
  [x]
  (fix x))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1586
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:1330-1333](https://github.com/clojure/clojurescript/blob/r1586/src/cljs/cljs/core.cljs#L1330-L1333)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/long` @ clojuredocs](http://clojuredocs.org/clojure.core/long)<br>
[`clojure.core/long` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/long/)<br>
[`clojure.core/long` @ crossclj](http://crossclj.info/fun/clojure.core/long.html)<br>
[`cljs.core/long` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/long.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_long.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "long",
 :signature ["[x]"],
 :history [["+" "0.0-1211"]],
 :type "function",
 :full-name-encode "cljs.core_long",
 :source {:code "(defn long\n  [x]\n  (fix x))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1586",
          :filename "src/cljs/cljs/core.cljs",
          :lines [1330 1333]},
 :full-name "cljs.core/long",
 :clj-symbol "clojure.core/long",
 :docstring "Coerce to long by stripping decimal places. Identical to `int'."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/long"]))
```

-->