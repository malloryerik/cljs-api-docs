## cljs.repl.browser/handle-post



 <table border="1">
<tr>
<td>multimethod</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__handle-post__ m _ _)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r3269/src/main/clojure/cljs/repl/browser.clj#L118):

```clj
(defmulti handle-post (fn [m _ _ ] (:type m)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3269
└── src
    └── main
        └── clojure
            └── cljs
                └── repl
                    └── <ins>[browser.clj:118](https://github.com/clojure/clojurescript/blob/r3269/src/main/clojure/cljs/repl/browser.clj#L118)</ins>
</pre>

-->

---

Dispatch method @ [github](https://github.com/clojure/clojurescript/blob/r3269/src/main/clojure/cljs/repl/browser.clj#L122-L128):

```clj
(defmethod handle-post :ready [_ conn _]
  (send-via es ordering (fn [_] {:expecting nil :fns {}}))
  (send-for-eval conn
    (cljsc/-compile
      '[(set! *print-fn* clojure.browser.repl/repl-print)
        (set! *print-newline* true)] {})
    identity))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3269
└── src
    └── main
        └── clojure
            └── cljs
                └── repl
                    └── <ins>[browser.clj:122-128](https://github.com/clojure/clojurescript/blob/r3269/src/main/clojure/cljs/repl/browser.clj#L122-L128)</ins>
</pre>
-->

---
Dispatch method @ [github](https://github.com/clojure/clojurescript/blob/r3269/src/main/clojure/cljs/repl/browser.clj#L149-L154):

```clj
(defmethod handle-post :print [{:keys [content order]} conn _ ]
  (constrain-order order
    (fn []
      (print (read-string content))
      (.flush *out*)))
  (server/send-and-close conn 200 "ignore__"))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3269
└── src
    └── main
        └── clojure
            └── cljs
                └── repl
                    └── <ins>[browser.clj:149-154](https://github.com/clojure/clojurescript/blob/r3269/src/main/clojure/cljs/repl/browser.clj#L149-L154)</ins>
</pre>
-->

---
Dispatch method @ [github](https://github.com/clojure/clojurescript/blob/r3269/src/main/clojure/cljs/repl/browser.clj#L156-L160):

```clj
(defmethod handle-post :result [{:keys [content order]} conn _ ]
  (constrain-order order
    (fn []
      (return-value content)
      (server/set-connection conn))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3269
└── src
    └── main
        └── clojure
            └── cljs
                └── repl
                    └── <ins>[browser.clj:156-160](https://github.com/clojure/clojurescript/blob/r3269/src/main/clojure/cljs/repl/browser.clj#L156-L160)</ins>
</pre>
-->

---


###### External doc links:

[`cljs.repl.browser/handle-post` @ crossclj](http://crossclj.info/fun/cljs.repl.browser/handle-post.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.repl.browser_handle-post.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.repl.browser",
 :name "handle-post",
 :signature ["[m _ _]"],
 :history [["+" "0.0-927"]],
 :type "multimethod",
 :full-name-encode "cljs.repl.browser_handle-post",
 :source {:code "(defmulti handle-post (fn [m _ _ ] (:type m)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r3269",
          :filename "src/main/clojure/cljs/repl/browser.clj",
          :lines [118]},
 :extra-sources ({:code "(defmethod handle-post :ready [_ conn _]\n  (send-via es ordering (fn [_] {:expecting nil :fns {}}))\n  (send-for-eval conn\n    (cljsc/-compile\n      '[(set! *print-fn* clojure.browser.repl/repl-print)\n        (set! *print-newline* true)] {})\n    identity))",
                  :title "Dispatch method",
                  :repo "clojurescript",
                  :tag "r3269",
                  :filename "src/main/clojure/cljs/repl/browser.clj",
                  :lines [122 128]}
                 {:code "(defmethod handle-post :print [{:keys [content order]} conn _ ]\n  (constrain-order order\n    (fn []\n      (print (read-string content))\n      (.flush *out*)))\n  (server/send-and-close conn 200 \"ignore__\"))",
                  :title "Dispatch method",
                  :repo "clojurescript",
                  :tag "r3269",
                  :filename "src/main/clojure/cljs/repl/browser.clj",
                  :lines [149 154]}
                 {:code "(defmethod handle-post :result [{:keys [content order]} conn _ ]\n  (constrain-order order\n    (fn []\n      (return-value content)\n      (server/set-connection conn))))",
                  :title "Dispatch method",
                  :repo "clojurescript",
                  :tag "r3269",
                  :filename "src/main/clojure/cljs/repl/browser.clj",
                  :lines [156 160]}),
 :full-name "cljs.repl.browser/handle-post"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.repl.browser/handle-post"]))
```

-->
