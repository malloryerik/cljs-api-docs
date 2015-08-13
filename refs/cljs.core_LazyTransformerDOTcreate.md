## cljs.core/LazyTransformer.create



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-2301"><img valign="middle" alt="[+] 0.0-2301" title="Added in 0.0-2301" src="https://img.shields.io/badge/+-0.0--2301-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__LazyTransformer.create__ xform coll)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r3148/src/cljs/cljs/core.cljs#L3548-L3550):

```clj
(set! (.-create LazyTransformer)
  (fn [xform coll]
    (LazyTransformer. (stepper xform (iter coll)) nil nil nil)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3148
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:3548-3550](https://github.com/clojure/clojurescript/blob/r3148/src/cljs/cljs/core.cljs#L3548-L3550)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/LazyTransformer.create` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/LazyTransformer.create.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_LazyTransformerDOTcreate.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "LazyTransformer.create",
 :signature ["[xform coll]"],
 :history [["+" "0.0-2301"]],
 :parent-type "LazyTransformer",
 :type "function",
 :full-name-encode "cljs.core_LazyTransformerDOTcreate",
 :source {:code "(set! (.-create LazyTransformer)\n  (fn [xform coll]\n    (LazyTransformer. (stepper xform (iter coll)) nil nil nil)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r3148",
          :filename "src/cljs/cljs/core.cljs",
          :lines [3548 3550]},
 :full-name "cljs.core/LazyTransformer.create"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/LazyTransformer.create"]))
```

-->
