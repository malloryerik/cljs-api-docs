## cljs.core/import-macros



 <table border="1">
<tr>
<td>macro</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__import-macros__ ns \[& vars\])<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r3291/src/main/clojure/cljs/core.clj#L48-L74):

```clj
(defmacro import-macros [ns [& vars]]
  (core/let [ns (find-ns ns)
             vars (map #(ns-resolve ns %) vars)
             syms (map
                    (core/fn [^clojure.lang.Var v]
                      (core/-> v .sym
                        (with-meta
                          (merge
                            {:macro true}
                            (update-in (select-keys (meta v) [:arglists :doc :file :line])
                              [:arglists] (core/fn [arglists] `(quote ~arglists)))))))
                    vars)
             defs (map
                    (core/fn [sym var]
                      (core/let [{:keys [arglists doc file line]} (meta sym)]
                        `(do
                           (def ~sym (deref ~var))
                           ;for AOT compilation
                           (alter-meta! (var ~sym) assoc
                             :macro true
                             :arglists ~arglists
                             :doc ~doc
                             :file ~file
                             :line ~line))))
                    syms vars)]
    `(do ~@defs
         :imported)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3291
└── src
    └── main
        └── clojure
            └── cljs
                └── <ins>[core.clj:48-74](https://github.com/clojure/clojurescript/blob/r3291/src/main/clojure/cljs/core.clj#L48-L74)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/import-macros` @ crossclj](http://crossclj.info/fun/cljs.core/import-macros.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_import-macros.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "import-macros",
 :type "macro",
 :signature ["[ns [& vars]]"],
 :source {:code "(defmacro import-macros [ns [& vars]]\n  (core/let [ns (find-ns ns)\n             vars (map #(ns-resolve ns %) vars)\n             syms (map\n                    (core/fn [^clojure.lang.Var v]\n                      (core/-> v .sym\n                        (with-meta\n                          (merge\n                            {:macro true}\n                            (update-in (select-keys (meta v) [:arglists :doc :file :line])\n                              [:arglists] (core/fn [arglists] `(quote ~arglists)))))))\n                    vars)\n             defs (map\n                    (core/fn [sym var]\n                      (core/let [{:keys [arglists doc file line]} (meta sym)]\n                        `(do\n                           (def ~sym (deref ~var))\n                           ;for AOT compilation\n                           (alter-meta! (var ~sym) assoc\n                             :macro true\n                             :arglists ~arglists\n                             :doc ~doc\n                             :file ~file\n                             :line ~line))))\n                    syms vars)]\n    `(do ~@defs\n         :imported)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r3291",
          :filename "src/main/clojure/cljs/core.clj",
          :lines [48 74]},
 :full-name "cljs.core/import-macros",
 :full-name-encode "cljs.core_import-macros",
 :history [["+" "0.0-927"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/import-macros"]))
```

-->
