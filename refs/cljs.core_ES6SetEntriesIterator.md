## cljs.core/ES6SetEntriesIterator



 <table border="1">
<tr>
<td>type</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-2371"><img valign="middle" alt="[+] 0.0-2371" title="Added in 0.0-2371" src="https://img.shields.io/badge/+-0.0--2371-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__ES6SetEntriesIterator.__ s)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r2725/src/cljs/cljs/core.cljs#L5170-L5177):

```clj
(deftype ES6SetEntriesIterator [^:mutable s]
  Object
  (next [_]
    (if-not (nil? s)
      (let [x (first s)]
        (set! s (next s))
        #js {:value #js [x x] :done false})
      #js {:value nil :done true})))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2725
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:5170-5177](https://github.com/clojure/clojurescript/blob/r2725/src/cljs/cljs/core.cljs#L5170-L5177)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/ES6SetEntriesIterator` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/ES6SetEntriesIterator.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_ES6SetEntriesIterator.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "ES6SetEntriesIterator",
 :type "type",
 :signature ["[s]"],
 :source {:code "(deftype ES6SetEntriesIterator [^:mutable s]\n  Object\n  (next [_]\n    (if-not (nil? s)\n      (let [x (first s)]\n        (set! s (next s))\n        #js {:value #js [x x] :done false})\n      #js {:value nil :done true})))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2725",
          :filename "src/cljs/cljs/core.cljs",
          :lines [5170 5177]},
 :full-name "cljs.core/ES6SetEntriesIterator",
 :full-name-encode "cljs.core_ES6SetEntriesIterator",
 :history [["+" "0.0-2371"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/ES6SetEntriesIterator"]))
```

-->
