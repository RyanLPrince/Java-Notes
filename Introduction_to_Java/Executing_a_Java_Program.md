# Executing a Java Program

## Compiling and Executing Java Programs

* The java file name should be the same as the class name (if public) with the `.java` extension. 
  * Java is case-sensitive 
 
 ###### HelloWorld.java
~~~
public class HelloWorld{
  public static void main(String [] args){
    System.out.println("Hello World!");
  }
}
~~~

~~~
$ javac HelloWorld.java           ⭠ The javac command compiles the HelloWorld.java source file
$ dir
HelloWorld.java HelloWorld.class  ⭠ After compilattion a HelloWorld.class file is produced - the corresponding Java bytecode.

$ javac *.java                    ⭠ Compiles all the java files in the directory.

$ java HelloWorld                 ⭠ Excecutes HelloWorld.class file. This command is used on the class with the main method. Note that the argument does not have the .class extension.
Hello World!                      ⭠ Output of the program is displayed on the comman line.
~~~

* If your java class is not public, the file name does not have to match the class name. 
e.g. we could save the following file as RandomName.java

* If your java class is not public the file name does not have to match the class name. 
e.g. we could save the following file as RandomName.java

~~~
class GoodbyeWorld{
  public static void main(String [] args){
    System.out.println("Goodbye World!");
  }
}
~~~

~~~
$ javac RandomName.java            ⭠ This creates a GoodByeWorld.class file, the corresponding Java byte code.
$ dir
RandomName.java GoodbyeWorld.class 

$ java GoodbyeWorld                ⭠ Excecutes GoodbyeWorld.class files
~~~

* If we do not remove the public access modifier then we get the following error:
~~~
$ javac RandomClassName.java
RandomClassName.java:1: error: class GoodbyeWorld is public, should be declared in a file named GoodbyeWorld.java
public class GoodbyeWorld{
       ^
1 error
~~~ 
