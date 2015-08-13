## cljs.core/volatile!



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-2496"><img valign="middle" alt="[+] 0.0-2496" title="Added in 0.0-2496" src="https://img.shields.io/badge/+-0.0--2496-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__volatile!__ val)<br>
</samp>

---



###### See Also:

[`cljs.core/volatile?`](cljs.core_volatileQMARK.md)<br>
[`cljs.core/vswap!`](cljs.core_vswapBANG.md)<br>
[`cljs.core/vreset!`](cljs.core_vresetBANG.md)<br>
[`cljs.core/Volatile`](cljs.core_Volatile.md)<br>

---


Source docstring:

```
Creates and returns a Volatile with an initial value of val.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r2755/src/cljs/cljs/core.cljs#L3604-L3607):

```clj
(defn volatile!
  [val]
  (Volatile. val))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2755
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:3604-3607](https://github.com/clojure/clojurescript/blob/r2755/src/cljs/cljs/core.cljs#L3604-L3607)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/volatile!` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/volatile%21.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_volatileBANG.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "volatile!",
 :signature ["[val]"],
 :history [["+" "0.0-2496"]],
 :type "function",
 :related ["cljs.core/volatile?"
           "cljs.core/vswap!"
           "cljs.core/vreset!"
           "cljs.core/Volatile"],
 :full-name-encode "cljs.core_volatileBANG",
 :source {:code "(defn volatile!\n  [val]\n  (Volatile. val))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2755",
          :filename "src/cljs/cljs/core.cljs",
          :lines [3604 3607]},
 :full-name "cljs.core/volatile!",
 :docstring "Creates and returns a Volatile with an initial value of val."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/volatile!"]))
```

-->
