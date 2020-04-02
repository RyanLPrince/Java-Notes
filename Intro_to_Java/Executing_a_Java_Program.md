# Executing a Java Program

## Compiling and Executing Java Programs

* The java file name should be the same as the class name (if public) with the `.java` extension. 
  * Java is case-sensitive 

###### HelloWorld.java
~~~
public class HelloWorld {
  public static void main (String [] args){
  }
}
~~~

~~~
$ javac HelloWorld.java           ⭠ This creates a HelloWorld.class file, the corresponding Java bytecode.
$ javac *.java                    ⭠ Compiles all the java files in the directory.

$ java HelloWorld                 ⭠ Excecutes HelloWorld.class files. This command is used on the class with the main method. 
~~~

* If your java class is not public the file name does not have to match the class name. 
e.g. we could save the following file as RandomName.java.

~~~
class GoodbyeWorld {
  public static void main (String [] args){
  }
}
~~~

~~~
$ javac RandomName.java           ⭠ This creates a GoodByeWorld.class file, the corresponding Java byte code.


$ java GoodbyeWorld               ⭠ Excecutes GoodbyeWorld.class files. This command is used on the class with the main method. 
~~~
