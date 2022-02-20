
## 
1. What’s the difference between PUT and PATCH?

- PUT: sends an enclosed entity of a resource to the server. If 
the entity already exists, the server updates its data. Otherwise
the server creates a new entity.

- PATCH: allows the modification of an entity of a resource. So, 
it can be applied to change only particular portions of an entity 
data.

2. Provide links to 3 services or tools that allow you to “mock
an API for development like JSON-server.

- Moockoon 
- Killgrave 
- MockServer 


3. Compare and contrast Swagger and APIDoc.js 1 Which HTTP status
codes should be sent with each type of unsuccessful API call?

**APIDoc :** is a documentation generator designe for API built with Python and given by SFR Business Team. ApiDoc consists of a command line interface. It is maintained in a single repository.

**Swagger :** allows you to describe the structure of your APIs so that machines can read them. The ability of APIs to describe their own structure is the root of all awesomeness in Swagger. Why is it so great? Well, by reading your API’s structure, we can automatically build beautiful and interactive API documentation. We can also automatically generate client libraries for your API in many languages and explore other possibilities like automated testing. Swagger does this by asking your API to return a YAML or JSON that contains a detailed description of your entire API

4. Compare and contrast SOAP and ReST.

- **SOAP :** is a protocol which was designed before REST and 
came into the picture. The main idea behind designing SOAP was to 
ensure that programs built on different platforms and programming 
languages could exchange data in an easy manner. SOAP stands for 
Simple Object Access Protocol.

- **ReST :**  was designed specifically for working with
components such as media components, files, or even objects on a
particular hardware device. Any web service that is defined on 
the principles of REST can be called a RestFul web service. A 
Restful service would use the normal HTTP verbs of GET, POST, PUT 
and DELETE for working with the required components. REST stands 
for Representational State Transfer.

## **Difference Between SOAP and REST**

SOAP stands for Simple Object Access Protocol whereas REST stands 
for Representational State Transfer. SOAP is a protocol whereas 
REST is an architectural pattern. SOAP uses service interfaces to 
expose its functionality to client applications while REST uses 
Uniform Service locators to access the components on the hardware 
device. SOAP needs more bandwidth for its usage whereas REST 
doesn’t need much bandwidth. Comparing SOAP vs REST API, SOAP 
only works with XML formats whereas REST work with plain text, 
XML, HTML, and JSON.SOAP cannot make use of REST whereas REST can 
make use of SOAP.

Each technique has its own advantages and disadvantages. Hence, 
it’s always good to understand in which situations each design 
should be used. REST is an Architectural style in which a web 
service can only be treated as a RESTful service if it follows 
the constraints of being a client ServerStatelessCacheableLayered 
SystemUniform InterfaceSOAP cannot make use of REST since SOAP is 
a protocol and REST is an architectural pattern. In SOAP, the 
WSDL file provides the client with the necessary information 
which can be used to understand what services the web service can 
offer. As seen from SOAP messages, all data passed is in XML 
format.

## **Term** 

Term | Definition
------------ | ------------
Web Server | It is a system or content that provides Internet services to users, and a web server consists of a physical server, the server operating system known as OS, and a special program to facilitate communication known as HTTP. It is a computer system that aims primarily to connect to the Internet, and download all files and pages stored on the Internet on the user's computer upon request, and a single web server can support many websites, and a single website can be viewed through many linked web servers with each other, or those that have identical copies
Express | Express is a Node framework that simplifies HTTP verbs and allows for concise creation of HTTP verb handlers, simple integration with different view engines (i.e. porting information into front end templates), creates common settings such as port to use for connecting, and allows for additional request processing (middleware) to be inserted into request handling. It is unopinionated, meaning that you can structure it in various ways and use many different middleware options in myriad configurations.
Routing | Routing defines the way in which the client requests are handled by the application endpoints.
WRRC | The web is a cycle of requests and responses that flow between clients and servers



# An introduction to NodeJS and Express

Express/Node introduction Overview: Express Nodejs Next In this first Express article we answer the questions "What is Node?"

If you want to export a complete object in one assignment instead of building it one property at a time, assign it to module.exports as shown below (you can also do this to make the root of the exports object a constructor or other function): module .

all ( '/secret' , function ( req , res , next ) { console .

You can use the express.static middleware to serve static files, including your images, CSS and JavaScript ( static() is the only middleware function that is actually part of Express).

These can return any content required, but must be called after all other app.use() and routes calls so that they are the last middleware in the request handling process!

This approach has the benefit that as a developer you can continue to think in terms of JavaScript objects rather than database semantics, and that there is an obvious place to perform validation and checking of incoming data.

[click me to read more about NODEJS and EXPRESS](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/Introduction) 🤏

![image](https://javabeat.net/wp-content/uploads/2015/09/Express-2.jpg)

# What is NPM?

npm is the package manager for the Node JavaScript platform. It puts modules in place so that node can find them, and manages dependency conflicts intelligently.

It is extremely configurable to support a wide variety of use cases. Most commonly, it is used to publish, discover, install, and develop node programs.

[click me to read more about NPM](https://docs.npmjs.com/about-npm) 🤏

![image](https://upload.wikimedia.org/wikipedia/commons/thumb/d/db/Npm-logo.svg/1200px-Npm-logo.svg.png)

# TDD

is software development approach in which test cases are developed to specify and validate what the code will do. In simple terms, test cases for each functionality are created and tested first and if the test fails then the new code is written in order to pass the test and making code simple and bug-free.

[click me to read more about TDD](https://www.agilealliance.org/glossary/tdd/#q=~(infinite~false~filters~(postType~(~'page~'post~'aa_book~'aa_event_session~'aa_experience_report~'aa_glossary~'aa_research_paper~'aa_video)~tags~(~'tdd))~searchTerm~'~sort~false~sortDirection~'asc~page~1)) 🤏

![image](https://marsner.com/wp-content/uploads/test-driven-development-TDD.png)

# CI/CD 

Automation is a core principle for achieving DevOps success and CI/CD is a critical component. CI/CD comprises continuous integration and continuous delivery or continuous deployment. Put together, they form a “CI/CD pipeline”—a series of automated workflows that help DevOps teams cut down on manual tasks:

Continuous integration (CI) automatically builds, tests, and integrates code changes within a shared repository; then
Continuous delivery (CD) automatically delivers code changes to production-ready environments for approval.
Continuous deployment (CD) automatically deploys code changes to customers directly.



[click me to watch video for more about CI/CD](https://www.youtube.com/watch?v=xSv_m3KhUO8) 🤏