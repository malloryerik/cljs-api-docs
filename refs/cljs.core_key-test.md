## cljs.core/key-test



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1424"><img valign="middle" alt="[+] 0.0-1424" title="Added in 0.0-1424" src="https://img.shields.io/badge/+-0.0--1424-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__key-test__ key other)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r1798/src/cljs/cljs/core.cljs#L4083-L4086):

```clj
(defn ^boolean key-test [key other]
  (if ^boolean (goog/isString key)
    (identical? key other)
    (= key other)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1798
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:4083-4086](https://github.com/clojure/clojurescript/blob/r1798/src/cljs/cljs/core.cljs#L4083-L4086)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/key-test` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/key-test.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_key-test.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:return-type boolean,
 :ns "cljs.core",
 :name "key-test",
 :signature ["[key other]"],
 :history [["+" "0.0-1424"]],
 :type "function",
 :full-name-encode "cljs.core_key-test",
 :source {:code "(defn ^boolean key-test [key other]\n  (if ^boolean (goog/isString key)\n    (identical? key other)\n    (= key other)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1798",
          :filename "src/cljs/cljs/core.cljs",
          :lines [4083 4086]},
 :full-name "cljs.core/key-test"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/key-test"]))
```

-->
