# lib-watch
A place where i can store interesting libs by category.

 *work in progress*


## ClojureScript
#### [Secretary](https://github.com/gf3/secretary "cljs routes lib") 
When I was messing around with reagent I found this lib inside the re-frame framework. 
It looks to be a pretty strong cljs routing lib, with some neat features around Route matchers and actions.

###Quick Look

Route matcher        | URI              | Parameters
---------------------|------------------|--------------------------
`"/:x/:y"`           | `"/foo/bar"`     | `{:x "foo" :y "bar"}`
`"/:x/:x"`           | `"/foo/bar"`     | `{:x ["foo" "bar"]}`
`"/files/*.:format"`  | `"/files/x.zip"` | `{:* "x" :format "zip"}`
`"*"`                | `"/any/thing"`   | `{:* "/any/thing"}`
`"/*/*"`             | `"/n/e/thing"`   | `{:* ["n" "e/thing"]}`
`"/*x/*y"`           | `"/n/e/thing"`   | `{:x "n" :y "e/thing"}`
`#"/[a-z]+/\d+"`     | `"/foo/123"`     | `["/foo/123"]`
`#"/([a-z]+)/(\d+)"` | `"/foo/123"`     | `["foo" "123"]`


 
###Quick links

  * [Basic routing and dispatch](https://github.com/gf3/secretary/blob/master/README.md#basic-routing-and-dispatch)
  * [Route matchers](https://github.com/gf3/secretary/blob/master/README.md#route-matchers)
  * [Parameter destructuring](https://github.com/gf3/secretary/blob/master/README.md#parameter-destructuring)
  * [Query parameters](https://github.com/gf3/secretary/blob/master/README.md#query-parameters)
  * [Named routes](https://github.com/gf3/secretary/blob/master/README.md#named-routes)

***

## Clojure
#### [Luminus](http://www.luminusweb.net/ "clj web framework")
This is a web app framework I played around with a while ago. 

| Positives  | Negatives | 
|:------------- |:---------------:| 
| Very easy to use    | tbc  |         
       

### Questions
1. Can I use re-frame as the front end part of luminus?

#### Quick look
```
$ lein new luminus my-app
$ cd my-app
$ lein run
Started server on port 3000
```
#### Quick links
* [Your First Application](http://www.luminusweb.net/docs/guestbook.md)
* [REPL Driven Development](http://www.luminusweb.net/docs/repl.md)
* [Application Profiles](http://www.luminusweb.net/docs/profiles.md)
* [HTML Templating](http://www.luminusweb.net/docs/html_templating.md)
* [ClojureScript]( http://www.luminusweb.net/docs/clojurescript.md)
* [Routing](http://www.luminusweb.net/docs/routes.md)
* [RESTful Services](http://www.luminusweb.net/docs/services.md)
* [Request types](http://www.luminusweb.net/docs/requests.md)
* [Response types](http://www.luminusweb.net/docs/responses.md)
* [Websockets](http://www.luminusweb.net/docs/websockets.md)
* [Middleware](http://www.luminusweb.net/docs/middleware.md)
* [Sessions and Cookies](http://www.luminusweb.net/docs/sessions_cookies.md)
* [Input Validation](http://www.luminusweb.net/docs/input_validation.md)
* [Security](http://www.luminusweb.net/docs/security.md)
* [Database Access](http://www.luminusweb.net/docs/database.md)
* [Database Migrations](http://www.luminusweb.net/docs/migrations.md)
* [Logging](http://www.luminusweb.net/docs/logging.md)
* [Internationalization](http://www.luminusweb.net/docs/i18n.md)
* [Testing](http://www.luminusweb.net/docs/testing.md)
* [Environment Variables](http://www.luminusweb.net/docs/environment.md)
* [Deployment](http://www.luminusweb.net/docs/deployment.md)
* [Useful Libraries](http://www.luminusweb.net/docs/useful_libraries.md)
* [Sample Applications](http://www.luminusweb.net/docs/apps.md)
* [Upgrading](http://www.luminusweb.net/docs/upgrading.md)
* [Clojure Resources](http://www.luminusweb.net/docs/learning_clojure.md)


***