## cljs.core/pr-with-opts



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__pr-with-opts__ objs opts)<br>
</samp>

---





Source docstring:

```
Prints a sequence of objects using string-print, observing all
the options given in opts
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r993/src/cljs/cljs/core.cljs#L2893-L2902):

```clj
(defn pr-with-opts
  [objs opts]
  (let [first-obj (first objs)]
    (doseq [obj objs]
      (when-not (identical? obj first-obj)
        (string-print " "))
      (doseq [string (pr-seq obj opts)]
        (string-print string)))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r993
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:2893-2902](https://github.com/clojure/clojurescript/blob/r993/src/cljs/cljs/core.cljs#L2893-L2902)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/pr-with-opts` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/pr-with-opts.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_pr-with-opts.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "pr-with-opts",
 :signature ["[objs opts]"],
 :history [["+" "0.0-927"]],
 :type "function",
 :full-name-encode "cljs.core_pr-with-opts",
 :source {:code "(defn pr-with-opts\n  [objs opts]\n  (let [first-obj (first objs)]\n    (doseq [obj objs]\n      (when-not (identical? obj first-obj)\n        (string-print \" \"))\n      (doseq [string (pr-seq obj opts)]\n        (string-print string)))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r993",
          :filename "src/cljs/cljs/core.cljs",
          :lines [2893 2902]},
 :full-name "cljs.core/pr-with-opts",
 :docstring "Prints a sequence of objects using string-print, observing all\nthe options given in opts"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/pr-with-opts"]))
```

-->
