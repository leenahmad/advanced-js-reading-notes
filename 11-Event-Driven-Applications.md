# Event-Driven-Applicationss

## Review, Research, and Discussion

1- Why is access control important?

limit access to information and information processing systems.

2- Describe an application that would need access control.

access control is a method of guaranteeing that users are who they say they are and that they have the appropriate access to
company data.

3- What is a role used for?

User Roles are permission sets that control access to areas and features within the Professional Archive Platform. Each User account requires a Role assignment.

4- Why is role based access control more scalable than discretionary or mandatory access control?

Role-based access control (RBAC), also known as role-based security, is a mechanism that restricts system access. It involves setting permissions and privileges to enable access to authorized users. Most large organizations use role-based access control to provide their employees with varying levels of access based on their roles and responsibilities. This protects sensitive data and ensures employees can only access information and perform actions they need to do their jobs.


# Term 

Term | Definition
------------ | ------------
Authorization | It is the function of determining the rights / privileges of access to resources, which is related to general information security and computer security, and access control in particular. More formally, "to authorize" is to define an access policy.
Role Based Access Control | Role-based access control or role-based security is a policy for restricting system access to authorized users. It is an approach to implement mandatory access control or discretionary access control.
Capabilities | It is the ability to carry out a specific course of action. The ability may or may not be accompanied by intent. The term is used in the defense industry but also in private industry.


-------------------------

# Event-Driven Programming in Node.js

Event-Driven Programming is a logical pattern that we can choose to confine our programming within to avoid issues of complexity and collision.

Overview For the most recognizable example of Event-Driven Programming for people at any level of programming skill, we’ll turn to our old friend The Web Browser.

When you click a button a click event is triggered.

const EventEmitter = require ( 'events' ) .

EventEmitter ; const chatRoomEvents = new EventEmitter ; function userJoined ( username ) { alertAllUsers ( 'User ' + username + ' has joined the chat.' ) ; }

emit ( 'userJoined' , username ) ; } We could expand further by creating events for when a user logs out, when a message is sent, when a message is received, or any other event we could possibly need for our chat room to be as dynamic as we want it.


![image](https://www.tutorialspoint.com/nodejs/images/event_loop.jpg)


[you can read more from here](https://nodejs.org/api/events.html)



