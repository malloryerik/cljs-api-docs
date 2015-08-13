## cljs.core/multi-stepper



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-2301"><img valign="middle" alt="[+] 0.0-2301" title="Added in 0.0-2301" src="https://img.shields.io/badge/+-0.0--2301-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__multi-stepper__ xform iters)<br>
</samp>
 <samp>
(__multi-stepper__ xform iters nexts)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r2725/src/cljs/cljs/core.cljs#L3181-L3199):

```clj
(defn multi-stepper
  ([xform iters]
     (multi-stepper xform iters
       (make-array (alength iters))))
  ([xform iters nexts]
     (letfn [(stepfn
               ([result]
                  (let [lt (if (reduced? result)
                             @result
                             result)]
                    (set! (.-stepper lt) nil)
                    lt))
               ([result input]
                  (let [lt result]
                    (set! (.-first lt) input)
                    (set! (.-rest lt) (lazy-transformer (.-stepper lt)))
                    (set! (.-stepper lt) nil)
                    (.-rest lt))))]
       (MultiStepper. (xform stepfn) iters nexts))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2725
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:3181-3199](https://github.com/clojure/clojurescript/blob/r2725/src/cljs/cljs/core.cljs#L3181-L3199)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/multi-stepper` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/multi-stepper.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_multi-stepper.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "multi-stepper",
 :type "function",
 :signature ["[xform iters]" "[xform iters nexts]"],
 :source {:code "(defn multi-stepper\n  ([xform iters]\n     (multi-stepper xform iters\n       (make-array (alength iters))))\n  ([xform iters nexts]\n     (letfn [(stepfn\n               ([result]\n                  (let [lt (if (reduced? result)\n                             @result\n                             result)]\n                    (set! (.-stepper lt) nil)\n                    lt))\n               ([result input]\n                  (let [lt result]\n                    (set! (.-first lt) input)\n                    (set! (.-rest lt) (lazy-transformer (.-stepper lt)))\n                    (set! (.-stepper lt) nil)\n                    (.-rest lt))))]\n       (MultiStepper. (xform stepfn) iters nexts))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2725",
          :filename "src/cljs/cljs/core.cljs",
          :lines [3181 3199]},
 :full-name "cljs.core/multi-stepper",
 :full-name-encode "cljs.core_multi-stepper",
 :history [["+" "0.0-2301"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/multi-stepper"]))
```

-->
