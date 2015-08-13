## cljs.core/run!



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-2301"><img valign="middle" alt="[+] 0.0-2301" title="Added in 0.0-2301" src="https://img.shields.io/badge/+-0.0--2301-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/run!</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/run!)
</td>
</tr>
</table>


 <samp>
(__run!__ proc coll)<br>
</samp>

---





Source docstring:

```
Runs the supplied procedure (via reduce), for purposes of side
effects, on successive items in the collection. Returns nil
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r3269/src/main/cljs/cljs/core.cljs#L8960-L8964):

```clj
(defn run!
  [proc coll]
  (reduce #(proc %2) nil coll))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3269
└── src
    └── main
        └── cljs
            └── cljs
                └── <ins>[core.cljs:8960-8964](https://github.com/clojure/clojurescript/blob/r3269/src/main/cljs/cljs/core.cljs#L8960-L8964)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/run!` @ clojuredocs](http://clojuredocs.org/clojure.core/run!)<br>
[`clojure.core/run!` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/run%21/)<br>
[`clojure.core/run!` @ crossclj](http://crossclj.info/fun/clojure.core/run%21.html)<br>
[`cljs.core/run!` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/run%21.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_runBANG.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "run!",
 :signature ["[proc coll]"],
 :history [["+" "0.0-2301"]],
 :type "function",
 :full-name-encode "cljs.core_runBANG",
 :source {:code "(defn run!\n  [proc coll]\n  (reduce #(proc %2) nil coll))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r3269",
          :filename "src/main/cljs/cljs/core.cljs",
          :lines [8960 8964]},
 :full-name "cljs.core/run!",
 :clj-symbol "clojure.core/run!",
 :docstring "Runs the supplied procedure (via reduce), for purposes of side\neffects, on successive items in the collection. Returns nil"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/run!"]))
```

-->
