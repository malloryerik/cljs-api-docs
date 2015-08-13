## cljs.reader/read-delimited-list



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__read-delimited-list__ delim rdr recursive?)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r1006/src/cljs/cljs/reader.cljs#L168-L181):

```clj
(defn read-delimited-list
  [delim rdr recursive?]
  (loop [a []]
    (let [ch (read-past whitespace? rdr)]
      (when-not ch (reader-error rdr "EOF"))
      (if (= delim ch)
        a
        (if-let [macrofn (get macros ch)]
          (let [mret (macrofn rdr ch)]
            (recur (if (= mret rdr) a (conj a mret))))
          (do
            (unread rdr ch)
            (let [o (read rdr true nil recursive?)]
              (recur (if (= o rdr) a (conj a o))))))))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1006
└── src
    └── cljs
        └── cljs
            └── <ins>[reader.cljs:168-181](https://github.com/clojure/clojurescript/blob/r1006/src/cljs/cljs/reader.cljs#L168-L181)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.reader/read-delimited-list` @ crossclj](http://crossclj.info/fun/cljs.reader.cljs/read-delimited-list.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.reader_read-delimited-list.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.reader",
 :name "read-delimited-list",
 :type "function",
 :signature ["[delim rdr recursive?]"],
 :source {:code "(defn read-delimited-list\n  [delim rdr recursive?]\n  (loop [a []]\n    (let [ch (read-past whitespace? rdr)]\n      (when-not ch (reader-error rdr \"EOF\"))\n      (if (= delim ch)\n        a\n        (if-let [macrofn (get macros ch)]\n          (let [mret (macrofn rdr ch)]\n            (recur (if (= mret rdr) a (conj a mret))))\n          (do\n            (unread rdr ch)\n            (let [o (read rdr true nil recursive?)]\n              (recur (if (= o rdr) a (conj a o))))))))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1006",
          :filename "src/cljs/cljs/reader.cljs",
          :lines [168 181]},
 :full-name "cljs.reader/read-delimited-list",
 :full-name-encode "cljs.reader_read-delimited-list",
 :history [["+" "0.0-927"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.reader/read-delimited-list"]))
```

-->
