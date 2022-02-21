# Express REST API 

1- Name 3 real world use cases where you’d want to change the request with custom middleware?

- Authenticate users(validate email users)
- time of req
- it can use to handel error

2- True or false: The route handler is middleware?

- *true*

3- In what ways can a middleware function end the process and send data to the browser?

- when  the response and request cycle or process end.
- when there is error in request.

4- At what point in the request lifecycle can you “inject” middleware?

between res and req


Term | Definition
------------ | ------------
Middleware | Middleware are collections of specialized network services that are shared between applications and users. These software elements allow applications and networks to communicate with each other and to exploit their common power to process data. Middleware also serves as integration elements between applications that use different data formats
Request Object| Request is used to describe an request to a server. Use with fetch() to perform the request and get a Response. Request, fetch(), and Response are a new, low level replacement for XMLHttpRequest.
Response Object | constructor. Represents a response from a web request initiated by fetch(). fetch(), Request and Response are a new, low level replacement for XMLHttpRequest..
Application Middleware | Middleware is software that provides common services and capabilities to applications outside of what's offered by the operating system. ... Middleware helps developers build applications more efficiently. It acts like the connective tissue between applications, data, and users.
Routing Middleware | It is a piece of code that comes in the middle of request and response . It kind of hijacks your request so that you can do anything that you want with your request or response eg: Modify the data or call the next middleware.
Test Driven Development | Test-oriented development is a software development process that relies on a very short development cycle: first, the programmer writes a failed automatic check state and this check state must define a specific improvement or new function.
Behavioral Testing | is a testing of the external behaviour of the program, also known as black box testing. It is usually a functional testing.

-----------

# Review: ES6 Classes

## Classes

Classes are a template for creating objects. They encapsulate data with code to work on that data. Classes in JS are built on prototypes but also have some syntax and semantics that are not shared with ES5 class-like semantics. One way to define a class is using a class declaration. To declare a class, you use the class keyword with the name of the class .

for example 

class Rectangle { 
    constructor(height, width) { 
        this.height = height; this.width = width; 
    }
    }

## Hoisting

An important difference between function declarations and class declarations is that while functions can be called in code that appears before they are defined, classes must be defined before they can be constructed. The name given to a named class expression is local to the class's body. However, it can be accessed via the name property. let Rectangle = class { constructor(height, width) { this.height = height; this.width = width; }};console.log(Rectangle.name); let Rectangle = class Rectangle2 { constructor(height, width) { this.height = height; this.width = width; }};console.log(Rectangle.name); Note: Class expressions must be declared before they can be used (they are subject to the same hoisting restrictions as described in the class declarations section). There can only be one special method with the name "constructor" in a class. Static members (properties and methods) are called without instantiating their class and cannot be called.


## Class body and method definitions

- Strict mode
- Constructor 
- Static initialization blocks 


---------- 

# Using Express Routing 

## *Routing*

Routing refers to how an application’s endpoints (URIs) respond to client requests. For an introduction to routing, see Basic routing. You define routing using methods of the Express app object that correspond to HTTP methods;for example, app.get() to handle GET requests and app.post to handle POST requests. You can also use app.all() to handle all HTTP methods and app.use() tospecify middleware as the callback function (See Using middleware for details).These routing methods specify a callback function (sometimes called “handler functions”) called when the application receives a request to the specified route (endpoint) and HTTP method. In fact, the routing methods can have more than one callback function as arguments.

## *Route methods*

A route method is derived from one of the HTTP methods, and is attached to an instance of the express class. The following code is an example of routes that are defined for the GET and the POST methods to the root of the app.// GET method routeapp.get('/', (req, res) => { res.send('GET request to the homepage')})// POST method routeapp.post('/', (req, res) => { res.send('POST request to the homepage')})Express supports methods that correspond to all HTTP request methods: get, post, and so on. METHOD.There is a special routing method, app.all(), used to load middleware functions at a path for all HTTP request methods. For example, the following handler is executed for requests to the route “/secret” whether using GET, POST, PUT, DELETE, or any other HTTP request method supported in the http module.app.all('/secret', (req, res, next) => { console.log('Accessing the secret section ...') next() // pass control to the next handler})

## *Route paths*

Route paths, in combination with a request method, define the endpoints at which requests can be made. +, *, and () are subsets of their regular expression counterparts. If you need to use the dollar character ($) in a path string, enclose it escaped within ([ and ]). Express Route Tester is a handy tool for testing basic Express routes, although it does not support pattern matching. Here are some examples of route paths based on strings. This route path will match requests to the root route, /.app.get('/', (req, res) => { res.send('root')})This route path will match requests to /about.app.get('/about', (req, res) => { res.send('about')})This route path will match requests to /random.text.app.get('/random.text', (req, res) => { res.send('random.text')})Here are some examples of route paths based on string patterns.

## *Route parameters*

Route parameters are named URL segments that are used to capture the values specified at their position in the URL. The captured values are populated in the req.params object, with the name of the route parameter specified in the path as their respective keys. Route path: /users/:userId/books/:bookIdRequest URL: http://localhost:3000/users/34/books/8989req.params: { "userId": "34", "bookId": "8989" }To define routes with route parameters, simply specify the route parameters in the path of the route as shown below.app.get('/users/:userId/books/:bookId', (req, res) => { res.send(req.params)})The name of route parameters must be made up of “word characters” ([A-Za-z0-9_]).Since the hyphen (-) and the dot (.) are interpreted literally, they can be used along with route parameters for useful purposes.

## *oute handlers*

You can provide multiple callback functions that behave like middleware to handle a request. The only exception is that these callbacks might invoke next('route') to bypass the remaining route callbacks. You can use this mechanism to impose pre-conditions on a route, then pass control to subsequent routes if there’s no reason to proceed with the current route. Route handlers can be in the form of a function, an array of functions, or combinations of both, as shown in the following examples. For example:app.get('/example/b', (req, res, next) => { console.log('the response will be sent by the next function ...') next()}, (req, res) => { res.send('Hello from B!')})An array of callback functions can handle a route.

## *Response methods*

The methods on the response object (res) in the following table can send a response to the client, and terminate the request-response cycle. If none of these methods are called from a route handler, the client request will be left hanging. MethodDescriptionres.download()Prompt a file to be downloaded.res.end()End the response process.res.json()Send a JSON response.res.jsonp()Send a JSON response with JSONP support.res.redirect()Redirect a request.res.render()Render a view template.res.send()Send a response of various types.res.sendFile()Send a file as an octet stream.res.sendStatus()Set the response status code and send its string representation as the response body.

## *app.route()*

You can create chainable route handlers for a route path by using app.route().Because the path is specified at a single location, creating modular routes is helpful, as is reducing redundancy and typos. For more information about routes, see: Router() documentation. Here is an example of chained route handlers that are defined by using app.route().app.route('/book') .get((req, res) => { res.send('Get a random book') }) .post((req, res) => { res.send('Add a book') }) .put((req, res) => { res.send('Update the book') })

Router class to create modular, mountable route handlers. A Router instance is a complete middleware and routing system; for this reason, it is often referred to as a “mini-app”.The following example creates a router as a module, loads a middleware function in it, defines some routes, and mounts the router module on a path in the main app. Create a router file named birds.js in the app directory, with the following content:const express = require('express')const router = express.

--------

# Express Routing

Since Express has such a large presence in our Node applications, let’s take a look at how we can use the new features in our applications, specifically the Router.
get ( '/about' , function ( req , res ) { res .
Route with Parameters /hello/:name Let’s say we wanted to have a route called /hello/:name where we could pass in a person’s name into the URL and the application would spit out Hello name ! .
We can run validations and then we’ll pass the new variable to our .get route by storing it in req .

------------