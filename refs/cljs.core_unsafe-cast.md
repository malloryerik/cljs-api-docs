## cljs.core/unsafe-cast



 <table border="1">
<tr>
<td>macro</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/1.7.107"><img valign="middle" alt="[+] 1.7.107" title="Added in 1.7.107" src="https://img.shields.io/badge/+-1.7.107-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__unsafe-cast__ t x)<br>
</samp>

---





Source docstring:

```
EXPERIMENTAL: Subject to change. Unsafely cast a value to a different type.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r1.7.107/src/main/clojure/cljs/core.cljc#L885-L889):

```clj
(core/defmacro unsafe-cast
  [t x]
  (core/let [cast-expr (core/str "~{} = /** @type {" t "} */ (~{})")]
    (core/list 'js* cast-expr x x)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1.7.107
└── src
    └── main
        └── clojure
            └── cljs
                └── <ins>[core.cljc:885-889](https://github.com/clojure/clojurescript/blob/r1.7.107/src/main/clojure/cljs/core.cljc#L885-L889)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/unsafe-cast` @ crossclj](http://crossclj.info/fun/cljs.core/unsafe-cast.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_unsafe-cast.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "unsafe-cast",
 :signature ["[t x]"],
 :history [["+" "1.7.107"]],
 :type "macro",
 :full-name-encode "cljs.core_unsafe-cast",
 :source {:code "(core/defmacro unsafe-cast\n  [t x]\n  (core/let [cast-expr (core/str \"~{} = /** @type {\" t \"} */ (~{})\")]\n    (core/list 'js* cast-expr x x)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1.7.107",
          :filename "src/main/clojure/cljs/core.cljc",
          :lines [885 889]},
 :full-name "cljs.core/unsafe-cast",
 :docstring "EXPERIMENTAL: Subject to change. Unsafely cast a value to a different type."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/unsafe-cast"]))
```

-->
