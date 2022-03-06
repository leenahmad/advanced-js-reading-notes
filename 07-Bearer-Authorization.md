# Bearer Authorization

## Review, Research, and Discussion

1- What can you do with an authorization code?

purchase, sell or transfer items, or to enter information into a security-protected space.

2- What can you do with an access token?

make API requests on behalf of a user.

3- What’s a benefit of using OAuth instead of your own basic authentication?

enables apps to obtain limited access (scopes) to a user's data without giving away a user's password

--------------------

## Term 


Term | Definition
------------ | ------------
Client ID | is an identifier associated with an application that assists with client / server OAuth 2.0 authentication for ArcGIS client APIs.
Client Secret | is a secret known only to your application and the authorization server.
Authentication Endpoint |  an authentication mechanism used to verify the identity of a network's external or remote connecting device. 
Access Token Endpoint | is where apps make a request to get an access token for a user.
API Endpoint | is one end of a communication channe
Authorization Code |  is an alphanumeric password that authorizes its user to purchase, sell or transfer items, or to enter information into a security-protected space
Access Token | is a string that the OAuth client uses to make requests to the resource server.

----------------------------

# Intro to JWT 


NEW: get the JWT Handbook for free and learn JWTs in depth!

Registered claims : These are a set of predefined claims which are not mandatory but recommended, to provide a set of useful, interoperable claims.

Do note that for signed tokens this information, though protected against tampering, is readable by anyone.

base64UrlEncode(payload), secret) The signature is used to verify the message wasn't changed along the way, and, in the case of tokens signed with a private key, it can also verify that the sender of the JWT is who it says it is.

Comparison of the length of an encoded JWT and an encoded SAML If you want to read more about JSON Web Tokens and even start using them to perform authentication in your own applications, browse to the JSON Web Token landing page at Auth0.

[you can read more from here](https://jwt.io/introduction/)

[watch the video](https://www.youtube.com/watch?v=926mknSW9Lo)

----------------

# Are JWTs Secure?

JWTs can be either signed, encrypted or both.

Mallory doesn't know that secret, but wants to interfere and change the JWT.

This means if she changes something, the signature won't match anymore, and Bob will simply not accept the JWT anymore.

Let's suppose, I send another person the message {"id":1} and sign it with Hash(content + secret). (
I use the SHA256 Hash function, and the signature I get is: 330e7b0775561c6e95797d4dd306a150046e239986f0a1373230fda0235bda8c.

[you can read more from here](https://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure)


--------------

# npm jsonwebtoken docs

jsonwebtoken Build Dependency An implementation of JSON Web Tokens.

It makes use of node-jws Install $ npm install jsonwebtoken Migration notes Usage (Asynchronous) If a callback is supplied, the callback is called with the err or the JWT.

complete : return an object with the decoded { payload, header, signature } instead of only the usual content of the payload.

ignoreExpiration : if true do not validate the expiration of the token.

It is expressed in seconds or a string describing a time span zeit/ms.

verify ( token , ' wrong-secret ' ) ; } catch ( err ) { } jwt .

[you can read more from here](https://www.npmjs.com/package/jsonwebtokene)
