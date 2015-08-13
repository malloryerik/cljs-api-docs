## cljs.core/IReversible



 <table border="1">
<tr>
<td>protocol</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1211"><img valign="middle" alt="[+] 0.0-1211" title="Added in 0.0-1211" src="https://img.shields.io/badge/+-0.0--1211-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.lang/Reversible</samp>](https://github.com/clojure/clojure/blob//src/jvm/clojure/lang/Reversible.java)
</td>
</tr>
</table>







Source docstring:

```
Protocol for reversing a seq.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r3264/src/main/cljs/cljs/core.cljs#L496-L499):

```clj
(defprotocol IReversible
  "Protocol for reversing a seq."
  (^clj -rseq [coll]
    "Returns a seq of the items in coll in reversed order."))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3264
└── src
    └── main
        └── cljs
            └── cljs
                └── <ins>[core.cljs:496-499](https://github.com/clojure/clojurescript/blob/r3264/src/main/cljs/cljs/core.cljs#L496-L499)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.lang/Reversible` @ clojuredocs](http://clojuredocs.org/clojure.lang/Reversible)<br>
[`clojure.lang/Reversible` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.lang/Reversible/)<br>
[`clojure.lang/Reversible` @ crossclj](http://crossclj.info/fun/clojure.lang/Reversible.html)<br>
[`cljs.core/IReversible` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/IReversible.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_IReversible.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "IReversible",
 :history [["+" "0.0-1211"]],
 :type "protocol",
 :full-name-encode "cljs.core_IReversible",
 :source {:code "(defprotocol IReversible\n  \"Protocol for reversing a seq.\"\n  (^clj -rseq [coll]\n    \"Returns a seq of the items in coll in reversed order.\"))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r3264",
          :filename "src/main/cljs/cljs/core.cljs",
          :lines [496 499]},
 :methods [{:name "-rseq",
            :signature ["[coll]"],
            :docstring "Returns a seq of the items in coll in reversed order."}],
 :full-name "cljs.core/IReversible",
 :clj-symbol "clojure.lang/Reversible",
 :docstring "Protocol for reversing a seq."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/IReversible"]))
```

-->
