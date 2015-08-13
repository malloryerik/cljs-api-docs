## cljs.core/uuid



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-3291"><img valign="middle" alt="[+] 0.0-3291" title="Added in 0.0-3291" src="https://img.shields.io/badge/+-0.0--3291-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__uuid__ s)<br>
</samp>

---

Creates a universally unique identifier (UUID) from the given string, using the
[`UUID`](cljs.core_UUID.md) type.

The string has an expected format `8-4-4-12` where the numbers represent the
number of hex digits.  No validation is performed.

To create a UUID literal (parsed and validated at compile time), use [`#uuid literal`](syntax_uuid-literal.md).

---

###### Examples:

```clj
(uuid "00000000-0000-0000-0000-000000000000")
;;=> #uuid "00000000-0000-0000-0000-000000000000"

(uuid "97bda55b-6175-4c39-9e04-7c0205c709dc")
;;=> #uuid "97bda55b-6175-4c39-9e04-7c0205c709dc"
```

No validation is performed:

```clj
(uuid "")
;;=> #uuid ""
```

---

###### See Also:

[`cljs.core/random-uuid`](cljs.core_random-uuid.md)<br>
[`#uuid literal`](syntax_uuid-literal.md)<br>

---




Source code @ [github](https://github.com/clojure/clojurescript/blob/r1.7.48/src/main/cljs/cljs/core.cljs#L9832-L9833):

```clj
(defn uuid [s]
  (UUID. s nil))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1.7.48
└── src
    └── main
        └── cljs
            └── cljs
                └── <ins>[core.cljs:9832-9833](https://github.com/clojure/clojurescript/blob/r1.7.48/src/main/cljs/cljs/core.cljs#L9832-L9833)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/uuid` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/uuid.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_uuid.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Creates a universally unique identifier (UUID) from the given string, using the\n[cljs.core/UUID] type.\n\nThe string has an expected format `8-4-4-12` where the numbers represent the\nnumber of hex digits.  No validation is performed.\n\nTo create a UUID literal (parsed and validated at compile time), use [syntax/uuid-literal].",
 :ns "cljs.core",
 :name "uuid",
 :signature ["[s]"],
 :history [["+" "0.0-3291"]],
 :type "function",
 :related ["cljs.core/random-uuid" "syntax/uuid-literal"],
 :full-name-encode "cljs.core_uuid",
 :source {:code "(defn uuid [s]\n  (UUID. s nil))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1.7.48",
          :filename "src/main/cljs/cljs/core.cljs",
          :lines [9832 9833]},
 :examples [{:id "d6491d",
             :content "```clj\n(uuid \"00000000-0000-0000-0000-000000000000\")\n;;=> #uuid \"00000000-0000-0000-0000-000000000000\"\n\n(uuid \"97bda55b-6175-4c39-9e04-7c0205c709dc\")\n;;=> #uuid \"97bda55b-6175-4c39-9e04-7c0205c709dc\"\n```\n\nNo validation is performed:\n\n```clj\n(uuid \"\")\n;;=> #uuid \"\"\n```"}],
 :full-name "cljs.core/uuid"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/uuid"]))
```

-->
