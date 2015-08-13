## cljs.test/IAsyncTest



 <table border="1">
<tr>
<td>protocol</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-2814"><img valign="middle" alt="[+] 0.0-2814" title="Added in 0.0-2814" src="https://img.shields.io/badge/+-0.0--2814-lightgrey.svg"></a> </td>
</tr>
</table>







Source docstring:

```
Marker protocol denoting CPS function to begin asynchronous
  testing.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r3308/src/main/cljs/cljs/test.cljs#L399-L401):

```clj
(defprotocol IAsyncTest
  "Marker protocol denoting CPS function to begin asynchronous
  testing.")
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3308
└── src
    └── main
        └── cljs
            └── cljs
                └── <ins>[test.cljs:399-401](https://github.com/clojure/clojurescript/blob/r3308/src/main/cljs/cljs/test.cljs#L399-L401)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.test/IAsyncTest` @ crossclj](http://crossclj.info/fun/cljs.test.cljs/IAsyncTest.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.test_IAsyncTest.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.test",
 :name "IAsyncTest",
 :type "protocol",
 :full-name-encode "cljs.test_IAsyncTest",
 :source {:code "(defprotocol IAsyncTest\n  \"Marker protocol denoting CPS function to begin asynchronous\n  testing.\")",
          :title "Source code",
          :repo "clojurescript",
          :tag "r3308",
          :filename "src/main/cljs/cljs/test.cljs",
          :lines [399 401]},
 :full-name "cljs.test/IAsyncTest",
 :docstring "Marker protocol denoting CPS function to begin asynchronous\n  testing.",
 :history [["+" "0.0-2814"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.test/IAsyncTest"]))
```

-->
