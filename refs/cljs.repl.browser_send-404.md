## cljs.repl.browser/send-404



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__send-404__ conn path)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r1236/src/clj/cljs/repl/browser.clj#L91-L97):

```clj
(defn send-404 [conn path]
  (send-and-close conn 404
                  (str "<html><body>"
                       "<h2>Page not found</h2>"
                       "No page " path " found on this server."
                       "</body></html>")
                  "text/html"))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1236
└── src
    └── clj
        └── cljs
            └── repl
                └── <ins>[browser.clj:91-97](https://github.com/clojure/clojurescript/blob/r1236/src/clj/cljs/repl/browser.clj#L91-L97)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.repl.browser/send-404` @ crossclj](http://crossclj.info/fun/cljs.repl.browser/send-404.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.repl.browser_send-404.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.repl.browser",
 :name "send-404",
 :type "function",
 :signature ["[conn path]"],
 :source {:code "(defn send-404 [conn path]\n  (send-and-close conn 404\n                  (str \"<html><body>\"\n                       \"<h2>Page not found</h2>\"\n                       \"No page \" path \" found on this server.\"\n                       \"</body></html>\")\n                  \"text/html\"))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1236",
          :filename "src/clj/cljs/repl/browser.clj",
          :lines [91 97]},
 :full-name "cljs.repl.browser/send-404",
 :full-name-encode "cljs.repl.browser_send-404",
 :history [["+" "0.0-927"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.repl.browser/send-404"]))
```

-->
