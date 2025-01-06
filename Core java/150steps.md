# Java Tutorial For Beginners

Welcome to this book on **"Learning Java In 150 Steps"**. 

I am **Ranga Karanam**, and I have more than two decades of programming experience. 

I love Programming. One of the aims I had when I started ```in28minutes``` was to make learning programming easy. Thanks for helping us provide amazing courses to 300,000 learners across the world.

At **In28Minutes**, we ask ourselves one question every day: "How do we create awesome learning experiences?" 

In this book, you will learn to write **object** **oriented** code with Java. You will be exposed to a lot of examples, exercises and tips. We will take up a lot of examples, and try and see how to write code for those in Java. 

Help us improve this guide - **Fork, Pull Requests, Shares and Likes are recommended**!

## Table of Contents

* [Chapter 01 - Introduction to Programming with Print-Multiplication-Table](#introduction-to-programming-with-print-multiplication-table)
* [Chapter 02 - Understanding Methods](#understanding-methods)
* [Chapter 03 - Understanding the Java Platform](#understanding-the-java-platform)
* [Chapter 04 - Eclipse](#eclipse)
* [Chapter 05 - Object Oriented Progamming (OOP)](#object-oriented-progamming-oop)
* [Chapter 06 - Primitive Data Types](#primitive-data-types)
* [Chapter 07 - Introducing Conditionals - if, switch and more](#introducing-conditionals---if-switch-and-more)
* [Chapter 08 - Loops](#loops)
* [Chapter 09 - Reference Types](#reference-types)
* [Chapter 10 - Arrays and ArrayList](#arrays-and-arraylist)
* [Chapter 11 - Object Oriented Programming (*OOP*) - Revisited](#object-oriented-programming-oop---revisited)
* [Chapter 12 - Introducing Collections](#introducing-collections)
* [Chapter 13 - Introducing Generics](#introducing-generics)
* [Chapter 14 - Introduction to Functional Programming](#introduction-to-functional-programming)
* [Chapter 15 - Threads and Concurrency](#threads-and-concurrency)
* [Chapter 16 - Introduction To Exception handling](#introduction-to-exception-handling)
* [Chapter 17 - File Operations](#file-operations)
* [Chapter 18 - Concurrency : Advanced Topics](#concurrency--advanced-topics)

## Our Approach

We did a study on why students give up on programming?

The popular answer was

> Difficulty in writing their first program

Put yourselves in the shoes of a beginner and look at this typical ```Java Hello World Example```.

```java
package com.in28minutes.firstjavaproject; 
public class HelloWorld 
{   
     public static void main(String[] args) {           
            System.out.println("Hello World");   
     } 
}
```

A ```Programming Beginner``` will be overwhelmed by this. I remember how I felt when I saw this almost 20 years back. Stunned.

Why?
- There are a number of keywords and concepts - package, public, class, static, void, String[] and a lot more..
- What if the programmer makes a typo? Will he be able to fix it?


**We believe that there has to be a better way to learn programming.**

- Why don't we learn programming step by step? 
- Why should it not be a lot of fun? 
- Why don't we solve a lot of problems and learn programming as a result?

This is the approach we took to writing this guide and develop our introductory programming courses for Java and Python. 

> Do you know? The first 3 hours of our Java Course is available [here](https://courses.in28minutes.com/p/java-tutorial-for-beginner-in-250-steps).



## Introduction to Programming with Print-Multiplication-Table

### Step 01: First Challenge : The Print-Multiplication-Table (*PMT-Challenge*)

Learning to program is a lot like learning to ride a bicycle. The first few steps are the most challenging ones. 

Once you use this stepwise approach to solve a few problems, it becomes a habit. 

In this book, we will introduce you to Java programming by taking on a few simple problems to start off. 

> Having fun along the way is what we will aim to do.
 
_Are you all geared up, to take on your first programming challenge? **Yes**?  Let's get started then!_

Our first *programming challenge* aims to do, what every kid does in math class: reading out a multiplication table.

#### The *PMT-Challenge*

1. Compute the multiplication table for ```5```, with entries from ```1``` to ```10```.
2. Display this table.

```
5 * 1  =  5
5 * 2  = 10
5 * 3  = 15
5 * 4  = 20
5 * 5  = 25
5 * 6  = 30
5 * 7  = 35
5 * 8  = 40
5 * 9  = 45
5 * 10 = 50
```

As part of solving the multiplication table problem, you will be introduced to:
* **JShell**
* **Statements**
* **Expressions**
* **Variables**
* **Literals**
* **Conditionals**
* **Loops**
* **Methods** 

#### Summary

In this step, we:

* Stated our first programming challenge, *PMT-Challenge*
* Identified basic Java concepts to learn, to solve this challenge

### Step 02: Introducing ```JShell```
- - - 

```JShell``` is a programming tool, introduced in Java SE 9. JShell is a **_REPL_** interface. The term **REPL** refers to this:

* **_'R'_** stands for **R**ead; *Read* the input Java code
* **_'E'_** means **E**val; *Evaluate* the source code
* **_'P'_** translates to **P**rint; *Print* out the result
* **_'L'_** indicates **L**oop; *Loop* around, and wait for the next input

How about starting off exploring Java? Are you game?

##### Snippet-1: Check the Java programming environment

You can use [https://tryjshell.org/](https://tryjshell.org/) to run the code for the first 25 steps. Or you can [Install Java 12+](https://github.com/in28minutes/java-a-course-for-beginners/blob/master/00-02-java-eclipse-installation.md#installing-java). Here's the [troubleshooting section](https://github.com/in28minutes/java-a-course-for-beginners/blob/master/00-02-java-eclipse-installation.md#troubleshooting) if you face problems.

Launch up command prompt or Terminal.

Let type in ```java -version``` on the terminal and press enter.

```

	in28minutes$>java -version
	java version "x.0.1"
	Java(TM) SE Runtime Environment (build x.0.1+11)
	Java HotSpot(TM) 64-bit Server VM (build x.0.1+11, mixed mode)
	in28minutes$>

```

A successful execution displays the version of Java installed your system. You need to have atleast Java 9 to pursue this book.

##### Snippet-2: Launch JShell

You can launch JShell by typing ```jshell``` at your terminal. 

```java

	in28minutes$>jshell

	|  Welcome to JShell version x.0.1
 	|  For an introduction type: /help intro
	jshell>

```

When run, this command displays basic information about the installed ```JShell``` program. A ```jshell``` prompt then appears, which waits for your input.

##### Snippet-3: Sample JShell input, using a built-in command

The ```JShell``` command ```/help```, with a parameter ```intro```, gives you basic guidelines on how you use the tool.

```java

	jshell> /help intro

	|
	| intro
	| The jshell tool allows you to execute Java code, getting immediate results.
	| You can enter a Java definition (variable, method, class, etc), like: int x =8
	| or a Java expression, like: x + x
	| or a Java statement or import.
	| These little chunks of Java code are called 'snippets'.
	| There are also jshell commands that allow you to understand and
	| control what you are doing, like: /list
	|
	| For a list of commands: /help
	
	jshell>

```


##### Snippet-4: Evaluating an expression

Type ```3+4``` at the Jshell prompt

```java

	jshell> 3 + 4
	$1 ==> 7
	jshell>

```

This was your first real **REPL** cycle! When you type in  ```3 + 4```, JShell evaluates it and prints the result. 

> The entity ```$1``` is actually a variable name assigned to the result. We will talk about this later. 

##### Snippet-5: Getting out of JShell

The ```/exit``` command terminates the ```JShell``` program, and we are back to the terminal prompt.


```java

	jshell> /exit
	|  Goodbye
	
	in28minutes$>

```


##### Snippet-6: Again, enter JShell and Exit it!

You can now effortlessly launch, feed code to, and exit from  ```JShell```!

```java

	in28minutes$> jshell
	
	|  Welcome to JShell version 9.0.1
	|  For an introduction type: /help intro
	jshell> /exit
	|  Goodbye
	
	in28minutes$>

```

#### Summary

In this step, we learned:

* How to launch ```JShell``` from our terminal, and run a few commands on it
* How to run Java code on the ```JShell``` prompt

### Step 03: Welcome to Problem Solving

Lets try to break down the *PMT-Challenge* problem to be able to solve it.

```
5 * 1  =  5
5 * 2  = 10
5 * 3  = 15
5 * 4  = 20
5 * 5  = 25
5 * 6  = 30
5 * 7  = 35
5 * 8  = 40
5 * 9  = 45
5 * 10 = 50
```


Here is how our draft steps look like
* Calculate ```5 * 3``` and print result as ```15```
* Print ```5 * 3 = 15``` (```15``` is result of previous calculation)
* Do this ten times, once for each table entry (going from ```1``` to ```10```)

#### Summary

In this step, we:

* Broke down the *PMT-Challenge* problem into sub-problems

### Step 04: Introducing Expressions 

The first part of solving our *PMT-Challenge* is to calculate the product of ```5``` and another number, say ```3```.

Let's start up jshell and type ```5 X 3```.

```java

	in28minutes$> jshell

	|  Welcome to JShell version x.0.1
	|  For an introduction type: /help intro
	jshell> 5 X 3
	| Error:
	| ';' expected
	| 5 X 3
	|  ^
	| Error:
	| not a statement
	| 5 X 3
	|   ^
	| Error:
	| ';' expected
	| 5 X 3
	|    ^
	| Error:
	| missing return statement
	| 5 X 3
	| ^---^
```
You probably look at the symbol 'X' as a multiplier, remembering your school days.

Java does not identify '```X```' as the multiplication operator! Java supports multiplication, but only if you use its *predefined* operator, ```*```.

Let's type in code shown below:

```java
	jshell> 5 * 3
	$1 ==> 15
	jshell>

```

Success!

Let's look at some terminology:
- ```5 * 3 ``` is an expression.
- ```5``` and ```3``` are operands. They are also called **literals** or constant values.
- ```*``` is an operator.


Java also has built-in operators to perform other numerical tasks, such as:

* Addition: ```+``` 
* Subtraction: ```-```
* Division: ```/```
* Modulo arithmetic: ```%``` 

The following examples illustrate how to use them.
 
```java

	jshell> 5 * 10
	$2 ==> 50
	jshell> 5 + 10
	$3 ==> 15
	jshell> 5 - 10
	$4 ==> -5
	jshell> 10 / 2
	$5 ==> 5
	jshell>

```

Your school math memories are still fresh, and the operators don't seem to disappoint either! ```+```, ```-``` and ```/``` are your bread-and-butter operators.

```%``` is the modulo operator, which gives you the remainder when integer division is performed. 

```java

	jshell> 9 % 2
	$6 ==> 1
	jshell> 8 % 2
	$7 ==> 0
	jshell>

```

##### Snippet: Complex Expressions, Anyone?

Java allows you to use more than one operator within an expression.

Let's look at some simple expressions with multiple operators.

```java
 
	jshell> 5 + 5 + 5
	$8 ==> 15
	jshell> 5 + 10 - 15
	$9 ==> 0
	jshell> 5 * 5 + 5
	$10 ==> 30
	jshell> 5 * 15 / 3
	$11 ==> 25

```

Each of above expressions have two operators and three operands.

#### Summary

In this step, we:

* Learned how to construct numeric expressions
* Discovered that operators are predefined symbols
* Combined several operators to form larger expressions
 
### Step 05: Programming Exercise PE-1 (With Solutions)

At this stage, your smile tells us that you enjoy evaluating Java expressions. What if we tickle your mind a bit, to make sure it hasn't fallen asleep? 

Okay, here comes a couple of programming exercises.

1. Write an expression to calculate the number of minutes in a day.
2. Write an expression to calculate the number of seconds in a day.

#### Solution 1

60 (minutes in an hour) multipled by 24 (hours in a day)

```java

	jshell> 60 * 24
	$1 ==> 1440
```

#### Solution 2

60 (seconds in a minute) multipled by 60 (minutes in an hour) multipled by 24 (hours in a day)

```java
$jshell>60 * 60 * 24

$1 ==> 86400
```

### Step 06: Operators

Lets look at a few more examples to understand operators.

#### Invalid Operators

Let's type in ```5 ** 6``` followed by ```5 $ 6``` in JShell

```java
	jshell> 5 ** 6
	| Error:
	| Illegal start of expression
	| 5 ** 6
	|     ^

	jshell> 5 $ 6 
	| Error:
	| ';' expected
	| 5 $ 6
	|  ^
	| Error:
	| not a statement
	| 5 $ 6
	|   ^
	| Error:
	| ';' expected
	| 5 $ 6
	|    ^

	jshell> 5 */ 6
	| Error:
	| Illegal start of expression
	| 5 */ 6
	|     ^
	
```

```JShell``` was not impressed with our efforts at all! 

Java has a set of grammar rules, called its **syntax**. Code that does not follow these rules throw errors. The compiler informs you by listing the errors, and also provides hints on how you can correct them. 

Now, why is an error being thrown?

Operators in Java are all predefined, and limited in number.  ```*``` is a valid operator, whereas ```**``` and ```$```  were rejected, with error messages.

#### Understanding Result of Expression with Mixed Types

Let's look at another example:

```java

	jshell> 5 / 2
	$1 ==> 2
	jshell>

```

Surprise, Surprise! ```JShell``` seems to evaluate ``` 5 / 2 ``` to ``` 2 ``` instead of ```2.5```. Where did we go wrong?

Read what follows, with the biggest magnifying lens you can find:

**The result of an expression when evaluated, depends on the operator context**. This context is determined by the operands passed to it

There are two kinds of numbers typically used in programming : integer (1,2,3,...) and floating-point (1.1,2.3, 56.7889 etc). These values are represented by different **types** in Java. Integers are commonly of type ```int```, and the floating-point numbers are ```double``` by default.

In the expression ```5/2```, both ```5``` and ```2``` are of type ```int```. So, the result is also of type ```int```. 

Let's try with a few floating point numbers: 

```java

	jshell> 5.0 / 2.0
	$2 ==> 2.5
```
Both ```5.0``` and ```2.0``` are of type ```double```, the result is ```double```. We get a result of ```2.5```, as expected. 

Let's do a mixed operation - using a floating point number and integer.

```java
	jshell> 5.0 / 2
	$3 ==> 2.5
	jshell>

```

Among the types ```int``` and ```double```, ```double``` is considered to be a *wider type*. When you perform a numeric operation between two types, the result will be of the wider type.



#### Understanding Precedence of Operators

Let's look at few complex examples of expressions with more than one operator.

```java

	jshell> 5 + 5 * 6
	$1 ==> 35
	jshell> 5 - 2 * 2
	$2 ==> 1
	jshell> 5 - 2 / 2
	$3 ==> 4
	jshell>

```

Surprised with the results?  You might expect 5 + 5 * 6 evaluate to 10 * 6 i.e. 60. Howeever, we got ```35```! 

> We write English left-to-right, and carry this habit to calculations as well. 

_In expressions with multiple operators, the order of sub-expression evaluation depends on **operator precedence**._

The basic rules for operator precedence are actually quite simple (we will look at other rules a little later). 

The operators in the set  {```*```, ```/```, ```%```} have higher precedence than the operators in the set {```+```, ```-```}.

In the expression ```5 + 5 * 6``` : 5*6 is evaluated first. So, 5 + 5 * 6 becomes 5 + 30 i.e. 35.

```5 - 2 * 2``` and ```5 - 2 / 2``` are evaluated by following the same rules.

#### Use paranthesis for clear code 

Java provides syntax elements, called **parentheses** ```(```   and   ```)```, to group parts of an expression.

```java

	jshell> (5 - 2) * 2
	$4 ==> 6
	jshell> 5 - (2 * 2)
	$5 ==> 1
	jshell>

```

When you put an expression in parenthesis, it is evaluated first. (5 - 2) * 2 => 3 * 2 => 6.

Parentheses lead to better readability as they reduce confusion and help avoid errors. 

The old adage **_A stitch in time saves nine_** rings very true here. Use parentheses to make your code easy to read, even when they might not be necessary.

#### Summary

In this step, we:

* Discovered that operators are all predefined
* Learned that result of operation depends on operand types
* Understood what operator precedence means
* Used parentheses to group parts of an expression
 
### Step 07: Introducing Console Output 

We have computed the product of two literals (as in ```5 * 3```) in earlier steps. 

The next step is to print this result in a customized format - ```5 * 3 = 15```.

How do we do this?

Let try typing it in into JShell

```java
jshell> 5 * 3 = 15
|  Error:
|  unexpected type
|    required: variable
|    found:    value
|  5 * 3 = 15
|  ^---^
```

Hmm! Error.

How do we print text?

Java has a built-in utility method called ```System.out.println()```, that displays text on the console. 

```java
jshell> System.out.println(3*4)
12
```

We formed an expression, ```3*4```, and *passed* it to ```System.out.println()```, which is a built-in Java **method**.

```System.out.println(3*4)``` is an example of a **statement**. It is a **method call**.

The syntax rules for method calls are quite strict, and all its parts are mandatory.

```java
jshell> System.out.println3*4)
| Error:
| ';' expected
| System.out.println3*4)
|___________________^
| Error:
| cannot find symbol
|       symbol: variable println3
| System.out.println3*4)
| ^---------------------^

jshell> System.out.println 3*4
|  Error:
|  ';' expected
|  System.out.println 3*4
|                    ^
|  Error:
|  cannot find symbol
|    symbol:   variable println
|  System.out.println 3*4
|  ^----------------^

```

What if we want to print an entry of the Multiplication Table, as part of our solution to *PMT-Challenge*? In other words, how do we print the exact text ```5 * 2 = 10``` on the console? 

```java

	jshell> System.out.println(5 * 2 = 10)
	| Error:
	| unexpected type
	| required:  variable
	| found:     value
	| System.out.println(5 * 2 = 10)
	|____________________^--------^

```

You wanted to print ```5 * 2 = 10``` on the console. However, we see that we cannot pass ```5 * 2 = 10``` as an argument to ```System.out.println()```.

```5 * 2 = 10``` is not a single value. It is a piece of text with numeric characters, ```*``` and ```=```. 

In Java, we represent text using ```String```. A ```String literal``` is a sequence of characters, enclosed within **double quotes**: ```"``` and ```"```. 

```java
	jshell> System.out.println("5 * 2 = 10")
	| 5 * 2 = 10
```

Congratulations! You have now figured out how to display not just numbers on the console, but text as well!

#### Summary

In this step, we:

* Were introduced to the ```System.out.println()``` method for console output
* Used this utility to print a single *PMT-Challenge* table entry

### Step 08: Programming Exercise PE-02

Try and solve the following exercises:

1. Print ```Hello World``` onto the console.

2. Print ```5 * 3```, as is.

3. Print the calculated value of ```5 * 3```.

4. Print the number of seconds in a day, using the ```System.out.println``` method.

5. Do a syntax revision for the code that you write for each of the above exercises. In your code, identify the following elements:
	* Numeric and string literals
	* Expressions
	* Operators
	* Operands
	* Method calls

### Step 09: Solutions to PE-02

#### Solution 1

```java

	jshell> System.out.println("Hello World")
	Hello World

```

#### Solution 2

```java

	jshell> System.out.println("5 * 3")
	5 * 3
	jshell>
```

#### Solution 3

```java

	jshell> System.out.println(5 * 3)
	15

```

#### Solution 4

```java

	jshell> System.out.println(60 * 60 * 24)
	86400

```

### Step 10: Whitespace, Case sensitiveness and Escape Characters
The term *whitespace* refers to any sequence of continuous space, tab or newline characters.

#### Whitespace

Let's see a few examples of whitespace in action.

Whitespace affects the output when used in-and-around string literals.

```java
jshell> System.out.println("Hello World")
Hello World
jshell> System.out.println("Hello      World")
Hello      World
jshell> System.out.println("HelloWorld")
HelloWorld
```


Whitespace is ignored by the compiler when used around numeric expressions. 
```java

	jshell> System.out.println(24 * 60 * 60)
	86400
	jshell> System.out.println(24    *    60    *    60)
	8
