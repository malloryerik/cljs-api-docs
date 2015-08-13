## cljs.repl.browser/firefox-clean-function



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-3053"><img valign="middle" alt="[+] 0.0-3053" title="Added in 0.0-3053" src="https://img.shields.io/badge/+-0.0--3053-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__firefox-clean-function__ f)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r3195/src/clj/cljs/repl/browser.clj#L372-L382):

```clj
(defn firefox-clean-function [f]
  (as-> f f
    (cond
      (string/blank? f) nil
      (not= (.indexOf f "</") -1)
      (let [idx (.indexOf f "</")]
        (.substring f (+ idx 2)))
      :else f)
    (-> f
      (string/replace #"<" "")
      (string/replace #"\/" ""))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3195
└── src
    └── clj
        └── cljs
            └── repl
                └── <ins>[browser.clj:372-382](https://github.com/clojure/clojurescript/blob/r3195/src/clj/cljs/repl/browser.clj#L372-L382)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.repl.browser/firefox-clean-function` @ crossclj](http://crossclj.info/fun/cljs.repl.browser/firefox-clean-function.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.repl.browser_firefox-clean-function.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.repl.browser",
 :name "firefox-clean-function",
 :type "function",
 :signature ["[f]"],
 :source {:code "(defn firefox-clean-function [f]\n  (as-> f f\n    (cond\n      (string/blank? f) nil\n      (not= (.indexOf f \"</\") -1)\n      (let [idx (.indexOf f \"</\")]\n        (.substring f (+ idx 2)))\n      :else f)\n    (-> f\n      (string/replace #\"<\" \"\")\n      (string/replace #\"\\/\" \"\"))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r3195",
          :filename "src/clj/cljs/repl/browser.clj",
          :lines [372 382]},
 :full-name "cljs.repl.browser/firefox-clean-function",
 :full-name-encode "cljs.repl.browser_firefox-clean-function",
 :history [["+" "0.0-3053"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.repl.browser/firefox-clean-function"]))
```

-->
