# Introduction to Java: Your First Java App

We're going to create a Java app together and identify the moving parts of a Java application.

## Goals

* Understand what a compile language is.
* Define a class in Java and describe what a class is.
* Identify how to compile a Java application with arguments.
* Create a simple console application in Java.
* Run the simple console application in Java.

## Java Terminal Commands

* We can find Java's version using `java -version`
* We can run Java apps using `java`
* We can compile Java apps using `javac`

## Final Result

```java
public class HelloWorld {
  public static void main(String[] args) {
    // Console.log() for Java
    System.out.println("Hello, friends.");
    // loop through our arguments
    // we must declare an incrementor
    // as an integer (int)
    for (int i = 0; i < args.length; i++) {
      System.out.println(args[i]);
    }
    System.out.println("All arguments should have been listed by now.");
    System.out.println("Have a great day! :)");
  }
}
```
