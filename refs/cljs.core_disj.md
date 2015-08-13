## cljs.core/disj



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/disj</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/disj)
</td>
</tr>
</table>


 <samp>
(__disj__ coll)<br>
</samp>
 <samp>
(__disj__ coll k)<br>
</samp>
 <samp>
(__disj__ coll k & ks)<br>
</samp>

---

disj(oin). Returns a new set of the same (hashed/sorted) type, that does not
contain key(s).

---


###### See Also:

[`cljs.core/dissoc`](cljs.core_dissoc.md)<br>
[`cljs.core/disj!`](cljs.core_disjBANG.md)<br>
[`clojure.set/difference`](clojure.set_difference.md)<br>

---


Source docstring:

```
disj[oin]. Returns a new set of the same (hashed/sorted) type, that
does not contain key(s).
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r1847/src/cljs/cljs/core.cljs#L1030-L1040):

```clj
(defn disj
  ([coll] coll)
  ([coll k]
     (-disjoin coll k))
  ([coll k & ks]
     (let [ret (disj coll k)]
       (if ks
         (recur ret (first ks) (next ks))
         ret))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1847
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:1030-1040](https://github.com/clojure/clojurescript/blob/r1847/src/cljs/cljs/core.cljs#L1030-L1040)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/disj` @ clojuredocs](http://clojuredocs.org/clojure.core/disj)<br>
[`clojure.core/disj` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/disj/)<br>
[`clojure.core/disj` @ crossclj](http://crossclj.info/fun/clojure.core/disj.html)<br>
[`cljs.core/disj` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/disj.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_disj.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "disj(oin). Returns a new set of the same (hashed/sorted) type, that does not\ncontain key(s).",
 :ns "cljs.core",
 :name "disj",
 :signature ["[coll]" "[coll k]" "[coll k & ks]"],
 :history [["+" "0.0-927"]],
 :type "function",
 :related ["cljs.core/dissoc"
           "cljs.core/disj!"
           "clojure.set/difference"],
 :full-name-encode "cljs.core_disj",
 :source {:code "(defn disj\n  ([coll] coll)\n  ([coll k]\n     (-disjoin coll k))\n  ([coll k & ks]\n     (let [ret (disj coll k)]\n       (if ks\n         (recur ret (first ks) (next ks))\n         ret))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1847",
          :filename "src/cljs/cljs/core.cljs",
          :lines [1030 1040]},
 :full-name "cljs.core/disj",
 :clj-symbol "clojure.core/disj",
 :docstring "disj[oin]. Returns a new set of the same (hashed/sorted) type, that\ndoes not contain key(s)."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/disj"]))
```

-->
