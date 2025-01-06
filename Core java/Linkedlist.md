
# Complete Java LinkedList Tutorial

A `LinkedList` in Java is part of the `java.util` package and provides a data structure where elements are stored in a sequence and each element (node) points to the next element in the list. LinkedLists are ideal for situations where you need efficient insertions and deletions at both ends of the list.

## Table of Contents:
1. [Introduction to LinkedList](#introduction-to-linkedlist)
2. [Creating a LinkedList](#creating-a-linkedlist)
3. [LinkedList Methods](#linkedlist-methods)
4. [LinkedList Example](#linkedlist-example)
5. [LinkedList Performance](#linkedlist-performance)
6. [Conclusion](#conclusion)

## 1. Introduction to LinkedList

In a LinkedList, each element is represented by a node. Each node contains two parts:
- **Data**: The actual value or element.
- **Reference to Next Node**: A pointer (or reference) to the next node in the list.

There are two types of LinkedLists in Java:
- **Singly LinkedList**: Each node points to the next node in the list.
- **Doubly LinkedList**: Each node has two pointers, one pointing to the next node and the other pointing to the previous node.

### Advantages of LinkedList:
- Efficient insertion and deletion at both ends (constant time operations).
- Can dynamically grow and shrink in size.

### Disadvantages of LinkedList:
- No random access (must traverse the list to find an element).
- More memory consumption than arrays due to extra references.

## 2. Creating a LinkedList

To use `LinkedList`, you need to import it from the `java.util` package:

```java
import java.util.LinkedList;

Creating a LinkedList

public class LinkedListExample {
    public static void main(String[] args) {
        // Creating an empty LinkedList of Strings
        LinkedList<String> list = new LinkedList<>();
        
        // Adding elements to the LinkedList
        list.add("Apple");
        list.add("Banana");
        list.add("Orange");
        
        System.out.println("LinkedList: " + list);
    }
}

Output:

LinkedList: [Apple, Banana, Orange]

3. LinkedList Methods

Java LinkedList provides several methods for performing operations. Here are some common ones:

add()

Adds an element to the end of the list.

list.add("Grapes");

addFirst() and addLast()

Adds an element at the beginning or end of the list.

list.addFirst("Mango"); // Adds Mango at the beginning
list.addLast("Papaya"); // Adds Papaya at the end

remove(), removeFirst(), and removeLast()

Removes an element from the list.

list.remove(); // Removes the first element
list.removeFirst(); // Removes the first element
list.removeLast(); // Removes the last element

get()

Returns the element at the specified position.

String fruit = list.get(1); // Returns the element at index 1 (Banana)

contains()

Checks if the list contains a specified element.

boolean isPresent = list.contains("Banana"); // Returns true if "Banana" is present

size()

Returns the size of the list.

int size = list.size(); // Returns the number of elements in the list

clear()

Removes all elements from the list.

list.clear(); // Clears the list

peek()

Returns the first element of the list without removing it (null if the list is empty).

String firstElement = list.peek(); // Returns the first element or null

poll()

Returns and removes the first element of the list (null if the list is empty).

String firstElement = list.poll(); // Removes and returns the first element or null

offer()

Adds an element to the end of the list.

list.offer("Cherry"); // Adds Cherry to the end of the list

4. LinkedList Example

Let’s explore a more detailed example, demonstrating the usage of various LinkedList methods.

import java.util.LinkedList;

public class LinkedListExample {
    public static void main(String[] args) {
        // Creating a LinkedList
        LinkedList<String> list = new LinkedList<>();
        
        // Adding elements to the LinkedList
        list.add("Apple");
        list.add("Banana");
        list.add("Orange");
        list.addFirst("Mango"); // Adds Mango at the beginning
        list.addLast("Papaya"); // Adds Papaya at the end
        
        System.out.println("LinkedList after additions: " + list);

        // Removing elements from the LinkedList
        list.removeFirst(); // Removes Mango
        list.removeLast();  // Removes Papaya
        list.remove("Banana"); // Removes Banana
        
        System.out.println("LinkedList after removals: " + list);

        // Checking if an element exists
        if (list.contains("Apple")) {
            System.out.println("Apple is present in the list");
        }

        // Getting the first element
        String firstElement = list.peek();
        System.out.println("First element: " + firstElement);
        
        // Getting the size of the list
        System.out.println("Size of the LinkedList: " + list.size());
        
        // Clearing the LinkedList
        list.clear();
        System.out.println("LinkedList after clear: " + list);
    }
}

Output:

LinkedList after additions: [Mango, Apple, Banana, Orange, Papaya]
LinkedList after removals: [Apple, Orange]
Apple is present in the list
First element: Apple
Size of the LinkedList: 2
LinkedList after clear: []

5. LinkedList Performance

Access time: O(n) — LinkedList does not allow random access, so accessing an element takes linear time.

Insertion and deletion at the beginning and end: O(1) — Efficient insertions and deletions at the beginning and end of the list.

Insertion and deletion in the middle: O(n) — Since the list is linked, operations in the middle require traversing the list.


When to use LinkedList:

When you need efficient insertions or deletions at both ends.

When memory usage is not a concern, as each element requires extra memory for storing the next node reference.


6. Conclusion

In this tutorial, we have explored how to use LinkedList in Java. We covered its creation, common methods, and performance characteristics. LinkedList is ideal for applications where you need efficient insertion and deletion at the ends of the list, though it may not be the best choice for random access scenarios.

Java’s LinkedList provides many powerful methods for manipulating lists efficiently, making it an essential data structure for Java developers.

