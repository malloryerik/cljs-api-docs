## cljs.core/bit-shift-right-zero-fill



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1211"><img valign="middle" alt="[+] 0.0-1211" title="Added in 0.0-1211" src="https://img.shields.io/badge/+-0.0--1211-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__bit-shift-right-zero-fill__ x n)<br>
</samp>

---





Source docstring:

```
DEPRECATED: Bitwise shift right with zero fill
```


Function code @ [github](https://github.com/clojure/clojurescript/blob/r2134/src/cljs/cljs/core.cljs#L1746-L1748):

```clj
(defn bit-shift-right-zero-fill
  [x n] (cljs.core/bit-shift-right-zero-fill x n))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2134
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:1746-1748](https://github.com/clojure/clojurescript/blob/r2134/src/cljs/cljs/core.cljs#L1746-L1748)</ins>
</pre>

-->

---

Macro code @ [github](https://github.com/clojure/clojurescript/blob/r2134/src/clj/cljs/core.clj#L507-L508):

```clj
(defmacro ^::ana/numeric bit-shift-right-zero-fill [x n]
  (core/list 'js* "(~{} >>> ~{})" x n))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2134
└── src
    └── clj
        └── cljs
            └── <ins>[core.clj:507-508](https://github.com/clojure/clojurescript/blob/r2134/src/clj/cljs/core.clj#L507-L508)</ins>
</pre>
-->

---


###### External doc links:

[`cljs.core/bit-shift-right-zero-fill` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/bit-shift-right-zero-fill.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_bit-shift-right-zero-fill.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "bit-shift-right-zero-fill",
 :signature ["[x n]"],
 :history [["+" "0.0-1211"]],
 :type "function",
 :full-name-encode "cljs.core_bit-shift-right-zero-fill",
 :source {:code "(defn bit-shift-right-zero-fill\n  [x n] (cljs.core/bit-shift-right-zero-fill x n))",
          :title "Function code",
          :repo "clojurescript",
          :tag "r2134",
          :filename "src/cljs/cljs/core.cljs",
          :lines [1746 1748]},
 :extra-sources [{:code "(defmacro ^::ana/numeric bit-shift-right-zero-fill [x n]\n  (core/list 'js* \"(~{} >>> ~{})\" x n))",
                  :title "Macro code",
                  :repo "clojurescript",
                  :tag "r2134",
                  :filename "src/clj/cljs/core.clj",
                  :lines [507 508]}],
 :full-name "cljs.core/bit-shift-right-zero-fill",
 :docstring "DEPRECATED: Bitwise shift right with zero fill"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/bit-shift-right-zero-fill"]))
```

-->
