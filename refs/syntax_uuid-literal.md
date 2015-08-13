## #uuid literal



 <table border="1">
<tr>
<td>tagged literal</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1211"><img valign="middle" alt="[+] 0.0-1211" title="Added in 0.0-1211" src="https://img.shields.io/badge/+-0.0--1211-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> clj doc](https://github.com/clojure/clojure/blob/clojure-1.6.0/src/clj/clojure/core.clj#L6947)
</td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/I8uNXHv.png"> edn doc](https://github.com/edn-format/edn#uuid-f81d4fae-7dec-11d0-a765-00a0c91e6bf6)
</td>
</tr>
</table>

<samp>#uuid "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"</samp><br>

---


Creates a universally unique identifier (UUID), using the [`UUID`](cljs.core_UUID.md) type.

The format is `#uuid "8-4-4-4-12"`, where the numbers represent the number of hex digits.

Representing UUIDs with `#uuid` rather than just a plain string has the following benefits:

- the reader will throw an exception on malformed UUIDs
- its UUID type is preserved and shown when serialized to [edn].

To create a UUID from an evaluated expression, use [cljs.core/uuid].

[edn]:https://github.com/edn-format/edn

---

###### Examples:

```clj
#uuid "00000000-0000-0000-0000-000000000000"
;;=> #uuid "00000000-0000-0000-0000-000000000000"

#uuid "97bda55b-6175-4c39-9e04-7c0205c709dc"
;;=> #uuid "97bda55b-6175-4c39-9e04-7c0205c709dc"

#uuid "asdf"
;; clojure.lang.ExceptionInfo: Invalid UUID string: asdf
```

Get as a string:

```clj
(def foo #uuid "97bda55b-6175-4c39-9e04-7c0205c709dc")
(str foo)
;;=> "97bda55b-6175-4c39-9e04-7c0205c709dc"
```

---

###### See Also:

[``](cljs.core_uuid.md)<br>
[``](cljs.core_random-uuid.md)<br>

---





Reader code @ [github](https://github.com/clojure/clojurescript/blob/r3196/src/clj/cljs/tagged_literals.clj#L10-L17):

```clj
(defn read-uuid
  [form]
  (when-not (string? form)
    (throw (RuntimeException. "UUID literal expects a string as its representation.")))
  (try
    (java.util.UUID/fromString form)
    (catch Throwable e
      (throw (RuntimeException. (.getMessage e))))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3196
└── src
    └── clj
        └── cljs
            └── <ins>[tagged_literals.clj:10-17](https://github.com/clojure/clojurescript/blob/r3196/src/clj/cljs/tagged_literals.clj#L10-L17)</ins>
</pre>
-->

---
Reader table @ [github](https://github.com/clojure/clojurescript/blob/r3196/src/clj/cljs/tagged_literals.clj#L44-L48):

```clj
(def ^:dynamic *cljs-data-readers*
  {'queue read-queue
   'uuid  read-uuid
   'inst  read-inst
   'js    read-js})
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3196
└── src
    └── clj
        └── cljs
            └── <ins>[tagged_literals.clj:44-48](https://github.com/clojure/clojurescript/blob/r3196/src/clj/cljs/tagged_literals.clj#L44-L48)</ins>
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

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/syntax_uuid-literal.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Creates a universally unique identifier (UUID), using the [cljs.core/UUID] type.\n\nThe format is `#uuid \"8-4-4-4-12\"`, where the numbers represent the number of hex digits.\n\nRepresenting UUIDs with `#uuid` rather than just a plain string has the following benefits:\n\n- the reader will throw an exception on malformed UUIDs\n- its UUID type is preserved and shown when serialized to [edn].\n\nTo create a UUID from an evaluated expression, use [cljs.core/uuid].\n\n[edn]:https://github.com/edn-format/edn",
 :ns "syntax",
 :name "uuid-literal",
 :history [["+" "0.0-1211"]],
 :type "tagged literal",
 :related ["cljs.core/uuid" "cljs.core/random-uuid"],
 :full-name-encode "syntax_uuid-literal",
 :extra-sources ({:code "(defn read-uuid\n  [form]\n  (when-not (string? form)\n    (throw (RuntimeException. \"UUID literal expects a string as its representation.\")))\n  (try\n    (java.util.UUID/fromString form)\n    (catch Throwable e\n      (throw (RuntimeException. (.getMessage e))))))",
                  :title "Reader code",
                  :repo "clojurescript",
                  :tag "r3196",
                  :filename "src/clj/cljs/tagged_literals.clj",
                  :lines [10 17]}
                 {:code "(def ^:dynamic *cljs-data-readers*\n  {'queue read-queue\n   'uuid  read-uuid\n   'inst  read-inst\n   'js    read-js})",
                  :title "Reader table",
                  :repo "clojurescript",
                  :tag "r3196",
                  :filename "src/clj/cljs/tagged_literals.clj",
                  :lines [44 48]}),
 :usage ["#uuid \"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx\""],
 :examples [{:id "12c0f0",
             :content "```clj\n#uuid \"00000000-0000-0000-0000-000000000000\"\n;;=> #uuid \"00000000-0000-0000-0000-000000000000\"\n\n#uuid \"97bda55b-6175-4c39-9e04-7c0205c709dc\"\n;;=> #uuid \"97bda55b-6175-4c39-9e04-7c0205c709dc\"\n\n#uuid \"asdf\"\n;; clojure.lang.ExceptionInfo: Invalid UUID string: asdf\n```\n\nGet as a string:\n\n```clj\n(def foo #uuid \"97bda55b-6175-4c39-9e04-7c0205c709dc\")\n(str foo)\n;;=> \"97bda55b-6175-4c39-9e04-7c0205c709dc\"\n```"}],
 :edn-doc "https://github.com/edn-format/edn#uuid-f81d4fae-7dec-11d0-a765-00a0c91e6bf6",
 :full-name "syntax/uuid-literal",
 :display "#uuid literal",
 :clj-doc "https://github.com/clojure/clojure/blob/clojure-1.6.0/src/clj/clojure/core.clj#L6947"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "syntax/uuid-literal"]))
```

-->
