## cljs.test/get-current-env



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-2496"><img valign="middle" alt="[+] 0.0-2496" title="Added in 0.0-2496" src="https://img.shields.io/badge/+-0.0--2496-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__get-current-env__)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r2843/src/cljs/cljs/test.cljs#L261-L262):

```clj
(defn get-current-env []
  (or *current-env* (empty-env)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2843
└── src
    └── cljs
        └── cljs
            └── <ins>[test.cljs:261-262](https://github.com/clojure/clojurescript/blob/r2843/src/cljs/cljs/test.cljs#L261-L262)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.test/get-current-env` @ crossclj](http://crossclj.info/fun/cljs.test.cljs/get-current-env.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.test_get-current-env.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.test",
 :name "get-current-env",
 :type "function",
 :signature ["[]"],
 :source {:code "(defn get-current-env []\n  (or *current-env* (empty-env)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2843",
          :filename "src/cljs/cljs/test.cljs",
          :lines [261 262]},
 :full-name "cljs.test/get-current-env",
 :full-name-encode "cljs.test_get-current-env",
 :history [["+" "0.0-2496"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.test/get-current-env"]))
```

-->
