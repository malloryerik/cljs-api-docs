## cljs.core/ensure-reduced



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-2411"><img valign="middle" alt="[+] 0.0-2411" title="Added in 0.0-2411" src="https://img.shields.io/badge/+-0.0--2411-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__ensure-reduced__ x)<br>
</samp>

---





Source docstring:

```
If x is already reduced?, returns it, else returns (reduced x)
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r2843/src/cljs/cljs/core.cljs#L908-L911):

```clj
(defn ensure-reduced
  [x]
  (if (reduced? x) x (reduced x)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2843
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:908-911](https://github.com/clojure/clojurescript/blob/r2843/src/cljs/cljs/core.cljs#L908-L911)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/ensure-reduced` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/ensure-reduced.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_ensure-reduced.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "ensure-reduced",
 :signature ["[x]"],
 :history [["+" "0.0-2411"]],
 :type "function",
 :full-name-encode "cljs.core_ensure-reduced",
 :source {:code "(defn ensure-reduced\n  [x]\n  (if (reduced? x) x (reduced x)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2843",
          :filename "src/cljs/cljs/core.cljs",
          :lines [908 911]},
 :full-name "cljs.core/ensure-reduced",
 :docstring "If x is already reduced?, returns it, else returns (reduced x)"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/ensure-reduced"]))
```

-->
