## cljs.core/IEncodeClojure



 <table border="1">
<tr>
<td>protocol</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1552"><img valign="middle" alt="[+] 0.0-1552" title="Added in 0.0-1552" src="https://img.shields.io/badge/+-0.0--1552-lightgrey.svg"></a> </td>
</tr>
</table>









Source code @ [github](https://github.com/clojure/clojurescript/blob/r1586/src/cljs/cljs/core.cljs#L6935-L6936):

```clj
(defprotocol IEncodeClojure
  (-js->clj [x] [x options] "Transforms JavaScript values to Clojure"))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1586
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:6935-6936](https://github.com/clojure/clojurescript/blob/r1586/src/cljs/cljs/core.cljs#L6935-L6936)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/IEncodeClojure` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/IEncodeClojure.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_IEncodeClojure.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "IEncodeClojure",
 :type "protocol",
 :full-name-encode "cljs.core_IEncodeClojure",
 :source {:code "(defprotocol IEncodeClojure\n  (-js->clj [x] [x options] \"Transforms JavaScript values to Clojure\"))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1586",
          :filename "src/cljs/cljs/core.cljs",
          :lines [6935 6936]},
 :methods [{:name "-js->clj",
            :signature ["[x]" "[x options]"],
            :docstring "Transforms JavaScript values to Clojure"}],
 :full-name "cljs.core/IEncodeClojure",
 :history [["+" "0.0-1552"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/IEncodeClojure"]))
```

-->
