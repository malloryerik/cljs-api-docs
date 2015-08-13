## cljs.core/println-str



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1011"><img valign="middle" alt="[+] 0.0-1011" title="Added in 0.0-1011" src="https://img.shields.io/badge/+-0.0--1011-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/println-str</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/println-str)
</td>
</tr>
</table>


 <samp>
(__println-str__ & objs)<br>
</samp>

---





Source docstring:

```
println to a string, returning it
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r2197/src/cljs/cljs/core.cljs#L6973-L6976):

```clj
(defn println-str
  [& objs]
  (prn-str-with-opts objs (assoc (pr-opts) :readably false)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2197
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:6973-6976](https://github.com/clojure/clojurescript/blob/r2197/src/cljs/cljs/core.cljs#L6973-L6976)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/println-str` @ clojuredocs](http://clojuredocs.org/clojure.core/println-str)<br>
[`clojure.core/println-str` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/println-str/)<br>
[`clojure.core/println-str` @ crossclj](http://crossclj.info/fun/clojure.core/println-str.html)<br>
[`cljs.core/println-str` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/println-str.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_println-str.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "println-str",
 :signature ["[& objs]"],
 :history [["+" "0.0-1011"]],
 :type "function",
 :full-name-encode "cljs.core_println-str",
 :source {:code "(defn println-str\n  [& objs]\n  (prn-str-with-opts objs (assoc (pr-opts) :readably false)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2197",
          :filename "src/cljs/cljs/core.cljs",
          :lines [6973 6976]},
 :full-name "cljs.core/println-str",
 :clj-symbol "clojure.core/println-str",
 :docstring "println to a string, returning it"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/println-str"]))
```

-->
