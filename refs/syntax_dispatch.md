## # dispatch



 <table border="1">
<tr>
<td>syntax</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> clj doc](http://clojure.org/reader#toc2)
</td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/I8uNXHv.png"> edn doc](https://github.com/edn-format/edn#-dispatch-character)
</td>
</tr>
</table>

<samp>#...</samp><br>

---


`#` is a prefix character that is called the dispatch macro, because it allows
the behavior of the reader to be dispatched to another table, indexed by the
character following the `#`.

Syntax forms prefixed with `#` are made to bear some similarity to their
original forms:

| original                           | with `#` prefix                                  | relation               |
|------------------------------------|--------------------------------------------------|------------------------|
| [`"" string`](syntax_string.md)                    | [`#"" regex`](syntax_regex.md)                                   | string-related         |
| [`() list`](syntax_list.md)                      | [`#() function`](syntax_function.md)                                | code-related           |
| [`{} map`](syntax_map.md)                       | [`#{} set`](syntax_set.md)                                     | lookup-related         |
| [`' quote`](syntax_quote.md)                     | [`#' var`](syntax_var.md)                                     | quote-related          |
| [`_ unused`](syntax_unused.md)                    | [`#_ ignore`](syntax_ignore.md)                                  | ignore-related         |
| [`foo (symbol)`](syntax_symbol.md)    | [`#foo (tagged literal)`](syntax_tagged-literal.md) | name-related           |
| [`? predicate`](syntax_predicate.md)                 | [`#? reader conditional`](syntax_cond.md)                                    | conditional-related    |

---

###### Examples:

The dispatch macro is not usable on its own.  Rather, it dispatches to other
syntax forms.

Regular expression:

```clj
#"[a-zA-Z0-9]+"
;;=> #"[a-zA-Z0-9]+"
```

Set:

```clj
#{:foo 1 2}
;;=> #{:foo 1 2}
```

Function:

```clj
#(foo 1 2)
;;=> #<function (){
;;   return cljs.user.foo.call(null,(1),(2));
;;   }>
```

Var reference:

```clj
(def a)
#'a
;;=> #'cljs.user/a
```

Ignore form:

```clj
#_foo
;; waits for next form since #_foo was ignored

#_123 456
;;=> 456
```

Tagged Literals:

```clj
#queue [1 2 3]
;;=> #queue [1 2 3]

#js {:foo 1}
;;=> #js {:foo 1}

#inst "2010-11-12T18:14:15.666-00:00"
;;=> #inst "2010-11-12T18:14:15.666-00:00"
```

Reader Conditional:

```clj
#?(:clj "Clojure" :cljs "ClojureScript")
;;=> "ClojureScript"
```

---

###### See Also:

[`#"" regex`](syntax_regex.md)<br>
[`#() function`](syntax_function.md)<br>
[`#{} set`](syntax_set.md)<br>
[`#' var`](syntax_var.md)<br>
[`#_ ignore`](syntax_ignore.md)<br>
[`# tagged literal`](syntax_tagged-literal.md)<br>
[`#? reader conditional`](syntax_cond.md)<br>

---





Reader code @ [github](https://github.com/clojure/tools.reader/blob/tools.reader-0.10.0-alpha3/src/main/clojure/clojure/tools/reader.clj#L66-L72):

```clj
(defn- read-dispatch
  [rdr _ opts pending-forms]
  (if-let [ch (read-char rdr)]
    (if-let [dm (dispatch-macros ch)]
      (dm rdr ch opts pending-forms)
      (read-tagged (doto rdr (unread ch)) ch opts pending-forms)) ;; ctor reader is implemented as a tagged literal
    (reader-error rdr "EOF while reading character")))
```

<!--
Repo - tag - source tree - lines:

 <pre>
tools.reader @ tools.reader-0.10.0-alpha3
└── src
    └── main
        └── clojure
            └── clojure
                └── tools
                    └── <ins>[reader.clj:66-72](https://github.com/clojure/tools.reader/blob/tools.reader-0.10.0-alpha3/src/main/clojure/clojure/tools/reader.clj#L66-L72)</ins>
</pre>
-->

---
Reader table @ [github](https://github.com/clojure/tools.reader/blob/tools.reader-0.10.0-alpha3/src/main/clojure/clojure/tools/reader.clj#L743-L762):

```clj
(defn- macros [ch]
  (case ch
    \" read-string*
    \: read-keyword
    \; read-comment
    \' (wrapping-reader 'quote)
    \@ (wrapping-reader 'clojure.core/deref)
    \^ read-meta
    \` read-syntax-quote ;;(wrapping-reader 'syntax-quote)
    \~ read-unquote
    \( read-list
    \) read-unmatched-delimiter
    \[ read-vector
    \] read-unmatched-delimiter
    \{ read-map
    \} read-unmatched-delimiter
    \\ read-char*
    \% read-arg
    \# read-dispatch
    nil))
```

<!--
Repo - tag - source tree - lines:

 <pre>
tools.reader @ tools.reader-0.10.0-alpha3
└── src
    └── main
        └── clojure
            └── clojure
                └── tools
                    └── <ins>[reader.clj:743-762](https://github.com/clojure/tools.reader/blob/tools.reader-0.10.0-alpha3/src/main/clojure/clojure/tools/reader.clj#L743-L762)</ins>
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

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/syntax_dispatch.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "`#` is a prefix character that is called the dispatch macro, because it allows\nthe behavior of the reader to be dispatched to another table, indexed by the\ncharacter following the `#`.\n\nSyntax forms prefixed with `#` are made to bear some similarity to their\noriginal forms:\n\n| original                           | with `#` prefix                                  | relation               |\n|------------------------------------|--------------------------------------------------|------------------------|\n| [syntax/string]                    | [syntax/regex]                                   | string-related         |\n| [syntax/list]                      | [syntax/function]                                | code-related           |\n| [syntax/map]                       | [syntax/set]                                     | lookup-related         |\n| [syntax/quote]                     | [syntax/var]                                     | quote-related          |\n| [syntax/unused]                    | [syntax/ignore]                                  | ignore-related         |\n| [`foo (symbol)`](syntax/symbol)    | [`#foo (tagged literal)`](syntax/tagged-literal) | name-related           |\n| [syntax/predicate]                 | [syntax/cond]                                    | conditional-related    |",
 :ns "syntax",
 :name "dispatch",
 :history [["+" "0.0-927"]],
 :type "syntax",
 :related ["syntax/regex"
           "syntax/function"
           "syntax/set"
           "syntax/var"
           "syntax/ignore"
           "syntax/tagged-literal"
           "syntax/cond"],
 :full-name-encode "syntax_dispatch",
 :extra-sources ({:code "(defn- read-dispatch\n  [rdr _ opts pending-forms]\n  (if-let [ch (read-char rdr)]\n    (if-let [dm (dispatch-macros ch)]\n      (dm rdr ch opts pending-forms)\n      (read-tagged (doto rdr (unread ch)) ch opts pending-forms)) ;; ctor reader is implemented as a tagged literal\n    (reader-error rdr \"EOF while reading character\")))",
                  :title "Reader code",
                  :repo "tools.reader",
                  :tag "tools.reader-0.10.0-alpha3",
                  :filename "src/main/clojure/clojure/tools/reader.clj",
                  :lines [66 72]}
                 {:code "(defn- macros [ch]\n  (case ch\n    \\\" read-string*\n    \\: read-keyword\n    \\; read-comment\n    \\' (wrapping-reader 'quote)\n    \\@ (wrapping-reader 'clojure.core/deref)\n    \\^ read-meta\n    \\` read-syntax-quote ;;(wrapping-reader 'syntax-quote)\n    \\~ read-unquote\n    \\( read-list\n    \\) read-unmatched-delimiter\n    \\[ read-vector\n    \\] read-unmatched-delimiter\n    \\{ read-map\n    \\} read-unmatched-delimiter\n    \\\\ read-char*\n    \\% read-arg\n    \\# read-dispatch\n    nil))",
                  :title "Reader table",
                  :repo "tools.reader",
                  :tag "tools.reader-0.10.0-alpha3",
                  :filename "src/main/clojure/clojure/tools/reader.clj",
                  :lines [743 762]}),
 :usage ["#..."],
 :examples [{:id "0a1f4c",
             :content "The dispatch macro is not usable on its own.  Rather, it dispatches to other\nsyntax forms.\n\nRegular expression:\n\n```clj\n#\"[a-zA-Z0-9]+\"\n;;=> #\"[a-zA-Z0-9]+\"\n```\n\nSet:\n\n```clj\n#{:foo 1 2}\n;;=> #{:foo 1 2}\n```\n\nFunction:\n\n```clj\n#(foo 1 2)\n;;=> #<function (){\n;;   return cljs.user.foo.call(null,(1),(2));\n;;   }>\n```\n\nVar reference:\n\n```clj\n(def a)\n#'a\n;;=> #'cljs.user/a\n```\n\nIgnore form:\n\n```clj\n#_foo\n;; waits for next form since #_foo was ignored\n\n#_123 456\n;;=> 456\n```\n\nTagged Literals:\n\n```clj\n#queue [1 2 3]\n;;=> #queue [1 2 3]\n\n#js {:foo 1}\n;;=> #js {:foo 1}\n\n#inst \"2010-11-12T18:14:15.666-00:00\"\n;;=> #inst \"2010-11-12T18:14:15.666-00:00\"\n```\n\nReader Conditional:\n\n```clj\n#?(:clj \"Clojure\" :cljs \"ClojureScript\")\n;;=> \"ClojureScript\"\n```"}],
 :edn-doc "https://github.com/edn-format/edn#-dispatch-character",
 :full-name "syntax/dispatch",
 :display "# dispatch",
 :clj-doc "http://clojure.org/reader#toc2"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "syntax/dispatch"]))
```

-->
