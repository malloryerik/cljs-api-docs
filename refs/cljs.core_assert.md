## cljs.core/assert



 <table border="1">
<tr>
<td>macro</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/assert</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/assert)
</td>
</tr>
</table>


 <samp>
(__assert__ expr)<br>
</samp>
 <samp>
(__assert__ expr message)<br>
</samp>

---

Evaluates expression `expr` and throws an exception if it does not evaluate to
logical true.  Exception will include `message` if given.

Returns `nil`.

---

###### Examples:

```clj
(assert true)
;;=> nil

(assert false)
;;=> Uncaught Error: Assert failed: false

(assert (= 1 2) "1 is not 2")
;;=> Uncaught Error: Assert failed: 1 is not 2
;;   (= 1 2)
```

---



Source docstring:

```
Evaluates expr and throws an exception if it does not evaluate to
logical true.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r3190/src/clj/cljs/core.clj#L1566-L1578):

```clj
(defmacro assert
  ([x]
     (when *assert*
       `(when-not ~x
          (throw (js/Error.
                  (cljs.core/str "Assert failed: " (cljs.core/pr-str '~x)))))))
  ([x message]
     (when *assert*
       `(when-not ~x
          (throw (js/Error.
                  (cljs.core/str "Assert failed: " ~message "\n" (cljs.core/pr-str '~x))))))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3190
└── src
    └── clj
        └── cljs
            └── <ins>[core.clj:1566-1578](https://github.com/clojure/clojurescript/blob/r3190/src/clj/cljs/core.clj#L1566-L1578)</ins>
</pre>

-->

---

Source code @ [github](https://github.com/clojure/clojure/blob/clojure-1.7.0-alpha6/src/clj/clojure/core.clj#L4610-L4621):

```clj
(defmacro assert
  ([x]
     (when *assert*
       `(when-not ~x
          (throw (new AssertionError (str "Assert failed: " (pr-str '~x)))))))
  ([x message]
     (when *assert*
       `(when-not ~x
          (throw (new AssertionError (str "Assert failed: " ~message "\n" (pr-str '~x))))))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojure @ clojure-1.7.0-alpha6
└── src
    └── clj
        └── clojure
            └── <ins>[core.clj:4610-4621](https://github.com/clojure/clojure/blob/clojure-1.7.0-alpha6/src/clj/clojure/core.clj#L4610-L4621)</ins>
</pre>
-->

---


###### External doc links:

[`clojure.core/assert` @ clojuredocs](http://clojuredocs.org/clojure.core/assert)<br>
[`clojure.core/assert` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/assert/)<br>
[`clojure.core/assert` @ crossclj](http://crossclj.info/fun/clojure.core/assert.html)<br>
[`cljs.core/assert` @ crossclj](http://crossclj.info/fun/cljs.core/assert.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_assert.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Evaluates expression `expr` and throws an exception if it does not evaluate to\nlogical true.  Exception will include `message` if given.\n\nReturns `nil`.",
 :ns "cljs.core",
 :name "assert",
 :signature ["[expr]" "[expr message]"],
 :history [["+" "0.0-927"]],
 :type "macro",
 :full-name-encode "cljs.core_assert",
 :source {:code "(defmacro assert\n  ([x]\n     (when *assert*\n       `(when-not ~x\n          (throw (js/Error.\n                  (cljs.core/str \"Assert failed: \" (cljs.core/pr-str '~x)))))))\n  ([x message]\n     (when *assert*\n       `(when-not ~x\n          (throw (js/Error.\n                  (cljs.core/str \"Assert failed: \" ~message \"\\n\" (cljs.core/pr-str '~x))))))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r3190",
          :filename "src/clj/cljs/core.clj",
          :lines [1566 1578]},
 :extra-sources ({:code "(defmacro assert\n  ([x]\n     (when *assert*\n       `(when-not ~x\n          (throw (new AssertionError (str \"Assert failed: \" (pr-str '~x)))))))\n  ([x message]\n     (when *assert*\n       `(when-not ~x\n          (throw (new AssertionError (str \"Assert failed: \" ~message \"\\n\" (pr-str '~x))))))))",
                  :title "Source code",
                  :repo "clojure",
                  :tag "clojure-1.7.0-alpha6",
                  :filename "src/clj/clojure/core.clj",
                  :lines [4610 4621]}),
 :examples [{:id "1dc16f",
             :content "```clj\n(assert true)\n;;=> nil\n\n(assert false)\n;;=> Uncaught Error: Assert failed: false\n\n(assert (= 1 2) \"1 is not 2\")\n;;=> Uncaught Error: Assert failed: 1 is not 2\n;;   (= 1 2)\n```"}],
 :full-name "cljs.core/assert",
 :clj-symbol "clojure.core/assert",
 :docstring "Evaluates expr and throws an exception if it does not evaluate to\nlogical true."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/assert"]))
```

-->
