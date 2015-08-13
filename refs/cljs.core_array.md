## cljs.core/array



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__array__ & args)<br>
</samp>

---

Creates a JavaScript array containing `args`.

The tagged literal `#js [1 2 3]` is equivalent to `(array 1 2 3)`

---

###### Examples:

```clj
(array 1 2 3)
;;=> #js [1 2 3]

(apply array [1 2 3])
;;=> #js [1 2 3]

#js [1 2 3]
;;=> #js [1 2 3]
```

---
###### Examples:

When creating nested JavaScript arrays, you can opt to use `clj->js` instead:

```clj
(array 1 2 (array 3 4))
;;=> #js [1 2 #js [3 4]]

(clj->js [1 2 [3 4]])
;;=> #js [1 2 #js [3 4]]
```

---

###### See Also:

[`cljs.core/aclone`](cljs.core_aclone.md)<br>
[`cljs.core/make-array`](cljs.core_make-array.md)<br>
[`cljs.core/clj->js`](cljs.core_clj-GTjs.md)<br>

---


Source docstring:

```
Creates a new javascript array.
@param {...*} var_args
```


Function code @ [github](https://github.com/clojure/clojurescript/blob/r2067/src/cljs/cljs/core.cljs#L150-L154):

```clj
(defn array
  [var-args]            ;; [& items]
  (.call (.-slice (.-prototype js/Array)) (cljs.core/js-arguments)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2067
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:150-154](https://github.com/clojure/clojurescript/blob/r2067/src/cljs/cljs/core.cljs#L150-L154)</ins>
</pre>

-->

---

Macro code @ [github](https://github.com/clojure/clojurescript/blob/r2067/src/clj/cljs/core.clj#L1283-L1288):

```clj
(defmacro array [& rest]
  (let [xs-str (->> (repeat "~{}")
                    (take (count rest))
                    (interpose ",")
                    (apply core/str))]
    (list* 'js* (core/str "[" xs-str "]") rest)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2067
└── src
    └── clj
        └── cljs
            └── <ins>[core.clj:1283-1288](https://github.com/clojure/clojurescript/blob/r2067/src/clj/cljs/core.clj#L1283-L1288)</ins>
</pre>
-->

---


###### External doc links:

[`cljs.core/array` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/array.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_array.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Creates a JavaScript array containing `args`.\n\nThe tagged literal `#js [1 2 3]` is equivalent to `(array 1 2 3)`",
 :ns "cljs.core",
 :name "array",
 :signature ["[& args]"],
 :history [["+" "0.0-927"]],
 :type "function",
 :related ["cljs.core/aclone"
           "cljs.core/make-array"
           "cljs.core/clj->js"],
 :full-name-encode "cljs.core_array",
 :source {:code "(defn array\n  [var-args]            ;; [& items]\n  (.call (.-slice (.-prototype js/Array)) (cljs.core/js-arguments)))",
          :title "Function code",
          :repo "clojurescript",
          :tag "r2067",
          :filename "src/cljs/cljs/core.cljs",
          :lines [150 154]},
 :extra-sources [{:code "(defmacro array [& rest]\n  (let [xs-str (->> (repeat \"~{}\")\n                    (take (count rest))\n                    (interpose \",\")\n                    (apply core/str))]\n    (list* 'js* (core/str \"[\" xs-str \"]\") rest)))",
                  :title "Macro code",
                  :repo "clojurescript",
                  :tag "r2067",
                  :filename "src/clj/cljs/core.clj",
                  :lines [1283 1288]}],
 :examples [{:id "3a546d",
             :content "```clj\n(array 1 2 3)\n;;=> #js [1 2 3]\n\n(apply array [1 2 3])\n;;=> #js [1 2 3]\n\n#js [1 2 3]\n;;=> #js [1 2 3]\n```"}
            {:id "cca945",
             :content "When creating nested JavaScript arrays, you can opt to use `clj->js` instead:\n\n```clj\n(array 1 2 (array 3 4))\n;;=> #js [1 2 #js [3 4]]\n\n(clj->js [1 2 [3 4]])\n;;=> #js [1 2 #js [3 4]]\n```"}],
 :full-name "cljs.core/array",
 :docstring "Creates a new javascript array.\n@param {...*} var_args"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/array"]))
```

-->
