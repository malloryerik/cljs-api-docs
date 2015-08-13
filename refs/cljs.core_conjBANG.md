## cljs.core/conj!



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1211"><img valign="middle" alt="[+] 0.0-1211" title="Added in 0.0-1211" src="https://img.shields.io/badge/+-0.0--1211-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/conj!</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/conj!)
</td>
</tr>
</table>


 <samp>
(__conj!__ tcoll val)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r1443/src/cljs/cljs/core.cljs#L2059-L2060):

```clj
(defn conj! [tcoll val]
  (-conj! tcoll val))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1443
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:2059-2060](https://github.com/clojure/clojurescript/blob/r1443/src/cljs/cljs/core.cljs#L2059-L2060)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/conj!` @ clojuredocs](http://clojuredocs.org/clojure.core/conj!)<br>
[`clojure.core/conj!` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/conj%21/)<br>
[`clojure.core/conj!` @ crossclj](http://crossclj.info/fun/clojure.core/conj%21.html)<br>
[`cljs.core/conj!` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/conj%21.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_conjBANG.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "conj!",
 :signature ["[tcoll val]"],
 :history [["+" "0.0-1211"]],
 :type "function",
 :full-name-encode "cljs.core_conjBANG",
 :source {:code "(defn conj! [tcoll val]\n  (-conj! tcoll val))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1443",
          :filename "src/cljs/cljs/core.cljs",
          :lines [2059 2060]},
 :full-name "cljs.core/conj!",
 :clj-symbol "clojure.core/conj!"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/conj!"]))
```

-->
