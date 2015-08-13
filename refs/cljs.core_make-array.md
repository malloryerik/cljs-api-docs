## cljs.core/make-array



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1211"><img valign="middle" alt="[+] 0.0-1211" title="Added in 0.0-1211" src="https://img.shields.io/badge/+-0.0--1211-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/make-array</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/make-array)
</td>
</tr>
</table>


 <samp>
(__make-array__ size)<br>
</samp>

---

Creates an empty JavaScript array of size `size`.

---


###### See Also:

[`cljs.core/aclone`](cljs.core_aclone.md)<br>
[`cljs.core/array`](cljs.core_array.md)<br>

---




Function code @ [github](https://github.com/clojure/clojurescript/blob/r1877/src/cljs/cljs/core.cljs#L138-L142):

```clj
(defn make-array
  ([size]
     (js/Array. size))
  ([type size]
     (make-array size)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1877
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:138-142](https://github.com/clojure/clojurescript/blob/r1877/src/cljs/cljs/core.cljs#L138-L142)</ins>
</pre>

-->

---

Macro code @ [github](https://github.com/clojure/clojurescript/blob/r1877/src/clj/cljs/core.clj#L1195-L1197):

```clj
(defmacro make-array
  [size]
  `(js/Array. ~size))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1877
└── src
    └── clj
        └── cljs
            └── <ins>[core.clj:1195-1197](https://github.com/clojure/clojurescript/blob/r1877/src/clj/cljs/core.clj#L1195-L1197)</ins>
</pre>
-->

---


###### External doc links:

[`clojure.core/make-array` @ clojuredocs](http://clojuredocs.org/clojure.core/make-array)<br>
[`clojure.core/make-array` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/make-array/)<br>
[`clojure.core/make-array` @ crossclj](http://crossclj.info/fun/clojure.core/make-array.html)<br>
[`cljs.core/make-array` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/make-array.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_make-array.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Creates an empty JavaScript array of size `size`.",
 :ns "cljs.core",
 :name "make-array",
 :signature ["[size]"],
 :history [["+" "0.0-1211"]],
 :type "function",
 :related ["cljs.core/aclone" "cljs.core/array"],
 :full-name-encode "cljs.core_make-array",
 :source {:code "(defn make-array\n  ([size]\n     (js/Array. size))\n  ([type size]\n     (make-array size)))",
          :title "Function code",
          :repo "clojurescript",
          :tag "r1877",
          :filename "src/cljs/cljs/core.cljs",
          :lines [138 142]},
 :extra-sources [{:code "(defmacro make-array\n  [size]\n  `(js/Array. ~size))",
                  :title "Macro code",
                  :repo "clojurescript",
                  :tag "r1877",
                  :filename "src/clj/cljs/core.clj",
                  :lines [1195 1197]}],
 :full-name "cljs.core/make-array",
 :clj-symbol "clojure.core/make-array"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/make-array"]))
```

-->
