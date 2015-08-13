## cljs.repl.nashorn/load-js-file



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-2814"><img valign="middle" alt="[+] 0.0-2814" title="Added in 0.0-2814" src="https://img.shields.io/badge/+-0.0--2814-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__load-js-file__ engine file)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r1.7.10/src/main/clojure/cljs/repl/nashorn.clj#L75-L76):

```clj
(defn load-js-file [engine file]
      (eval-str engine (format "nashorn_load(\"%s\");" file)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1.7.10
└── src
    └── main
        └── clojure
            └── cljs
                └── repl
                    └── <ins>[nashorn.clj:75-76](https://github.com/clojure/clojurescript/blob/r1.7.10/src/main/clojure/cljs/repl/nashorn.clj#L75-L76)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.repl.nashorn/load-js-file` @ crossclj](http://crossclj.info/fun/cljs.repl.nashorn/load-js-file.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.repl.nashorn_load-js-file.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.repl.nashorn",
 :name "load-js-file",
 :type "function",
 :signature ["[engine file]"],
 :source {:code "(defn load-js-file [engine file]\n      (eval-str engine (format \"nashorn_load(\\\"%s\\\");\" file)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1.7.10",
          :filename "src/main/clojure/cljs/repl/nashorn.clj",
          :lines [75 76]},
 :full-name "cljs.repl.nashorn/load-js-file",
 :full-name-encode "cljs.repl.nashorn_load-js-file",
 :history [["+" "0.0-2814"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.repl.nashorn/load-js-file"]))
```

-->
