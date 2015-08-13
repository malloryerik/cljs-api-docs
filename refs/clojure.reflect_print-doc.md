## clojure.reflect/print-doc



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1503"><img valign="middle" alt="[+] 0.0-1503" title="Added in 0.0-1503" src="https://img.shields.io/badge/+-0.0--1503-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__print-doc__ {:keys \[name method-params doc\]})<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r1909/src/cljs/clojure/reflect.cljs#L38-L42):

```clj
(defn print-doc [{:keys [name method-params doc]}]
  (when-not (empty? name)
    (println name)
    (println method-params)
    (println doc)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1909
└── src
    └── cljs
        └── clojure
            └── <ins>[reflect.cljs:38-42](https://github.com/clojure/clojurescript/blob/r1909/src/cljs/clojure/reflect.cljs#L38-L42)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.reflect/print-doc` @ crossclj](http://crossclj.info/fun/clojure.reflect.cljs/print-doc.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/clojure.reflect_print-doc.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "clojure.reflect",
 :name "print-doc",
 :type "function",
 :signature ["[{:keys [name method-params doc]}]"],
 :source {:code "(defn print-doc [{:keys [name method-params doc]}]\n  (when-not (empty? name)\n    (println name)\n    (println method-params)\n    (println doc)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1909",
          :filename "src/cljs/clojure/reflect.cljs",
          :lines [38 42]},
 :full-name "clojure.reflect/print-doc",
 :full-name-encode "clojure.reflect_print-doc",
 :history [["+" "0.0-1503"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "clojure.reflect/print-doc"]))
```

-->
