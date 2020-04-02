# What is Java?

* Java is first and foremost a **programming language**.
* Java is also a **platform**, because it provides a collection of programs, that help to develop, and run programs written in the Java programming language. 
  * *Platform*: Any hardware or software environment in which a program runs, is known as a platform. <br> 

## Types of Java Application

1) Standalone Application
'Desktop applications'. Traditional software that needs to be installed on each client system. Access to the application is limited to the systems that have the application installed. Standalone applications can be advantageous when there is no need for networking (application is needed only on a single system) or for hardware support such as barcode printers, webcams, biometric devices, LED panels, etc.

2) Web Application
A web application is an application that is stored on a remote server and delivered over the internet to a client.
* *Client:* Computer hardware or software that accesses a service made available by a server. <br>
* *Server:* Device that provides services to clients. <br>

Web applications are distributed applications that communicate with clients through a network or server. Web browsers are a common example of a client that access web applications that run on server side. Web applicaitions offer the ability to update and maintain an application without having to deploy and install software on every client.

A web server is a piece of software or hardware that recieves and processes client requests and sends an appropriate response back to the client. Web servers runs on some physical machine and listens to client requests on specific ports. A web client is a software that helps in communicating with the server. For example, a web browser requests services from the server (via URLs). The browser takes care of creating a request, sending it to server and then parsing the server response, before finally presenting it to the user.

3) Enterprise Application
An enterprise application is a large-scale application that is designed to satisfy the needs of an organization rather than an individual e.g. a banking application. The features that differentiate enterpise applications include, their high-level security, scalability, and reliability. These features increase the complexity of the application beyond that of a simple application. Enterpise applications need not only be sequestered for large corporations. The benefits of an enterprise application are helpful, even essential, for individual developers and small organizations in an increasingly networked world. 

4) Mobile Application
Software application designed to run on a mobile device such as a phone, tablet, or watch.

## Java Platforms / Editions

1) Java SE (Java Standard Edition) <br>
Java SE is a programming platform. It includes Java programming APIs (libraries) such as java.lang, java.io, java.net, java.util, java.sql, java.math etc. It includes core topics like OOPs, String, Regex, Exception, Inner classes, Multithreading, I/O Stream, Networking, AWT, Swing, Reflection, Collection, etc.

2) Java EE (Java Enterprise Edition) <br>
An enterprise platform which is mainly used to develop web and enterprise applications. It is built on top of the Java SE platform. It includes topics like Servlets, JSP, Web Services, EJB, JPA, etc.

3) Java ME (Java Micro Edition) <br>
It is a micro platform which is mainly used to develop mobile applications.

4) JavaFX <br>
It is used to develop rich internet applications. It uses a light-weight user interface API.

### Applets
A Java applet is a special kind of Java program that a Java enabled browser can download from the internet and run. An applet is typically embedded inside a web page and runs in the context of a browser. In the past, they were used to display data provided by the server, handle user input, or provide simple functions, such as a loan calculator. Applets execute locally, rather than on the server. In essence, the applet allowed some functionality to be moved from the server to the client. Applets have been replaced by newer mechanisms and are not supported in most modern browsers. 

### Servlets
A servlet is a small program that executes on the server. Servlets are used to create dynamically generated content that is then served to the client. For example, an online store might use a servlet to look up the price for an item in a database. The price information is then used to dynamically generate a web page that is sent to the browser. 

## Features of Java

1) **Simple**<br>
* Syntax based on C++.
* Removes complicated features e.g. explicit pointers, operator overloading.
* Automatic garbage collection of unreferenced objects.
2) **Object-Oriented**<br> 
* Helps manage complexity.
* Promotes code and object reuse. 
* Focus on higher level of programming, functionality over implementation.
* Simplifies design for larger projects.
3) **Portable** <br>
* Platform independent can be run on multiple different platforms and operating systems once compiled to bytecode. 
4) **Secure** <br>
* No explicit pointer.
* Java Programs run inside a virtual machine sandbox (JVM) so that they cannot access other parts of the computer. 
* Classloader: Classloader in Java is a part of the Java Runtime Environment(JRE) which is used to load Java classes into the Java Virtual Machine dynamically. It adds security by separating the package for the classes of the local file system from those that are imported from network sources.
* Bytecode Verifier: It checks the code fragments for illegal code that can violate access rights to objects.
* Security Manager: It determines what resources a class can access such as reading and writing to the local disk.
5) **Robust**
* It uses strong memory management. Strongly typed (code checked at compile time and run time). 
* Lack of pointers avoids security problems.
* Automatic garbage collection  runs on the Java Virtual Machine (JVM) to get rid of objects which are not being used by a Java application anymore.
* Exception handling and the type checking mechanism.
6) **Architecture neutral** <br>
* No implementation dependent features, e.g. the size of primitive types are fixed.
  - Compare with C : int data type occupies 2 bytes of memory for 32-bit architecture and 4 bytes of memory for 64-bit architecture.
  - In Java int occupies 4 bytes of memory for both 32 and 64-bit architectures.
7) **Performance** <br>
* Java is faster than other traditional interpreted programming languages because Java bytecode is "close" to native code.
* It is still a little bit slower than a compiled language (e.g., C++). 
* Java is an interpreted language that is why it is slower than compiled languages, e.g., C, C++, etc.
8) **Distributed** <br>
* Java handles TCP/IP protocols
* RMI and EJB are used for creating distributed applications. 
9) **Multithreading** <br>
* A thread is like a separate program, executing concurrently. 
* We can write Java programs that deal with many tasks at once by defining multiple threads. 
* The main advantage of multi-threading is that it doesn't occupy memory for each thread. It shares a common memory area. 
* Threads are important for multi-media, Web applications, etc.
10) **Dynamic** <br>
* Dynamic loading of classes: classes are loaded on demand. 
* Dynamic compilation and automatic memory management (garbage collection).

## Why Should we Program in Java?

1. Java is easy to learn. With a fluid English syntax and few 'magic characters' i.e angular brackets
2. Java is object-oriented so that programs are modular, flexible, and extensible.
3. Java has a rich API.
4. Support of powerful dev tools e.g. IntelliJ, Eclipse, netbeans.
5. Vast selection of open source libraries contributed to by organizations such as, Google and Apache. 
6. Enourmous community support.
7. Java is open source and free.
8. Great documentation (Javadocs).
9. Java is portable, you can develop on a Windows machine and then run on Linux (as long as it has a JVM). 
