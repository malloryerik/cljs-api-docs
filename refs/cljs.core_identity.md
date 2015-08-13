## cljs.core/identity



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/identity</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/identity)
</td>
</tr>
</table>


 <samp>
(__identity__ x)<br>
</samp>

---

Returns its argument.

---


###### See Also:

[`cljs.core/nil?`](cljs.core_nilQMARK.md)<br>

---




Source code @ [github](https://github.com/clojure/clojurescript/blob/r1820/src/cljs/cljs/core.cljs#L2503):

```clj
(defn identity [x] x)
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1820
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:2503](https://github.com/clojure/clojurescript/blob/r1820/src/cljs/cljs/core.cljs#L2503)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/identity` @ clojuredocs](http://clojuredocs.org/clojure.core/identity)<br>
[`clojure.core/identity` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/identity/)<br>
[`clojure.core/identity` @ crossclj](http://crossclj.info/fun/clojure.core/identity.html)<br>
[`cljs.core/identity` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/identity.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_identity.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Returns its argument.",
 :ns "cljs.core",
 :name "identity",
 :signature ["[x]"],
 :history [["+" "0.0-927"]],
 :type "function",
 :related ["cljs.core/nil?"],
 :full-name-encode "cljs.core_identity",
 :source {:code "(defn identity [x] x)",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1820",
          :filename "src/cljs/cljs/core.cljs",
          :lines [2503]},
 :full-name "cljs.core/identity",
 :clj-symbol "clojure.core/identity"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/identity"]))
```

-->
