# Java Basics

> *Click &#9733; if you like the project. Your contributions are heartily ♡ welcome.*

<br/>

## Related Topics

* *[Multithreading](multithreading-questions.md)*
* *[Collections](collections-questions.md)*
* *[Java Database Connectivity (JDBC)](JDBC-questions.md)*
* *[Java Programs](java-programs.md)*
* *[Java String Methods](java-string-methods.md)*
* *[Jakarta Server Pages (JSP)](jsp-questions.md)*
* *[Servlets](servlets-questions.md)*
* *[Java Multiple Choice Questions](java-multiple-choice-questions-answers.md)*
* *[Java Design Pattern](https://github.com/learning-zone/java-design-patterns)*
* *[Hibernate](https://github.com/learning-zone/hibernate-basics)*
* *[Spring Framework Basics](https://github.com/learning-zone/spring-basics)*

<br/>

## Table of Contents

* [Introduction](#-1-introduction)
* [Java Architecture](#-2-java-architecture)
* [Java Data Types](#-3-java-data-types)
* [Java Methods](#-4-java-methods)
* [Java Functional programming](#-5-java-functional-programming)
* [Java Lambda expressions](#-6-java-lambda-expressions)
* [Java Classes](#-7-java-classes)
* [Java Constructors](#-8-java-constructors)
* [Java Array](#-9-java-array)
* [Java Strings](#-10-java-strings)
* [Java Reflection](#-11-java-reflection)
* [Java Streams](#-12-java-streams)
* [Java Regular Expressions](#-13-java-regular-expressions)
* [Java File Handling](#-14-java-file-handling)
* [Java Exceptions](#-15-java-exceptions)
* [Java Inheritance](#-16-java-inheritance)
* [Java Method Overriding](#-17-java-method-overriding)
* [Java Polymorphism](#-18-java-polymorphism)
* [Java Abstraction](#-19-java-abstraction)
* [Java Interfaces](#-20-java-interfaces)
* [Java Encapsulation](#-21-java-encapsulation)
* [Java Generics](#-22-java-generics)
* [Miscellaneous](#-23-miscellaneous)

<br/>

## # 1. INTRODUCTION

<br/>

## Q. What are the important features of Java 8 release?

* Interface methods by default;
* Lambda expressions;
* Functional interfaces;
* References to methods and constructors;
* Repeatable annotations
* Annotations on data types;
* Reflection for method parameters;
* Stream API for working with collections;
* Parallel sorting of arrays;
* New API for working with dates and times;
* New JavaScript Nashorn Engine ;
* Added several new classes for thread safe operation;
* Added a new API for `Calendar`and `Locale`;
* Added support for Unicode 6.2.0 ;
* Added a standard class for working with Base64 ;
* Added support for unsigned arithmetic;
* Improved constructor `java.lang.String(byte[], *)` and method performance `java.lang.String.getBytes()`;
* A new implementation `AccessController.doPrivileged` that allows you to set a subset of privileges without having to check all * other access levels;
* Password-based algorithms have become more robust;
* Added support for SSL / TLS Server Name Indication (NSI) in JSSE Server ;
* Improved keystore (KeyStore);
* Added SHA-224 algorithm;
* Removed JDBC Bridge - ODBC;
* PermGen is removed , the method for storing meta-data of classes is changed;
* Ability to create profiles for the Java SE platform, which include not the entire platform, but some part of it;
* Tools
    * Added utility `jjs` for using JavaScript Nashorn;
    * The command `java` can run JavaFX applications;
    * Added utility `jdeps` for analyzing .class files.

<div align="right">
    <b><a href="#related-topics">↥ back to top</a></b>
</div>

## Q. What is Nashorn?

**Nashorn** is a JavaScript engine developed in Java by Oracle. Designed to provide the ability to embed JavaScript code in Java applications. Compared to Rhino , which is supported by the Mozilla Foundation, Nashorn provides 2 to 10 times better performance, as it compiles code and transfers bytecode to the Java virtual machine directly in memory. Nashorn can compile JavaScript code and generate Java classes that are loaded with a special loader. It is also possible to call Java code directly from JavaScript.

<div align="right">
    <b><a href="#related-topics">↥ back to top</a></b>
</div>

## Q. What is jjs?

`jjs` - This is a command line utility that allows you to execute JavaScript programs directly in the console.

<div align="right">
    <b><a href="#related-topics">↥ back to top</a></b>
</div>

## Q. In Java, How many ways you can take input from the console?

In Java, there are three different ways for reading input from the user in the command line environment ( console ).

**1. Using Buffered Reader Class:**

This method is used by wrapping the System.in ( standard input stream ) in an InputStreamReader which is wrapped in a BufferedReader, we can read input from the user in the command line.

```java
/**
 * Buffered Reader Class
 */
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class Test {
    public static void main(String[] args) throws IOException {
        // Enter data using BufferReader
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));

        // Reading data using readLine
        String name = reader.readLine();

        // Printing the read line
        System.out.println(name);
    }
}
```

**2. Using Scanner Class:**

The main purpose of the Scanner class is to parse primitive types and strings using regular expressions, however it is also can be used to read input from the user in the command line.

```java
/**
 * Scanner Class
 */
import java.util.Scanner;

class GetInputFromUser {
    public static void main(String args[]) {
        // Using Scanner for Getting Input from User
        Scanner in = new Scanner(System.in);

        String s = in.nextLine();
        System.out.println("You entered string " + s);

        int a = in.nextInt();
        System.out.println("You entered integer " + a);

        float b = in.nextFloat();
        System.out.println("You entered float " + b);
    }
}
```  

**3. Using Console Class:**

It has been becoming a preferred way for reading user\'s input from the command line. In addition, it can be used for reading password-like input without echoing the characters entered by the user; the format string syntax can also be used ( like System.out.printf() ).

```java
/**
 * Console Class
 */
public class Sample {
    public static void main(String[] args) {
        // Using Console to input data from user
        String name = System.console().readLine();
        System.out.println(name);
    }
}
```

<div align="right">
    <b><a href="#related-topics">↥ back to top</a></b>
</div>

## Q. What is the purpose of using javap?

The **javap** command displays information about the fields, constructors and methods present in a class file. The javap command ( also known as the Java Disassembler ) disassembles one or more class files.

 ```java
 /**
  * Java Disassembler
  */
class Simple {
    public static void main(String args[]) {
        System.out.println("Hello World");
    }
}
```

```cmd
cmd> javap Simple.class  
```

Output

```java
Compiled from ".java"  
class Simple {  
  Simple();  
  public static void main(java.lang.String[]);  
}  
```

<div align="right">
    <b><a href="#related-topics">↥ back to top</a></b>
</div>

## Q. Explain the expression `System.out::println`?

The specified expression illustrates passing a reference to a static method of a `println()`class `System.out`.

<div align="right">
    <b><a href="#related-topics">↥ back to top</a></b>
</div>

## Q. Tell us about parallel processing in Java 8?

Streams can be sequential and parallel. Operations on sequential streams are performed in one processor thread, on parallel streams - using several processor threads. Parallel streams use the shared stream `ForkJoinPool`through the static `ForkJoinPool.commonPool()`method. In this case, if the environment is not multi-core, then the stream will be executed as sequential. In fact, the use of parallel streams is reduced to the fact that the data in the streams will be divided into parts, each part is processed on a separate processor core, and in the end these parts are connected, and final operations are performed on them.

You can also use the `parallelStream()`interface method to create a parallel stream from the collection `Collection`.

To make a regular sequential stream parallel, you must call the `Stream`method on the object `parallel()`. The method `isParallel()`allows you to find out if the stream is parallel.

Using, methods `parallel()`and `sequential()`it is possible to determine which operations can be parallel, and which only sequential. You can also make a parallel stream from any sequential stream and vice versa:

```java
collection
  .stream ()
  .peek ( ... ) // operation is sequential
  .parallel ()
  .map ( ... ) // the operation can be performed in parallel,
  .sequential ()
  .reduce ( ... ) // operation is sequential again
```

As a rule, elements are transferred to the stream in the same order in which they are defined in the data source. When working with parallel streams, the system preserves the sequence of elements. An exception is a method `forEach()`that can output elements in random order. And in order to maintain the order, it is necessary to apply the method `forEachOrdered()`.

* Criteria that may affect performance in parallel streams:
* Data size - the more data, the more difficult it is to separate the data first, and then combine them.
* The number of processor cores. Theoretically, the more cores in a computer, the faster the program will work. If the machine has one core, it makes no sense to use parallel threads.
* The simpler the data structure the stream works with, the faster operations will occur. For example, data from is `ArrayList`easy to use, since the structure of this collection assumes a sequence of unrelated data. But a type collection  `LinkedList`is not the best option, since in a sequential list all the elements are connected with previous / next. And such  data is difficult to parallelize.
* Operations with primitive types will be faster than with class objects.
* It is highly recommended that you do not use parallel streams for any long operations (for example, network connections),  since all parallel streams work with one `ForkJoinPool`, such long operations can stop all parallel streams in the JVM due to  the lack of available threads in the pool, etc. e. parallel streams should be used only for short operations where the count  goes for milliseconds, but not for those where the count can go for seconds and minutes;
* Saving order in parallel streams increases execution costs, and if order is not important, it is possible to disable its  saving and thereby increase productivity by using an intermediate operation `unordered()`:

```java
collection.parallelStream ()
    .sorted ()
    .unordered ()
    .collect ( Collectors . toList ());
```

<div align="right">
    <b><a href="#related-topics">↥ back to top</a></b>
</div>

## # 2. JAVA ARCHITECTURE

<br/>

## Q. What is JVM and is it platform independent?

Java Virtual Machine (JVM) is a specification that provides runtime environment in which java bytecode(.class files) can be executed. The JVM is the platform. The JVM acts as a "virtual" machine or processor. Java\'s platform independence consists mostly of its Java Virtual Machine (JVM). JVM makes this possible because it is aware of the specific instruction lengths and other particularities of the platform (Operating System).

The JVM is not platform independent. Java Virtual Machine (JVM) provides the environment to execute the java file(. Class file). So at the end it's depends on kernel and kernel is differ from OS (Operating System) to OS. The JVM is used to both translate the bytecode into the machine language for a particular computer and actually execute the corresponding machine-language instructions as well.

<div align="right">
    <b><a href="#related-topics">↥ back to top</a></b>
</div>

## Q. What is JIT compiler in Java?

The Just-In-Time (JIT) compiler is a component of the runtime environment that improves the performance of Java applications by compiling bytecodes to native machine code at run time.

Java programs consists of classes, which contain platform-neutral bytecodes that can be interpreted by a JVM on many different computer architectures. At run time, the JVM loads the class files, determines the semantics of each individual bytecode, and performs the appropriate computation. The additional processor and memory usage during interpretation means that a Java application performs more slowly than a native application. The JIT compiler helps improve the performance of Java programs by compiling bytecodes into native machine code at run time. The JIT compiler is enabled by default. When a method has been compiled, the JVM calls the compiled code of that method directly instead of interpreting it.

<div align="right">
    <b><a href="#related-topics">↥ back to top</a></b>
</div>

## Q. What is Classloader in Java?

The **Java ClassLoader** is a part of the Java Runtime Environment that dynamically loads Java classes into the Java Virtual Machine. Java code is compiled into class file by javac compiler and JVM executes Java program, by executing byte codes written in class file. ClassLoader is responsible for loading class files from file system, network or any other source.

**Types of ClassLoader:**

**1. Bootstrap Class Loader**:

It loads standard JDK class files from rt.jar and other core classes. It loads class files from jre/lib/rt.jar. For example, java.lang package class.

**2. Extensions Class Loader**:

It loads classes from the JDK extensions directly usually `JAVA_HOME/lib/ext` directory or any other directory as java.ext.dirs.

**3. System Class Loader**:

It loads application specific classes from the CLASSPATH environment variable. It can be set while invoking program using -cp or classpath command line options.

<div align="right">
    <b><a href="#related-topics">↥ back to top</a></b>
</div>

## Q. Java Compiler is stored in JDK, JRE or JVM?

**1. JDK**:

Java Development Kit is the core component of Java Environment and provides all the tools, executables and binaries required to compile, debug and execute a Java Program.

**2. JVM**:

JVM is responsible for converting Byte code to the machine specific code. JVM is also platform dependent and provides core java functions like memory management, garbage collection, security etc. JVM is customizable and we can use java options to customize it, for example allocating minimum and maximum memory to JVM. JVM is called virtual because it provides an interface that does not depend on the underlying operating system and machine hardware.

**2. JRE**:

Java Runtime Environment provides a platform to execute java programs. JRE consists of JVM and java binaries and other classes to execute any program successfully.

<p align="center">
  <img src="assets/jdk.jpg" alt="Java Compiler" width="500px"  />
</p>

<div align="right">
    <b><a href="#related-topics">↥ back to top</a></b>
</div>

## Q. What is difference between Heap and Stack Memory in java?

**1. Java Heap Space:**  

Java Heap space is used by java runtime to allocate memory to **Objects** and **JRE classes**. Whenever we create any object, it\'s always created in the Heap space.

Garbage Collection runs on the heap memory to free the memory used by objects that doesn\'t have any reference. Any object created in the heap space has global access and can be referenced from anywhere of the application.

**2. Java Stack Memory:**

Stack in java is a section of memory which contains **methods**, **local variables** and **reference variables**. Local variables are created in the stack.

Stack memory is always referenced in LIFO ( Last-In-First-Out ) order. Whenever a method is invoked, a new block is created in the stack memory for the method to hold local primitive values and reference to other objects in the method.

As soon as method ends, the block becomes unused and become available for next method. Stack memory size is very less compared to Heap memory.

**Difference:**  

|Parameter	       |Stack Memory	               |Heap Space                       |
|------------------|-----------------------------|-----------------------------------|
|Application	   |Stack is used in parts, one at a time during execution of a thread|	The entire application uses Heap space during runtime|
|Size	           |Stack has size limits depending upon OS and is usually smaller then Heap|There is no size limit on Heap|
|Storage	       |Stores only primitive variables and references to objects that are created in Heap Space|All the newly created objects are stored here|
|Order	           |It is accessed using Last-in First-out (LIFO) memory allocation system|	This memory is accessed via complex memory management techniques that include Young Generation, Old or Tenured Generation, and Permanent Generation.|
|Life	           |Stack memory only exists as long as the current method is running|Heap space exists as long as the application runs|
|Efficiency	       |Comparatively much faster to allocate when compared to heap| Slower to allocate when compared to stack|
|Allocation/Deallocation| This Memory is automatically allocated and deallocated when a method is called and returned respectively|Heap space is allocated when new objects are created and deallocated by Gargabe Collector when they are no longer referenced |

<div align="right">
    <b><a href="#related-topics">↥ back to top</a></b>
</div>

## Q. How many types of memory areas are allocated by JVM?

JVM is a program which takes Java bytecode and converts the byte code (line by line) into machine understandable code. JVM perform some particular types of operations:

* Loading of code
* Verification of code
* Executing the code
* It provide run-time environment to the users

**Types of Memory areas allocated by the JVM:**  

**1. Classloader**: Classloader is a subsystem of JVM that is used to load class files.

**2. Class(Method) Area**: Class(Method) Area stores per-class structures such as the runtime constant pool, field and method data, the code for methods.

**3. Heap**: It is the runtime data area in which objects are allocated.  

**4. Stack**: Java Stack stores frames.It holds local variables and partial results, and plays a part in method invocation and return. Each thread has a private JVM stack, created at the same time as thread.

**5. Program Counter Register**: PC (program counter) register. It contains the address of the Java virtual machine instruction currently being executed.  

**6. Native Method Stack**: It contains all the native methods used in the application.

<div align="right">
    <b><a href="#related-topics">↥ back to top</a></b>
</div>

## # 3. JAVA DATA TYPES

<br/>

## Q. What are autoboxing and unboxing?

The automatic conversion of primitive data types into its equivalent Wrapper type is known as boxing and opposite operation is known as unboxing.

**Example:** Autoboxing

```java
/**
 * Autoboxing
 */
class BoxingExample {
    public static void main(String args[]) {
        int a = 50;
        Integer a2 = new Integer(a); // Boxing
        Integer a3 = 5; // Boxing

        System.out.println(a2 + " " + a3);
    }
} 
```

**Example:** Unboxing

```java
/**
 * Unboxing
 */
class UnboxingExample {
    public static void main(String args[]) {
        Integer i = new Integer(50);
        int a = i;

        System.out.println(a);
    }
}
```

<div align="right">
    <b><a href="#related-topics">↥ back to top</a></b>
</div>

## Q. What is the difference between transient and volatile variable in Java?

**1. Transient:**

The transient modifier tells the Java object serialization subsystem to exclude the field when serializing an instance of the class. When the object is then deserialized, the field will be initialized to the default value; i.e. null for a reference type, and zero or false for a primitive type.

