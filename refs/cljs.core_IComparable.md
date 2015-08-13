## cljs.core/IComparable



 <table border="1">
<tr>
<td>protocol</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1424"><img valign="middle" alt="[+] 0.0-1424" title="Added in 0.0-1424" src="https://img.shields.io/badge/+-0.0--1424-lightgrey.svg"></a> </td>
</tr>
</table>









Source code @ [github](https://github.com/clojure/clojurescript/blob/r2156/src/cljs/cljs/core.cljs#L364-L365):

```clj
(defprotocol IComparable
  (^number -compare [x y]))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2156
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:364-365](https://github.com/clojure/clojurescript/blob/r2156/src/cljs/cljs/core.cljs#L364-L365)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/IComparable` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/IComparable.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_IComparable.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "IComparable",
 :type "protocol",
 :full-name-encode "cljs.core_IComparable",
 :source {:code "(defprotocol IComparable\n  (^number -compare [x y]))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2156",
          :filename "src/cljs/cljs/core.cljs",
          :lines [364 365]},
 :methods [{:name "-compare", :signature ["[x y]"], :docstring nil}],
 :full-name "cljs.core/IComparable",
 :history [["+" "0.0-1424"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/IComparable"]))
```

-->
