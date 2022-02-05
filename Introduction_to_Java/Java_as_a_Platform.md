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

## Why is Exactly is Java Considered More Portable than C or C++?

> When we use portability in this context we are really asking "how easily one can I take a program and run it on a different platform". After a Java file and a C file are compiled we are left with bytecode and a C excecuteable file respectively. To run the bytecode on a different platform that specific platform must have a JVM implementation for the platform's architecture. To run the C excecuteable file at the very least recompilation will be necessary, with a compiller that matches the platform's architecture. Now we can see it necessary to consider the merits of implementing the JVM over porting a C program. 

> The Java language specification is stricter. Types like 'int' have a specific size in Java (eg: int is always 32-bits), while in C and C++ the size varies depending on platform and compiler. This apparent flexibility in C/C++ becomes a hurdle when porting to different architectures. In adition to the language specification, Java has a set of standard libraries that C++ does not e.g. for threading and networking, that are built into the JVM. Where C and C++ are concerned these libraries can vary between platforms. Porting the JRE to a new platform is something that is only necessary to do once. In fact, this task is generally done by the core maintainer/developers of the program and/or the platform. Once it is ported, every Java application should now theoretically (consider the JNI) run on the new machine. In that sense, the JRE forms an abstraction layer, completely hiding the machine, allowing easy porting. Where C/C++ is concerned porting the compiler as well as some core libraries of the language, source codes (and not binaries) can sometimes be enough to run a program on a new machine, but not always. 

### JIT (Just-in-Time Compilation)

HotSpot technology was introduced not long after Java’s initial release. HotSpot provides a Just-In-Time (JIT) compiler for bytecode. When a JIT compiler is part of the JVM, selected portions of bytecode are compiled into executable code in real time, on a demand basis. It is important to understand that an entire Java program is not compiled into executable code all at once. Instead, a JIT compiler compiles code as it is needed, during execution. Furthermore, not all sequences of bytecode are compiled—only those that will benefit from compilation. The remaining code is simply interpreted. However, the just-in-time approach still yields a significant performance boost. 

### AoT (Ahead of Time Compilation)

Some Java environments also include an ahead-of-time compiler that can be used to compile bytecode into native code prior to execution by the JVM, rather than on-the-fly. The goal of AoT is to improve start-up times of Java applications. JIT compilers are fast but for large Java programs it can take a while for the JIT to warm up completely. Infrequently-used Java methods might never be compiled at all, potentially incurring a performance penalty due to repeated interpreted invocations. Ahead of time compilation is a specialized feature, and it does not replace Java’s traditional approach just described. Furthermore, ahead-of-time compilation has several restrictions and is as of yet, not fully rolled out.

## JRE (Java Runtime Environment)

* Set of software components for running a Java application.
* JRE is made up of the JVM, Java libraries and the Java class loader.
* Provides runtime environment to exceute bytecode, and manage program resources during execution. 

![JRE](https://github.com/RyanLPrince/Java-Notes/blob/main/Introduction_to_Java/Resources/Images/JRE.png)

The JRE contains everything necessary to run an **already compiled Java program**, including the Java Virtual Machine (JVM) and other infrastructure. However, it cannot be used to create new programs. The JDK contains everything the JRE has, but also the compiler (javac) and other tools required for creating and compiling new programs.

## JVM (Java Virtual Machine)

* The JVM is an abstract machine. 
* The JVM is the specification for a software program that executes Java bytecode and provides the runtime environment for that code.
* The JVM has 3 parts:
  * **Specification**: List of detailed requirements for a JVM implementor. 
    * JVM specification provides definitions for the: memory area, class file format, register set, garbage-collected heap, fatal error reporting etc. 
  * **Implementation**: The implementation of the spec.
    * Implementations of JVM are known as Java Runtime Environments (JREs).
    * JREs for a given platform can excecute any compiled java program on the given platform.
    * JREs can also run programs written in other languages...provided they are first compiled to Java bytecode. 
  * **Instance/Runtime**: Whenever a Java program is excecuted, an instance of the JVM is created. 

### What does the JVM do?

1) Loads code.
2) Verifies code.
3) Exceutes code.
4) Provides runtime environment. 

![JVM](https://github.com/RyanLPrince/Java-Notes/blob/main/Introduction_to_Java/Resources/Images/JVM.png)
 
1) Classloader
* Loads class files (Java bytecode).
* Whenever a Java program is run, it is first loaded by the classloader.
* There are three built-in classloaders in Java. 
  * Bootstrap ClassLoader: 
    - Loads rt.jar file.
      - rt.jar contains all class files of the Java SE e.g. java.lang, java.util packages (compiled java runtime libraries).
    - Loads other core libraries located in $JAVA_HOME/jre/lib directory   
  * Extension Classloader: 
    - Child of Bootstrap.
    - Loads the jar files located inside $JAVA_HOME/jre/lib/ext directory.
      - so that these extensions of the core java libraries are available to all applications running on the platform.
  * System/Application ClassLoader: 
    - Child of extension classloader
    - Loads application level classes into the JVM. 
    - It loads files found in the classpath environment variable.
    - Loads new classes you have written. 
~~~
String.class.getClassLoader()   //null because String class is part of rt.jar and hence loaded by the native Bootstrap classloader
MyClass.class.getClassLoader()  // sun.misc.Launcher$AppClassLoader@4e0e2f2a 
~~~
2) Class Area
* Class Area stores class structures such as:
  - Runtime constants. 
  - Field and method data.
  - Code for methods.
  - Stores class.
3) Heap 
* Runtime data area.  
* Memory for all class instances are allocated.
* Stores instance of a class.
4) Stack
* JVM creates a separate stack each time a thread is created.
* Each method call performed by the thread and corresponding local variables will be stored in the stack.
* For every method call a separate 'frame' will be added to the stack.
* Frames store local variables, partial results, and plays a part in method invocation and return. 
* After completing the method call the corresponding frame will be removed from the stack.
* After all the method calls are complete the stack will become empty and the empty stack will be destroyed by the JVM.
5) Program Counter Register
* PC register contains the address of the Java virtual machine instruction currently being executed.
6) Native Method Stack 
* It contains all the native methods used in the application.
* A native method is a Java method whose implementation is written in another programming language such as C. 
  - Write faster code on a critical section with better CPU assembly instructions (not CPU portable).
  - Make direct system calls (not OS portable).
7) Execution Engine
* It contains:
  - A virtual processor.
  - Interpreter: Read bytecode stream then execute the instructions.
  - Just-In-Time(JIT) compiler.
8) Java Native Interface 
* Java Native Interface (JNI) is a framework which provides an interface to communicate with another application written in another language like C, C++, Assembly etc. 
* Java uses JNI framework to send output to the Console or interact with OS libraries.
