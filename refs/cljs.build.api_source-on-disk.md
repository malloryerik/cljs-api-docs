## cljs.build.api/source-on-disk



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-3291"><img valign="middle" alt="[+] 0.0-3291" title="Added in 0.0-3291" src="https://img.shields.io/badge/+-0.0--3291-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__source-on-disk__ opts ijs)<br>
</samp>

---





Source docstring:

```
Ensure that the given IJavaScript exists on disk in the output directory.
Return updated IJavaScript with the new location if necessary.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r3291/src/main/clojure/cljs/build/api.clj#L106-L110):

```clj
(defn source-on-disk
  [opts ijs]
  (closure/source-on-disk opts ijs))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3291
└── src
    └── main
        └── clojure
            └── cljs
                └── build
                    └── <ins>[api.clj:106-110](https://github.com/clojure/clojurescript/blob/r3291/src/main/clojure/cljs/build/api.clj#L106-L110)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.build.api/source-on-disk` @ crossclj](http://crossclj.info/fun/cljs.build.api/source-on-disk.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.build.api_source-on-disk.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.build.api",
 :name "source-on-disk",
 :signature ["[opts ijs]"],
 :history [["+" "0.0-3291"]],
 :type "function",
 :full-name-encode "cljs.build.api_source-on-disk",
 :source {:code "(defn source-on-disk\n  [opts ijs]\n  (closure/source-on-disk opts ijs))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r3291",
          :filename "src/main/clojure/cljs/build/api.clj",
          :lines [106 110]},
 :full-name "cljs.build.api/source-on-disk",
 :docstring "Ensure that the given IJavaScript exists on disk in the output directory.\nReturn updated IJavaScript with the new location if necessary."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.build.api/source-on-disk"]))
```

-->
