## cljs.reader/read-raw-string\*



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-2261"><img valign="middle" alt="[+] 0.0-2261" title="Added in 0.0-2261" src="https://img.shields.io/badge/+-0.0--2261-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__read-raw-string\*__ reader _)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r2725/src/cljs/cljs/reader.cljs#L304-L317):

```clj
(defn read-raw-string*
  [reader _]
  (loop [buffer (gstring/StringBuffer.)
         ch (read-char reader)]
    (cond
      (nil? ch) (reader-error reader "EOF while reading")
      (identical? "\\" ch) (do (.append buffer ch)
                             (let [nch (read-char reader)]
                               (if (nil? nch)
                                 (reader-error reader "EOF while reading")
                                 (recur (doto buffer (.append nch))
                                        (read-char reader)))))
      (identical? "\"" ch) (.toString buffer)
      :else (recur (doto buffer (.append ch)) (read-char reader)))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2725
└── src
    └── cljs
        └── cljs
            └── <ins>[reader.cljs:304-317](https://github.com/clojure/clojurescript/blob/r2725/src/cljs/cljs/reader.cljs#L304-L317)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.reader/read-raw-string*` @ crossclj](http://crossclj.info/fun/cljs.reader.cljs/read-raw-string*.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.reader_read-raw-stringSTAR.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.reader",
 :name "read-raw-string*",
 :type "function",
 :signature ["[reader _]"],
 :source {:code "(defn read-raw-string*\n  [reader _]\n  (loop [buffer (gstring/StringBuffer.)\n         ch (read-char reader)]\n    (cond\n      (nil? ch) (reader-error reader \"EOF while reading\")\n      (identical? \"\\\\\" ch) (do (.append buffer ch)\n                             (let [nch (read-char reader)]\n                               (if (nil? nch)\n                                 (reader-error reader \"EOF while reading\")\n                                 (recur (doto buffer (.append nch))\n                                        (read-char reader)))))\n      (identical? \"\\\"\" ch) (.toString buffer)\n      :else (recur (doto buffer (.append ch)) (read-char reader)))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2725",
          :filename "src/cljs/cljs/reader.cljs",
          :lines [304 317]},
 :full-name "cljs.reader/read-raw-string*",
 :full-name-encode "cljs.reader_read-raw-stringSTAR",
 :history [["+" "0.0-2261"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.reader/read-raw-string*"]))
```

-->
