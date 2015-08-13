## cljs.core/load-file\*



 <table border="1">
<tr>
<td>macro</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-2719"><img valign="middle" alt="[+] 0.0-2719" title="Added in 0.0-2719" src="https://img.shields.io/badge/+-0.0--2719-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__load-file\*__ f)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r2719/src/clj/cljs/core.clj#L1694-L1699):

```clj
(defmacro load-file* [f]
  (core/let [{:keys [target output-dir]} (:options @env/*compiler*)]
    (core/condp = target
      ;; under Node.js, always relative to JVM working directory
      :nodejs `(. js/goog (~'nodeGlobalRequire (str ~output-dir ~File/separator ~f)))
      `(. js/goog (~'importScript_ ~f)))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2719
└── src
    └── clj
        └── cljs
            └── <ins>[core.clj:1694-1699](https://github.com/clojure/clojurescript/blob/r2719/src/clj/cljs/core.clj#L1694-L1699)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/load-file*` @ crossclj](http://crossclj.info/fun/cljs.core/load-file*.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_load-fileSTAR.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "load-file*",
 :type "macro",
 :signature ["[f]"],
 :source {:code "(defmacro load-file* [f]\n  (core/let [{:keys [target output-dir]} (:options @env/*compiler*)]\n    (core/condp = target\n      ;; under Node.js, always relative to JVM working directory\n      :nodejs `(. js/goog (~'nodeGlobalRequire (str ~output-dir ~File/separator ~f)))\n      `(. js/goog (~'importScript_ ~f)))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2719",
          :filename "src/clj/cljs/core.clj",
          :lines [1694 1699]},
 :full-name "cljs.core/load-file*",
 :full-name-encode "cljs.core_load-fileSTAR",
 :history [["+" "0.0-2719"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/load-file*"]))
```

-->
