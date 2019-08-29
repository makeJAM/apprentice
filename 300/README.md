# SECTION 300 Python Competency 1: Secret Student Class 

## Purpose:

This assignment will introduce you to the concept of classes, reading/writing 
to files and string/type manipulation in Python.  By the end of this 
competency, you should have a basic ability to create your own classes and 
work with strings effectively. Trainees will be expected to explain these 
concepts to the Training Lead or a qualified signer. 

Estimated Time to Complete:  2 weeks. 

Platform: Linux 

## Competency:

Refer to Appendix B for a formatted file called student.txt. Design a class 
with a secondary constructor that creates an object from this file. Note that 
the class must be able to hold all the pertinent information in the file.  The 
primary constructor should instantiate the object by requiring all the class 
attributes (except maybe 2) as parameters. The class should also be able to 
produce a mean and standard deviation from the data in the file. It will be 
your job to decode (Base64) the file and determine the relevant data.

## Requirements:

1. The class shall have 2 constructors. see above for details. 
2. The class shall have a method to reproduce the file initially read in. ​Note:​ You may not store the original file in a buffer and use that buffer to write out to a file. 
3. The class shall have a method such that calling str(YourClassInstance) 
returns a string representing the instance of the class.

## Functions / Concepts to be used:

1. Classes and Objects.
2. File IO. 
3. String manipulation. 
4. Encoding.