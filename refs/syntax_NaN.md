## NaN



 <table border="1">
<tr>
<td>special symbol</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1853"><img valign="middle" alt="[+] 0.0-1853" title="Added in 0.0-1853" src="https://img.shields.io/badge/+-0.0--1853-lightgrey.svg"></a> </td>
</tr>
</table>



The IEEE 754 Floating Point representation of NaN (not a number), an undefined
or unrepresentable value.

To test for NaN, use the native JavaScript [`js/isNaN`] or the safer [`js/Number.isNaN`].

[`js/isNaN`]:https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/isNaN
[`js/Number.isNaN`]:https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/isNaN

---

###### Examples:

```clj
NaN
;;=> NaN
```

Testing for NaN:

```clj
(js/Number.isNaN (/ 0 0))
;;=> true

(js/Number.isNaN 1)
;;=> false
```

Equivalent to the JavaScript symbol:

```clj
js/NaN
;;=> NaN
```

---

###### See Also:

[`Infinity`](syntax_Infinity.md)<br>
[`nil`](syntax_nil.md)<br>

---





Reader code @ [github](https://github.com/clojure/tools.reader/blob/tools.reader-0.9.2/src/main/clojure/clojure/tools/reader.clj#L297-L323):

```clj
(defn- read-symbol
  [rdr initch]
  (let [[line column] (starting-line-col-info rdr)]
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
                  (merge
                   (when-let [file (get-file-name rdr)]
                     {:file file})
                   (let [[end-line end-column] (ending-line-col-info rdr)]
                     {:line line
                      :column column
                      :end-line end-line
                      :end-column end-column})))))
            (reader-error rdr "Invalid token: " token))))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
tools.reader @ tools.reader-0.9.2
└── src
    └── main
        └── clojure
            └── clojure
                └── tools
                    └── <ins>[reader.clj:297-323](https://github.com/clojure/tools.reader/blob/tools.reader-0.9.2/src/main/clojure/clojure/tools/reader.clj#L297-L323)</ins>
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

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/syntax_NaN.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "The IEEE 754 Floating Point representation of NaN (not a number), an undefined\nor unrepresentable value.\n\nTo test for NaN, use the native JavaScript [`js/isNaN`] or the safer [`js/Number.isNaN`].\n\n[`js/isNaN`]:https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/isNaN\n[`js/Number.isNaN`]:https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/isNaN",
 :ns "syntax",
 :name "NaN",
 :history [["+" "0.0-1853"]],
 :type "special symbol",
 :related ["syntax/Infinity" "syntax/nil"],
 :full-name-encode "syntax_NaN",
 :extra-sources [{:code "(defn- read-symbol\n  [rdr initch]\n  (let [[line column] (starting-line-col-info rdr)]\n    (when-let [token (read-token rdr initch)]\n      (case token\n\n        ;; special symbols\n        \"nil\" nil\n        \"true\" true\n        \"false\" false\n        \"/\" '/\n        \"NaN\" Double/NaN\n        \"-Infinity\" Double/NEGATIVE_INFINITY\n        (\"Infinity\" \"+Infinity\") Double/POSITIVE_INFINITY\n\n        (or (when-let [p (parse-symbol token)]\n              (with-meta (symbol (p 0) (p 1))\n                (when line\n                  (merge\n                   (when-let [file (get-file-name rdr)]\n                     {:file file})\n                   (let [[end-line end-column] (ending-line-col-info rdr)]\n                     {:line line\n                      :column column\n                      :end-line end-line\n                      :end-column end-column})))))\n            (reader-error rdr \"Invalid token: \" token))))))",
                  :title "Reader code",
                  :repo "tools.reader",
                  :tag "tools.reader-0.9.2",
                  :filename "src/main/clojure/clojure/tools/reader.clj",
                  :lines [297 323]}],
 :examples [{:id "9661ba",
             :content "```clj\nNaN\n;;=> NaN\n```\n\nTesting for NaN:\n\n```clj\n(js/Number.isNaN (/ 0 0))\n;;=> true\n\n(js/Number.isNaN 1)\n;;=> false\n```\n\nEquivalent to the JavaScript symbol:\n\n```clj\njs/NaN\n;;=> NaN\n```"}],
 :full-name "syntax/NaN",
 :display "NaN"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "syntax/NaN"]))
```

-->
