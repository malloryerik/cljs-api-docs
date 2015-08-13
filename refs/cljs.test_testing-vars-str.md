## cljs.test/testing-vars-str



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-2496"><img valign="middle" alt="[+] 0.0-2496" title="Added in 0.0-2496" src="https://img.shields.io/badge/+-0.0--2496-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.test/testing-vars-str</samp>](http://clojure.github.io/clojure/branch-master/clojure.test-api.html#clojure.test/testing-vars-str)
</td>
</tr>
</table>


 <samp>
(__testing-vars-str__ m)<br>
</samp>

---





Source docstring:

```
Returns a string representation of the current test.  Renders names
in *testing-vars* as a list, then the source file and line of
current assertion.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r3211/src/cljs/cljs/test.cljs#L279-L287):

```clj
(defn testing-vars-str
  [m]
  (let [{:keys [file line column]} m]
    (str
      (reverse (map #(:name (meta %)) (:testing-vars (get-current-env))))
      " (" file ":" line (when column (str ":" column)) ")")))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3211
└── src
    └── cljs
        └── cljs
            └── <ins>[test.cljs:279-287](https://github.com/clojure/clojurescript/blob/r3211/src/cljs/cljs/test.cljs#L279-L287)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.test/testing-vars-str` @ clojuredocs](http://clojuredocs.org/clojure.test/testing-vars-str)<br>
[`clojure.test/testing-vars-str` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.test/testing-vars-str/)<br>
[`clojure.test/testing-vars-str` @ crossclj](http://crossclj.info/fun/clojure.test/testing-vars-str.html)<br>
[`cljs.test/testing-vars-str` @ crossclj](http://crossclj.info/fun/cljs.test.cljs/testing-vars-str.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.test_testing-vars-str.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.test",
 :name "testing-vars-str",
 :signature ["[m]"],
 :history [["+" "0.0-2496"]],
 :type "function",
 :full-name-encode "cljs.test_testing-vars-str",
 :source {:code "(defn testing-vars-str\n  [m]\n  (let [{:keys [file line column]} m]\n    (str\n      (reverse (map #(:name (meta %)) (:testing-vars (get-current-env))))\n      \" (\" file \":\" line (when column (str \":\" column)) \")\")))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r3211",
          :filename "src/cljs/cljs/test.cljs",
          :lines [279 287]},
 :full-name "cljs.test/testing-vars-str",
 :clj-symbol "clojure.test/testing-vars-str",
 :docstring "Returns a string representation of the current test.  Renders names\nin *testing-vars* as a list, then the source file and line of\ncurrent assertion."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.test/testing-vars-str"]))
```

-->
