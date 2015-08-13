## boolean literal



 <table border="1">
<tr>
<td>special symbol</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> clj doc](http://clojure.org/reader#toc1)
</td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/I8uNXHv.png"> edn doc](https://github.com/edn-format/edn#booleans)
</td>
</tr>
</table>

<samp>true</samp><br>
<samp>false</samp><br>

---


Special symbols representing the boolean literals `true` and `false`.
Both evaluate to themselves.

---

###### Examples:

```clj
true
;;=> true

false
;;=> false
```

---

###### See Also:

[`cljs.core/boolean`](cljs.core_boolean.md)<br>
[`if`](special_if.md)<br>
[`cljs.core/not`](cljs.core_not.md)<br>
[`cljs.core/true?`](cljs.core_trueQMARK.md)<br>
[`cljs.core/false?`](cljs.core_falseQMARK.md)<br>

---





Reader code @ [github](https://github.com/clojure/tools.reader/blob/tools.reader-0.8.3/src/main/clojure/clojure/tools/reader.clj#L263-L285):

```clj
(defn- read-symbol
  [rdr initch]
  (let [[line column] (when (indexing-reader? rdr)
                        [(get-line-number rdr) (int (dec (get-column-number rdr)))])]
    (when-let [token (read-token rdr initch)]
      (case token

        ;; special symbols
        "nil" nil
        "true" true
        "false" false
        "/" '/
        "NaN" Double/NaN
        "-Infinity" Double/NEGATIVE_INFINITY
        ("Infinity" "+Infinity") Double/POSITIVE_INFINITY

        (or (when-let [p (parse-symbol token)]
              (with-meta (symbol (p 0) (p 1))
                (when line
                  {:line line :column column
                   :end-line (get-line-number rdr)
                   :end-column (int (get-column-number rdr))})))
            (reader-error rdr "Invalid token: " token))))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
tools.reader @ tools.reader-0.8.3
└── src
    └── main
        └── clojure
            └── clojure
                └── tools
                    └── <ins>[reader.clj:263-285](https://github.com/clojure/tools.reader/blob/tools.reader-0.8.3/src/main/clojure/clojure/tools/reader.clj#L263-L285)</ins>
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

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/syntax_boolean.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Special symbols representing the boolean literals `true` and `false`.\nBoth evaluate to themselves.",
 :ns "syntax",
 :name "boolean",
 :history [["+" "0.0-927"]],
 :type "special symbol",
 :related ["cljs.core/boolean"
           "special/if"
           "cljs.core/not"
           "cljs.core/true?"
           "cljs.core/false?"],
 :full-name-encode "syntax_boolean",
 :extra-sources [{:code "(defn- read-symbol\n  [rdr initch]\n  (let [[line column] (when (indexing-reader? rdr)\n                        [(get-line-number rdr) (int (dec (get-column-number rdr)))])]\n    (when-let [token (read-token rdr initch)]\n      (case token\n\n        ;; special symbols\n        \"nil\" nil\n        \"true\" true\n        \"false\" false\n        \"/\" '/\n        \"NaN\" Double/NaN\n        \"-Infinity\" Double/NEGATIVE_INFINITY\n        (\"Infinity\" \"+Infinity\") Double/POSITIVE_INFINITY\n\n        (or (when-let [p (parse-symbol token)]\n              (with-meta (symbol (p 0) (p 1))\n                (when line\n                  {:line line :column column\n                   :end-line (get-line-number rdr)\n                   :end-column (int (get-column-number rdr))})))\n            (reader-error rdr \"Invalid token: \" token))))))",
                  :title "Reader code",
                  :repo "tools.reader",
                  :tag "tools.reader-0.8.3",
                  :filename "src/main/clojure/clojure/tools/reader.clj",
                  :lines [263 285]}],
 :usage ["true" "false"],
 :examples [{:id "1afc59",
             :content "```clj\ntrue\n;;=> true\n\nfalse\n;;=> false\n```"}],
 :edn-doc "https://github.com/edn-format/edn#booleans",
 :full-name "syntax/boolean",
 :display "boolean literal",
 :clj-doc "http://clojure.org/reader#toc1"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "syntax/boolean"]))
```

-->
