# wtf is re-frame
A look into the [re-frame](https://github.com/Day8/re-frame) clojurescript lib. 

*work in progress*

> "re-frame is a pattern for writing SPAs in ClojureScript, using Reagent."


As taken from the readme, 

>To build a re-frame app, you:
>
* design your app's data structure (data layer)
* write and register subscription functions (query layer)
* write Reagent component functions (view layer)
* write and register event handler functions (control layer and/or state transition layer)

*Quotes*

MVC? or?
>Perhaps it is a RACES framework - Reactive-Atom Component Event Subscription framework (I love the smell of acronym in the morning).
>
>Or, if we distill to pure essence, DDATWD - Derived Data All The Way Down.

***

[what is reactive programming?](https://gist.github.com/staltz/868e7e9bc2a7b8c1f754)

https://github.com/Day8/re-frame#the-big-ratom

https://github.com/Day8/re-frame#how-flow-happens-in-reagent

https://github.com/Day8/re-frame#the-signal-graph

https://github.com/Day8/re-frame#event-flow

#### Data Layer
#### Query Layer
##### Subscribe

* Components should know as little as possible about the structure of ``` app-db```
* Subscription functions must return a value that changes over time (a Signal). They'll be returning a ```reaction``` or a ```ratom``` produced by a ```reaction```.
* Components never source data directly from ``ap-db``, instead they use a subscription.
* Subscriptions are only ever used by components (never event handlers).

Example

```
(defn greet         ;; outer, setup function, called once
  []
  (let [name-ratom  (subscribe [:name-query])]    ;; <---- subscribing happens here
     (fn []        ;; the inner, render function, potentially called many times.
         [:div "Hello" @name-ratom])))    
```

**subscribe is always called like this:**

   ``(subscribe  [query-id some optional query parameters])``


#### View Layer
* Reagent components
* Pure functions
* Data in, Hiccup out. (DOM)

```
(defn greet
  []
  [:div "Hello ratoms and reactions"])

;;And if we call it:

(greet)
;; ==>  [:div "Hello ratoms and reactions"]
```

#### Control Layer / State Transition Layer

