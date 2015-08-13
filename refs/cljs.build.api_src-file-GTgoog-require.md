## cljs.build.api/src-file->goog-require



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-2629"><img valign="middle" alt="[+] 0.0-2629" title="Added in 0.0-2629" src="https://img.shields.io/badge/+-0.0--2629-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__src-file->goog-require__ src)<br>
</samp>
 <samp>
(__src-file->goog-require__ src options)<br>
</samp>
 <samp>
(__src-file->goog-require__ state src options)<br>
</samp>

---





Source docstring:

```
Given a ClojureScript or Google Closure style JavaScript source file return
the goog.require statement for it.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r1.7.48/src/main/clojure/cljs/build/api.clj#L109-L122):

```clj
(defn ^String src-file->goog-require
  ([src] (src-file->goog-require src nil))
  ([src options]
   (src-file->goog-require
     (if-not (nil? env/*compiler*)
       env/*compiler*
       (env/default-compiler-env))
     src options))
  ([state src options]
   (env/with-compiler-env state
     (binding [ana/*cljs-warning-handlers* (:warning-handlers options ana/*cljs-warning-handlers*)]
       (closure/src-file->goog-require src options)))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1.7.48
└── src
    └── main
        └── clojure
            └── cljs
                └── build
                    └── <ins>[api.clj:109-122](https://github.com/clojure/clojurescript/blob/r1.7.48/src/main/clojure/cljs/build/api.clj#L109-L122)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.build.api/src-file->goog-require` @ crossclj](http://crossclj.info/fun/cljs.build.api/src-file-%3Egoog-require.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.build.api_src-file-GTgoog-require.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:return-type String,
 :ns "cljs.build.api",
 :name "src-file->goog-require",
 :signature ["[src]" "[src options]" "[state src options]"],
 :history [["+" "0.0-2629"]],
 :type "function",
 :full-name-encode "cljs.build.api_src-file-GTgoog-require",
 :source {:code "(defn ^String src-file->goog-require\n  ([src] (src-file->goog-require src nil))\n  ([src options]\n   (src-file->goog-require\n     (if-not (nil? env/*compiler*)\n       env/*compiler*\n       (env/default-compiler-env))\n     src options))\n  ([state src options]\n   (env/with-compiler-env state\n     (binding [ana/*cljs-warning-handlers* (:warning-handlers options ana/*cljs-warning-handlers*)]\n       (closure/src-file->goog-require src options)))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1.7.48",
          :filename "src/main/clojure/cljs/build/api.clj",
          :lines [109 122]},
 :full-name "cljs.build.api/src-file->goog-require",
 :docstring "Given a ClojureScript or Google Closure style JavaScript source file return\nthe goog.require statement for it."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.build.api/src-file->goog-require"]))
```

-->
