## cljs.core/regexp?



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1424"><img valign="middle" alt="[+] 0.0-1424" title="Added in 0.0-1424" src="https://img.shields.io/badge/+-0.0--1424-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__regexp?__ o)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r2498/src/cljs/cljs/core.cljs#L7954-L7955):

```clj
(defn regexp? [o]
  (instance? js/RegExp o))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2498
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:7954-7955](https://github.com/clojure/clojurescript/blob/r2498/src/cljs/cljs/core.cljs#L7954-L7955)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/regexp?` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/regexp%3F.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_regexpQMARK.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "regexp?",
 :type "function",
 :signature ["[o]"],
 :source {:code "(defn regexp? [o]\n  (instance? js/RegExp o))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2498",
          :filename "src/cljs/cljs/core.cljs",
          :lines [7954 7955]},
 :full-name "cljs.core/regexp?",
 :full-name-encode "cljs.core_regexpQMARK",
 :history [["+" "0.0-1424"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/regexp?"]))
```

-->
