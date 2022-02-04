# Java as a Platform


* Java is a platform because it is a piece of software that excecutes a program. 
* Java has 3 main software components: Java Development Kit (JDK), Java Runtime Environment (JRE) and Java Virtual Machine (JVM), each with a specific configuation for a target operating system.

## JDK (Java Development Kit)

* Software development environment which is used to develop and run Java applications.
* Contains JRE & development tools needed to develop a program in Java.
* JDK contains a private JVM and other resources to complete the development of a java Application:
  - Compiler (javac).
    - Transforms Java source code into bytecode (that can then be run on any machine that implements the JVM).
  - Interpreter (java).
    - Executes compiled Java bytecode   
  - Archiver (jar).
    - JAR (Java ARchive) packaging (aggregating) Java class files and associated metadata  
  - Document generator (javadoc).

![JDK](https://github.com/RyanLPrince/Java-Notes/blob/main/Introduction_to_Java/Resources/Images/JDK.png)

### Bytecode

* A compiler transforms statements written in a high-level programming language (the source language) into another lower level programming langauge (usually low level excecuteable machine language).
* Unlike C, the output of a Java compiler is not excecutable code, rather, it is bytecode.
* Bytecode is a highly optimized set of instructions designed to be executed by the JVM.
* The JVM was essentially designed to be an interpreter for bytecode.
* An Interpreter directly executes instructions written in a progrmming language (without them being previously compiled into machine code).
* Many modern programs are compiled languages (implementors compile langage from source code to machine code), as compiled langages are typically faster, but becuase bytecode is highly optimized the differential is minimized.

<br>

**Executing code in C:** HelloWorld.c -> `compiler` -> HelloWorld.exe

<br>

**Executing code in Java:** HelloWorld.java -> `complier` -> HelloWorld.class (bytecode) -> `JVM interpreter`

<br><br>

### Portability

* The advantage of translating a Java source code into bytecode is that it much easier to run a program in a wide variety of environments.
  * Only the JVM needs to be implemented for each platform
* C is not considered to be very portable because, not only is it tied to a specific OS in many cases, it is also always tied to a specific hardware architecture once it has been compiled.
  * e.g. the int data type occupies 2 bytes of memory for 32-bit architecture and 4 bytes of memory for 64-bit architecture. 
* Bytecode will run on any machine that implements the JVM.

> To summarise Java source code is **compilled once** to bytecode and can then be excecuted on any platform with a JVM, C and C++ source code will generally have to be **recompilled for each platform**. Although the details of the JVM will differ from platform to platform, every JVM implementation understands the same Java bytecode. If Java programs were compiled to native code, then different versions of the same program would have to exist for each type of CPU connected to the Internet. This is, of course, not a feasible solution. Thus, the execution of bytecode by the JVM is how Java achieves its portablity. 

### JIT (Just-in-Time Compilation)

HotSpot technology was introduced not long after Java’s initial release. HotSpot provides a Just-In-Time (JIT) compiler for bytecode. When a JIT compiler is part of the JVM, selected portions of bytecode are compiled into executable code in real time, on a demand basis. It is important to understand that an entire Java program is not compiled into executable code all at once. Instead, a JIT compiler compiles code as it is needed, during execution. Furthermore, not all sequences of bytecode are compiled—only those that will benefit from compilation. The remaining code is simply interpreted. However, the just-in-time approach still yields a significant performance boost. 

## AoT ( Ahead of Time Compilation)

Some Java environments also include an ahead-of-time compiler that can be used to compile bytecode into native code prior to execution by the JVM, rather than on-the-fly. The goal of AoT is to improve start-up times of Java applications. JIT compilers are fast but for large Java programs it can take a while for the JIT to warm up completely. Infrequently-used Java methods might never be compiled at all, potentially incurring a performance penalty due to repeated interpreted invocations. Ahead of time compilation is a specialized feature, and it does not replace Java’s traditional approach just described. Furthermore, ahead-of-time compilation has several restrictions and is as of yet, not fully rolled out.



 
