## cljs.core/\*



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/\*</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/*)
</td>
</tr>
</table>


 <samp>
(__\*__)<br>
</samp>
 <samp>
(__\*__ x)<br>
</samp>
 <samp>
(__\*__ x y)<br>
</samp>
 <samp>
(__\*__ x y & more)<br>
</samp>

---

Returns the product of nums.

`(*)` returns 1.

---

###### Examples:

```clj
;; there is an implicit 1
(*)
;;=> 1

;; the implicit 1 comes into play
(* 6)
;;=> 6

(* 2 3)
;;=> 6

(* 2 3 4)
;;=> 24
```

---

###### See Also:

[`cljs.core/+`](cljs.core_PLUS.md)<br>
[`cljs.core//`](cljs.core_SLASH.md)<br>

---


Source docstring:

```
Returns the product of nums. (*) returns 1.
```


Function code @ [github](https://github.com/clojure/clojurescript/blob/r2075/src/cljs/cljs/core.cljs#L1443-L1448):

```clj
(defn ^number *
  ([] 1)
  ([x] x)
  ([x y] (cljs.core/* x y))
  ([x y & more] (reduce * (cljs.core/* x y) more)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2075
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:1443-1448](https://github.com/clojure/clojurescript/blob/r2075/src/cljs/cljs/core.cljs#L1443-L1448)</ins>
</pre>

-->

---

Macro code @ [github](https://github.com/clojure/clojurescript/blob/r2075/src/clj/cljs/core.clj#L394-L398):

```clj
(defmacro ^::ana/numeric *
  ([] 1)
  ([x] x)
  ([x y] (core/list 'js* "(~{} * ~{})" x y))
  ([x y & more] `(* (* ~x ~y) ~@more)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2075
└── src
    └── clj
        └── cljs
            └── <ins>[core.clj:394-398](https://github.com/clojure/clojurescript/blob/r2075/src/clj/cljs/core.clj#L394-L398)</ins>
</pre>
-->

---


###### External doc links:

[`clojure.core/*` @ clojuredocs](http://clojuredocs.org/clojure.core/*)<br>
[`clojure.core/*` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/*/)<br>
[`clojure.core/*` @ crossclj](http://crossclj.info/fun/clojure.core/*.html)<br>
[`cljs.core/*` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/*.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_STAR.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Returns the product of nums.\n\n`(*)` returns 1.",
 :return-type number,
 :ns "cljs.core",
 :name "*",
 :signature ["[]" "[x]" "[x y]" "[x y & more]"],
 :history [["+" "0.0-927"]],
 :type "function",
 :related ["cljs.core/+" "cljs.core//"],
 :full-name-encode "cljs.core_STAR",
 :source {:code "(defn ^number *\n  ([] 1)\n  ([x] x)\n  ([x y] (cljs.core/* x y))\n  ([x y & more] (reduce * (cljs.core/* x y) more)))",
          :title "Function code",
          :repo "clojurescript",
          :tag "r2075",
          :filename "src/cljs/cljs/core.cljs",
          :lines [1443 1448]},
 :extra-sources [{:code "(defmacro ^::ana/numeric *\n  ([] 1)\n  ([x] x)\n  ([x y] (core/list 'js* \"(~{} * ~{})\" x y))\n  ([x y & more] `(* (* ~x ~y) ~@more)))",
                  :title "Macro code",
                  :repo "clojurescript",
                  :tag "r2075",
                  :filename "src/clj/cljs/core.clj",
                  :lines [394 398]}],
 :examples [{:id "bc4a1f",
             :content "```clj\n;; there is an implicit 1\n(*)\n;;=> 1\n\n;; the implicit 1 comes into play\n(* 6)\n;;=> 6\n\n(* 2 3)\n;;=> 6\n\n(* 2 3 4)\n;;=> 24\n```"}],
 :full-name "cljs.core/*",
 :clj-symbol "clojure.core/*",
 :docstring "Returns the product of nums. (*) returns 1."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/*"]))
```

-->
