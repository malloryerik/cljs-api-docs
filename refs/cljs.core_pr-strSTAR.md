## cljs.core/pr-str\*



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1806"><img valign="middle" alt="[+] 0.0-1806" title="Added in 0.0-1806" src="https://img.shields.io/badge/+-0.0--1806-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__pr-str\*__ obj)<br>
</samp>

---





Source docstring:

```
Support so that collections can implement toString without
loading all the printing machinery.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r3148/src/cljs/cljs/core.cljs#L645-L653):

```clj
(defn pr-str*
  [^not-native obj]
  (let [sb (StringBuffer.)
        writer (StringBufferWriter. sb)]
    (-pr-writer obj writer (pr-opts))
    (-flush writer)
    (str sb)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3148
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:645-653](https://github.com/clojure/clojurescript/blob/r3148/src/cljs/cljs/core.cljs#L645-L653)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/pr-str*` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/pr-str*.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_pr-strSTAR.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "pr-str*",
 :signature ["[obj]"],
 :history [["+" "0.0-1806"]],
 :type "function",
 :full-name-encode "cljs.core_pr-strSTAR",
 :source {:code "(defn pr-str*\n  [^not-native obj]\n  (let [sb (StringBuffer.)\n        writer (StringBufferWriter. sb)]\n    (-pr-writer obj writer (pr-opts))\n    (-flush writer)\n    (str sb)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r3148",
          :filename "src/cljs/cljs/core.cljs",
          :lines [645 653]},
 :full-name "cljs.core/pr-str*",
 :docstring "Support so that collections can implement toString without\nloading all the printing machinery."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/pr-str*"]))
```

-->
