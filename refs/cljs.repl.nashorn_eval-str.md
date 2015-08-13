## cljs.repl.nashorn/eval-str



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-2814"><img valign="middle" alt="[+] 0.0-2814" title="Added in 0.0-2814" src="https://img.shields.io/badge/+-0.0--2814-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__eval-str__ engine s)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r2985/src/clj/cljs/repl/nashorn.clj#L75-L76):

```clj
(defn eval-str [^ScriptEngine engine ^String s]
  (.eval engine s))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2985
└── src
    └── clj
        └── cljs
            └── repl
                └── <ins>[nashorn.clj:75-76](https://github.com/clojure/clojurescript/blob/r2985/src/clj/cljs/repl/nashorn.clj#L75-L76)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.repl.nashorn/eval-str` @ crossclj](http://crossclj.info/fun/cljs.repl.nashorn/eval-str.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.repl.nashorn_eval-str.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.repl.nashorn",
 :name "eval-str",
 :type "function",
 :signature ["[engine s]"],
 :source {:code "(defn eval-str [^ScriptEngine engine ^String s]\n  (.eval engine s))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2985",
          :filename "src/clj/cljs/repl/nashorn.clj",
          :lines [75 76]},
 :full-name "cljs.repl.nashorn/eval-str",
 :full-name-encode "cljs.repl.nashorn_eval-str",
 :history [["+" "0.0-2814"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.repl.nashorn/eval-str"]))
```

-->
