## cljs.test/test-all-vars-block



 <table border="1">
<tr>
<td>macro</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-2814"><img valign="middle" alt="[+] 0.0-2814" title="Added in 0.0-2814" src="https://img.shields.io/badge/+-0.0--2814-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__test-all-vars-block__ \[quote ns\])<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r2850/src/clj/cljs/test.clj#L305-L327):

```clj
(defmacro test-all-vars-block
  ([[quote ns]]
   `(let [env# (cljs.test/get-current-env)]
      (concat
       [(fn []
          (when (nil? env#)
            (cljs.test/set-env! (cljs.test/empty-env)))
          ~(when (ana-api/ns-resolve ns 'cljs-test-once-fixtures)
             `(cljs.test/update-current-env! [:once-fixtures] assoc '~ns
                                             ~(symbol (name ns) "cljs-test-once-fixtures")))
          ~(when (ana-api/ns-resolve ns 'cljs-test-each-fixtures)
             `(cljs.test/update-current-env! [:each-fixtures] assoc '~ns
                                             ~(symbol (name ns) "cljs-test-each-fixtures"))))]
       (cljs.test/test-vars-block
        [~@(map
            (fn [[k _]]
              `(var ~(symbol (name ns) (name k))))
            (filter
             (fn [[_ v]] (:test v))
             (ana-api/ns-interns ns)))])
       [(fn []
          (when (nil? env#)
            (cljs.test/clear-env!)))]))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2850
└── src
    └── clj
        └── cljs
            └── <ins>[test.clj:305-327](https://github.com/clojure/clojurescript/blob/r2850/src/clj/cljs/test.clj#L305-L327)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.test/test-all-vars-block` @ crossclj](http://crossclj.info/fun/cljs.test/test-all-vars-block.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.test_test-all-vars-block.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.test",
 :name "test-all-vars-block",
 :type "macro",
 :signature ["[[quote ns]]"],
 :source {:code "(defmacro test-all-vars-block\n  ([[quote ns]]\n   `(let [env# (cljs.test/get-current-env)]\n      (concat\n       [(fn []\n          (when (nil? env#)\n            (cljs.test/set-env! (cljs.test/empty-env)))\n          ~(when (ana-api/ns-resolve ns 'cljs-test-once-fixtures)\n             `(cljs.test/update-current-env! [:once-fixtures] assoc '~ns\n                                             ~(symbol (name ns) \"cljs-test-once-fixtures\")))\n          ~(when (ana-api/ns-resolve ns 'cljs-test-each-fixtures)\n             `(cljs.test/update-current-env! [:each-fixtures] assoc '~ns\n                                             ~(symbol (name ns) \"cljs-test-each-fixtures\"))))]\n       (cljs.test/test-vars-block\n        [~@(map\n            (fn [[k _]]\n              `(var ~(symbol (name ns) (name k))))\n            (filter\n             (fn [[_ v]] (:test v))\n             (ana-api/ns-interns ns)))])\n       [(fn []\n          (when (nil? env#)\n            (cljs.test/clear-env!)))]))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2850",
          :filename "src/clj/cljs/test.clj",
          :lines [305 327]},
 :full-name "cljs.test/test-all-vars-block",
 :full-name-encode "cljs.test_test-all-vars-block",
 :history [["+" "0.0-2814"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.test/test-all-vars-block"]))
```

-->
