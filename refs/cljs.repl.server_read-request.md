## cljs.repl.server/read-request



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1503"><img valign="middle" alt="[+] 0.0-1503" title="Added in 0.0-1503" src="https://img.shields.io/badge/+-0.0--1503-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__read-request__ rdr)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r3178/src/clj/cljs/repl/server.clj#L92-L97):

```clj
(defn read-request [rdr]
  (let [line (.readLine rdr)]
    (cond
      (.startsWith line "POST") (read-post line rdr)
      (.startsWith line "GET") (read-get line rdr)
      :else {:method :unknown :content line})))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3178
└── src
    └── clj
        └── cljs
            └── repl
                └── <ins>[server.clj:92-97](https://github.com/clojure/clojurescript/blob/r3178/src/clj/cljs/repl/server.clj#L92-L97)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.repl.server/read-request` @ crossclj](http://crossclj.info/fun/cljs.repl.server/read-request.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.repl.server_read-request.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.repl.server",
 :name "read-request",
 :type "function",
 :signature ["[rdr]"],
 :source {:code "(defn read-request [rdr]\n  (let [line (.readLine rdr)]\n    (cond\n      (.startsWith line \"POST\") (read-post line rdr)\n      (.startsWith line \"GET\") (read-get line rdr)\n      :else {:method :unknown :content line})))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r3178",
          :filename "src/clj/cljs/repl/server.clj",
          :lines [92 97]},
 :full-name "cljs.repl.server/read-request",
 :full-name-encode "cljs.repl.server_read-request",
 :history [["+" "0.0-1503"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.repl.server/read-request"]))
```

-->
