## cljs.build.api/add-dependencies



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-3291"><img valign="middle" alt="[+] 0.0-3291" title="Added in 0.0-3291" src="https://img.shields.io/badge/+-0.0--3291-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__add-dependencies__ opts & ijss)<br>
</samp>

---





Source docstring:

```
Given one or more IJavaScript objects in dependency order, produce
a new sequence of IJavaScript objects which includes the input list
plus all dependencies in dependency order.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r3297/src/main/clojure/cljs/build/api.clj#L126-L131):

```clj
(defn add-dependencies
  [opts & ijss]
  (closure/add-dependencies opts ijss))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3297
└── src
    └── main
        └── clojure
            └── cljs
                └── build
                    └── <ins>[api.clj:126-131](https://github.com/clojure/clojurescript/blob/r3297/src/main/clojure/cljs/build/api.clj#L126-L131)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.build.api/add-dependencies` @ crossclj](http://crossclj.info/fun/cljs.build.api/add-dependencies.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.build.api_add-dependencies.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.build.api",
 :name "add-dependencies",
 :signature ["[opts & ijss]"],
 :history [["+" "0.0-3291"]],
 :type "function",
 :full-name-encode "cljs.build.api_add-dependencies",
 :source {:code "(defn add-dependencies\n  [opts & ijss]\n  (closure/add-dependencies opts ijss))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r3297",
          :filename "src/main/clojure/cljs/build/api.clj",
          :lines [126 131]},
 :full-name "cljs.build.api/add-dependencies",
 :docstring "Given one or more IJavaScript objects in dependency order, produce\na new sequence of IJavaScript objects which includes the input list\nplus all dependencies in dependency order."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.build.api/add-dependencies"]))
```

-->
