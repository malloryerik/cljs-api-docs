## cljs.core/dotimes



 <table border="1">
<tr>
<td>macro</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/dotimes</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/dotimes)
</td>
</tr>
</table>


 <samp>
(__dotimes__ \[name n\] & body)<br>
</samp>

---

Repeatedly executes `body` (presumably for side-effects) with `name` bound to
integers from 0 through `n`-1.

---


###### See Also:

[`cljs.core/repeat`](cljs.core_repeat.md)<br>
[`cljs.core/for`](cljs.core_for.md)<br>
[`cljs.core/doseq`](cljs.core_doseq.md)<br>

---


Source docstring:

```
bindings => name n

Repeatedly executes body (presumably for side-effects) with name
bound to integers from 0 through n-1.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r2120/src/clj/cljs/core.clj#L1419-L1431):

```clj
(defmacro dotimes
  [bindings & body]
  (let [i (first bindings)
        n (second bindings)]
    `(let [n# ~n]
       (loop [~i 0]
         (when (< ~i n#)
           ~@body
           (recur (inc ~i)))))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2120
└── src
    └── clj
        └── cljs
            └── <ins>[core.clj:1419-1431](https://github.com/clojure/clojurescript/blob/r2120/src/clj/cljs/core.clj#L1419-L1431)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/dotimes` @ clojuredocs](http://clojuredocs.org/clojure.core/dotimes)<br>
[`clojure.core/dotimes` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/dotimes/)<br>
[`clojure.core/dotimes` @ crossclj](http://crossclj.info/fun/clojure.core/dotimes.html)<br>
[`cljs.core/dotimes` @ crossclj](http://crossclj.info/fun/cljs.core/dotimes.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_dotimes.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Repeatedly executes `body` (presumably for side-effects) with `name` bound to\nintegers from 0 through `n`-1.",
 :ns "cljs.core",
 :name "dotimes",
 :signature ["[[name n] & body]"],
 :history [["+" "0.0-927"]],
 :type "macro",
 :related ["cljs.core/repeat" "cljs.core/for" "cljs.core/doseq"],
 :full-name-encode "cljs.core_dotimes",
 :source {:code "(defmacro dotimes\n  [bindings & body]\n  (let [i (first bindings)\n        n (second bindings)]\n    `(let [n# ~n]\n       (loop [~i 0]\n         (when (< ~i n#)\n           ~@body\n           (recur (inc ~i)))))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2120",
          :filename "src/clj/cljs/core.clj",
          :lines [1419 1431]},
 :full-name "cljs.core/dotimes",
 :clj-symbol "clojure.core/dotimes",
 :docstring "bindings => name n\n\nRepeatedly executes body (presumably for side-effects) with name\nbound to integers from 0 through n-1."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/dotimes"]))
```

-->
