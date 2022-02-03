# A Brief History of Java

## The Birth of Modern Programing: C

* The C programming language was born out of the need for a structured, efficient, high-level language, that could replace assembly code when creating system programs.
* Prior to C, programmers had to chose between programs that optimized a certain set of traits or another e.g.
  
  **Assembly Code** - Efficient but difficult to learn. <br><br>
  **FORTRAN** - Efficient for scientific applications but not extensible for use in system programs. <br><br>
  **BASIC** - Easy to learn but not very powerful (very basic indeed). <br><br>
  **PASCAL** - Structured but rigid. <br><br>
  
 > Another compounding problem was that computer languages, such as BASIC, COBOL, and FORTRAN were not designed around structured principles. Instead, they relied upon GOTO as the primary means of program control, whereby a GOTO statement would perform a one-way transfer of control to another line of code. A consquence of writing programs in these languages, was to produce 'spaghetti code'- a mass of tangled jumps and conditional branches that make a program virtually impossible to follow. In contrast, C divides a problem into smaller modules called functions or procedures, each of which handles a particular responsibility. These functions return control after its responsibility has been fulfilled.

* C reconcilled conflicting attributes that dogged early programming languages.
* Unlike the programming languages that came before it, that were created as an academic or bureaucratic excercise, C was designed, implemented, and developed by real, working programmers, reflecting the way that they approached the job of programming.
* From its inception in the early 1970s through to the 1980s, C became the dominant computer language and its creation is considered by many to have marked the beginning of the modern age of computer programming.

## The Next Step: C++

* By the early 1980s, many projects were pushing the structured approach championed by C to the limits of complexity that could be managed.
* As a procedure-oriented programming language, C is characterized by programs that are conceptually organized around its code - what is happening, as a series of linear steps. 
* A new programming paradigm was invented called object-oriented programming (OOP), to push the boundaries of complexity.
* OOP is a programming paradigm which helps organize complex programs through the use of the principles of inheritance, abstraction, encapsulation, and polymorphism, programs are organized around its data - who is being affected, as a set of well-defined interfaces.
* C++ (originally originally called 'C with classes' which alludes to some of the features encorporated) was built on the foundations of C, including many of the features and benefits - a key reason for its success - while also extending C with OOP aspects.
 
## A Problem of Portability: Java

* C and C++ are what are known as compiled languages, this means they are designed to be compilled for a specific target platform. 
* A compiler is a computer program that translates computer code written in one programming language (the source language) into another lower level (machine-oriented) language (the target language).
* To compile a C++ program for a specific CPU would require a dedicated C++ compiler designed to produce an excecuteable program for that CPU.
* Portability describes how easily one can take a program and run it on a variety of different platforms.
* After a C or C++ program is compiled, the output is an excecuteable that is almost always platform specific.
* This means a program must be recompilled for every unique platform it is intended to run on.
  * C and C++ are not considered to be very portable when the cost and time to create a full compiler is considered.   

<br>

  HelloWorld.c -> (compiler) -> HelloWorld.exe

<br>

* The impetus behind Java was the need for a platform-independent langauge that could be used to create software embedded in various consumer electronic devices, such as microwave ovens or remote controls with various CPUs.
* The conception of the idea of Java in 1991 conincided with the development of the world wide web.
* The internet linked different computers, operating systems, and CPUs which all would be desired to run the same programs.
  * By 1993 it became obvious that the same problem of portability in embedded controllers was also found when attempting to create software for the internet.
  * The internet ultimately led to Java's success.

<br>

HelloWorld.java -> (complier) -> HelloWorld.class -> (JVM interpreter) 

<br>

* Java achieves its portablity from the JVM (Java Virtual Machine).
* To excecute a Java program on a given platform, the platform need only implement the JVM.
* Any Java program that has been compiled can be excecuted by the JVM.
  * There is no need to recompile Java code for a specific target, compiled Java code will run on any platform that implements the JVM. 

<br>

* Java derives many of its characteristics from C and C++. With its syntactical similarities to C, and its use of object-orientated features found in C++, it was able to attract a large audience. 
* Java was the perfect response to the demands of the then newly emerging, highly distributed computing universe.


