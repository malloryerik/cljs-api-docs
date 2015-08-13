## cljs.core/chunk-next



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1424"><img valign="middle" alt="[+] 0.0-1424" title="Added in 0.0-1424" src="https://img.shields.io/badge/+-0.0--1424-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__chunk-next__ s)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r1895/src/cljs/cljs/core.cljs#L2237-L2240):

```clj
(defn chunk-next [s]
  (if (satisfies? IChunkedNext s false)
    (-chunked-next s)
    (seq (-chunked-rest s))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1895
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:2237-2240](https://github.com/clojure/clojurescript/blob/r1895/src/cljs/cljs/core.cljs#L2237-L2240)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/chunk-next` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/chunk-next.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_chunk-next.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "chunk-next",
 :type "function",
 :signature ["[s]"],
 :source {:code "(defn chunk-next [s]\n  (if (satisfies? IChunkedNext s false)\n    (-chunked-next s)\n    (seq (-chunked-rest s))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1895",
          :filename "src/cljs/cljs/core.cljs",
          :lines [2237 2240]},
 :full-name "cljs.core/chunk-next",
 :full-name-encode "cljs.core_chunk-next",
 :history [["+" "0.0-1424"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/chunk-next"]))
```

-->
