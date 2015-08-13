## cljs.js/load-source-map!



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/1.7.10"><img valign="middle" alt="[+] 1.7.10" title="Added in 1.7.10" src="https://img.shields.io/badge/+-1.7.10-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__load-source-map!__ state ns sm-json)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r1.7.48/src/main/cljs/cljs/js.cljs#L118-L120):

```clj
(defn load-source-map! [state ns sm-json]
  (let [sm (sm/decode (.parse js/JSON sm-json))]
    (swap! state assoc-in [:source-maps ns] sm)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1.7.48
└── src
    └── main
        └── cljs
            └── cljs
                └── <ins>[js.cljs:118-120](https://github.com/clojure/clojurescript/blob/r1.7.48/src/main/cljs/cljs/js.cljs#L118-L120)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.js/load-source-map!` @ crossclj](http://crossclj.info/fun/cljs.js.cljs/load-source-map%21.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.js_load-source-mapBANG.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.js",
 :name "load-source-map!",
 :type "function",
 :signature ["[state ns sm-json]"],
 :source {:code "(defn load-source-map! [state ns sm-json]\n  (let [sm (sm/decode (.parse js/JSON sm-json))]\n    (swap! state assoc-in [:source-maps ns] sm)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1.7.48",
          :filename "src/main/cljs/cljs/js.cljs",
          :lines [118 120]},
 :full-name "cljs.js/load-source-map!",
 :full-name-encode "cljs.js_load-source-mapBANG",
 :history [["+" "1.7.10"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.js/load-source-map!"]))
```

-->
