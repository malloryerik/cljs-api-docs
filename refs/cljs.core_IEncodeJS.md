## cljs.core/IEncodeJS



 <table border="1">
<tr>
<td>protocol</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1552"><img valign="middle" alt="[+] 0.0-1552" title="Added in 0.0-1552" src="https://img.shields.io/badge/+-0.0--1552-lightgrey.svg"></a> </td>
</tr>
</table>









Source code @ [github](https://github.com/clojure/clojurescript/blob/r2080/src/cljs/cljs/core.cljs#L7133-L7136):

```clj
(defprotocol IEncodeJS
  (-clj->js [x] "Recursively transforms clj values to JavaScript")
  (-key->js [x] "Transforms map keys to valid JavaScript keys. Arbitrary keys are
  encoded to their string representation via (pr-str x)"))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2080
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:7133-7136](https://github.com/clojure/clojurescript/blob/r2080/src/cljs/cljs/core.cljs#L7133-L7136)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/IEncodeJS` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/IEncodeJS.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_IEncodeJS.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "IEncodeJS",
 :type "protocol",
 :full-name-encode "cljs.core_IEncodeJS",
 :source {:code "(defprotocol IEncodeJS\n  (-clj->js [x] \"Recursively transforms clj values to JavaScript\")\n  (-key->js [x] \"Transforms map keys to valid JavaScript keys. Arbitrary keys are\n  encoded to their string representation via (pr-str x)\"))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2080",
          :filename "src/cljs/cljs/core.cljs",
          :lines [7133 7136]},
 :methods [{:name "-clj->js",
            :signature ["[x]"],
            :docstring "Recursively transforms clj values to JavaScript"}
           {:name "-key->js",
            :signature ["[x]"],
            :docstring "Transforms map keys to valid JavaScript keys. Arbitrary keys are\n  encoded to their string representation via (pr-str x)"}],
 :full-name "cljs.core/IEncodeJS",
 :history [["+" "0.0-1552"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/IEncodeJS"]))
```

-->
