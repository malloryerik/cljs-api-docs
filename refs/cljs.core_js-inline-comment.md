## cljs.core/js-inline-comment



 <table border="1">
<tr>
<td>macro</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/1.7.107"><img valign="middle" alt="[+] 1.7.107" title="Added in 1.7.107" src="https://img.shields.io/badge/+-1.7.107-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__js-inline-comment__ comment)<br>
</samp>

---





Source docstring:

```
Emit an inline JavaScript comment.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r1.7.107/src/main/clojure/cljs/core.cljc#L891-L894):

```clj
(core/defmacro js-inline-comment
  [comment]
  (core/list 'js* (core/str "/**" comment "*/")))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1.7.107
└── src
    └── main
        └── clojure
            └── cljs
                └── <ins>[core.cljc:891-894](https://github.com/clojure/clojurescript/blob/r1.7.107/src/main/clojure/cljs/core.cljc#L891-L894)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/js-inline-comment` @ crossclj](http://crossclj.info/fun/cljs.core/js-inline-comment.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_js-inline-comment.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "js-inline-comment",
 :signature ["[comment]"],
 :history [["+" "1.7.107"]],
 :type "macro",
 :full-name-encode "cljs.core_js-inline-comment",
 :source {:code "(core/defmacro js-inline-comment\n  [comment]\n  (core/list 'js* (core/str \"/**\" comment \"*/\")))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1.7.107",
          :filename "src/main/clojure/cljs/core.cljc",
          :lines [891 894]},
 :full-name "cljs.core/js-inline-comment",
 :docstring "Emit an inline JavaScript comment."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/js-inline-comment"]))
```

-->
