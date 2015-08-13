## cljs.core/iteration



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-2301"><img valign="middle" alt="[+] 0.0-2301" title="Added in 0.0-2301" src="https://img.shields.io/badge/+-0.0--2301-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__iteration__ xform coll)<br>
</samp>

---





Source docstring:

```
Returns an iterable/seqable/reducible sequence of applications of
the transducer to the items in coll. Note that these applications
will be performed every time iterator/seq/reduce is called.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r2311/src/cljs/cljs/core.cljs#L8187-L8192):

```clj
(defn iteration
  [xform coll]
  (Iteration. xform coll))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2311
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:8187-8192](https://github.com/clojure/clojurescript/blob/r2311/src/cljs/cljs/core.cljs#L8187-L8192)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/iteration` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/iteration.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_iteration.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "iteration",
 :signature ["[xform coll]"],
 :history [["+" "0.0-2301"]],
 :type "function",
 :full-name-encode "cljs.core_iteration",
 :source {:code "(defn iteration\n  [xform coll]\n  (Iteration. xform coll))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2311",
          :filename "src/cljs/cljs/core.cljs",
          :lines [8187 8192]},
 :full-name "cljs.core/iteration",
 :docstring "Returns an iterable/seqable/reducible sequence of applications of\nthe transducer to the items in coll. Note that these applications\nwill be performed every time iterator/seq/reduce is called."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/iteration"]))
```

-->