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




Source code @ [github](https://github.com/clojure/clojurescript/blob/r1424/src/cljs/cljs/core.cljs#L986-L987):

```clj
(defn ^boolean number? [n]
  (goog/isNumber n))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1424
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:986-987](https://github.com/clojure/clojurescript/blob/r1424/src/cljs/cljs/core.cljs#L986-L987)</ins>
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
 :source {:code "(defn ^boolean number? [n]\n  (goog/isNumber n))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1424",
          :filename "src/cljs/cljs/core.cljs",
          :lines [986 987]},
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
