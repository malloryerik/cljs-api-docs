## cljs.core/es6-iterable



 <table border="1">
<tr>
<td>macro</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-2411"><img valign="middle" alt="[+] 0.0-2411" title="Added in 0.0-2411" src="https://img.shields.io/badge/+-0.0--2411-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__es6-iterable__ ty)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r3190/src/clj/cljs/core.clj#L1997-L2001):

```clj
(defmacro es6-iterable [ty]
  `(aset (.-prototype ~ty) cljs.core/ITER_SYMBOL
     (fn []
       (this-as this#
         (cljs.core/es6-iterator this#)))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3190
└── src
    └── clj
        └── cljs
            └── <ins>[core.clj:1997-2001](https://github.com/clojure/clojurescript/blob/r3190/src/clj/cljs/core.clj#L1997-L2001)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/es6-iterable` @ crossclj](http://crossclj.info/fun/cljs.core/es6-iterable.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_es6-iterable.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "es6-iterable",
 :type "macro",
 :signature ["[ty]"],
 :source {:code "(defmacro es6-iterable [ty]\n  `(aset (.-prototype ~ty) cljs.core/ITER_SYMBOL\n     (fn []\n       (this-as this#\n         (cljs.core/es6-iterator this#)))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r3190",
          :filename "src/clj/cljs/core.clj",
          :lines [1997 2001]},
 :full-name "cljs.core/es6-iterable",
 :full-name-encode "cljs.core_es6-iterable",
 :history [["+" "0.0-2411"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/es6-iterable"]))
```

-->
