## cljs.core/chunked-seq?



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1424"><img valign="middle" alt="[+] 0.0-1424" title="Added in 0.0-1424" src="https://img.shields.io/badge/+-0.0--1424-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__chunked-seq?__ x)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r1885/src/cljs/cljs/core.cljs#L1126-L1127):

```clj
(defn ^boolean chunked-seq?
  [x] (satisfies? IChunkedSeq x false))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1885
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:1126-1127](https://github.com/clojure/clojurescript/blob/r1885/src/cljs/cljs/core.cljs#L1126-L1127)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/chunked-seq?` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/chunked-seq%3F.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_chunked-seqQMARK.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:return-type boolean,
 :ns "cljs.core",
 :name "chunked-seq?",
 :signature ["[x]"],
 :history [["+" "0.0-1424"]],
 :type "function",
 :full-name-encode "cljs.core_chunked-seqQMARK",
 :source {:code "(defn ^boolean chunked-seq?\n  [x] (satisfies? IChunkedSeq x false))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1885",
          :filename "src/cljs/cljs/core.cljs",
          :lines [1126 1127]},
 :full-name "cljs.core/chunked-seq?"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/chunked-seq?"]))
```

-->
