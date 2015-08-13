## cljs.reader/wrapping-reader



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__wrapping-reader__ sym)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r2134/src/cljs/cljs/reader.cljs#L349-L352):

```clj
(defn wrapping-reader
  [sym]
  (fn [rdr _]
    (list sym (read rdr true nil true))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2134
└── src
    └── cljs
        └── cljs
            └── <ins>[reader.cljs:349-352](https://github.com/clojure/clojurescript/blob/r2134/src/cljs/cljs/reader.cljs#L349-L352)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.reader/wrapping-reader` @ crossclj](http://crossclj.info/fun/cljs.reader.cljs/wrapping-reader.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.reader_wrapping-reader.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.reader",
 :name "wrapping-reader",
 :type "function",
 :signature ["[sym]"],
 :source {:code "(defn wrapping-reader\n  [sym]\n  (fn [rdr _]\n    (list sym (read rdr true nil true))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2134",
          :filename "src/cljs/cljs/reader.cljs",
          :lines [349 352]},
 :full-name "cljs.reader/wrapping-reader",
 :full-name-encode "cljs.reader_wrapping-reader",
 :history [["+" "0.0-927"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.reader/wrapping-reader"]))
```

-->
