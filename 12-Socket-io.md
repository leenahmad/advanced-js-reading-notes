# Socket.io

## Review, Research, and Discussion

1- What is the benefit of transforming data into packets?

enable new innovations, services, and business opportunities.

2- UDP is often refereed to as a connectionless protocol. Why is this?

because it is analogous to sending a letter where you don't acknowledge receipt.

3- Can a socket server application have multiple socket connections?


Multiple connections on the same server can share the same server-side IP/Port pair as long as they are associated with different client-side IP/Port pairs,

4- Can a socket connection application be connected to multiple socket servers?

You cannot use a single socket to connect to multiple servers. You must create a separate socket for each connection. 

4- Can an application be both a socket server and a socket connection?

You can use the same socket for whatever you want, as long as your protocol handles it. 

---------------------

# Term


Term | Definition
------------ | ------------
Observer Pattern | a subscription model in which objects subscribe to an event and get notified when the event occurs. 
Listener | a procedure in JavaScript that waits for an event to occur.
Event Handler |  that invokes a specific piece of code when a particular action happens on an HTML element
Event Driven Programming | Everything starts by following an event. The event could be the DOM is loaded, or an asynchronous request that finishes fetching, or a user clicking an element or scrolling the page, or the user types on the keyboard.
Event Loop |  responsible for executing the code, collecting and processing events, and executing queued sub-tasks
Event Queue |  responsible for sending new functions to the stack for processing.
Call Stack | a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions
Emit | on() function that allows one or more functions to be attached to named events emitted by the object.
Raise |  throws a user-defined exception
Trigger | The trigger() method triggers the specified event and the default behavior of an event (like form submission) for the selected elements. 
Subscribe | observable of interest 
database | a javascript SQL database. It allows you to create a relational database and query it entirely in the browser.

---------------

# Web Sockets 

Computer network protocol WebSocket A diagram describing a connection using WebSocket International standard RFC 6455 Developed by IETF Industry Computer science Connector type TCP Website Official website WebSocket is a computer communications protocol, providing full-duplex communication channels over a single TCP connection.

To achieve compatibility, the WebSocket handshake uses the HTTP Upgrade header[1] to change from the HTTP protocol to the WebSocket protocol.

onclose = function ( event ) { onSocketClose ( event ); }; // Fired when a connection with a WebSocket has been closed because of an error, socket .

It is better to use tokens or similar protection mechanisms to authenticate the WebSocket connection when sensitive (private) data is being transferred over the WebSocket. A live example of vulnerability was seen in 2020 in the form of Cable Haunt.

While the WebSocket protocol itself is unaware of proxy servers and firewalls, it features an HTTP-compatible handshake, thus allowing HTTP servers to share their default HTTP and HTTPS ports (80 and 443 respectively) with a WebSocket gateway or server.

See also [ edit ] Notes [ edit ] a b requiring extra code to integrate with existing WebSocket-enabled code.

![image](https://ambassadorpatryk.com/wp-content/uploads/2020/02/web-socket.png)

[you can read more from here](https://en.wikipedia.org/wiki/WebSocket)

----------------------

# Socket.io Tutorial

IO enables real-time bidirectional event-based communication.

It works on every platform, browser or device, focusing equally on reliability and speed.

IO is built on top of the WebSockets API (Client side) and Node.js.

This tutorial has been created for anyone who has a basic knowledge of HTML, Javascript and Node.js work.

If the readers are not acquainted with these, we will suggest them to go through these tutorials first.


[you can read more from here](https://www.tutorialspoint.com/socket.io/)

--------------

# Socket.io vs Web Sockets 


Difference Between WebSocket and Socket.io WebSocket is the communication Protocol that provides bidirectional communication between the Client and the Server over a TCP connection; WebSocket remains open all the time, so they allow real-time data transfer.

IO is a library that enables real-time and full-duplex communication between the Client and the Web servers.
It also lives up to the standards and provides the accuracy and efficiency stream events to and from with negligible latency.

Head To Head Comparison Between WebSocket and Socket.io (Infographics) Below is the top 5 comparison of WebSocket vs Socket.io: Key Differences between WebSocket and socket.io Both WebSocket vs Socket.io are popular choices in the market; let us discuss some of the major 

Difference Between WebSocket vs Socket.io: It provides the Connection over TCP, while Socket.io is a library to abstract the WebSocket connections.

There is not much theoretically to learn about these topics.

Here we also discuss the WebSocket vs Socket.io key differences with infographics and comparison table.

[you can read more from here](https://www.educba.com/websocket-vs-socket-io/)

--------------------------------

### Socket.io Documentation 

Socket.IO is a library that enables low-latency, bidirectional and event-based communication between a client and a server.


![image](https://socket.io/images/bidirectional-communication2.png)

[Socket.io Documentation](https://socket.io/docs/v4/)

-----------------------------

### Server API


![image](https://socket.io/images/server-class-diagram-server.png)

[Socket.io Server API](https://socket.io/docs/v4/server-api)


--------------------

### Client API

[Socket.io Client API](https://socket.io/docs/v4/client-api)

--------------------------------

### tool to test socket


[Socket Testing Tool](https://amritb.github.io/socketio-client-tool/)