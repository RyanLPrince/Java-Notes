# What is Java?

* Java is first and foremost a **programming language**.
* Java is also a **platform**, because it provides a collection of programs (JVM and Java API) that help to develop and run code that is written in the Java programming language. 
  * *Platform*: Any hardware or software environment in which a program runs, is known as a platform.

## Java Editions

1) Java Standard Edition (Java SE)
* Java SE is a programming platform that includes standard Java programming APIs (libraries) such as java.lang, java.io, java.net, java.util, java.sql, java.math etc and  core topics like OOPs, String, Regex, Exception, Inner classes, Multithreading, I/O Stream, Networking, AWT, Swing, Reflection, Collections, etc.
* 'Desktop applications'.
* Traditional software that needs to be installed on each client system. 
* Access to the application is limited to the systems that have the application installed. 
* Advantageous when there is no need for networking (application is needed only on a single system) or for hardware support such as barcode printers, webcams, biometric devices, LED panels, etc.
2) Java Enterprise Edition (Java EE)
* An enterprise platform which is mainly used to develop web and enterprise applications. It is built on top of the Java SE platform. It includes topics like Servlets, JSP, Web Services, EJB, JPA, etc.
* An enterprise application is a large-scale application that is designed to satisfy the needs of an organization rather than an individual e.g. a banking application. 
* The features that differentiate enterpise applications include high-level security, scalability, and reliability.
* Enterpise applications need not only be sequestered for large corporations, the benefits of an enterprise application are useful for individual developers and small organizations in an increasingly networked world. 
* A web application is an application that is stored on a remote server and delivered over the internet to a client. 
* Web applications are distributed applications that communicate with clients through a network or server. 
* Web browsers are a common example of a client that access web applications that run on server side. 
* Web applicaitions offer the ability to update and maintain an application without having to deploy and install software on every client.

> A web server is a piece of software or hardware that recieves and processes client requests and sends an appropriate response back to the client. Web servers runs on some physical machine and listens to client requests on specific ports. A web client is a software that helps in communicating with the server. For example, a web browser requests services from the server (via URLs). The browser takes care of creating a request, sending it to server and then parsing the server response, before finally presenting it to the user.
3) Java Micro Edition (Java ME)
* It is a platform which is mainly used to develop mobile applications.
4) JavaFX
* JavaFX is a set of graphics and media packages that enables developers to design, create, test, debug, and deploy rich client applications that operate consistently across diverse platforms.

## Why Should we Program in Java?

1) **Simple**<br>
* Java is easy to learn, with a fluid English syntax based on C++ and few 'magic characters' i.e angular brackets.
* Removes complicated features e.g. explicit pointers, operator overloading.
* Automatic garbage collection of unreferenced objects.
3) **Object-Oriented**<br> 
* Helps manage complexity.
* Promotes code and object reuse. 
* Focus on higher level of programming, functionality over implementation.
* Simplifies design for larger projects.
4) **Portable** <br>
* Platform independent can be run on multiple different platforms and operating systems once compiled to bytecode. 
5) **Secure** <br>
* No explicit pointer.
* Java programs run inside a virtual machine sandbox (JVM) so that they cannot access other parts of the computer. 
* Classloader: Classloader in Java is a part of the Java Runtime Environment(JRE) which is used to load Java classes into the Java Virtual Machine dynamically. It adds security by separating the package for the classes of the local file system from those that are imported from network sources.
* Bytecode Verifier: It checks the code fragments for illegal code that can violate access rights to objects.
* Security Manager: It determines what resources a class can access such as reading and writing to the local disk.
6) **Robust**
* It uses strong memory management. Strongly typed (code checked at compile time and run time). 
* Lack of pointers avoids security problems.
* Automatic garbage collection  runs on the Java Virtual Machine (JVM) to get rid of objects which are not being used by a Java application anymore.
* Exception handling and the type checking mechanism.
7) **Architecture Neutral** <br>
* No implementation dependent features, e.g. the size of primitive types are fixed.
  - Compare with C : int data type occupies 2 bytes of memory for 32-bit architecture and 4 bytes of memory for 64-bit architecture.
  - In Java int occupies 4 bytes of memory for both 32 and 64-bit architectures.
8) **Performance** <br>
* Java is faster than other traditional interpreted programming languages because Java bytecode is "close" to native code.
  * It is still a little bit slower than a compiled language (e.g., C++). 
9) **Distributed** <br>
* Java handles TCP/IP protocols.
* RMI and EJB are used for creating distributed applications. 
10) **Multithreading** <br>
* Utilize CPU effectively.
11) **Dynamic** <br>
* Dynamic loading of classes: classes are loaded on demand. 
* Dynamic compilation and automatic memory management (garbage collection).
12) **Rich API and Dev Support**
* Dev tools such as Eclipse, IntelliJ.
* Vast selection of open libraries.
* Community support.
* Documentation.
13) **Open Source**
 
