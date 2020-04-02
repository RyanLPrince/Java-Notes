# The History of Java

## The Birth of Modern Programming : C

The C programming language fundamentally changed the way programming was approached and thought about. C addressed the need for a **structured, efficient, high-level language**, that could replace assembly code when creating system programs. Early computer langauges were designed with certain trade-offs, such as:

* Ease-of-Use Vs Power   
* Safety Vs Efficiency
* Rigidity Vs Extensibility

Prior to C, programmers usually had to choose between languages that optimized one set of traits or the other.
For example:
  
  * **FORTRAN** could be used to write efficient programs for scientific applications but it was not very useful for system code. 
  * **BASIC** was easy to learn but the lacked power and structure necessary for large programs. 
  * **Assembly language** can be used to produce highly efficient programs but it is not easy to learn, use or debug effectively. 
  * **PASCAL** was somewhat structured but it lacked efficiency and was too rigid for system level code. 
  
Another compounding problem was that computer languages, such as BASIC, COBOL, and FORTRAN were not designed around structured principles. Instead, they relied upon *GOTO* as the primary means of program control. Essentailly, a GOTO statement would perform a one-way transfer of control to another line of code. A consquence of writing programs in these languages, was to produce 'spaghetti code'- a mass of tangled jumps and conditional branches that make a program virtually impossible to understand. In contrast, C divides a problem into smaller modules called functions or procedures each of which handles a particular responsibility. These functions return control after its responsibility has been fulfilled. 

C successfully reconciled the conflicting attributes that dogged early programming languages. Unlike the programming languages before it, that were created as an academic or bureaucratic excercise, C was was designed, implemented, and developed by real, working programmers, reflecting the way that they approached the job of programming. From its inception in the early 1970s through to the early 1980s, C became the dominant computer language and its creation is considered by many to have marked the beginning of the modern age of computer programming.

## The Next Step: C++

The 1960s gave birth to structured programming. This is the method of programming championed by C. The use of structured languages enabled programmers to write moderately complex programs fairly easily. However, even with structured programming, once a project reaches a certain size, its complexity exceeds what a programmer can realistically manage. By the early 1980s, many projects were pushing the traditional structured approach past its limits. To solve this problem, a new way of programming  was invented, called object-oriented programming (OOP). OOP is a programming paradigm which helps organize complex programs through the use of the principles of inheritance, abstraction, encapsulation, and polymorphism. C++ encorporates these features and enabled the complexity threshold of C to be surpassed. Programmers could, for the first time, comprehend and manage much larger and complex programs. 

C++ was invented by Bjarne Stroustrup in 1979. Stroustrup initially called the new language “C with Classes.” However, in 1983, the name was changed to C++. C++ extends C by adding object-oriented features. Because C++ is built on the foundation of C, it includes a lot of C’s features, attributes, and benefits. The invention of C++ was not an attempt to create a entirely new programming language. Instead, it was an enhancement to an already highly successful one. This was a crucial reason for the success of C++ as a language.

## Enter Java

The idea of Java was conceived in 1991. The impetus behind Java was the need for a platform-independent (architecture-neutral) langauge that could be used to create software embedded in various consumer electronic devices, such as microwave ovens or remote controls. Such electronic devices contain a variety of different CPUs. C and C++ fall under the category of compiled languages. This is problematic because compiled languages are designed to be compilled for a specific target platform. A compiler is a computer program that translates computer code written in one programming language (the source language) into another language (the target language). To compile a C++ program for a specific CPU would require a dedicated C++ compiler designed to produce an excecuteable program for that CPU. Portability describes how easily one can take a program and run it on a variety of different platforms. After a C or C++ program is compiled, the output is an excecuteable that is almost always platform specific. This means a program must be recompilled for every unique platform it is intended to run on. The portability of C and C++ suffers when the cost and time to create a full compiler is considered. 

The development of Java coincided with the emergence of the world wide web. The Internet is a universe populated with various types of computers, operating systems, and CPUs. Even though many kinds of platforms are attached to the Internet, users would like them all to be able to run the same program. By 1993, it became obvious to members of the Java design team that the problems of portability frequently encountered when creating code for embedded controllers are also found when attempting to create code for the Internet. In fact, the same problem that Java was initially designed to solve on a small scale could also be applied to the Internet on a large scale. This realization caused the focus of Java to switch from consumer electronics to Internet programming. While the desire for an architecture-neutral programming language provided the initial spark, the Internet ultimately led to Java’s large-scale success. 

Java achieves its portablity from the JVM (Java Virtual Machine). To excecute a Java program on a given platform, the platform need only implement the JVM. Any Java program that has been compiled can be excecuted by the JVM. In contrast, C excecutables will at the very least need to be recompilled before they can be run on a different platform. To understand exactly why implementing the JVM is preferable to porting C programs, it is necessary to delve into the low level details of the JVM. For now it is sufficient to understand that it is a lot easier to take a Java program written on one platform and run it on another than it is to do the same with a program written in C or C++.

Java derives many of its characteristics from C and C++. With its syntactical similarities to C, and its use of object-orientated features found in C++, it was able to attract a large audience.  Java was the perfect response to the demands of the then newly emerging, highly distributed computing universe.    
