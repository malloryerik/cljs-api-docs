## cljs.repl.rhino/rhino-setup



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__rhino-setup__ repl-env opts)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r2911/src/clj/cljs/repl/rhino.clj#L118-L130):

```clj
(defn rhino-setup [repl-env opts]
  (let [env   (ana/empty-env)
        scope (:scope repl-env)]
    (ScriptableObject/putProperty scope "__repl_opts"
      (Context/javaToJS opts scope))
    (repl/load-file repl-env "cljs/core.cljs" opts)
    (ScriptableObject/putProperty scope
      "out" (Context/javaToJS *out* scope))
    (binding [ana/*cljs-ns* 'cljs.core]
      (repl/evaluate-form repl-env env "<cljs repl>"
        '(do
           (set! (.-isProvided_ js/goog) (fn [_] false))
           (set! *print-fn* (fn [x] (.write js/out x))))))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2911
└── src
    └── clj
        └── cljs
            └── repl
                └── <ins>[rhino.clj:118-130](https://github.com/clojure/clojurescript/blob/r2911/src/clj/cljs/repl/rhino.clj#L118-L130)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.repl.rhino/rhino-setup` @ crossclj](http://crossclj.info/fun/cljs.repl.rhino/rhino-setup.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.repl.rhino_rhino-setup.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.repl.rhino",
 :name "rhino-setup",
 :type "function",
 :signature ["[repl-env opts]"],
 :source {:code "(defn rhino-setup [repl-env opts]\n  (let [env   (ana/empty-env)\n        scope (:scope repl-env)]\n    (ScriptableObject/putProperty scope \"__repl_opts\"\n      (Context/javaToJS opts scope))\n    (repl/load-file repl-env \"cljs/core.cljs\" opts)\n    (ScriptableObject/putProperty scope\n      \"out\" (Context/javaToJS *out* scope))\n    (binding [ana/*cljs-ns* 'cljs.core]\n      (repl/evaluate-form repl-env env \"<cljs repl>\"\n        '(do\n           (set! (.-isProvided_ js/goog) (fn [_] false))\n           (set! *print-fn* (fn [x] (.write js/out x))))))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2911",
          :filename "src/clj/cljs/repl/rhino.clj",
          :lines [118 130]},
 :full-name "cljs.repl.rhino/rhino-setup",
 :full-name-encode "cljs.repl.rhino_rhino-setup",
 :history [["+" "0.0-927"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.repl.rhino/rhino-setup"]))
```

-->
