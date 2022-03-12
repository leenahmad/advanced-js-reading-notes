# Authorization/Authentication

## Review, Research, and Discussion


1. What header(s) are used in authentication and authorization?


```
The HTTP Authorization request header can be used to provide credentials that authenticate a user agent with a server, allowing access to a protected resource. The Authorization header is usually, but not always, sent after the user agent first attempts to request a protected resource without credentials

```
2. What is safe to put into a JWT?

```
It's an encoded, URL-safe string that can contain an unlimited amount of data (unlike a cookie) and is cryptographically signed. When a server receives a JWT, it can guarantee the data it contains can be trusted because it's signed by the source. No middleman can modify a JWT once it's sent.
```


3. How are JWTs validated?

```
When the client receives the ID token, the client validates the signature using a key as well

```
---------------------


# Term

Term | Definition
------------ | ------------
RBAC | Role-based access control or role-based security is a policy for restricting system access to authorized users. It is an approach to implement mandatory access control or discretionary access control.
User Roles | a  role is a database object that groups together one or more privileges and can be assigned to users. A user that is assigned a role receives all of the privileges of that role. A user can have multiple roles.
JWT Token | It is a proposed Internet standard for creating data with an optional signature and/or optional encoding that carries its JSON payload that corroborates a number of claims. Tokens are signed using either a private secret or a public/private key. For example, the server can generate a token containing the prompt to "Sign in as administrator" and present that to a client.
















