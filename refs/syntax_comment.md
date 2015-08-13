## ; comment



 <table border="1">
<tr>
<td>syntax</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> clj doc](http://clojure.org/reader#toc2)
</td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/I8uNXHv.png"> edn doc](https://github.com/edn-format/edn#comments)
</td>
</tr>
</table>



"Comments out" everything after `;` on the current line.

---

###### Examples:

Add comments to code:

```clj
(def a 1) ; this is a comment
```

It is common to use `;;` for comments that have their own line:

```clj
;; this comment is on its own line
```

---

###### See Also:

[`#_ ignore`](syntax_ignore.md)<br>
[`cljs.core/comment`](cljs.core_comment.md)<br>
[`#! shebang`](syntax_shebang.md)<br>

---




 @ [github](https://github.com/clojure/clojure/blob/clojure-1.4.0/src/jvm/clojure/lang/LispReader.java#L):

```clj

```

<!--
Repo - tag - source tree - lines:

 <pre>
clojure @ clojure-1.4.0
└── src
    └── jvm
        └── clojure
            └── lang
                └── <ins>[LispReader.java:](https://github.com/clojure/clojure/blob/clojure-1.4.0/src/jvm/clojure/lang/LispReader.java#L)</ins>
</pre>

-->

---




 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/syntax_comment.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "\"Comments out\" everything after `;` on the current line.",
 :ns "syntax",
 :name "comment",
 :history [["+" "0.0-927"]],
 :type "syntax",
 :related ["syntax/ignore" "cljs.core/comment" "syntax/shebang"],
 :full-name-encode "syntax_comment",
 :source {:repo "clojure",
          :tag "clojure-1.4.0",
          :filename "src/jvm/clojure/lang/LispReader.java",
          :lines [nil]},
 :examples [{:id "ab62d2",
             :content "Add comments to code:\n\n```clj\n(def a 1) ; this is a comment\n```\n\nIt is common to use `;;` for comments that have their own line:\n\n```clj\n;; this comment is on its own line\n```"}],
 :edn-doc "https://github.com/edn-format/edn#comments",
 :full-name "syntax/comment",
 :display "; comment",
 :clj-doc "http://clojure.org/reader#toc2"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "syntax/comment"]))
```

-->