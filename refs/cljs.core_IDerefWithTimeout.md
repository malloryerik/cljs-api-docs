## cljs.core/IDerefWithTimeout



 <table border="1">
<tr>
<td>protocol</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>









Source code @ [github](https://github.com/clojure/clojurescript/blob/r3115/src/cljs/cljs/core.cljs#L444-L445):

```clj
(defprotocol IDerefWithTimeout
  (-deref-with-timeout [o msec timeout-val]))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3115
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:444-445](https://github.com/clojure/clojurescript/blob/r3115/src/cljs/cljs/core.cljs#L444-L445)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/IDerefWithTimeout` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/IDerefWithTimeout.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_IDerefWithTimeout.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "IDerefWithTimeout",
 :type "protocol",
 :full-name-encode "cljs.core_IDerefWithTimeout",
 :source {:code "(defprotocol IDerefWithTimeout\n  (-deref-with-timeout [o msec timeout-val]))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r3115",
          :filename "src/cljs/cljs/core.cljs",
          :lines [444 445]},
 :methods [{:name "-deref-with-timeout",
            :signature ["[o msec timeout-val]"],
            :docstring nil}],
 :full-name "cljs.core/IDerefWithTimeout",
 :history [["+" "0.0-927"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/IDerefWithTimeout"]))
```

-->
