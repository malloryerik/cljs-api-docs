## ! impure



 <table border="1">
<tr>
<td>convention</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> clj doc](http://clojure.org/cheatsheet)
</td>
</tr>
</table>

<samp>foo!</samp><br>

---


A naming convention for impure functions (unenforced).

Impure functions are those that have side-effects on some state.

Some impure functions which use this convention:

- [`set!`](special_setBANG.md)
- [`swap!`](cljs.core_swapBANG.md)
- [cljs.core/conj!]
- [cljs.core/specify!]

---

###### Examples:

The following causes a side-effect in the state of `a`:

```clj
(def a (atom 1))
@a
;;=> 1

(reset! a 2)
@a
;;=> 2
```

---

###### See Also:

[`? predicate`](syntax_predicate.md)<br>

---








 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/syntax_impure.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "A naming convention for impure functions (unenforced).\n\nImpure functions are those that have side-effects on some state.\n\nSome impure functions which use this convention:\n\n- [special/set!]\n- [cljs.core/swap!]\n- [cljs.core/conj!]\n- [cljs.core/specify!]",
 :ns "syntax",
 :name "impure",
 :history [["+" "0.0-927"]],
 :type "convention",
 :related ["syntax/predicate"],
 :full-name-encode "syntax_impure",
 :usage ["foo!"],
 :examples [{:id "c1dbc0",
             :content "The following causes a side-effect in the state of `a`:\n\n```clj\n(def a (atom 1))\n@a\n;;=> 1\n\n(reset! a 2)\n@a\n;;=> 2\n```"}],
 :full-name "syntax/impure",
 :display "! impure",
 :clj-doc "http://clojure.org/cheatsheet"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "syntax/impure"]))
```

-->
