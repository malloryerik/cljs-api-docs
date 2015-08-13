## cljs.reader/reader-error



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__reader-error__ rdr & msg)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r2067/src/cljs/cljs/reader.cljs#L68-L70):

```clj
(defn reader-error
  [rdr & msg]
  (throw (js/Error. (apply str msg))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2067
└── src
    └── cljs
        └── cljs
            └── <ins>[reader.cljs:68-70](https://github.com/clojure/clojurescript/blob/r2067/src/cljs/cljs/reader.cljs#L68-L70)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.reader/reader-error` @ crossclj](http://crossclj.info/fun/cljs.reader.cljs/reader-error.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.reader_reader-error.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.reader",
 :name "reader-error",
 :type "function",
 :signature ["[rdr & msg]"],
 :source {:code "(defn reader-error\n  [rdr & msg]\n  (throw (js/Error. (apply str msg))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2067",
          :filename "src/cljs/cljs/reader.cljs",
          :lines [68 70]},
 :full-name "cljs.reader/reader-error",
 :full-name-encode "cljs.reader_reader-error",
 :history [["+" "0.0-927"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.reader/reader-error"]))
```

-->
