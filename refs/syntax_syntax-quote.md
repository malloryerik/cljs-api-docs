## ` syntax quote



 <table border="1">
<tr>
<td>syntax</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> clj doc](http://clojure.org/reader#toc2)
</td>
</tr>
</table>



(Only intended for use in Clojure macros, which can be used from but not
written in ClojureScript.)

Prevent evaluation of the following form.

Adds namespace-qualification to any symbols inside the following form by
resolving them in the current context.

Any non-namespaced symbols ending with `#` are replaced with unique symbols.
See [`# auto-gensym`](syntax_auto-gensym.md).

---

###### Examples:

```clj
`foo
;;=> cljs.user/foo

`foo#
;;=> foo__20418__auto__

`(def foo 1)
;;=> (def cljs.user/foo 1)
```

---

###### See Also:

[`# auto-gensym`](syntax_auto-gensym.md)<br>
[`' quote`](syntax_quote.md)<br>
[`~ unquote`](syntax_unquote.md)<br>
[`~@ unquote splicing`](syntax_unquote-splicing.md)<br>

---




 @ [github](https://github.com/clojure/clojure/blob/clojure-1.5.1/src/jvm/clojure/lang/LispReader.java#L):

```clj

```

<!--
Repo - tag - source tree - lines:

 <pre>
clojure @ clojure-1.5.1
└── src
    └── jvm
        └── clojure
            └── lang
                └── <ins>[LispReader.java:](https://github.com/clojure/clojure/blob/clojure-1.5.1/src/jvm/clojure/lang/LispReader.java#L)</ins>
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

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/syntax_syntax-quote.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "(Only intended for use in Clojure macros, which can be used from but not\nwritten in ClojureScript.)\n\nPrevent evaluation of the following form.\n\nAdds namespace-qualification to any symbols inside the following form by\nresolving them in the current context.\n\nAny non-namespaced symbols ending with `#` are replaced with unique symbols.\nSee [syntax/auto-gensym].",
 :ns "syntax",
 :name "syntax-quote",
 :history [["+" "0.0-927"]],
 :type "syntax",
 :related ["syntax/auto-gensym"
           "syntax/quote"
           "syntax/unquote"
           "syntax/unquote-splicing"],
 :full-name-encode "syntax_syntax-quote",
 :source {:repo "clojure",
          :tag "clojure-1.5.1",
          :filename "src/jvm/clojure/lang/LispReader.java",
          :lines [nil]},
 :examples [{:id "bffbdf",
             :content "```clj\n`foo\n;;=> cljs.user/foo\n\n`foo#\n;;=> foo__20418__auto__\n\n`(def foo 1)\n;;=> (def cljs.user/foo 1)\n```"}],
 :full-name "syntax/syntax-quote",
 :display "` syntax quote",
 :clj-doc "http://clojure.org/reader#toc2"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "syntax/syntax-quote"]))
```

-->
