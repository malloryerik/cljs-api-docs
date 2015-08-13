## cljs.repl.server/dispatch-on



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1503"><img valign="middle" alt="[+] 0.0-1503" title="Added in 0.0-1503" src="https://img.shields.io/badge/+-0.0--1503-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__dispatch-on__ method pred handler)<br>
</samp>
 <samp>
(__dispatch-on__ method {:as m})<br>
</samp>

---





Source docstring:

```
Registers a handler to be dispatched based on a request method and a
predicate.

pred should be a function that accepts an options map, a connection,
and a request map and returns a boolean value based on whether or not
that request should be dispatched to the related handler.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r2740/src/clj/cljs/repl/server.clj#L45-L57):

```clj
(defn dispatch-on
  ([method pred handler]
    (dispatch-on method {:pred pred :handler handler}))
  ([method {:as m}]
    (swap! handlers
      (fn [old]
        (update-in old [method] #(conj (vec %) m))))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2740
└── src
    └── clj
        └── cljs
            └── repl
                └── <ins>[server.clj:45-57](https://github.com/clojure/clojurescript/blob/r2740/src/clj/cljs/repl/server.clj#L45-L57)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.repl.server/dispatch-on` @ crossclj](http://crossclj.info/fun/cljs.repl.server/dispatch-on.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.repl.server_dispatch-on.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.repl.server",
 :name "dispatch-on",
 :signature ["[method pred handler]" "[method {:as m}]"],
 :history [["+" "0.0-1503"]],
 :type "function",
 :full-name-encode "cljs.repl.server_dispatch-on",
 :source {:code "(defn dispatch-on\n  ([method pred handler]\n    (dispatch-on method {:pred pred :handler handler}))\n  ([method {:as m}]\n    (swap! handlers\n      (fn [old]\n        (update-in old [method] #(conj (vec %) m))))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2740",
          :filename "src/clj/cljs/repl/server.clj",
          :lines [45 57]},
 :full-name "cljs.repl.server/dispatch-on",
 :docstring "Registers a handler to be dispatched based on a request method and a\npredicate.\n\npred should be a function that accepts an options map, a connection,\nand a request map and returns a boolean value based on whether or not\nthat request should be dispatched to the related handler."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.repl.server/dispatch-on"]))
```

-->
