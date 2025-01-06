
# Java String Tutorial

In Java, `String` is a sequence of characters. The `String` class in Java is used to create and manipulate strings of characters.

## 1. String Declaration

In Java, you can declare a string in two ways:

```java
// Using String literal
String str1 = "Hello, World!";

// Using the new keyword
String str2 = new String("Hello, Java!");

2. String Length

The length() method returns the length of a string.

public class StringExample {
    public static void main(String[] args) {
        String str = "Hello";
        System.out.println("Length of the string: " + str.length());
    }
}

Output:

Length of the string: 5

3. String Concatenation

You can concatenate strings using the + operator or concat() method.

Using + Operator

public class StringExample {
    public static void main(String[] args) {
        String str1 = "Hello, ";
        String str2 = "World!";
        String result = str1 + str2;
        System.out.println(result);
    }
}

Output:

Hello, World!

Using concat() Method

public class StringExample {
    public static void main(String[] args) {
        String str1 = "Hello, ";
        String str2 = "World!";
        String result = str1.concat(str2);
        System.out.println(result);
    }
}

Output:

Hello, World!

4. String Comparison

Using equals() Method

The equals() method compares the content of two strings.

public class StringExample {
    public static void main(String[] args) {
        String str1 = "Java";
        String str2 = "java";
        System.out.println(str1.equals(str2));  // Output: false
    }
}

Output:

false

Using equalsIgnoreCase() Method

The equalsIgnoreCase() method compares two strings, ignoring case differences.

public class StringExample {
    public static void main(String[] args) {
        String str1 = "JAVA";
        String str2 = "java";
        System.out.println(str1.equalsIgnoreCase(str2));  // Output: true
    }
}

Output:

true

5. String Conversion

Convert String to Uppercase and Lowercase

public class StringExample {
    public static void main(String[] args) {
        String str = "Hello, Java!";
        System.out.println(str.toUpperCase());  // Output: HELLO, JAVA!
        System.out.println(str.toLowerCase());  // Output: hello, java!
    }
}

Output:

HELLO, JAVA!
hello, java!

6. Substring

The substring() method extracts a part of a string.

public class StringExample {
    public static void main(String[] args) {
        String str = "Hello, Java!";
        String substr = str.substring(7, 11);
        System.out.println(substr);  // Output: Java
    }
}

Output:

Java

7. String Trimming

The trim() method removes leading and trailing whitespace characters.

public class StringExample {
    public static void main(String[] args) {
        String str = "  Hello, Java!  ";
        System.out.println(str.trim());  // Output: Hello, Java!
    }
}

Output:

Hello, Java!

8. String Split

The split() method splits a string into an array of substrings based on a given delimiter.

public class StringExample {
    public static void main(String[] args) {
        String str = "Java,Python,C++";
        String[] languages = str.split(",");
        for (String language : languages) {
            System.out.println(language);
        }
    }
}

Output:

Java
Python
C++

9. String Replacement

The replace() method replaces occurrences of a character or substring in a string.

public class StringExample {
    public static void main(String[] args) {
        String str = "Hello, Java!";
        String replacedStr = str.replace("Java", "World");
        System.out.println(replacedStr);  // Output: Hello, World!
    }
}

Output:

Hello, World!

10. StringBuffer and StringBuilder

Strings in Java are immutable, meaning once created, they cannot be modified. However, StringBuffer and StringBuilder are mutable alternatives for strings.

StringBuffer Example

public class StringExample {
    public static void main(String[] args) {
        StringBuffer sb = new StringBuffer("Hello");
        sb.append(" World");
        System.out.println(sb);  // Output: Hello World
    }
}

StringBuilder Example

public class StringExample {
    public static void main(String[] args) {
        StringBuilder sb = new StringBuilder("Hello");
        sb.append(" World");
        System.out.println(sb);  // Output: Hello World
    }
}

Output:

Hello World

11. String Interning

String interning is a process of storing only one copy of each distinct string value in memory.

public class StringExample {
    public static void main(String[] args) {
        String str1 = new String("Java");
        String str2 = "Java";
        System.out.println(str1 == str2); // Output: false
        System.out.println(str1.intern() == str2); // Output: true
    }
}

Output:

false
true

Conclusion

In this tutorial, we've covered various aspects of Java String, including its declaration, manipulation, and comparison techniques. Understanding how to use strings efficiently is essential for building robust Java applications.

