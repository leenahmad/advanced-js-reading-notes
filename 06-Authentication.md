# Review, Research, and Discussion

1- Explain what a “Singleton” is (in Computer Science terms)?

A singleton is a class that allows only a single instance of itself to be created and gives access to that created instance. It contains static variables that can accommodate unique and private instances of itself.


2- Explain how the Singleton pattern can be used with Node modules, specifically with classes?

We need singleton when we want to make sure there is only one object instantiated. Therefore, instead of creating a new object we need to ensure the constructor was called only once and then we reuse the instance.
We can achieve this by refactoring our class to have:
hidden (private)constructor
public getInstance method that returns instance of the class



3- If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?


use method as a callback. If we want to a middleware function to be called only when a request of one request method is called, then we can pass it to the app.


------------------
# Term


Term | Definition
------------ | ------------
Router Middleware | It is a piece of code that comes in the middle of request and response . It kind of hijacks your request so that you can do anything that you want with your request or response eg: Modify the data or call the next middleware.
Dynamic Module Loading | Dynamic loading is a mechanism by which a computer program can, at run time, load a library (or other binary) into memory, retrieve the addresses of functions and variables contained in the library, execute those functions or access those variables, and unload the library from memory.
Singleton Pattern | The Singleton Pattern limits the number of instances of a particular object to just one. This single instance is called the singleton.
CRUD-> REST Method Matches | Create, Read, Update, and Delete — CRUD — are the four major functions for interacting with database applications. CRUD functions often play a role in web-based REST APIs, where they map (albeit poorly) to the HTTP methods GET, POST, DELETE, PUT, and PATCH.
Mock Testing | it is creating a fake version of an external or internal service that can stand in for the real one, helping your tests run more quickly and more reliably. When your implementation interacts with an object's properties, rather than its function or behavior, a mock can be used.


-------------------------

# Securing Passwords 

Passwords are the first line of defense against cyber criminals.

Many desktop applications and almost every web service including, blogs, forums eventually need to store a collection of user data and the passwords, that has to be stored using a hashing algorithm.

But why do we always hear about passwords being cracked?

There are some weaknesses in cryptographic hash algorithm that allows an attacker to calculate the original value of a hashed password, as explained below: PROBLEMS WITH CRYPTOGRAPHIC HASH ALGORITHM Brute Force attack: Hashes can't be reversed, so i nstead of reversing the hash of the password, an attacker can simply keep trying different inputs until he does not find the right now that generates the same hash value, called brute force attack.

BCrypt, IT's SLOW AND STRONG AS HELL To overcome such issues, we need algorithms which can make the brute force attacks slower and minimize the impact.

[read more from here](https://thehackernews.com/2014/04/securing-passwords-with-bcrypt-hashing.html)

-----------------------

# Basic Auth 

In the context of an HTTP transaction, basic access authentication is a method for an HTTP user agent (e.g. a web browser) to provide a user name and password when making a request.

In basic HTTP authentication, a request contains a header field in the form of Authorization: Basic , where credentials is the Base64 encoding of ID and password joined by a single colon : .

It was originally implemented by Ari Luotonen at CERN in 1993  and defined in the HTTP 1.0 specification in 1996. [
Features [ edit ] HTTP Basic authentication (BA) implementation is the simplest technique for enforcing access controls to web resources because it does not require cookies, session identifiers, or login pages; rather, HTTP Basic authentication uses standard fields in the HTTP header.

Client side [ edit ] When the user agent wants to send authentication credentials to the server, it may use the Authorization header field.
The resulting string is encoded into an octet sequence.

[read more from here](https://en.wikipedia.org/wiki/Basic_access_authentication)

--------------

# OWASP auth cheatsheet

Authentication Cheat Sheet¶ Authentication is the process of verifying that an individual, entity or website is whom it claims to be.

The Password Storage Cheat Sheet provides further guidance on how to handle passwords that are longer than the maximum length.

Compare Password Hashes Using Safe Functions¶ Where possible, the user-supplied password should be compared to the stored password hash using a secure password comparison function provided by the language or framework, such as the password_verify() function in PHP.

While this technique can prevent the user from having to type a password (thus protecting against an average keylogger from stealing it), it is still considered a good idea to consider using both a password and TLS client authentication combined.

Open Authorization (OAuth) is a protocol that allows an application to authenticate against a server as a user, without requiring passwords or any third party server that acts as an identity provider.

However, since OAuth1.0a does not rely on HTTPS for security, it can be more suited for higher-risk transactions.


[read more from here](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)

--------------------

# bcrypt docs 

You can read about bcrypt in Wikipedia as well as in the following article: How To Safely Store A Password If You Are Submitting Bugs or Issues Verify that the node version you are using is a stable version; it has an even major release number.

compare ( someOtherPlaintextPassword , hash , function ( err , result ) { // result == false } ) ; A Note on Timing Attacks with promises bcrypt uses whatever Promise implementation is available in global.

If cb is not specified, a Promise is returned if Promise support is available.

hashSync(data, salt) data - [REQUIRED] - the data to be encrypted.

We don't need to be careful that an attacker is going to learn anything, and our comparison function serves to provide a comparison of hashes, it is a utility to the overall purpose of the library.


[read more from here](https://www.npmjs.com/package/bcrypt)
