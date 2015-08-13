## if



 <table border="1">
<tr>
<td>special form</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/if</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/if)
</td>
</tr>
</table>


 <samp>
(__if__ test then else?)<br>
</samp>

---

If `test` is not false or nil, `then` is evaluated and returned. Otherwise,
`else?` is evaluated and returned. `else?` defaults to nil if not provided.

`if` is one of ClojureScript's [special forms](http://clojure.org/special_forms)
and is a fundamental building block of the language. All other conditionals in
ClojureScript are based on `if`s notion of truthiness (ie: anything other than
false or nil).

---

###### Examples:

```clj
(def v [1 2])

(if (empty? v) "empty!" "filled!")
;;=> "filled!"

(str "This vector is "
  (if (empty? v) "empty!" "filled!"))
;;=> "This vector is filled!"
```

---

###### See Also:

[`cljs.core/cond`](cljs.core_cond.md)<br>
[`cljs.core/when`](cljs.core_when.md)<br>
[`cljs.core/if-let`](cljs.core_if-let.md)<br>
[`cljs.core/if-not`](cljs.core_if-not.md)<br>

---


Source docstring:

```
Evaluates test. If not the singular values nil or false,
evaluates and yields then, otherwise, evaluates and yields else. If
else is not supplied it defaults to nil.
```


Parser code @ [github](https://github.com/clojure/clojurescript/blob/r3148/src/clj/cljs/analyzer.clj#L674-L684):

```clj
(defmethod parse 'if
  [op env [_ test then else :as form] name _]
  (when (< (count form) 3)
    (throw (error env "Too few arguments to if")))
  (let [test-expr (disallowing-recur (analyze (assoc env :context :expr) test))
        then-expr (allowing-redef (analyze env then))
        else-expr (allowing-redef (analyze env else))]
    {:env env :op :if :form form
     :test test-expr :then then-expr :else else-expr
     :unchecked @*unchecked-if*
     :children [test-expr then-expr else-expr]}))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3148
└── src
    └── clj
        └── cljs
            └── <ins>[analyzer.clj:674-684](https://github.com/clojure/clojurescript/blob/r3148/src/clj/cljs/analyzer.clj#L674-L684)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/if` @ clojuredocs](http://clojuredocs.org/clojure.core/if)<br>
[`clojure.core/if` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/if/)<br>
[`clojure.core/if` @ crossclj](http://crossclj.info/fun/clojure.core/if.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/special_if.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "If `test` is not false or nil, `then` is evaluated and returned. Otherwise,\n`else?` is evaluated and returned. `else?` defaults to nil if not provided.\n\n`if` is one of ClojureScript's [special forms](http://clojure.org/special_forms)\nand is a fundamental building block of the language. All other conditionals in\nClojureScript are based on `if`s notion of truthiness (ie: anything other than\nfalse or nil).",
 :ns "special",
 :name "if",
 :signature ["[test then else?]"],
 :history [["+" "0.0-927"]],
 :type "special form",
 :related ["cljs.core/cond"
           "cljs.core/when"
           "cljs.core/if-let"
           "cljs.core/if-not"],
 :full-name-encode "special_if",
 :source {:code "(defmethod parse 'if\n  [op env [_ test then else :as form] name _]\n  (when (< (count form) 3)\n    (throw (error env \"Too few arguments to if\")))\n  (let [test-expr (disallowing-recur (analyze (assoc env :context :expr) test))\n        then-expr (allowing-redef (analyze env then))\n        else-expr (allowing-redef (analyze env else))]\n    {:env env :op :if :form form\n     :test test-expr :then then-expr :else else-expr\n     :unchecked @*unchecked-if*\n     :children [test-expr then-expr else-expr]}))",
          :title "Parser code",
          :repo "clojurescript",
          :tag "r3148",
          :filename "src/clj/cljs/analyzer.clj",
          :lines [674 684]},
 :examples [{:id "e591ff",
             :content "```clj\n(def v [1 2])\n\n(if (empty? v) \"empty!\" \"filled!\")\n;;=> \"filled!\"\n\n(str \"This vector is \"\n  (if (empty? v) \"empty!\" \"filled!\"))\n;;=> \"This vector is filled!\"\n```"}],
 :full-name "special/if",
 :clj-symbol "clojure.core/if",
 :docstring "Evaluates test. If not the singular values nil or false,\nevaluates and yields then, otherwise, evaluates and yields else. If\nelse is not supplied it defaults to nil."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "special/if"]))
```

-->
