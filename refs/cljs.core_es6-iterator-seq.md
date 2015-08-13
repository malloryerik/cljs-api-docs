## cljs.core/es6-iterator-seq



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-2411"><img valign="middle" alt="[+] 0.0-2411" title="Added in 0.0-2411" src="https://img.shields.io/badge/+-0.0--2411-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__es6-iterator-seq__ iter)<br>
</samp>

---





Source docstring:

```
EXPERIMENTAL: Given an ES2015 compatible iterator return a seq.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r1.7.10/src/main/cljs/cljs/core.cljs#L1147-L1153):

```clj
(defn es6-iterator-seq
  [iter]
  (let [v (.next iter)]
    (if (.-done v)
      ()
      (ES6IteratorSeq. (.-value v) iter nil))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1.7.10
└── src
    └── main
        └── cljs
            └── cljs
                └── <ins>[core.cljs:1147-1153](https://github.com/clojure/clojurescript/blob/r1.7.10/src/main/cljs/cljs/core.cljs#L1147-L1153)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/es6-iterator-seq` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/es6-iterator-seq.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_es6-iterator-seq.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "es6-iterator-seq",
 :signature ["[iter]"],
 :history [["+" "0.0-2411"]],
 :type "function",
 :full-name-encode "cljs.core_es6-iterator-seq",
 :source {:code "(defn es6-iterator-seq\n  [iter]\n  (let [v (.next iter)]\n    (if (.-done v)\n      ()\n      (ES6IteratorSeq. (.-value v) iter nil))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1.7.10",
          :filename "src/main/cljs/cljs/core.cljs",
          :lines [1147 1153]},
 :full-name "cljs.core/es6-iterator-seq",
 :docstring "EXPERIMENTAL: Given an ES2015 compatible iterator return a seq."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/es6-iterator-seq"]))
```

-->
