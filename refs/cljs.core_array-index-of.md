## cljs.core/array-index-of



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-3178"><img valign="middle" alt="[+] 0.0-3178" title="Added in 0.0-3178" src="https://img.shields.io/badge/+-0.0--3178-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__array-index-of__ arr k)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r1.7.48/src/main/cljs/cljs/core.cljs#L5714-L5726):

```clj
(defn array-index-of [arr k]
  (cond
    (keyword? k) (array-index-of-keyword? arr k)

    (or ^boolean (goog/isString k) (number? k))
    (array-index-of-identical? arr k)

    (symbol? k) (array-index-of-symbol? arr k)

    (nil? k)
    (array-index-of-nil? arr)

    :else (array-index-of-equiv? arr k)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1.7.48
└── src
    └── main
        └── cljs
            └── cljs
                └── <ins>[core.cljs:5714-5726](https://github.com/clojure/clojurescript/blob/r1.7.48/src/main/cljs/cljs/core.cljs#L5714-L5726)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/array-index-of` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/array-index-of.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_array-index-of.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "array-index-of",
 :type "function",
 :signature ["[arr k]"],
 :source {:code "(defn array-index-of [arr k]\n  (cond\n    (keyword? k) (array-index-of-keyword? arr k)\n\n    (or ^boolean (goog/isString k) (number? k))\n    (array-index-of-identical? arr k)\n\n    (symbol? k) (array-index-of-symbol? arr k)\n\n    (nil? k)\n    (array-index-of-nil? arr)\n\n    :else (array-index-of-equiv? arr k)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1.7.48",
          :filename "src/main/cljs/cljs/core.cljs",
          :lines [5714 5726]},
 :full-name "cljs.core/array-index-of",
 :full-name-encode "cljs.core_array-index-of",
 :history [["+" "0.0-3178"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/array-index-of"]))
```

-->
