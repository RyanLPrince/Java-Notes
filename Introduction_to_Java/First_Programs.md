# First Programs
Programing in Java involves:
1) Defining a class: Fields and Methods.
2) Using a class template to create one or more instances of that class (Object).

## Creating a Class
~~~
public class HelloWorld{
  public static void main (String [] args){
    System.out.println("Hello World");
  }
}
~~~

### Key words explained:
* **public**- Access modifier, public indicates this class is visible to all other classes and that the main method can be invoked outside of the class.   
* **class**- Indicates that we are defining a class (HelloWorld is the name of the class). 
* **main** - `main` is the name of the method. The main method indicates start point for the flow of execution.
* **void** - void is the return type. A void return type indicates that nothing is returned by this method.
* **static** - Static methods belong to the class rather than any instance (object) of the class.
  * Static methods can be invoked without creating an instance of the class (*Classname.methodName*). e.g. Math.sqrt()
  * This is necessary since `main( )` is called by the JVM before any objects are made.
  * Static methods can access static data and change its value directly. 
* **String [] args** - An array of strings called args, that holds command line arguments.
* **System.out.println()** - Calls the method println for the class System. println prints the argument provided to it in the console.

~~~
public class PrintArguments{
  public static void main (String [] args){
    System.out.println(args [0])
  }
}
~~~
~~~
$ java PrintArguments Hello World
Hello
~~~

## Creating a field 

* A field stores values for an object.
* Known as instance variables.
* Define the state of an object.
* Have an associated type.

~~~
public class Ticket{
  public int price;
  private String destination = "London";
}
~~~

* Java is strongly typed, this means every variable must be declared with a type. 
* `int` is the type given to the field named `price`.
* `String` is the type given to the field named `destination`. We have also given a value to this field (`London`).
* `private` & `public` are access modifiers and define how we can access these fields.

## Creating a Method

* A method is a collection of statements that are grouped together to perform an operation.
* Method signature: 
  - Combination of method name and parameters which can uniquely identify a method. 
  - Short description of what a  method does.
  - e.g. public void changePrice(int newPrice){}
 
* Parameter: A variable that is passed to a method. 
  - public Ticket (int cost) {} // Formal parameter
  - Ticket tm =  new Ticket (10); // Actual parameter (argument) 
* Methods have a return type that tell us what type of data is returned.
  - public int increment() {} // int is the return type 

### Types of Methods

#### Constructors

* Create and initate an objects. 
* Assign necessary memory to the creates object.
* Same name as class.
* Typically store inital values into fields.
  - Often from external arguments.
* **No return type.**
~~~
public Ticket (int cost){
  price = cost;
}
~~~


#### Accessor Methods
* *getter* 
* provide information about an object's state.
~~~
public int getPrice(){
  return price;
}
~~~

#### Mutator Methods
* *setters*
* change (mutate) an object's state.
~~~
public void changePrice (int newPrice){
  price = newPrice;
}
~~~

## Class Conventions

* Class names are written in PascalCase e.g public class TicketMachine{}
* Method names are written in camelCase e.g public void printTicket(){}
* Field names are written in camelCase e.g. public int ticketPrice;
* Constants are written in ALL_CAPS with an underscore separating words e.g. 
public static final String TICKET_ERROR_101="Train has already departed";
* Constructors are (almost) always public.
* No direct access to fields (mark fields as private and access via accessors and mutators);
* User does not need to know how a class is implemented to use/insantiate it.
* Use of class is defined by its collection of methods.

## Comments
~~~
// This is an inline comment 
/*
* This is a
* block comment 
*/
~~~
* Java ignores comments.

~~~
public class Ticket{
  
  //field
  private int ticketPrice; 
  
  //Constructor method, has same name as class (note captilalization), no return type (not even void)!  
  public Ticket (int price){ 
    ticketPrice=price;
  }
  
  //Mutator method
  public void changePrice(int newPrice){
    ticketPrice=newPrice;
  }
  
  //Accessor method
  public int getPrice(){
    return ticketPrice;
  }    
}
~~~
