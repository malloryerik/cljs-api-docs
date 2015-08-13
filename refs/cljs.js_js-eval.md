## cljs.js/js-eval



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/1.7.10"><img valign="middle" alt="[+] 1.7.10" title="Added in 1.7.10" src="https://img.shields.io/badge/+-1.7.10-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__js-eval__ {:keys \[source\], :as resource})<br>
</samp>

---





Source docstring:

```
A default JavaScript evaluation function.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r1.7.28/src/main/cljs/cljs/js.cljs#L95-L98):

```clj
(defn js-eval
  [{:keys [source] :as resource}]
  (js/eval source))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1.7.28
└── src
    └── main
        └── cljs
            └── cljs
                └── <ins>[js.cljs:95-98](https://github.com/clojure/clojurescript/blob/r1.7.28/src/main/cljs/cljs/js.cljs#L95-L98)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.js/js-eval` @ crossclj](http://crossclj.info/fun/cljs.js.cljs/js-eval.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.js_js-eval.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.js",
 :name "js-eval",
 :signature ["[{:keys [source], :as resource}]"],
 :history [["+" "1.7.10"]],
 :type "function",
 :full-name-encode "cljs.js_js-eval",
 :source {:code "(defn js-eval\n  [{:keys [source] :as resource}]\n  (js/eval source))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1.7.28",
          :filename "src/main/cljs/cljs/js.cljs",
          :lines [95 98]},
 :full-name "cljs.js/js-eval",
 :docstring "A default JavaScript evaluation function."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.js/js-eval"]))
```

-->
