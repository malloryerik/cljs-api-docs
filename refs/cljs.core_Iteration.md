## cljs.core/Iteration



 <table border="1">
<tr>
<td>type</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-2301"><img valign="middle" alt="[+] 0.0-2301" title="Added in 0.0-2301" src="https://img.shields.io/badge/+-0.0--2301-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__Iteration.__ xform coll)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r2307/src/cljs/cljs/core.cljs#L8158-L8169):

```clj
(deftype Iteration [xform coll]
   ISequential
   
   ISeqable
   (-seq [_] (seq (sequence xform coll)))

   IReduce
   (-reduce [_ f init] (transduce xform f init coll))

   IPrintWithWriter
   (-pr-writer [coll writer opts]
     (pr-sequential-writer writer pr-writer "(" " " ")" opts coll)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2307
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:8158-8169](https://github.com/clojure/clojurescript/blob/r2307/src/cljs/cljs/core.cljs#L8158-L8169)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/Iteration` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/Iteration.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_Iteration.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "Iteration",
 :type "type",
 :signature ["[xform coll]"],
 :source {:code "(deftype Iteration [xform coll]\n   ISequential\n   \n   ISeqable\n   (-seq [_] (seq (sequence xform coll)))\n\n   IReduce\n   (-reduce [_ f init] (transduce xform f init coll))\n\n   IPrintWithWriter\n   (-pr-writer [coll writer opts]\n     (pr-sequential-writer writer pr-writer \"(\" \" \" \")\" opts coll)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2307",
          :filename "src/cljs/cljs/core.cljs",
          :lines [8158 8169]},
 :full-name "cljs.core/Iteration",
 :full-name-encode "cljs.core_Iteration",
 :history [["+" "0.0-2301"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/Iteration"]))
```

-->
