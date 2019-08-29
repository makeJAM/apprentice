# SECTION 400 Assembly Competency 1: abc -> ABC 
 
## Purpose:

This assignment will introduce you to string manipulation using assembly.  By 
the end of this competency, you should have a basic understanding of the 
assembly syntax, functions, control flow (i.e. loops and conditional jumps), 
segment types, and memory and string manipulation. Trainees will be expected 
to explain these concepts to the Training Lead or a qualified signer. 

Estimated Time to Complete:  1 week. 

Platform: Linux 

## Competency: 

You are required to write a program that takes a string and 
capitalizes all the letters.  The string can be static within the program or 
taken as an argument. 

NOTE: Remember that strings and arrays must end with 0 (aka 0x00).  If you do 
not end your strings and literals appropriately your program will fail.  

## To link and compile your program using NASM do the following: 

1. In the command prompt type: “nasm –f elf –g filename.asm” 
2. This will result in filename.o. 
3. “ld –o filename filename.o” 
4. There should now be an executable named filename. 

NOTE: During your development there is a mathematical hint relating to the 
number 32 and the ASCII table.  Figure this out and it will help you during 
your string conversion process. 
 