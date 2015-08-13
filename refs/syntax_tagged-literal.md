## # tagged literal



 <table border="1">
<tr>
<td>syntax</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1211"><img valign="middle" alt="[+] 0.0-1211" title="Added in 0.0-1211" src="https://img.shields.io/badge/+-0.0--1211-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> clj doc](http://clojure.org/reader#toc4)
</td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/I8uNXHv.png"> edn doc](https://github.com/edn-format/edn#tagged-elements)
</td>
</tr>
</table>

<samp>#foo ...</samp><br>

---


A tagged literal is a way to tag another core syntax literal to represent a
single, new literal.

- `#foo []`
- `#foo {}`
- `#foo "bar"`
- `#foo 123`
- ...

If a [symbol](syntax_symbol.md) is prefixed by `#`, that symbol is considered a
__tag__ for the following form.  Together they represent a new value.  Real
examples:

- `#js {:foo 1}`, map -> JavaScript object
- `#inst "2015-01-12"` string -> Date

In these examples, the values `{:foo 1}` and `"2015-01-12"` are read normally,
but are further interpretted by their registered tag handlers to produce new
values: a JavaScript object and Date, respectively.

These tagged literals are the "extensible" part of extensible data notation
([edn]), with ClojureScript being a superset of edn.

[edn]:https://github.com/edn-format/edn#tagged-elements

ClojureScript supports the following tagged literals:

- [`#inst literal`](syntax_inst-literal.md)
- [`#uuid literal`](syntax_uuid-literal.md)
- [`#js literal`](syntax_js-literal.md)
- [`#queue literal`](syntax_queue-literal.md)

---

###### Examples:

(Tagged literals are printed as themselves, just like core syntax literals.)

literal JavaScript object:

```clj
#js {:foo 1}
;;=> #js {:foo 1}

(def foo 1)
#js {:foo foo}
;;=> #js {:foo 1}
```

literal queue:

```clj
#queue [1 2 3]
;;=> #queue [1 2 3]

(conj #queue [1 2 3] 4)
;;=> #queue [1 2 3 4]
```

literal instant of time (date):

```clj
#inst "2014-10-13"
;;=> #inst "2014-10-13T00:00:00.000-00:00"
```

literal UUID:

```clj
#uuid "97bda55b-6175-4c39-9e04-7c0205c709dc"
;;=> #uuid "97bda55b-6175-4c39-9e04-7c0205c709dc"
```

---

###### See Also:

[`# dispatch`](syntax_dispatch.md)<br>

---





Reader code @ [github](https://github.com/clojure/tools.reader/blob/tools.reader-0.8.4/src/main/clojure/clojure/tools/reader.clj#L660-L671):

```clj
(defn- read-tagged [rdr initch]
  (let [tag (read rdr true nil false)]
    (if-not (symbol? tag)
      (reader-error rdr "Reader tag must be a symbol"))
    (if-let [f (or (*data-readers* tag)
                   (default-data-readers tag))]
      (read-tagged* rdr tag f)
      (if (.contains (name tag) ".")
        (read-ctor rdr tag)
        (if-let [f *default-data-reader-fn*]
          (f tag (read rdr true nil true))
          (reader-error rdr "No reader function for tag " (name tag)))))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
tools.reader @ tools.reader-0.8.4
└── src
    └── main
        └── clojure
            └── clojure
                └── tools
                    └── <ins>[reader.clj:660-671](https://github.com/clojure/tools.reader/blob/tools.reader-0.8.4/src/main/clojure/clojure/tools/reader.clj#L660-L671)</ins>
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

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/syntax_tagged-literal.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "A tagged literal is a way to tag another core syntax literal to represent a\nsingle, new literal.\n\n- `#foo []`\n- `#foo {}`\n- `#foo \"bar\"`\n- `#foo 123`\n- ...\n\nIf a [symbol](syntax/symbol) is prefixed by `#`, that symbol is considered a\n__tag__ for the following form.  Together they represent a new value.  Real\nexamples:\n\n- `#js {:foo 1}`, map -> JavaScript object\n- `#inst \"2015-01-12\"` string -> Date\n\nIn these examples, the values `{:foo 1}` and `\"2015-01-12\"` are read normally,\nbut are further interpretted by their registered tag handlers to produce new\nvalues: a JavaScript object and Date, respectively.\n\nThese tagged literals are the \"extensible\" part of extensible data notation\n([edn]), with ClojureScript being a superset of edn.\n\n[edn]:https://github.com/edn-format/edn#tagged-elements\n\nClojureScript supports the following tagged literals:\n\n- [syntax/inst-literal]\n- [syntax/uuid-literal]\n- [syntax/js-literal]\n- [syntax/queue-literal]",
 :ns "syntax",
 :name "tagged-literal",
 :history [["+" "0.0-1211"]],
 :type "syntax",
 :related ["syntax/dispatch"],
 :full-name-encode "syntax_tagged-literal",
 :extra-sources [{:code "(defn- read-tagged [rdr initch]\n  (let [tag (read rdr true nil false)]\n    (if-not (symbol? tag)\n      (reader-error rdr \"Reader tag must be a symbol\"))\n    (if-let [f (or (*data-readers* tag)\n                   (default-data-readers tag))]\n      (read-tagged* rdr tag f)\n      (if (.contains (name tag) \".\")\n        (read-ctor rdr tag)\n        (if-let [f *default-data-reader-fn*]\n          (f tag (read rdr true nil true))\n          (reader-error rdr \"No reader function for tag \" (name tag)))))))",
                  :title "Reader code",
                  :repo "tools.reader",
                  :tag "tools.reader-0.8.4",
                  :filename "src/main/clojure/clojure/tools/reader.clj",
                  :lines [660 671]}],
 :usage ["#foo ..."],
 :examples [{:id "e84f6a",
             :content "(Tagged literals are printed as themselves, just like core syntax literals.)\n\nliteral JavaScript object:\n\n```clj\n#js {:foo 1}\n;;=> #js {:foo 1}\n\n(def foo 1)\n#js {:foo foo}\n;;=> #js {:foo 1}\n```\n\nliteral queue:\n\n```clj\n#queue [1 2 3]\n;;=> #queue [1 2 3]\n\n(conj #queue [1 2 3] 4)\n;;=> #queue [1 2 3 4]\n```\n\nliteral instant of time (date):\n\n```clj\n#inst \"2014-10-13\"\n;;=> #inst \"2014-10-13T00:00:00.000-00:00\"\n```\n\nliteral UUID:\n\n```clj\n#uuid \"97bda55b-6175-4c39-9e04-7c0205c709dc\"\n;;=> #uuid \"97bda55b-6175-4c39-9e04-7c0205c709dc\"\n```"}],
 :edn-doc "https://github.com/edn-format/edn#tagged-elements",
 :full-name "syntax/tagged-literal",
 :display "# tagged literal",
 :clj-doc "http://clojure.org/reader#toc4"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "syntax/tagged-literal"]))
```

-->
