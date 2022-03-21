# Message Queues

## Review, Research, and Discussion.

1. What does it mean that web sockets are bidirectional? 
Why is this useful?   
BIDIRECTIONAL. Whereas HTTP relies on a client request to 
receive a response from the server for every exchange, 
WebSockets allow for full-duplex bidirectional 
communication. This enables the server to send real-time 
updates asynchronously, without requiring the client to 
submit a request each time.


2. Does socket.io use HTTP? Why?  
WebSocket uses HTTP as the initial transport mechanism, but 
keeps the TCP connection alive after the HTTP response is 
received so that it can be used for sending messages 
between client and server. WebSockets allow us to build 
“real-time” applications without the use of long-polling.

3. What happens when a client emits an event? 
send a message to all the connected clients

 
---------
## Term
Term | Definition
------------ | ------------
Socket | It is a logical communication channel opened between two parties in order to exchange data between them. Opening that channel requires that the port be defined on each end so that the channel is requested to be opened on that gateway. Socket is a low-level and outdated concept, and it is based on either TCP, UDP, or a raw socket.
Socket.io | It is a JavaScript library for real-time web applications. Enables real-time bi-directional communication between web clients and servers. It has two sections: a client-side library running in the browser and a server-side library for Node.js. Both components have an almost identical API. Like Node.js, it's event driven.
Web Socket | It is a computer communications protocol that provides two-way communication channels over a single TCP connection. The WebSocket protocol was standardized by the IETF as RFC 6455 in 2011. The current specification is known as the HTML Living Standard.
Client | the low-level engine that establishes the connection to the server (by using transports like WebSocket or HTTP long-polling). The Manager handles the reconnection logic.
Server |  is a library that enables real-time, bidirectional and event-based communication between the browser and the server. 
OSI Model | The Open Systems Interconnection Model or Communication Reference Model is an abstract model that describes and defines standards for the functions of telecommunication or computer systems without regard to their internal structure and the technologies that compose them.
TCP Model | The Internet Protocol Suite, the Internet model, or the Department of Defense model is an abstract model that links the work of a set of communication protocols used on the Internet and in other computer networks. This model is known as the Internet model, abbreviated as the code, which combines the Internet Protocol and the Transfer Control Protocol.
TCP | Transmission Control Protocol, Transmission Control Protocol, or Transmission Control Protocol is a basic protocol in the Internet Protocol packet, described in a document, that provides reliable, error-free transmission of a stream of bytes between two hosts communicating with each other over an IP-enabled network.
UDP | User Data Protocol is one of the main members of the Internet Protocol family, a group of networking protocols that are used for the Internet.
Packets | A data packet or data packet is a unit of data intended for transmission in packet-switched networks.

--------------

## Socket.io Chat Example

Writing a chat application with popular web applications stacks like LAMP (PHP) has normally been very hard. It involves polling the server for changes, keeping track of timestamps, and it’s a lot slower than it should be.

Sockets have traditionally been the solution around which most real-time chat systems are architected, providing a bi-directional communication channel between a client and a server.

This means that the server can push messages to clients. Whenever you write a chat message, the idea is that the server will get it and push it to all other connected clients.

[click here to ream more about Socket.io Chat Example](https://socket.io/get-started/chat/)



