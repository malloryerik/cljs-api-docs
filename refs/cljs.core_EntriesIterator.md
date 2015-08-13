## cljs.core/EntriesIterator



 <table border="1">
<tr>
<td>type</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-2268"><img valign="middle" alt="[+] 0.0-2268" title="Added in 0.0-2268" src="https://img.shields.io/badge/+-0.0--2268-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__EntriesIterator.__ s)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r2307/src/cljs/cljs/core.cljs#L4827-L4834):

```clj
(deftype EntriesIterator [^:mutable s]
  Object
  (next [_]
    (if-not (nil? s)
      (let [[k v] (first s)]
        (set! s (next s))
        #js {:value #js [k v] :done false})
      #js {:value nil :done true})))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2307
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:4827-4834](https://github.com/clojure/clojurescript/blob/r2307/src/cljs/cljs/core.cljs#L4827-L4834)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/EntriesIterator` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/EntriesIterator.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_EntriesIterator.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "EntriesIterator",
 :type "type",
 :signature ["[s]"],
 :source {:code "(deftype EntriesIterator [^:mutable s]\n  Object\n  (next [_]\n    (if-not (nil? s)\n      (let [[k v] (first s)]\n        (set! s (next s))\n        #js {:value #js [k v] :done false})\n      #js {:value nil :done true})))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2307",
          :filename "src/cljs/cljs/core.cljs",
          :lines [4827 4834]},
 :full-name "cljs.core/EntriesIterator",
 :full-name-encode "cljs.core_EntriesIterator",
 :history [["+" "0.0-2268"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/EntriesIterator"]))
```

-->
