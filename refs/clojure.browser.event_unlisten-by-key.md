## clojure.browser.event/unlisten-by-key



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__unlisten-by-key__ key)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r1844/src/cljs/clojure/browser/event.cljs#L71-L73):

```clj
(defn unlisten-by-key
  [key]
  (goog.events/unlistenByKey key))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1844
└── src
    └── cljs
        └── clojure
            └── browser
                └── <ins>[event.cljs:71-73](https://github.com/clojure/clojurescript/blob/r1844/src/cljs/clojure/browser/event.cljs#L71-L73)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.browser.event/unlisten-by-key` @ crossclj](http://crossclj.info/fun/clojure.browser.event.cljs/unlisten-by-key.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/clojure.browser.event_unlisten-by-key.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "clojure.browser.event",
 :name "unlisten-by-key",
 :type "function",
 :signature ["[key]"],
 :source {:code "(defn unlisten-by-key\n  [key]\n  (goog.events/unlistenByKey key))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1844",
          :filename "src/cljs/clojure/browser/event.cljs",
          :lines [71 73]},
 :full-name "clojure.browser.event/unlisten-by-key",
 :full-name-encode "clojure.browser.event_unlisten-by-key",
 :history [["+" "0.0-927"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "clojure.browser.event/unlisten-by-key"]))
```

-->
