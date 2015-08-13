## clojure.string/join



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.string/join</samp>](http://clojure.github.io/clojure/branch-master/clojure.string-api.html#clojure.string/join)
</td>
</tr>
</table>


 <samp>
(__join__ coll)<br>
</samp>
 <samp>
(__join__ separator coll)<br>
</samp>

---

Returns a string of all elements in `coll`, as returned by `(seq coll)`,
separated by an optional separator.

---




Source docstring:

```
Returns a string of all elements in coll, as returned by (seq coll),
separated by an optional separator.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r3291/src/main/cljs/clojure/string.cljs#L49-L66):

```clj
(defn join
  ([coll]
   (loop [sb (StringBuffer.) coll (seq coll)]
     (if coll
       (recur (. sb (append (str (first coll)))) (next coll))
       (.toString sb))))
  ([separator coll]
   (loop [sb (StringBuffer.) coll (seq coll)]
     (if coll
       (do
         (. sb (append (str (first coll))))
         (let [coll (next coll)]
           (when-not (nil? coll)
             (. sb (append separator)))
           (recur sb coll)))
       (.toString sb)))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3291
└── src
    └── main
        └── cljs
            └── clojure
                └── <ins>[string.cljs:49-66](https://github.com/clojure/clojurescript/blob/r3291/src/main/cljs/clojure/string.cljs#L49-L66)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.string/join` @ clojuredocs](http://clojuredocs.org/clojure.string/join)<br>
[`clojure.string/join` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.string/join/)<br>
[`clojure.string/join` @ crossclj](http://crossclj.info/fun/clojure.string/join.html)<br>
[`clojure.string/join` @ crossclj](http://crossclj.info/fun/clojure.string.cljs/join.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/clojure.string_join.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Returns a string of all elements in `coll`, as returned by `(seq coll)`,\nseparated by an optional separator.",
 :ns "clojure.string",
 :name "join",
 :signature ["[coll]" "[separator coll]"],
 :history [["+" "0.0-927"]],
 :type "function",
 :full-name-encode "clojure.string_join",
 :source {:code "(defn join\n  ([coll]\n   (loop [sb (StringBuffer.) coll (seq coll)]\n     (if coll\n       (recur (. sb (append (str (first coll)))) (next coll))\n       (.toString sb))))\n  ([separator coll]\n   (loop [sb (StringBuffer.) coll (seq coll)]\n     (if coll\n       (do\n         (. sb (append (str (first coll))))\n         (let [coll (next coll)]\n           (when-not (nil? coll)\n             (. sb (append separator)))\n           (recur sb coll)))\n       (.toString sb)))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r3291",
          :filename "src/main/cljs/clojure/string.cljs",
          :lines [49 66]},
 :full-name "clojure.string/join",
 :clj-symbol "clojure.string/join",
 :docstring "Returns a string of all elements in coll, as returned by (seq coll),\nseparated by an optional separator."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "clojure.string/join"]))
```

-->
