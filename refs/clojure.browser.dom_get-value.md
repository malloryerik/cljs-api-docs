## clojure.browser.dom/get-value



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__get-value__ e)<br>
</samp>

---





Source docstring:

```
Get the value of an element.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r1843/src/cljs/clojure/browser/dom.cljs#L131-L134):

```clj
(defn get-value
  [e]
  (.-value (ensure-element e)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1843
└── src
    └── cljs
        └── clojure
            └── browser
                └── <ins>[dom.cljs:131-134](https://github.com/clojure/clojurescript/blob/r1843/src/cljs/clojure/browser/dom.cljs#L131-L134)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.browser.dom/get-value` @ crossclj](http://crossclj.info/fun/clojure.browser.dom.cljs/get-value.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/clojure.browser.dom_get-value.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "clojure.browser.dom",
 :name "get-value",
 :signature ["[e]"],
 :history [["+" "0.0-927"]],
 :type "function",
 :full-name-encode "clojure.browser.dom_get-value",
 :source {:code "(defn get-value\n  [e]\n  (.-value (ensure-element e)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1843",
          :filename "src/cljs/clojure/browser/dom.cljs",
          :lines [131 134]},
 :full-name "clojure.browser.dom/get-value",
 :docstring "Get the value of an element."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "clojure.browser.dom/get-value"]))
```

-->
