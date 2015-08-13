## cljs.js/require



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/1.7.10"><img valign="middle" alt="[+] 1.7.10" title="Added in 1.7.10" src="https://img.shields.io/badge/+-1.7.10-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__require__ name cb)<br>
</samp>
 <samp>
(__require__ name opts cb)<br>
</samp>
 <samp>
(__require__ bound-vars name opts cb)<br>
</samp>
 <samp>
(__require__ bound-vars name reload opts cb)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r1.7.28/src/main/cljs/cljs/js.cljs#L161-L232):

```clj
(defn require
  ([name cb]
    (require name nil cb))
  ([name opts cb]
    (require nil name opts cb))
  ([bound-vars name opts cb]
   (require bound-vars name nil opts cb))
  ([bound-vars name reload opts cb]
   (let [bound-vars (merge
                      {:*compiler*     (env/default-compiler-env)
                       :*data-readers* tags/*cljs-data-readers*
                       :*load-macros*  (or (:load-macros opts) true)
                       :*analyze-deps* (or (:analyze-deps opts) true)
                       :*load-fn*      (or (:load opts) *load-fn*)
                       :*eval-fn*      (or (:eval opts) *eval-fn*)}
                      bound-vars)
         name (cond-> name (:macro-ns opts) ana/macro-ns-name)]
     (when (= :reload reload)
       (swap! *loaded* disj name))
     (when (= :reload-all reload)
       (reset! *loaded* #{}))
     (when (:verbose opts)
       (debug-prn (str "Loading " name (when (:macros-ns opts) " macros") " namespace")))
     (if-not (contains? @*loaded* name)
       (let [env (:*env* bound-vars)]
         (try
           ((:*load-fn* bound-vars)
             {:name name
              :macros (:macros-ns opts)
              :path (ns->relpath name)}
             (fn [resource]
               (assert (or (map? resource) (nil? resource))
                 "*load-fn* may only return a map or nil")
               (if resource
                 (let [{:keys [lang source cache source-map]} resource]
                   (condp = lang
                     :clj (eval-str* bound-vars source name opts
                            (fn [res]
                              (if (:error res)
                                (cb res)
                                (do
                                  (swap! *loaded* conj name)
                                  (cb {:value true})))))
                     :js  (let [res (try
                                      ((:*eval-fn* bound-vars) resource)
                                      (when cache
                                        (load-analysis-cache!
                                          (:*compiler* bound-vars) name cache))
                                      (when source-map
                                        (load-source-map!
                                          (:*compiler* bound-vars) name source-map))
                                      (catch :default cause
                                        (wrap-error
                                          (ana/error env
                                            (str "Could not require " name) cause))))]
                            (if (:error res)
                              (cb res)
                              (do
                                (swap! *loaded* conj name)
                                (cb {:value true}))))
                     (cb (wrap-error
                           (ana/error env
                             (str "Invalid :lang specified " lang ", only :clj or :js allowed"))))))
                 (cb (wrap-error
                       (ana/error env
                         (ana/error-message :undeclared-ns
                           {:ns-sym name :js-provide (cljs.core/name name)})))))))
           (catch :default cause
             (cb (wrap-error
                   (ana/error env
                     (str "Could not require " name) cause))))))
       (cb {:value true})))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1.7.28
└── src
    └── main
        └── cljs
            └── cljs
                └── <ins>[js.cljs:161-232](https://github.com/clojure/clojurescript/blob/r1.7.28/src/main/cljs/cljs/js.cljs#L161-L232)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.js/require` @ crossclj](http://crossclj.info/fun/cljs.js.cljs/require.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.js_require.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.js",
 :name "require",
 :type "function",
 :signature ["[name cb]"
             "[name opts cb]"
             "[bound-vars name opts cb]"
             "[bound-vars name reload opts cb]"],
 :source {:code "(defn require\n  ([name cb]\n    (require name nil cb))\n  ([name opts cb]\n    (require nil name opts cb))\n  ([bound-vars name opts cb]\n   (require bound-vars name nil opts cb))\n  ([bound-vars name reload opts cb]\n   (let [bound-vars (merge\n                      {:*compiler*     (env/default-compiler-env)\n                       :*data-readers* tags/*cljs-data-readers*\n                       :*load-macros*  (or (:load-macros opts) true)\n                       :*analyze-deps* (or (:analyze-deps opts) true)\n                       :*load-fn*      (or (:load opts) *load-fn*)\n                       :*eval-fn*      (or (:eval opts) *eval-fn*)}\n                      bound-vars)\n         name (cond-> name (:macro-ns opts) ana/macro-ns-name)]\n     (when (= :reload reload)\n       (swap! *loaded* disj name))\n     (when (= :reload-all reload)\n       (reset! *loaded* #{}))\n     (when (:verbose opts)\n       (debug-prn (str \"Loading \" name (when (:macros-ns opts) \" macros\") \" namespace\")))\n     (if-not (contains? @*loaded* name)\n       (let [env (:*env* bound-vars)]\n         (try\n           ((:*load-fn* bound-vars)\n             {:name name\n              :macros (:macros-ns opts)\n              :path (ns->relpath name)}\n             (fn [resource]\n               (assert (or (map? resource) (nil? resource))\n                 \"*load-fn* may only return a map or nil\")\n               (if resource\n                 (let [{:keys [lang source cache source-map]} resource]\n                   (condp = lang\n                     :clj (eval-str* bound-vars source name opts\n                            (fn [res]\n                              (if (:error res)\n                                (cb res)\n                                (do\n                                  (swap! *loaded* conj name)\n                                  (cb {:value true})))))\n                     :js  (let [res (try\n                                      ((:*eval-fn* bound-vars) resource)\n                                      (when cache\n                                        (load-analysis-cache!\n                                          (:*compiler* bound-vars) name cache))\n                                      (when source-map\n                                        (load-source-map!\n                                          (:*compiler* bound-vars) name source-map))\n                                      (catch :default cause\n                                        (wrap-error\n                                          (ana/error env\n                                            (str \"Could not require \" name) cause))))]\n                            (if (:error res)\n                              (cb res)\n                              (do\n                                (swap! *loaded* conj name)\n                                (cb {:value true}))))\n                     (cb (wrap-error\n                           (ana/error env\n                             (str \"Invalid :lang specified \" lang \", only :clj or :js allowed\"))))))\n                 (cb (wrap-error\n                       (ana/error env\n                         (ana/error-message :undeclared-ns\n                           {:ns-sym name :js-provide (cljs.core/name name)})))))))\n           (catch :default cause\n             (cb (wrap-error\n                   (ana/error env\n                     (str \"Could not require \" name) cause))))))\n       (cb {:value true})))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1.7.28",
          :filename "src/main/cljs/cljs/js.cljs",
          :lines [161 232]},
 :full-name "cljs.js/require",
 :full-name-encode "cljs.js_require",
 :history [["+" "1.7.10"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.js/require"]))
```

-->
