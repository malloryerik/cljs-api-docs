## cljs.repl/load-namespace



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__load-namespace__ repl-env sym)<br>
</samp>
 <samp>
(__load-namespace__ repl-env sym opts)<br>
</samp>

---





Source docstring:

```
Load a namespace and all of its dependencies into the evaluation environment.
The environment is responsible for ensuring that each namespace is loaded once and
only once.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r3117/src/clj/cljs/repl.clj#L162-L191):

```clj
(defn load-namespace
  ([repl-env sym] (load-namespace repl-env sym nil))
  ([repl-env sym opts]
   (let [sym      (if (and (seq? sym)
                        (= (first sym) 'quote))
                    (second sym)
                    sym)
         ;; TODO: add pre-condition to source-on-disk, the
         ;; source must supply at least :url - David
         sources  (cljsc/add-dependencies
                    (merge (env->opts repl-env) opts)
                    {:requires [(name sym)] :type :seed
                     :url (:uri (cljsc/source-for-namespace
                                  sym env/*compiler*))})
         deps     (->> sources
                    (remove (comp #{["goog"]} :provides))
                    (remove (comp #{:seed} :type))
                    (map #(select-keys % [:provides :url])))]
     (if (:output-dir opts)
       ;; REPLs that read from :output-dir just need to add deps,
       ;; environment will handle actual loading - David
       (doseq [source (map #(cljsc/source-on-disk opts %) sources)]
         (-evaluate repl-env "<cljs repl>" 1
           (cljsc/add-dep-string opts source)))
       ;; REPLs that stream must manually load each dep - David
       (doseq [{:keys [url provides]} deps]
         (-load repl-env provides url))))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3117
└── src
    └── clj
        └── cljs
            └── <ins>[repl.clj:162-191](https://github.com/clojure/clojurescript/blob/r3117/src/clj/cljs/repl.clj#L162-L191)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.repl/load-namespace` @ crossclj](http://crossclj.info/fun/cljs.repl/load-namespace.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.repl_load-namespace.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.repl",
 :name "load-namespace",
 :signature ["[repl-env sym]" "[repl-env sym opts]"],
 :history [["+" "0.0-927"]],
 :type "function",
 :full-name-encode "cljs.repl_load-namespace",
 :source {:code "(defn load-namespace\n  ([repl-env sym] (load-namespace repl-env sym nil))\n  ([repl-env sym opts]\n   (let [sym      (if (and (seq? sym)\n                        (= (first sym) 'quote))\n                    (second sym)\n                    sym)\n         ;; TODO: add pre-condition to source-on-disk, the\n         ;; source must supply at least :url - David\n         sources  (cljsc/add-dependencies\n                    (merge (env->opts repl-env) opts)\n                    {:requires [(name sym)] :type :seed\n                     :url (:uri (cljsc/source-for-namespace\n                                  sym env/*compiler*))})\n         deps     (->> sources\n                    (remove (comp #{[\"goog\"]} :provides))\n                    (remove (comp #{:seed} :type))\n                    (map #(select-keys % [:provides :url])))]\n     (if (:output-dir opts)\n       ;; REPLs that read from :output-dir just need to add deps,\n       ;; environment will handle actual loading - David\n       (doseq [source (map #(cljsc/source-on-disk opts %) sources)]\n         (-evaluate repl-env \"<cljs repl>\" 1\n           (cljsc/add-dep-string opts source)))\n       ;; REPLs that stream must manually load each dep - David\n       (doseq [{:keys [url provides]} deps]\n         (-load repl-env provides url))))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r3117",
          :filename "src/clj/cljs/repl.clj",
          :lines [162 191]},
 :full-name "cljs.repl/load-namespace",
 :docstring "Load a namespace and all of its dependencies into the evaluation environment.\nThe environment is responsible for ensuring that each namespace is loaded once and\nonly once."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.repl/load-namespace"]))
```

-->
