# Contents

- [OOP - Object Oriented Programming](#object-oriented-programming)
- [Maven](#maven)
- [Generics](#generics)
- [Wrappers](#wrappers)
- [Collections](#collections)
  - [Lists](#lists)
    - [ArrayLists](#arraylists)
  - [Sets](#sets)
    - [HashSet](#hashsets)
  - [Maps](#maps)
    - [HashMaps](#hashmaps)

<br><br><br>

## Primitive Data Types


| Data Type | Size | Description |
|-----------|------|-------------|
| byte      | 1 byte | Stores whole numbers from -128 to 127 |
| short     | 2 bytes | Stores whole numbers from -32,768 to 32,767 |
| int       | 4 bytes | Stores whole numbers from -2,147,483,648 to 2,147,483,647 |
| long      | 8 bytes | Stores whole numbers from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 |
| float     | 4 bytes | Stores fractional numbers. Sufficient for storing 6 to 7 decimal digits |
| double    | 8 bytes | Stores fractional numbers. Sufficient for storing 15 decimal digits |
| boolean   | 1 bit | Stores true or false values |
| char      | 2 bytes | Stores a single character/letter or ASCII values |

## Use example on variables below

```java
int myNum = 9;
float myFloatNum = 8.99f;
char myLetter = 'A';
boolean myBool = false;
String myText = "Hello World";
```

## Non-primitive Data Types

- Strings
- Class
- Object
- Array
- Interface (Similar to Ruby helper class/method)

## Operators

| Operator Type | Operators                                          |
|---------------|----------------------------------------------------|
| Arithmetic    | +, -, *, /, %                                      |
| Assignment    | =, +=, -=, *=, /=, %=, &=, ^=, \|=, <<=, >>=, >>>= |
| Bitwise       | ^, &, \|                                           |
| Logical       | &&, \|\|                                           |
| Relational    | <, >, <=, >=, ==, !=                               |
| Shift         | <<, >>, >>>                                        |
| Ternary       | ?:                                                 |
| Unary         | ++x, -x, x++, x--, +x, -x, !, ~                    |

## How to accept user input

```java
import java.util.Scanner;

public class Main {
    
    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        System.out.println("What is your name? ");
        String name = scanner.nextLine();
        System.out.println("Hello "+ name);
        // will print to the console "What is your name?". The user inputs their name and "Hello name" appears.
    }
}
```

### Static vs. Public

You will often see Java programs that have either static or public attributes and methods.

In the example above, we created a static method, which means that it can be accessed without creating an object of the class, unlike public, which can only be accessed by objects:

<br><br><br>

## Object Oriented Programming

### Java Access Modifiers

Public

- We can access the public modifier from anywhere. We can access public modifiers from within the class as well as from outside the class and also within the package and outside the package.

Protected

- Can access the protected modifier within the same package and also from outside the package with the help of the child class. If we do not make the child class, we cannot access it from outside the package. So inheritance is a must for accessing it from outside the package.

Private

- Can access the private modifier only within the same class and not from outside the class.

Default

- Can access the default modifier only within the same package and not from outside the package. And also, if we do not specify any access modifier it will automatically consider it as default.

## 4 Pillars of OOP

### 1. Abstraction

- Only expose operations you want to allow others to use

 or

- Encapsulation in Java is an object-oriented procedure of combining the data members and data methods of the class inside the user-defined class. It is important to declare this class as private.

### 2. Encapsulation

- Keep code(methods, data etc) private and contained. This allows control over how data and methods are used

### 3. Inheritance

### 4. Polymorphism

<br><br><br>

## Maven

### New Project Set up

Group id:

- How Maven organizes projects as a convention for Maven's online repository
- This is typically a backwards URL (e.g. com.cooksys)

Artifact id:

- Name of the project

<br><br><br>

## Arrays Class

- Characteristics
  - Fixed size: Once an array is created, its size cannot be changed.
  - Indexed: Array elements are accessed using indices, starting from 0.
  - Homogeneous: All elements in an array are of the same type.

### Examples

1. Creating an Array with a Specific Size
When you know the size of the array but don't have the values yet:

```java
  // Create an array of integers with a size of 5
  int[] numbers = new int[5];

  // Create an array of Strings with a size of 3
  String[] fruits = new String[3];

```

2. Creating and Initializing an Array with Values
When you know the values you want to store in the array:

```java
  // Create and initialize an array of integers
  int[] numbers = {1, 2, 3, 4, 5};
  
  // Create and initialize an array of Strings
  String[] fruits = {"Apple", "Banana", "Cherry"};

```

3. Creating an Array and Assigning Values Later
You can also create an empty array and then assign values to its elements individually:

```java
  // Create an array of integers with a size of 3
  int[] numbers = new int[3];
  
  // Assign values to the array elements
  numbers[0] = 10;
  numbers[1] = 20;
  numbers[2] = 30;
  
  // Accessing an element in the array
  int firstNumber = numbers[0]; // 10

  // Create an array of integers with a size of 5
  int[] numbers = new int[5];

  // Create an array of Strings with a size of 3
  String[] fruits = new String[3];

  
  // Create and initialize an array of integers
  int[] numbers = {1, 2, 3, 4, 5};
  
  // Create and initialize an array of Strings
  String[] fruits = {"Apple", "Banana", "Cherry"};
```

## Common Array methods

.asList()

```java
// Changes an array to a list
  
int[] original = {1, 2, 3, 4, 5};
int[] copy = Arrays.copyOf(original, 3); // Copy first 3 elements
  
System.out.println(Arrays.toString(copy)); // Output: [1, 2, 3]
```

.copyOf()

```java

// creates a new array by copying the specified length from the original array
    
int[] original = {1, 2, 3, 4, 5};
int[] copy = Arrays.copyOf(original, 3); // Copy first 3 elements

System.out.println(Arrays.toString(copy)); // Output: [1, 2, 3]
    
```

.copyOfRange()

```java
// creates a new array by copying elements from a specified range of the original array.

int[] original = {1, 2, 3, 4, 5};
int[] rangeCopy = Arrays.copyOfRange(original, 1, 4); // Copy elements from index 1 to 3

System.out.println(Arrays.toString(rangeCopy)); // Output: [2, 3, 4]
```

.toString()

```java
//returns a string representation of the array
  
int[] numbers = {1, 2, 3, 4, 5};
String arrayString = Arrays.toString(numbers);

System.out.println(arrayString); // Output: [1, 2, 3, 4, 5]
```

## Generics

Generics enable types (classes and interfaces) to be parameters when defining:
classes, interfaces and methods.
A benefit is to eliminate the need to create multiple versions of methods or classes for various data types.
Uses 1 version of a method/class for all reference data types.

Parameterized types, like methods. You can pass various kinds of parameters into a generic method.
It is a compile time safety check to know we are passing as a parameter where were expecting to be passing in.
PRO - better type safety over upcasting

### Generics Example

```java
  Integer[] intArray = {1, 2, 3, 4}; //displayArray returns 1 2 3 4
  Double[] doubleArray = {1.1, 2.2, 3.3}; //displayArray returns 1.1 2.2 3.3 4.4
  
  // Instead of creating two methods for each array  
  // we create one method that can take either as a parameter
  
  displayArray(intArray);
  
  public static <T> void displayArray(T[] array) {
      for(T x : array) {
          System.out.print(x+" ")
      }
      
      System.out.println();
  }
```

## Wrappers

### Wrappers Example

```java
  // primitive data type declaration
  
  int age = 25;
  double price = 19.99;
  char grade = 'A';
  boolean isAvailable = true;
  
  // reference data types with wrappers
  
  Integer age = 25;            // Reference type for int
  Double price = 19.99;        // Reference type for double
  Character grade = 'A';       // Reference type for char
  Boolean isAvailable = true;  // Reference type for boolean
```

## Collections

## Lists

- All lists maintain insertion order
- Can contain duplicate values
- Can directly access values based on their index
- Lists use generics, cannot use primitive types
- Not thread safe, should use vector instead

### ArrayLists

A dynamic array. Stores only reference data types

## Sets

A set is a Collection that cannot contain duplicate elements. It models the mathematical set abstraction. The Set interface contains only methods inherited from Collection and adds the restriction that duplicate elements are prohibited.
Stores objects using hashing in a hash table.

### HashSets

- Characteristics
  - looks like array
  - has no order
  - no duplicate elements allowed

<br>

- Use case
  - When you need a collection of data with none duplicate data and don't care about the sequence

  ```java
    // create new HashSet
    HashSet<String> fruits = new HashSet<>();
   
    // add to set
    fruits.add("Apple");
    fruits.add("Banana");
    fruits.add("Cherry");
      
    System.out.println(fruits): // prints  [ "Apple", "Banana", "Cherry"]
      
    // remove from set
    // cannot remove elements based on index 
    fruits.remove("Apple");  // prints  ["Banana", "Cherry"]
      
    for (String fruit: fruits) {
        System.out.println(fruit);
    }
  
    // or to print each element
    fruits.forEach(System.out::println);
  ```

  <br>

  Removing duplicates from an ArrayList
  
  ```java
    List<Integer> numberList = new ArrayList<>();
    numberList.add(1);
    numberList.add(1);
    numberList.add(2);
    numberList.add(3);
    
    System.out.println(numberList); // prints [1, 1, 2, 3]
    
    // add to set to remove duplicates
    Set<Integer> numberSet = new HashSet<>();
    numberSet.addAll(numberList);
    System.out.println(numberSet); // prints [1, 2, 3]
    
    // or pass into new HashSet constructor
    Set<Integer> numberSet = new HashSet<>(numberList); 
  ```
  
## Maps

- Characteristics
  - Don't maintain insertion order
  - Stores values related to a key
  - All keys unique
  - Values can contain duplicates
  - Can access values directly using their key, but <ins>cannot access keys directly</ins>

<br>

### HashMaps

<br>

```java
  // Create a new HashMap
  HashMap<String, Integer> fruitPrices = new HashMap<>();

  // Add key-value pairs to the HashMap
  fruitPrices.put("Apple", 3);
  fruitPrices.put("Banana", 2);

  // Print the HashMap
  System.out.println(fruitPrices);
  
  // Print output
  {Apple=3, Banana=2}
```

### Common Collections Class Methods

- .copy()
- .sort()
- .shuffle()
- .reverse()
- .synchronized*()
- .unmodifiable*()
