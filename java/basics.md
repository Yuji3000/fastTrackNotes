# Contents

- [OOP - Object Oriented Programming](#object-oriented-programming)
- [Mavin](#maven)
- [Keyboard Short Cuts](#keyboard-short-cuts)



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

<br><br><br>

# Keyboard Short Cuts for Eclipse

| Shortcut Key Mac                 | Description                                  |
| -------------------------------- |--------------------------------------------- |
|CTRL + Space + Enter              |	 Template ``public static void main(String[] args)``|										      
| CMD + Option + S| Generate Constructor |
| | Getters and Setters
| CMD + Shift + O | Auto Object/Class Import|
|"syso" followed by CRTL + Space | ``System.out.println()`` |

