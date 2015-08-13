## cljs.core/key->js



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1798"><img valign="middle" alt="[+] 0.0-1798" title="Added in 0.0-1798" src="https://img.shields.io/badge/+-0.0--1798-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__key->js__ k)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r2496/src/cljs/cljs/core.cljs#L8520-L8528):

```clj
(defn key->js [k]
  (if (satisfies? IEncodeJS k)
    (-clj->js k)
    (if (or (string? k)
            (number? k)
            (keyword? k)
            (symbol? k))
      (clj->js k)
      (pr-str k))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2496
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:8520-8528](https://github.com/clojure/clojurescript/blob/r2496/src/cljs/cljs/core.cljs#L8520-L8528)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/key->js` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/key-%3Ejs.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_key-GTjs.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "key->js",
 :type "function",
 :signature ["[k]"],
 :source {:code "(defn key->js [k]\n  (if (satisfies? IEncodeJS k)\n    (-clj->js k)\n    (if (or (string? k)\n            (number? k)\n            (keyword? k)\n            (symbol? k))\n      (clj->js k)\n      (pr-str k))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2496",
          :filename "src/cljs/cljs/core.cljs",
          :lines [8520 8528]},
 :full-name "cljs.core/key->js",
 :full-name-encode "cljs.core_key-GTjs",
 :history [["+" "0.0-1798"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/key->js"]))
```

-->
