# SECTION 100 Intermittent Debugging

## References:

You will be provided with the source code to a fully functioning 
implementation of a linked list. Your task will be to employ debugging 
techniques to answer the questions below. You will want to call the 
testList ​ function that has been implemented for you to answer the 
questions appropriately.

Use the source code listing in Appendix A to answer the following 
questions. 


### 100.1

Using the variables window, demonstrate the value of the client1, client2
and client3 variables.  Demonstrate the value of each member of those
structs.  Show the value of client1 in the memory browser window. 


### 100.2

Demonstrate how the data of myList is modified with the first call to 
​addMember ​ . Given your knowledge of linked list is this what you would 
expect? 


### 100.3

Demonstrate how the data of myList is modified with the second call to 
​addMember. Given your knowledge of linked list is this what you would 
expect?


### 100.4

What sequence of functions are called in the first call to ​removeMember?
Describe why each of those functions is called.


### 100.5

What sequence of functions are called in the second call to ​removeMember?
Describe why each of those functions is called. 


### 100.6

What sequence of functions are called in the third call to ​removeMember?
Describe why each of those functions is called.


### 100.7

Rerun in debug mode from the beginning. After the second call to ​addMember
change the value of myList->next to 0x111111111111. Continue stepping 
through the code. Where does the program crash and why? 
