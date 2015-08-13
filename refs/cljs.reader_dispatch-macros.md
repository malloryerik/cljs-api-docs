## cljs.reader/dispatch-macros



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__dispatch-macros__ s)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r1820/src/cljs/cljs/reader.cljs#L406-L413):

```clj
(defn dispatch-macros [s]
  (cond
   (identical? s "{") read-set
   (identical? s "<") (throwing-reader "Unreadable form")
   (identical? s "\"") read-regex
   (identical? s"!") read-comment
   (identical? s "_") read-discard
   :else nil))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1820
└── src
    └── cljs
        └── cljs
            └── <ins>[reader.cljs:406-413](https://github.com/clojure/clojurescript/blob/r1820/src/cljs/cljs/reader.cljs#L406-L413)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.reader/dispatch-macros` @ crossclj](http://crossclj.info/fun/cljs.reader.cljs/dispatch-macros.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.reader_dispatch-macros.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.reader",
 :name "dispatch-macros",
 :type "function",
 :signature ["[s]"],
 :source {:code "(defn dispatch-macros [s]\n  (cond\n   (identical? s \"{\") read-set\n   (identical? s \"<\") (throwing-reader \"Unreadable form\")\n   (identical? s \"\\\"\") read-regex\n   (identical? s\"!\") read-comment\n   (identical? s \"_\") read-discard\n   :else nil))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1820",
          :filename "src/cljs/cljs/reader.cljs",
          :lines [406 413]},
 :full-name "cljs.reader/dispatch-macros",
 :full-name-encode "cljs.reader_dispatch-macros",
 :history [["+" "0.0-927"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.reader/dispatch-macros"]))
```

-->
