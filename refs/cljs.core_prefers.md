## cljs.core/prefers



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/prefers</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/prefers)
</td>
</tr>
</table>


 <samp>
(__prefers__ multifn)<br>
</samp>

---





Source docstring:

```
Given a multimethod, returns a map of preferred value -> set of other values
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r3291/src/main/cljs/cljs/core.cljs#L9491-L9493):

```clj
(defn prefers
  [multifn] (-prefers multifn))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3291
└── src
    └── main
        └── cljs
            └── cljs
                └── <ins>[core.cljs:9491-9493](https://github.com/clojure/clojurescript/blob/r3291/src/main/cljs/cljs/core.cljs#L9491-L9493)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/prefers` @ clojuredocs](http://clojuredocs.org/clojure.core/prefers)<br>
[`clojure.core/prefers` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/prefers/)<br>
[`clojure.core/prefers` @ crossclj](http://crossclj.info/fun/clojure.core/prefers.html)<br>
[`cljs.core/prefers` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/prefers.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_prefers.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "prefers",
 :signature ["[multifn]"],
 :history [["+" "0.0-927"]],
 :type "function",
 :full-name-encode "cljs.core_prefers",
 :source {:code "(defn prefers\n  [multifn] (-prefers multifn))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r3291",
          :filename "src/main/cljs/cljs/core.cljs",
          :lines [9491 9493]},
 :full-name "cljs.core/prefers",
 :clj-symbol "clojure.core/prefers",
 :docstring "Given a multimethod, returns a map of preferred value -> set of other values"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/prefers"]))
```

-->
