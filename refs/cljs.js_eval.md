## cljs.js/eval



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/1.7.10"><img valign="middle" alt="[+] 1.7.10" title="Added in 1.7.10" src="https://img.shields.io/badge/+-1.7.10-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__eval__ state form cb)<br>
</samp>
 <samp>
(__eval__ state form opts cb)<br>
</samp>

---





Source docstring:

```
Evaluate a single ClojureScript form. The parameters:

state (atom)
  the compiler state

form (s-expr)
  the ClojureScript source

opts (map)
  compilation options.

  :eval - the eval function to invoke, see *eval-fn*
  :load - library resolution function, see *load-fn*

cb (function)
  callback, will be invoked with a map. If successful the map will contain
  a :value key with the result of evalution. If unsuccessful the map wil
  contain a :error key with an ex-info instance describing the cause of
  failure.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r1.7.58/src/main/cljs/cljs/js.cljs#L501-L531):

```clj
(defn eval
  ([state form cb]
   (eval state form nil cb))
  ([state form opts cb]
   (eval*
     {:*compiler*     state
      :*data-readers* tags/*cljs-data-readers*
      :*analyze-deps* (or (:analyze-deps opts) true)
      :*load-macros*  (or (:load-macros opts) true)
      :*load-fn*      (or (:load opts) *load-fn*)
      :*eval-fn*      (or (:eval opts) *eval-fn*)}
     form opts cb)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1.7.58
└── src
    └── main
        └── cljs
            └── cljs
                └── <ins>[js.cljs:501-531](https://github.com/clojure/clojurescript/blob/r1.7.58/src/main/cljs/cljs/js.cljs#L501-L531)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.js/eval` @ crossclj](http://crossclj.info/fun/cljs.js.cljs/eval.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.js_eval.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.js",
 :name "eval",
 :signature ["[state form cb]" "[state form opts cb]"],
 :history [["+" "1.7.10"]],
 :type "function",
 :full-name-encode "cljs.js_eval",
 :source {:code "(defn eval\n  ([state form cb]\n   (eval state form nil cb))\n  ([state form opts cb]\n   (eval*\n     {:*compiler*     state\n      :*data-readers* tags/*cljs-data-readers*\n      :*analyze-deps* (or (:analyze-deps opts) true)\n      :*load-macros*  (or (:load-macros opts) true)\n      :*load-fn*      (or (:load opts) *load-fn*)\n      :*eval-fn*      (or (:eval opts) *eval-fn*)}\n     form opts cb)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1.7.58",
          :filename "src/main/cljs/cljs/js.cljs",
          :lines [501 531]},
 :full-name "cljs.js/eval",
 :docstring "Evaluate a single ClojureScript form. The parameters:\n\nstate (atom)\n  the compiler state\n\nform (s-expr)\n  the ClojureScript source\n\nopts (map)\n  compilation options.\n\n  :eval - the eval function to invoke, see *eval-fn*\n  :load - library resolution function, see *load-fn*\n\ncb (function)\n  callback, will be invoked with a map. If successful the map will contain\n  a :value key with the result of evalution. If unsuccessful the map wil\n  contain a :error key with an ex-info instance describing the cause of\n  failure."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.js/eval"]))
```

-->
