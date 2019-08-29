# SECTION 200 

C Competency 1: Chat Client/Server 


## Purpose:

This assignment will introduce you to the concept of multithreading in C.  
By the end of this competency, you should have a basic understanding of linked
lists, and how to send information between multiple client and a single 
server. Trainees will be expected to explain these concepts to the Training 
Lead or a qualified signer.

Estimated Time to Complete:  2 weeks. 

Platform: Linux 


## Competency:

Create two separate programs, a client and a server.  The 
following guidelines are to be followed: 
1. Using a configurable IP and Port create a connection between the client and 
server.
2. Display a message upon each connection. 
3. All members should receive all messages, except the client who sent the 
message.
4. The server should log all messages between clients with some way of 
distinguishing each client.


## Requirements:

1. All requirements of Competency 2. 
2. Use a linked list to store clients. 
3. Properly manage disconnected clients by removing them from the linked list. 
4. Properly manage memory using mutexes when needed. 
5. Clean up threads for clients when they disconnect. 


## Functions / Concepts to be used:

1. Follow the same guidelines from the previous C competencies. 
2. You may create your own linked list, but you may also use the pre-existing
macros provided by ​sys/queue.h. 
3. New threads shall be created using ​pthread​, not fork. 
