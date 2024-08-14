# Contents

- [OOP - Object Oriented Programming](#object-oriented-programming)
- [Mavin](#maven)
- [Keyboard Short Cuts](#keyboard-short-cuts)
- [Generics](#generics)
- [Wrappers](#wrappers)
- [Collections](#collections)
	- [HashSet](#hashet)


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
```
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


<br><br><br>
## Operators

| Operator Type | Operators |
|---------------|-----------|
| Arithmetic    | +, – , *, / , % |
| Assignment    | =, +=, -=, *=, /=, %=, &=, ^=, |=, <<=, >>=, >>>= |
| Bitwise       | ^, &, \| |
| Logical       | &&, \|\| |
| Relational    | <, >, <=, >=, ==, != |
| Shift         | <<, >>, >>> |
| Ternary       | ?: |
| Unary         | ++x, –x, x++, x–, +x, –x, !, ~ |


## How to accept user input
```
import java.util.Scanner;

public class Main {
public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        System.out.println("What is your name? ");
        String name = scanner.nextLine();
        System.out.println("hello "+name );
    }
}
```
### This will print to the console "What is your name?". The user inputs their name and "hello name" appears.

### Static vs. Public
You will often see Java programs that have either static or public attributes and methods.

In the example above, we created a static method, which means that it can be accessed without creating an object of the class, unlike public, which can only be accessed by objects:

<br><br><br>
# Object Oriented Programming

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
# Maven

### New Project Set up

Group id: 
- How Maven organizes projects as a convention for Maven's online repository
- This is typically a backwards URL (e.g. com.cooksys)

Artifact id: 
- Name of the project

<<<<<<< HEAD
<br><br><br>

# Keyboard Short Cuts for Eclipse

| Shortcut Key Mac                 | Description                                  |
| -------------------------------- |--------------------------------------------- |
|CTRL + Space + Enter              |	 Template ``public static void main(String[] args)``|										      
| CMD + Option + S| Generate Constructor |
| | Getters and Setters
| CMD + Shift + O | Auto Object/Class Import|
| "syso" followed by CRTL + Space | ``System.out.println()`` |
| CTRL + Space | Suggested Completions |


<br><br><br>

# Generics

Generics enable types (classes and interfaces) to be parameters when defining:
classes, interfaces and methods.
A benefit is to eliminate the need to create multiple versions of methods or classes for various data types.
Uses 1 version of a method/class for all reference data types.

Parameterized types, like methods. You can pass various kinds of parameters into a generic method.
It is a compile time safety check to know we are passing as a parameter where were expecting to be passing in.
PRO - better type safety over upcasting




## example-generic.java

```
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

example

```
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


# Collections

## Lists
All lists maintain insertion order
Can contain duplicate values
Can directly access values based on their index
Lists use generics, cannot use primitive types
Not thread safe, should use vector instead

 ArrayList - A dynamic array. Stores only reference data types


## Sets
A set is a Collection that cannot contain duplicate elements. It models the mathematical set abstraction. The Set interface contains only methods inherited from Collection and adds the restriction that duplicate elements are prohibited.
Stores objects using hashing in a hash table. 

### HashSet

- Characteristics
    - looks like array 
    - has no order 
    - no duplicate elements allowed 

<br>

- Use case 
	- When you need a collection of data with none duplicate data and don't care about the sequence


  
  ```
	 // create new HashSet
	 HashSet<String> fruits = new HashSet<>();
	 
	 // add to set
	 fruits.add("Apple");
	 fruits.add("Banana");
	 fruits.add("Cherry");
      
      System.out.println(fruits): // prints  [ "Apple", "Banana", "Cherry"]
      
      // remove from set
      // cannot remove elements based on index 
      fruits.remove("Apple);  // prints  ["Banana", "Cherry"]
      
	for (String fruit: fruits) {
		System.out.println(fruit);
	}
	
	// or to print each element
	fruits.forEach(System.out::println);
	
  ```
  
  
  
  Removing duplicates from an ArrayList
  
  ```
  
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
  

# Maps
- Characteristics
    - Don't maintain insertion order
    - Stores values related to a key
    - All keys unique
    - Values can contain duplicates
    - Can access values directly using their key, but <ins>cannot access keys directly</ins>

<br>


### HashMap

<br>

```
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






=======
<br><br><br>
>>>>>>> baddb56b15dee79fc87d2b83f6919cb602a9fac7
