## \*earmuffs\*



 <table border="1">
<tr>
<td>convention</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> clj doc](http://clojure.org/cheatsheet)
</td>
</tr>
</table>

<samp>\*foo\*</samp><br>

---


A naming convention for dynamic vars (unenforced).

`(def ^:dynamic *foo* 1)`

Dynamic vars are global vars that you intend to temporarily rebind with
[`binding`](cljs.core_binding.md).

NOTE: Sometimes, the core library uses the earmuffs convention for non-dynamic
special global vars (e.g. [`*clojurescript-version*`](cljs.core_STARclojurescript-versionSTAR.md),
[`*main-cli-fn*`](cljs.core_STARmain-cli-fnSTAR.md)).

---

###### Examples:

```clj
(def ^:dynamic *foo* 1)

(def print-foo []
  (println *foo*))

(print-foo)
;; 1

(binding [*foo* 2]
  (print-foo))
;; 2

(print-foo)
;; 1
```

---

###### See Also:

[`cljs.core/binding`](cljs.core_binding.md)<br>

---








 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/syntax_earmuffs.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "A naming convention for dynamic vars (unenforced).\n\n`(def ^:dynamic *foo* 1)`\n\nDynamic vars are global vars that you intend to temporarily rebind with\n[cljs.core/binding].\n\nNOTE: Sometimes, the core library uses the earmuffs convention for non-dynamic\nspecial global vars (e.g. [cljs.core/*clojurescript-version*],\n[cljs.core/*main-cli-fn*]).",
 :ns "syntax",
 :name "earmuffs",
 :history [["+" "0.0-927"]],
 :type "convention",
 :related ["cljs.core/binding"],
 :full-name-encode "syntax_earmuffs",
 :usage ["*foo*"],
 :examples [{:id "91cf10",
             :content "```clj\n(def ^:dynamic *foo* 1)\n\n(def print-foo []\n  (println *foo*))\n\n(print-foo)\n;; 1\n\n(binding [*foo* 2]\n  (print-foo))\n;; 2\n\n(print-foo)\n;; 1\n```"}],
 :full-name "syntax/earmuffs",
 :display "*earmuffs*",
 :clj-doc "http://clojure.org/cheatsheet"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "syntax/earmuffs"]))
```

-->
