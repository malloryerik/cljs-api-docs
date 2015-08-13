## cljs.repl.browser/send-and-close



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__send-and-close__ conn status form)<br>
</samp>
 <samp>
(__send-and-close__ conn status form content-type)<br>
</samp>

---





Source docstring:

```
Use the passed connection to send a form to the browser. Send a
proper HTTP response.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r1450/src/clj/cljs/repl/browser.clj#L69-L90):

```clj
(defn send-and-close
  ([conn status form]
     (send-and-close conn status form "text/html"))
  ([conn status form content-type]
     (let [utf-8-form (.getBytes form "UTF-8")
           content-length (count utf-8-form)
           headers (map #(.getBytes (str % "\r\n"))
                        [(status-line status)
                         "Server: ClojureScript REPL"
                         (str "Content-Type: "
                              content-type
                              "; charset=utf-8")
                         (str "Content-Length: " content-length)
                         ""])]
       (with-open [os (.getOutputStream conn)]
         (do (doseq [header headers]
               (.write os header 0 (count header)))
             (.write os utf-8-form 0 content-length)
             (.flush os)
             (.close conn))))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1450
└── src
    └── clj
        └── cljs
            └── repl
                └── <ins>[browser.clj:69-90](https://github.com/clojure/clojurescript/blob/r1450/src/clj/cljs/repl/browser.clj#L69-L90)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.repl.browser/send-and-close` @ crossclj](http://crossclj.info/fun/cljs.repl.browser/send-and-close.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.repl.browser_send-and-close.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.repl.browser",
 :name "send-and-close",
 :signature ["[conn status form]" "[conn status form content-type]"],
 :history [["+" "0.0-927"]],
 :type "function",
 :full-name-encode "cljs.repl.browser_send-and-close",
 :source {:code "(defn send-and-close\n  ([conn status form]\n     (send-and-close conn status form \"text/html\"))\n  ([conn status form content-type]\n     (let [utf-8-form (.getBytes form \"UTF-8\")\n           content-length (count utf-8-form)\n           headers (map #(.getBytes (str % \"\\r\\n\"))\n                        [(status-line status)\n                         \"Server: ClojureScript REPL\"\n                         (str \"Content-Type: \"\n                              content-type\n                              \"; charset=utf-8\")\n                         (str \"Content-Length: \" content-length)\n                         \"\"])]\n       (with-open [os (.getOutputStream conn)]\n         (do (doseq [header headers]\n               (.write os header 0 (count header)))\n             (.write os utf-8-form 0 content-length)\n             (.flush os)\n             (.close conn))))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1450",
          :filename "src/clj/cljs/repl/browser.clj",
          :lines [69 90]},
 :full-name "cljs.repl.browser/send-and-close",
 :docstring "Use the passed connection to send a form to the browser. Send a\nproper HTTP response."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.repl.browser/send-and-close"]))
```

-->
