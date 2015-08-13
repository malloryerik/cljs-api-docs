## cljs.core/extend-type



 <table border="1">
<tr>
<td>macro</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/extend-type</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/extend-type)
</td>
</tr>
</table>


 <samp>
(__extend-type__ tsym & impls)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r927/src/clj/cljs/core.clj#L198-L234):

```clj
(defmacro extend-type [tsym & impls]
  (let [resolve #(let [ret (:name (cljs.compiler/resolve-var (dissoc &env :locals) %))]
                   (assert ret (str "Can't resolve: " %))
                   ret)
        impl-map (loop [ret {} s impls]
                   (if (seq s)
                     (recur (assoc ret (first s) (take-while seq? (next s)))
                            (drop-while seq? (next s)))
                     ret))]
    (if (base-type tsym)
      (let [t (base-type tsym)
            assign-impls (fn [[p sigs]]
                           (let [psym (resolve p)
				 pfn-prefix (subs (str psym) 0 (clojure.core/inc (.lastIndexOf (str psym) ".")))]
                             (cons `(aset ~psym ~t true)
                                   (map (fn [[f & meths]]
                                          `(aset ~(symbol (str pfn-prefix f)) ~t (fn* ~@meths)))
                                        sigs))))]
        `(do ~@(mapcat assign-impls impl-map)))
      (let [t (resolve tsym)
            prototype-prefix (str t ".prototype.")
            assign-impls (fn [[p sigs]]
                           (let [psym (resolve p)
				 pprefix (protocol-prefix psym)]
			     (if (= p 'Object)
			       (let [adapt-params (fn [[sig & body]]
						    (let [[tname & args] sig]
						      (list (with-meta (vec args) (meta sig))
							    (list* 'this-as tname body))))]
				 (map (fn [[f & meths]]
					`(set! ~(symbol (str prototype-prefix f)) (fn* ~@(map adapt-params meths))))
				      sigs))
			       (cons `(set! ~(symbol (str prototype-prefix pprefix)) true)
				     (map (fn [[f & meths]]
					    `(set! ~(symbol (str prototype-prefix pprefix f)) (fn* ~@meths)))
					  sigs)))))]
        `(do ~@(mapcat assign-impls impl-map))))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r927
└── src
    └── clj
        └── cljs
            └── <ins>[core.clj:198-234](https://github.com/clojure/clojurescript/blob/r927/src/clj/cljs/core.clj#L198-L234)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/extend-type` @ clojuredocs](http://clojuredocs.org/clojure.core/extend-type)<br>
[`clojure.core/extend-type` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/extend-type/)<br>
[`clojure.core/extend-type` @ crossclj](http://crossclj.info/fun/clojure.core/extend-type.html)<br>
[`cljs.core/extend-type` @ crossclj](http://crossclj.info/fun/cljs.core/extend-type.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core_extend-type.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "extend-type",
 :signature ["[tsym & impls]"],
 :history [["+" "0.0-927"]],
 :type "macro",
 :full-name-encode "cljs.core_extend-type",
 :source {:code "(defmacro extend-type [tsym & impls]\n  (let [resolve #(let [ret (:name (cljs.compiler/resolve-var (dissoc &env :locals) %))]\n                   (assert ret (str \"Can't resolve: \" %))\n                   ret)\n        impl-map (loop [ret {} s impls]\n                   (if (seq s)\n                     (recur (assoc ret (first s) (take-while seq? (next s)))\n                            (drop-while seq? (next s)))\n                     ret))]\n    (if (base-type tsym)\n      (let [t (base-type tsym)\n            assign-impls (fn [[p sigs]]\n                           (let [psym (resolve p)\n\t\t\t\t pfn-prefix (subs (str psym) 0 (clojure.core/inc (.lastIndexOf (str psym) \".\")))]\n                             (cons `(aset ~psym ~t true)\n                                   (map (fn [[f & meths]]\n                                          `(aset ~(symbol (str pfn-prefix f)) ~t (fn* ~@meths)))\n                                        sigs))))]\n        `(do ~@(mapcat assign-impls impl-map)))\n      (let [t (resolve tsym)\n            prototype-prefix (str t \".prototype.\")\n            assign-impls (fn [[p sigs]]\n                           (let [psym (resolve p)\n\t\t\t\t pprefix (protocol-prefix psym)]\n\t\t\t     (if (= p 'Object)\n\t\t\t       (let [adapt-params (fn [[sig & body]]\n\t\t\t\t\t\t    (let [[tname & args] sig]\n\t\t\t\t\t\t      (list (with-meta (vec args) (meta sig))\n\t\t\t\t\t\t\t    (list* 'this-as tname body))))]\n\t\t\t\t (map (fn [[f & meths]]\n\t\t\t\t\t`(set! ~(symbol (str prototype-prefix f)) (fn* ~@(map adapt-params meths))))\n\t\t\t\t      sigs))\n\t\t\t       (cons `(set! ~(symbol (str prototype-prefix pprefix)) true)\n\t\t\t\t     (map (fn [[f & meths]]\n\t\t\t\t\t    `(set! ~(symbol (str prototype-prefix pprefix f)) (fn* ~@meths)))\n\t\t\t\t\t  sigs)))))]\n        `(do ~@(mapcat assign-impls impl-map))))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r927",
          :filename "src/clj/cljs/core.clj",
          :lines [198 234]},
 :full-name "cljs.core/extend-type",
 :clj-symbol "clojure.core/extend-type"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/extend-type"]))
```

-->
