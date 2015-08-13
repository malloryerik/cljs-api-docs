## cljs.core/IPending



 <table border="1">
<tr>
<td>protocol</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.lang/IPending</samp>](https://github.com/clojure/clojure/blob//src/jvm/clojure/lang/IPending.java)
</td>
</tr>
</table>









Source code @ [github](https://github.com/clojure/clojurescript/blob/r1449/src/cljs/cljs/core.cljs#L241-L242):

```clj
(defprotocol IPending
  (-realized? [d]))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1449
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:241-242](https://github.com/clojure/clojurescript/blob/r1449/src/cljs/cljs/core.cljs#L241-L242)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.lang/IPending` @ clojuredocs](http://clojuredocs.org/clojure.lang/IPending)<br>
[`clojure.lang/IPending` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.lang/IPending/)<br>
[`clojure.lang/IPending` @ crossclj](http://crossclj.info/fun/clojure.lang/IPending.html)<br>
[`cljs.core/IPending` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/IPending.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_IPending.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "IPending",
 :history [["+" "0.0-927"]],
 :type "protocol",
 :full-name-encode "cljs.core_IPending",
 :source {:code "(defprotocol IPending\n  (-realized? [d]))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1449",
          :filename "src/cljs/cljs/core.cljs",
          :lines [241 242]},
 :methods [{:name "-realized?", :signature ["[d]"], :docstring nil}],
 :full-name "cljs.core/IPending",
 :clj-symbol "clojure.lang/IPending"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/IPending"]))
```

-->
