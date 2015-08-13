## cljs.core/not-any?



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/not-any?</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/not-any?)
</td>
</tr>
</table>


 <samp>
(__not-any?__ pred coll)<br>
</samp>

---

Returns false if `(pred x)` is logical true for any `x` in `coll`, else true.

---


###### See Also:

[`cljs.core/every?`](cljs.core_everyQMARK.md)<br>
[`cljs.core/some`](cljs.core_some.md)<br>

---


Source docstring:

```
Returns false if (pred x) is logical true for any x in coll,
else true.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r1424/src/cljs/cljs/core.cljs#L2154-L2157):

```clj
(defn ^boolean not-any?
  [pred coll] (not (some pred coll)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1424
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:2154-2157](https://github.com/clojure/clojurescript/blob/r1424/src/cljs/cljs/core.cljs#L2154-L2157)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/not-any?` @ clojuredocs](http://clojuredocs.org/clojure.core/not-any_q)<br>
[`clojure.core/not-any?` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/not-any%3F/)<br>
[`clojure.core/not-any?` @ crossclj](http://crossclj.info/fun/clojure.core/not-any%3F.html)<br>
[`cljs.core/not-any?` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/not-any%3F.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_not-anyQMARK.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Returns false if `(pred x)` is logical true for any `x` in `coll`, else true.",
 :return-type boolean,
 :ns "cljs.core",
 :name "not-any?",
 :signature ["[pred coll]"],
 :history [["+" "0.0-927"]],
 :type "function",
 :related ["cljs.core/every?" "cljs.core/some"],
 :full-name-encode "cljs.core_not-anyQMARK",
 :source {:code "(defn ^boolean not-any?\n  [pred coll] (not (some pred coll)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1424",
          :filename "src/cljs/cljs/core.cljs",
          :lines [2154 2157]},
 :full-name "cljs.core/not-any?",
 :clj-symbol "clojure.core/not-any?",
 :docstring "Returns false if (pred x) is logical true for any x in coll,\nelse true."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/not-any?"]))
```

-->
