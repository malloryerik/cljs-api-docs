## cljs.core/macroexpand-1



 <table border="1">
<tr>
<td>macro</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-3165"><img valign="middle" alt="[+] 0.0-3165" title="Added in 0.0-3165" src="https://img.shields.io/badge/+-0.0--3165-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/macroexpand-1</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/macroexpand-1)
</td>
</tr>
</table>


 <samp>
(__macroexpand-1__ quoted)<br>
</samp>

---





Source docstring:

```
If form represents a macro form, returns its expansion,
else returns form.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r1.7.28/src/main/clojure/cljs/core.cljc#L2554-L2561):

```clj
(core/defmacro macroexpand-1
  [quoted]
  (core/assert (core/= (core/first quoted) 'quote)
    "Argument to macroexpand-1 must be quoted")
  (core/let [form (second quoted)]
    `(quote ~(ana/macroexpand-1 &env form))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1.7.28
└── src
    └── main
        └── clojure
            └── cljs
                └── <ins>[core.cljc:2554-2561](https://github.com/clojure/clojurescript/blob/r1.7.28/src/main/clojure/cljs/core.cljc#L2554-L2561)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/macroexpand-1` @ clojuredocs](http://clojuredocs.org/clojure.core/macroexpand-1)<br>
[`clojure.core/macroexpand-1` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/macroexpand-1/)<br>
[`clojure.core/macroexpand-1` @ crossclj](http://crossclj.info/fun/clojure.core/macroexpand-1.html)<br>
[`cljs.core/macroexpand-1` @ crossclj](http://crossclj.info/fun/cljs.core/macroexpand-1.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_macroexpand-1.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "macroexpand-1",
 :signature ["[quoted]"],
 :history [["+" "0.0-3165"]],
 :type "macro",
 :full-name-encode "cljs.core_macroexpand-1",
 :source {:code "(core/defmacro macroexpand-1\n  [quoted]\n  (core/assert (core/= (core/first quoted) 'quote)\n    \"Argument to macroexpand-1 must be quoted\")\n  (core/let [form (second quoted)]\n    `(quote ~(ana/macroexpand-1 &env form))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1.7.28",
          :filename "src/main/clojure/cljs/core.cljc",
          :lines [2554 2561]},
 :full-name "cljs.core/macroexpand-1",
 :clj-symbol "clojure.core/macroexpand-1",
 :docstring "If form represents a macro form, returns its expansion,\nelse returns form."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/macroexpand-1"]))
```

-->
