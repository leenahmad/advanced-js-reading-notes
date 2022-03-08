#  Access Control (ACL)

## Review, Research, and Discussion

When is Basic Authorization used vs. Bearer Authorization?

```
Basic Authorization : typically used in conjunction with HTTPS to provide confidentiality.to provide a username and password when making a request.

Bearer Authorization : for documentation purposes, as a hint to the clients.

```

What does the JSON Web Token package do?

```
share security information between two parties — a client and a server.

```
What considerations should we make when 
creating and storing a SECRET?

```
- Encrypt Data Using a KMS.
- Rotate Secrets Frequently.
- Store Secrets Responsibly.
- Detect Unauthorized Access.
```

-----------

# Term

Term | Definition
------------ | ------------
encryption | Encryption deals with the science of information that is in the form of simple text when stored on various storage media or when transmitted on plaintext networks, so that it becomes unreadable to anyone except for those who have special knowledge or a private key to reconvert the ciphertext into readable text. This decryption process is done by what is called the encryption key.
token |
bearer |  is an HTTP authentication scheme that involves security tokens called bearer tokens. 
secret |it is a key that contains all personal data
JSON Web Token(jwt) | Generates data with an optional signature and/or an optional encoding that carries its JSON payload that confirms a number of claims. Tokens are signed using either a private secret or a public/private key. For example, the server can generate a token containing the prompt to "Sign in as administrator" and present that to a client.


-----------

# RBAC

***RBAC definition***

RBAC is the idea of assigning system access to users based on their role within an organization. The system needs of a given workforce are analyzed, with users grouped into roles based on common job responsibilities and system access needs. Access is then assigned to each person based strictly on their role assignment. With tight adherence to access requirements established for each role, access management becomes much easier.


***RBAC implementation*** 

1. Inventory your systems.
2. Analyze your workforce and create roles.
3. Assign people to roles.
4. Never make one-off changes.
5. Audit.

![image](https://www.dnsstuff.com/wp-content/uploads/2019/10/role-based-access-control.jpg)

[you can read more from here](https://www.csoonline.com/article/3060780/5-steps-to-simple-role-based-access-control.html)


[watch this video](https://www.youtube.com/watch?v=C4NP8Eon3cA)

[this resource is helpful](https://en.wikipedia.org/wiki/Role-based_access_control)  👈 

------------


