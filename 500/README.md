# SECTION 500 Assembly Competency 2: Number Equivalency 

## Purpose: 

This assignment will introduce you to number manipulation using assembly.  By 
the end of this competency, you should have a strong understanding of the 
assembly syntax, functions, control flow (i.e. loops and conditional jumps), 
segment types, memory manipulation and data storage. Trainees will be expected 
to explain these concepts to the Training Lead or a qualified signer. 

Estimated Time to Complete:  1 week. 

Platform: Linux 

## Competency: 

You are required to write a program that determines which input is greater.  
The order of logic is as follows: 
1. Ask for first input. 
2. Print first input to the screen. 
3. Ask for second input. 
4. Print second input to the screen.
5. Determine if the first input is less than or greater than the second. 
6. Print the result.
 
NOTE: Remember that strings and arrays must end with 0 (aka 0x00).  If you do
not end your strings and literals appropriately your program will fail.  

#To link and compile your program using NASM do the following:

1. In the command prompt type: 
2. “nasm –f elf –g filename.asm” 
3. This will result in filename.o. 
4. “ld –o filename filename.o” 
5. There should now be an executable named filename.
 
NOTE: During your development you will be making system calls repeatedly.  In 
assembler you can use the %define much like the #define in C.  By using define 
you can alleviate having to remember syscall amounts by making string 
literals. 
 
 