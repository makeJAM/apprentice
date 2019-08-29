# SECTION 700 Capstone Project 

## Purpose​:

This capstone project will incorporate various concepts covered in the JQR. 
Software will be developed in Python, C and Assembly to create a command and 
control environment to perform the following tasks: 
 
Upon completion, the trainee will attain basic developer status and be 
prepared to contribute as a member of a development team.  
Estimated Time to Complete​: 3 weeks. 
Platform​: Linux 

## Competency​: 1

Write a server in C that has the following Command and Control
capabilities:

a. Server will listen for commands based on a protocol that you will define. 
b. The server will be capable of the following separate tasks:

1. Retrieve operating system information from the proc/cpuinfo file and return 
that information back to the client

2. Query for a list of running processes and return that information to the
client

3. Query for the contents of a directory that is specified by the client and 
return the contents to the client

4. Execute assembly shell code directly in memory.  The shell code should be 
capable of accepting an argument and the server should reply to the client 
whether or not the function succeeded based on its return value. (Hint: look 
up the mprotect function).

## Competency: 2

Develop a client, in Python, that will connect to the server. It shall have a
user interface to allow the user to send commands and receive the results.

a. There shall be a menu for the user to choose from one of the four tasks the
server is capable of performing.

b. In the case where sending assembly code is chosen, the client should send
the function argument and the bytes of the shell code to the server.

c. Write assembly code that will accept a process id as an argument and kill
that process.  It should return the return value of the system call for
killing the process.

There must be an assembly source file, although the code will be sent over as
the compiled machine code bytes.

## Requirements​:

1. Create and document a fundamental design plan for all three pieces.

2. Write a User’s Guide so that someone without coding knowledge will be able
to use your client.

3. The server will reside on disk on the target machine and will be executed
via normal command line execution.

## Software:

Wireshark or comparable packet sniffer GNU Debugger or comparable
NASM or equivalent compiler Python 2.7 or 3.4 C compiler for *nux development
platform  

This project is to be completed by the trainee and at no time will sharing of
source code with other trainees be allowed. Guidance from development trainers
is encouraged and is allowed.  
