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

