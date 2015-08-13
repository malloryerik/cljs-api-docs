## cljs.core/write-all



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1503"><img valign="middle" alt="[+] 0.0-1503" title="Added in 0.0-1503" src="https://img.shields.io/badge/+-0.0--1503-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__write-all__ writer & ss)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r2277/src/cljs/cljs/core.cljs#L7162-L7164):

```clj
(defn write-all [writer & ss]
  (doseq [s ss]
    (-write writer s)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2277
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:7162-7164](https://github.com/clojure/clojurescript/blob/r2277/src/cljs/cljs/core.cljs#L7162-L7164)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/write-all` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/write-all.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_write-all.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "write-all",
 :type "function",
 :signature ["[writer & ss]"],
 :source {:code "(defn write-all [writer & ss]\n  (doseq [s ss]\n    (-write writer s)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2277",
          :filename "src/cljs/cljs/core.cljs",
          :lines [7162 7164]},
 :full-name "cljs.core/write-all",
 :full-name-encode "cljs.core_write-all",
 :history [["+" "0.0-1503"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/write-all"]))
```

-->
