## cljs.core/create-ns



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/1.7.10"><img valign="middle" alt="[+] 1.7.10" title="Added in 1.7.10" src="https://img.shields.io/badge/+-1.7.10-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/create-ns</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/create-ns)
</td>
</tr>
</table>


 <samp>
(__create-ns__ sym)<br>
</samp>
 <samp>
(__create-ns__ sym ns-obj)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r1.7.107/src/main/cljs/cljs/core.cljs#L10142-L10146):

```clj
(defn create-ns
  ([sym]
   (create-ns sym (find-ns-obj sym)))
  ([sym ns-obj]
   (Namespace. ns-obj sym)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1.7.107
└── src
    └── main
        └── cljs
            └── cljs
                └── <ins>[core.cljs:10142-10146](https://github.com/clojure/clojurescript/blob/r1.7.107/src/main/cljs/cljs/core.cljs#L10142-L10146)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/create-ns` @ clojuredocs](http://clojuredocs.org/clojure.core/create-ns)<br>
[`clojure.core/create-ns` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/create-ns/)<br>
[`clojure.core/create-ns` @ crossclj](http://crossclj.info/fun/clojure.core/create-ns.html)<br>
[`cljs.core/create-ns` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/create-ns.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_create-ns.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "create-ns",
 :signature ["[sym]" "[sym ns-obj]"],
 :history [["+" "1.7.10"]],
 :type "function",
 :full-name-encode "cljs.core_create-ns",
 :source {:code "(defn create-ns\n  ([sym]\n   (create-ns sym (find-ns-obj sym)))\n  ([sym ns-obj]\n   (Namespace. ns-obj sym)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1.7.107",
          :filename "src/main/cljs/cljs/core.cljs",
          :lines [10142 10146]},
 :full-name "cljs.core/create-ns",
 :clj-symbol "clojure.core/create-ns"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/create-ns"]))
```

-->
