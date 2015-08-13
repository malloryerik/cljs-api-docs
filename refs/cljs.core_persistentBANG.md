## cljs.core/persistent!



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1211"><img valign="middle" alt="[+] 0.0-1211" title="Added in 0.0-1211" src="https://img.shields.io/badge/+-0.0--1211-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/persistent!</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/persistent!)
</td>
</tr>
</table>


 <samp>
(__persistent!__ tcoll)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r1424/src/cljs/cljs/core.cljs#L2042-L2043):

```clj
(defn persistent! [tcoll]
  (-persistent! tcoll))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1424
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:2042-2043](https://github.com/clojure/clojurescript/blob/r1424/src/cljs/cljs/core.cljs#L2042-L2043)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/persistent!` @ clojuredocs](http://clojuredocs.org/clojure.core/persistent!)<br>
[`clojure.core/persistent!` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/persistent%21/)<br>
[`clojure.core/persistent!` @ crossclj](http://crossclj.info/fun/clojure.core/persistent%21.html)<br>
[`cljs.core/persistent!` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/persistent%21.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_persistentBANG.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "persistent!",
 :signature ["[tcoll]"],
 :history [["+" "0.0-1211"]],
 :type "function",
 :full-name-encode "cljs.core_persistentBANG",
 :source {:code "(defn persistent! [tcoll]\n  (-persistent! tcoll))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1424",
          :filename "src/cljs/cljs/core.cljs",
          :lines [2042 2043]},
 :full-name "cljs.core/persistent!",
 :clj-symbol "clojure.core/persistent!"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/persistent!"]))
```

-->
