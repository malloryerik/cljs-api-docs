## whitespace



 <table border="1">
<tr>
<td>special character</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> clj doc](https://github.com/edn-format/edn#general-considerations)
</td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/I8uNXHv.png"> edn doc](https://github.com/edn-format/edn#general-considerations)
</td>
</tr>
</table>



The amount of whitespace between syntax forms does not affect syntax
correctness.  Elements are free to be aligned as desired.

Indentation is conventionally two spaces, no tab characters.
[More indentation conventions here](https://github.com/bbatsov/clojure-style-guide#source-code-layout--organization)

Whitespace around collection delimiters is not required:

```clj
(a(b(c)))
```

```clj
#js[1 2 3]
#inst"2015-10-12"
```

A [comma](syntax_comma.md) is considered whitespace:

```clj
[1, 2, 3]
{:foo 1, :bar 2}
```

---


###### See Also:

[`, comma`](syntax_comma.md)<br>

---








 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/syntax_whitespace.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "The amount of whitespace between syntax forms does not affect syntax\ncorrectness.  Elements are free to be aligned as desired.\n\nIndentation is conventionally two spaces, no tab characters.\n[More indentation conventions here](https://github.com/bbatsov/clojure-style-guide#source-code-layout--organization)\n\nWhitespace around collection delimiters is not required:\n\n```clj\n(a(b(c)))\n```\n\n```clj\n#js[1 2 3]\n#inst\"2015-10-12\"\n```\n\nA [comma](syntax/comma) is considered whitespace:\n\n```clj\n[1, 2, 3]\n{:foo 1, :bar 2}\n```",
 :ns "syntax",
 :name "whitespace",
 :history [["+" "0.0-927"]],
 :type "special character",
 :related ["syntax/comma"],
 :full-name-encode "syntax_whitespace",
 :edn-doc "https://github.com/edn-format/edn#general-considerations",
 :full-name "syntax/whitespace",
 :display "whitespace",
 :clj-doc "https://github.com/edn-format/edn#general-considerations"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "syntax/whitespace"]))
```

-->
