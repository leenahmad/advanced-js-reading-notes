# API Integration

What is a dynamic API?

The Dynamic API is a thin layer on top of the data object layer. It is designed to further ease the use of . NET with RDF data and to provide a model for persisting data in systems that make use of the .NET dynamic keyword

##  Support all REST/HTTP methods

- GET: Retrieve record(s) from a data source.
    - All.
    - One (by id).
    - Some (by filtering).
- POST: Create a new record in a data source.
- PUT: Update a single full record in a data source.
- PATCH: Update part of a single record in a data source.
- DELETE: Delete a record in a data source.


## Obey a standard output format
- Results will be returned in JSON format
- Results will be served with the correct HTTP header - application/json
- The GET Route, when not retrieving by ID, must return a full header, with count ,pages, and a results array
- All other routes must return a single object, representing the state of the entity following the operation


# Authentication Server / Module

An authentication module is a plug-in that collects user information such as a user ID and password, and compares the information against entries in a database.

Our business is expanding! We have a real need to manage a list of users of many types, and control their access to our data accordingly. The system to be built will have the following core features:

1- Users can create an account, associated with a “role”.

2- User Roles will be pre-defined and will each have a list of allowed capabilities.

    - admin can read, create, update, delete
    - editor can read, create, update
    - writer can read, create
    - user can read
3- Users can then login with a valid username and password

4- Alternatively, users can login using an OAuth provider such as Google or GitHub

    - In this case, users should be automatically assigned the role of user
5- Once logged in, Users can then access any route on the server, so long as they are permitted by the capabilities that match their role.

    - For example, a route that deletes records should only work if your user role is “admin”


[Review API Server Build](https://codefellows.github.io/code-401-javascript-guide/curriculum/apps-and-libraries/api-server/)

[Review Auth Server Build](https://codefellows.github.io/code-401-javascript-guide/curriculum/apps-and-libraries/auth-server/)

