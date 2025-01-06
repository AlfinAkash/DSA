
# Java Arrays - Complete Tutorial

## Introduction to Arrays
An array is a collection of elements of the same data type stored in contiguous memory locations.

### Key Features:
- Fixed size
- Homogeneous elements
- Indexed-based (starting at `0`)

---

## Declaring and Initializing Arrays

### Declaration Syntax
```java
// Syntax
dataType[] arrayName;

// Example
int[] arr;

Instantiation

// Syntax
arrayName = new dataType[size];

// Example
arr = new int[5];

Combined Declaration and Instantiation

int[] arr = new int[5];

Initialization

// Manual Initialization
arr[0] = 10;
arr[1] = 20;

// Inline Initialization
int[] arr = {10, 20, 30, 40, 50};


---

Types of Arrays

1D Array

A single-dimensional array stores elements in a linear form.

int[] arr = {1, 2, 3};
for (int i = 0; i < arr.length; i++) {
    System.out.println(arr[i]);
}

2D Array

A two-dimensional array is like a matrix with rows and columns.

int[][] arr = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};
System.out.println(arr[1][2]); // Access element in the 2nd row, 3rd column

Jagged Array

A jagged array has rows of unequal lengths.

int[][] jaggedArray = new int[3][];
jaggedArray[0] = new int[2]; // 2 elements in the first row
jaggedArray[1] = new int[3]; // 3 elements in the second row
jaggedArray[2] = new int[1]; // 1 element in the third row


---

Operations on Arrays

1. Traversing an Array

int[] arr = {1, 2, 3, 4, 5};
for (int i = 0; i < arr.length; i++) {
    System.out.println(arr[i]);
}

// Using Enhanced for Loop
for (int num : arr) {
    System.out.println(num);
}

2. Copying an Array

int[] original = {1, 2, 3};
int[] copy = new int[original.length];
System.arraycopy(original, 0, copy, 0, original.length);

3. Sorting an Array

import java.util.Arrays;

int[] arr = {3, 1, 4, 1, 5};
Arrays.sort(arr);
System.out.println(Arrays.toString(arr)); // [1, 1, 3, 4, 5]

4. Searching in an Array

int[] arr = {3, 1, 4, 1, 5};
int index = Arrays.binarySearch(arr, 4); // Array must be sorted
System.out.println(index);

5. Multidimensional Array Traversal

int[][] matrix = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};

for (int i = 0; i < matrix.length; i++) {
    for (int j = 0; j < matrix[i].length; j++) {
        System.out.print(matrix[i][j] + " ");
    }
    System.out.println();
}


---

Array Utilities

1. toString()

int[] arr = {1, 2, 3};
System.out.println(Arrays.toString(arr)); // [1, 2, 3]

2. fill()

int[] arr = new int[5];
Arrays.fill(arr, 10);
System.out.println(Arrays.toString(arr)); // [10, 10, 10, 10, 10]

3. equals()

int[] arr1 = {1, 2, 3};
int[] arr2 = {1, 2, 3};
System.out.println(Arrays.equals(arr1, arr2)); // true


---

Common Mistakes with Arrays

1. Array Index Out of Bounds Exception

int[] arr = {1, 2, 3};
System.out.println(arr[3]); // Exception


2. NullPointerException

int[] arr = null;
System.out.println(arr.length); // Exception




---

Advanced Topics

1. Cloning an Array

int[] original = {1, 2, 3};
int[] clone = original.clone();
System.out.println(Arrays.equals(original, clone)); // true

2. Streams with Arrays

import java.util.stream.IntStream;

int[] arr = {1, 2, 3, 4, 5};
IntStream stream = Arrays.stream(arr);
stream.forEach(System.out::println);

3. Using Lists with Arrays

import java.util.*;

int[] arr = {1, 2, 3};
List<Integer> list = Arrays.asList(1, 2, 3);
System.out.println(list);


---

Real-World Examples

1. Finding the Maximum Value

int[] arr = {3, 5, 7, 2, 8};
int max = arr[0];
for (int num : arr) {
    if (num > max) max = num;
}
System.out.println("Max: " + max);

2. Reversing an Array

int[] arr = {1, 2, 3, 4, 5};
for (int i = 0; i < arr.length / 2; i++) {
    int temp = arr[i];
    arr[i] = arr[arr.length - i - 1];
    arr[arr.length - i - 1] = temp;
}
System.out.println(Arrays.toString(arr)); // [5, 4, 3, 2, 1]

3. Rotating an Array

int[] arr = {1, 2, 3, 4, 5};
int k = 2; // Number of rotations

for (int i = 0; i < k; i++) {
    int temp = arr[0];
    for (int j = 0; j < arr.length - 1; j++) {
        arr[j] = arr[j + 1];
    }
    arr[arr.length - 1] = temp;
}
System.out.println(Arrays.toString(arr)); // [3, 4, 5, 1, 2]


---



