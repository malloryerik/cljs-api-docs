## clojure.browser.net/xpc-config-fields



 <table border="1">
<tr>
<td>var</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>









Source code @ [github](https://github.com/clojure/clojurescript/blob/r1843/src/cljs/clojure/browser/net.cljs#L75-L81):

```clj
(def xpc-config-fields
  (into {}
        (map
         (fn [[k v]]
           [(keyword (. k (toLowerCase)))
            v])
         (js->clj goog.net.xpc.CfgFields))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1843
└── src
    └── cljs
        └── clojure
            └── browser
                └── <ins>[net.cljs:75-81](https://github.com/clojure/clojurescript/blob/r1843/src/cljs/clojure/browser/net.cljs#L75-L81)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.browser.net/xpc-config-fields` @ crossclj](http://crossclj.info/fun/clojure.browser.net.cljs/xpc-config-fields.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/clojure.browser.net_xpc-config-fields.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "clojure.browser.net",
 :name "xpc-config-fields",
 :type "var",
 :source {:code "(def xpc-config-fields\n  (into {}\n        (map\n         (fn [[k v]]\n           [(keyword (. k (toLowerCase)))\n            v])\n         (js->clj goog.net.xpc.CfgFields))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1843",
          :filename "src/cljs/clojure/browser/net.cljs",
          :lines [75 81]},
 :full-name "clojure.browser.net/xpc-config-fields",
 :full-name-encode "clojure.browser.net_xpc-config-fields",
 :history [["+" "0.0-927"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "clojure.browser.net/xpc-config-fields"]))
```

-->
