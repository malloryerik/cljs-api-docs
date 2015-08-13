## do



 <table border="1">
<tr>
<td>special form</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/do</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/do)
</td>
</tr>
</table>


 <samp>
(__do__ exprs\*)<br>
</samp>

---





Source docstring:

```
Evaluates the expressions in order and returns the value of
the last. If no expressions are supplied, returns nil.
```


Parser code @ [github](https://github.com/clojure/clojurescript/blob/r3196/src/clj/cljs/analyzer.clj#L1063-L1072):

```clj
(defmethod parse 'do
  [op env [_ & exprs :as form] _ _]
  (let [statements (disallowing-recur
                     (seq (map #(analyze (assoc env :context :statement) %) (butlast exprs))))
        ret (if (<= (count exprs) 1)
              (analyze env (first exprs))
              (analyze (assoc env :context (if (= :statement (:context env)) :statement :return)) (last exprs)))]
    {:env env :op :do :form form
     :statements statements :ret ret
     :children (conj (vec statements) ret)}))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3196
└── src
    └── clj
        └── cljs
            └── <ins>[analyzer.clj:1063-1072](https://github.com/clojure/clojurescript/blob/r3196/src/clj/cljs/analyzer.clj#L1063-L1072)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/do` @ clojuredocs](http://clojuredocs.org/clojure.core/do)<br>
[`clojure.core/do` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/do/)<br>
[`clojure.core/do` @ crossclj](http://crossclj.info/fun/clojure.core/do.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/special_do.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "special",
 :name "do",
 :signature ["[exprs*]"],
 :history [["+" "0.0-927"]],
 :type "special form",
 :full-name-encode "special_do",
 :source {:code "(defmethod parse 'do\n  [op env [_ & exprs :as form] _ _]\n  (let [statements (disallowing-recur\n                     (seq (map #(analyze (assoc env :context :statement) %) (butlast exprs))))\n        ret (if (<= (count exprs) 1)\n              (analyze env (first exprs))\n              (analyze (assoc env :context (if (= :statement (:context env)) :statement :return)) (last exprs)))]\n    {:env env :op :do :form form\n     :statements statements :ret ret\n     :children (conj (vec statements) ret)}))",
          :title "Parser code",
          :repo "clojurescript",
          :tag "r3196",
          :filename "src/clj/cljs/analyzer.clj",
          :lines [1063 1072]},
 :full-name "special/do",
 :clj-symbol "clojure.core/do",
 :docstring "Evaluates the expressions in order and returns the value of\nthe last. If no expressions are supplied, returns nil."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "special/do"]))
```

-->
