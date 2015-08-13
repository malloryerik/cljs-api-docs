## cljs.repl/IParseStacktrace



 <table border="1">
<tr>
<td>protocol</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-2843"><img valign="middle" alt="[+] 0.0-2843" title="Added in 0.0-2843" src="https://img.shields.io/badge/+-0.0--2843-lightgrey.svg"></a> </td>
</tr>
</table>









Source code @ [github](https://github.com/clojure/clojurescript/blob/r2913/src/clj/cljs/repl.clj#L109-L120):

```clj
(defprotocol IParseStacktrace
  (-parse-stacktrace [repl-env stacktrace error build-options]
    "Given the original JavaScript stacktrace string, the entire original error
     value and current compiler build options, parse the stacktrace into the
     canonical form:

     [{:file <string>
       :function <string>
       :line <integer>
       :column <integer>}*]

     :file must be a URL path (without protocol) relative to :output-dir."))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2913
└── src
    └── clj
        └── cljs
            └── <ins>[repl.clj:109-120](https://github.com/clojure/clojurescript/blob/r2913/src/clj/cljs/repl.clj#L109-L120)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.repl/IParseStacktrace` @ crossclj](http://crossclj.info/fun/cljs.repl/IParseStacktrace.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.repl_IParseStacktrace.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.repl",
 :name "IParseStacktrace",
 :type "protocol",
 :full-name-encode "cljs.repl_IParseStacktrace",
 :source {:code "(defprotocol IParseStacktrace\n  (-parse-stacktrace [repl-env stacktrace error build-options]\n    \"Given the original JavaScript stacktrace string, the entire original error\n     value and current compiler build options, parse the stacktrace into the\n     canonical form:\n\n     [{:file <string>\n       :function <string>\n       :line <integer>\n       :column <integer>}*]\n\n     :file must be a URL path (without protocol) relative to :output-dir.\"))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2913",
          :filename "src/clj/cljs/repl.clj",
          :lines [109 120]},
 :methods [{:name "-parse-stacktrace",
            :signature ["[repl-env stacktrace error build-options]"],
            :docstring "Given the original JavaScript stacktrace string, the entire original error\n     value and current compiler build options, parse the stacktrace into the\n     canonical form:\n\n     [{:file <string>\n       :function <string>\n       :line <integer>\n       :column <integer>}*]\n\n     :file must be a URL path (without protocol) relative to :output-dir."}],
 :full-name "cljs.repl/IParseStacktrace",
 :history [["+" "0.0-2843"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.repl/IParseStacktrace"]))
```

-->
