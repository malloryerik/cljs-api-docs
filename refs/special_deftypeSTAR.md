## deftype\*



 <table border="1">
<tr>
<td>special form</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>









Parser code @ [github](https://github.com/clojure/clojurescript/blob/r1877/src/clj/cljs/analyzer.clj#L747-L759):

```clj
(defmethod parse 'deftype*
  [_ env [_ tsym fields pmasks :as form] _]
  (let [t (:name (resolve-var (dissoc env :locals) tsym))]
    (swap! namespaces update-in [(-> env :ns :name) :defs tsym]
           (fn [m]
             (let [m (assoc (or m {})
                       :name t
                       :type true
                       :num-fields (count fields))]
               (merge m
                 {:protocols (-> tsym meta :protocols)}
                 (source-info tsym env)))))
    {:env env :op :deftype* :form form :t t :fields fields :pmasks pmasks}))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1877
└── src
    └── clj
        └── cljs
            └── <ins>[analyzer.clj:747-759](https://github.com/clojure/clojurescript/blob/r1877/src/clj/cljs/analyzer.clj#L747-L759)</ins>
</pre>

-->

---




 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/special_deftypeSTAR.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "special",
 :name "deftype*",
 :type "special form",
 :source {:code "(defmethod parse 'deftype*\n  [_ env [_ tsym fields pmasks :as form] _]\n  (let [t (:name (resolve-var (dissoc env :locals) tsym))]\n    (swap! namespaces update-in [(-> env :ns :name) :defs tsym]\n           (fn [m]\n             (let [m (assoc (or m {})\n                       :name t\n                       :type true\n                       :num-fields (count fields))]\n               (merge m\n                 {:protocols (-> tsym meta :protocols)}\n                 (source-info tsym env)))))\n    {:env env :op :deftype* :form form :t t :fields fields :pmasks pmasks}))",
          :title "Parser code",
          :repo "clojurescript",
          :tag "r1877",
          :filename "src/clj/cljs/analyzer.clj",
          :lines [747 759]},
 :full-name "special/deftype*",
 :full-name-encode "special_deftypeSTAR",
 :history [["+" "0.0-927"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "special/deftype*"]))
```

-->
