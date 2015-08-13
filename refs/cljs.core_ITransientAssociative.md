## cljs.core/ITransientAssociative



 <table border="1">
<tr>
<td>protocol</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1211"><img valign="middle" alt="[+] 0.0-1211" title="Added in 0.0-1211" src="https://img.shields.io/badge/+-0.0--1211-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.lang/ITransientAssociative</samp>](https://github.com/clojure/clojure/blob//src/jvm/clojure/lang/ITransientAssociative.java)
</td>
</tr>
</table>









Source code @ [github](https://github.com/clojure/clojurescript/blob/r1913/src/cljs/cljs/core.cljs#L322-L323):

```clj
(defprotocol ITransientAssociative
  (-assoc! [tcoll key val]))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1913
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:322-323](https://github.com/clojure/clojurescript/blob/r1913/src/cljs/cljs/core.cljs#L322-L323)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.lang/ITransientAssociative` @ clojuredocs](http://clojuredocs.org/clojure.lang/ITransientAssociative)<br>
[`clojure.lang/ITransientAssociative` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.lang/ITransientAssociative/)<br>
[`clojure.lang/ITransientAssociative` @ crossclj](http://crossclj.info/fun/clojure.lang/ITransientAssociative.html)<br>
[`cljs.core/ITransientAssociative` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/ITransientAssociative.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_ITransientAssociative.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "ITransientAssociative",
 :history [["+" "0.0-1211"]],
 :type "protocol",
 :full-name-encode "cljs.core_ITransientAssociative",
 :source {:code "(defprotocol ITransientAssociative\n  (-assoc! [tcoll key val]))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1913",
          :filename "src/cljs/cljs/core.cljs",
          :lines [322 323]},
 :methods [{:name "-assoc!",
            :signature ["[tcoll key val]"],
            :docstring nil}],
 :full-name "cljs.core/ITransientAssociative",
 :clj-symbol "clojure.lang/ITransientAssociative"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/ITransientAssociative"]))
```

-->
