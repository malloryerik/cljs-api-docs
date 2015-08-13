## cljs.core/dec



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/dec</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/dec)
</td>
</tr>
</table>


 <samp>
(__dec__ x)<br>
</samp>

---

Returns a number one less than `x`.

---


###### See Also:

[`cljs.core/inc`](cljs.core_inc.md)<br>

---


Source docstring:

```
Returns a number one less than num.
```


Function code @ [github](https://github.com/clojure/clojurescript/blob/r1552/src/cljs/cljs/core.cljs#L1302-L1304):

```clj
(defn dec
  [x] (- x 1))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1552
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:1302-1304](https://github.com/clojure/clojurescript/blob/r1552/src/cljs/cljs/core.cljs#L1302-L1304)</ins>
</pre>

-->

---

Macro code @ [github](https://github.com/clojure/clojurescript/blob/r1552/src/clj/cljs/core.clj#L268-L269):

```clj
(defmacro dec [x]
  `(- ~x 1))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1552
└── src
    └── clj
        └── cljs
            └── <ins>[core.clj:268-269](https://github.com/clojure/clojurescript/blob/r1552/src/clj/cljs/core.clj#L268-L269)</ins>
</pre>
-->

---


###### External doc links:

[`clojure.core/dec` @ clojuredocs](http://clojuredocs.org/clojure.core/dec)<br>
[`clojure.core/dec` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/dec/)<br>
[`clojure.core/dec` @ crossclj](http://crossclj.info/fun/clojure.core/dec.html)<br>
[`cljs.core/dec` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/dec.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_dec.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Returns a number one less than `x`.",
 :ns "cljs.core",
 :name "dec",
 :signature ["[x]"],
 :history [["+" "0.0-927"]],
 :type "function",
 :related ["cljs.core/inc"],
 :full-name-encode "cljs.core_dec",
 :source {:code "(defn dec\n  [x] (- x 1))",
          :title "Function code",
          :repo "clojurescript",
          :tag "r1552",
          :filename "src/cljs/cljs/core.cljs",
          :lines [1302 1304]},
 :extra-sources [{:code "(defmacro dec [x]\n  `(- ~x 1))",
                  :title "Macro code",
                  :repo "clojurescript",
                  :tag "r1552",
                  :filename "src/clj/cljs/core.clj",
                  :lines [268 269]}],
 :full-name "cljs.core/dec",
 :clj-symbol "clojure.core/dec",
 :docstring "Returns a number one less than num."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/dec"]))
```

-->
