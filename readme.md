# Node 2

## Top-Level Middleware

**Middleware** is any piece of logic that gets executed before an endpoint gets hit.

**Top-Level Middleware** is specifically middleware that is run before _every_ endpoint in our server.
  * We add Top-Level Middleware to our server by using the express method `app.use()`, passing in any logic to be run as an argument.

### express.json()

`express.json()` is Top-Level Middleware that comes from the _express_ framework. It is used to take incoming JSON in the body of a request and transform it into readable Javascript.
  * We invoke _express.json()_ as an argument of _app.use()_ to use it as Top-Level-Middleware: `app.use(express.json())`
  * NOTE: make sure all Top-Level-Middleware is placed above the endopints in your code. Otherwise it won't run in the correct order.

## Postman

The browser only allows us to make `get` requests to an api. If we want to make `post`, `put`, or `delete` requests, we need to use axios in our code or some other tool.

*Postman* is a development tool used to test _all_ endpoints, not just `get` endpoints.