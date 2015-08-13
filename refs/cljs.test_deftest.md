## cljs.test/deftest



 <table border="1">
<tr>
<td>macro</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-2496"><img valign="middle" alt="[+] 0.0-2496" title="Added in 0.0-2496" src="https://img.shields.io/badge/+-0.0--2496-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.test/deftest</samp>](http://clojure.github.io/clojure/branch-master/clojure.test-api.html#clojure.test/deftest)
</td>
</tr>
</table>


 <samp>
(__deftest__ name & body)<br>
</samp>

---





Source docstring:

```
Defines a test function with no arguments.  Test functions may call
other tests, so tests may be composed.  If you compose tests, you
should also define a function named test-ns-hook; run-tests will
call test-ns-hook instead of testing all vars.

Note: Actually, the test body goes in the :test metadata on the var,
and the real function (the value of the var) calls test-var on
itself.

When cljs.analyzer/*load-tests* is false, deftest is ignored.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r2913/src/clj/cljs/test.clj#L204-L220):

```clj
(defmacro deftest
  [name & body]
  (when ana/*load-tests*
    `(do
       (def ~(vary-meta name assoc :test `(fn [] ~@body))
         (fn [] (cljs.test/test-var (.-cljs$lang$var ~name))))
       (set! (.-cljs$lang$var ~name) (var ~name)))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2913
└── src
    └── clj
        └── cljs
            └── <ins>[test.clj:204-220](https://github.com/clojure/clojurescript/blob/r2913/src/clj/cljs/test.clj#L204-L220)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.test/deftest` @ clojuredocs](http://clojuredocs.org/clojure.test/deftest)<br>
[`clojure.test/deftest` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.test/deftest/)<br>
[`clojure.test/deftest` @ crossclj](http://crossclj.info/fun/clojure.test/deftest.html)<br>
[`cljs.test/deftest` @ crossclj](http://crossclj.info/fun/cljs.test/deftest.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.test_deftest.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.test",
 :name "deftest",
 :signature ["[name & body]"],
 :history [["+" "0.0-2496"]],
 :type "macro",
 :full-name-encode "cljs.test_deftest",
 :source {:code "(defmacro deftest\n  [name & body]\n  (when ana/*load-tests*\n    `(do\n       (def ~(vary-meta name assoc :test `(fn [] ~@body))\n         (fn [] (cljs.test/test-var (.-cljs$lang$var ~name))))\n       (set! (.-cljs$lang$var ~name) (var ~name)))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2913",
          :filename "src/clj/cljs/test.clj",
          :lines [204 220]},
 :full-name "cljs.test/deftest",
 :clj-symbol "clojure.test/deftest",
 :docstring "Defines a test function with no arguments.  Test functions may call\nother tests, so tests may be composed.  If you compose tests, you\nshould also define a function named test-ns-hook; run-tests will\ncall test-ns-hook instead of testing all vars.\n\nNote: Actually, the test body goes in the :test metadata on the var,\nand the real function (the value of the var) calls test-var on\nitself.\n\nWhen cljs.analyzer/*load-tests* is false, deftest is ignored."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.test/deftest"]))
```

-->
