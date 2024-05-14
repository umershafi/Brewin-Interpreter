# Brewin# Interpreter

## Overview
The Brewin Interpreter Suite is a robust interpreter capable of handling a variety of programming constructs, including functions, object-oriented programming, first-class functions, closures, and prototypal inheritance. It is designed to execute Brewin# programs, each adding layers of functionality to support more complex software development paradigms.

## Click [here]([quora.com/profile/Ashish-Kulkarni-100](https://barista-f23.fly.dev/)) to use the Interpreter

## Functionality
- Basic Language Constructs: Supports integer, string, boolean, and nil values.
- Control Structures: Includes if, if/else statements, and while loops with basic error handling mechanisms.
- Function Definitions: Functions can be defined with varying parameters, supporting recursion, function overloading, and closures.
- Object-Oriented Features: Enables object-oriented programming without classes, allowing objects to have methods and fields, with support for prototypal inheritance.
- Error Handling: Implements comprehensive error handling including specific error types like NAME_ERROR and TYPE_ERROR.
## Usage
To execute a Brewin program, use one of the following commands depending on the feature set of your program:
```python
python3 interpreterv4.py [file.brewin]
```
## Features
### Extended Operations
Supports all binary integer arithmetic operations, boolean logic operations, string manipulation, and comparisons.
Dynamic scoping is utilized for variable and function visibility, with environments that respect the call stack.
### First-Class Functions and Closures
Functions are first-class citizens that can be passed as arguments, returned from other functions, or stored in variables.
Closures capture and maintain their lexical environment, allowing for powerful functional programming patterns.
### Object-Oriented Programming
Introduces objects that can have both fields and methods, with the capability to add or modify these at runtime.
Supports prototypal inheritance, where objects can inherit fields and methods from a prototype object.
## Known Issues/Bugs
As of the latest release, there are no critical issues known. The interpreter has been extensively tested with a variety of test cases to ensure functionality and stability.
## Additional Notes
The interpreter is based on the foundational InterpreterBase class, which provides essential functionalities and should not be modified to maintain the integrity of the execution environment.
Developers are encouraged to extend the functionalities and participate in debugging and enhancing the interpreter by submitting patches and improvements.
## Example
### Basic Function Definition and Calls
This example demonstrates defining a simple function and calling it:

```
func main() {
  print("Hello, Brewin!");
}
```
### Recursive Function for Calculating Factorial
This example shows a function that calculates the factorial of a number using recursion:

```
func factorial(n) {
  if (n <= 1) { return 1; }
  return n * factorial(n-1);
}

func main() {
  print(factorial(5));  // Outputs 120
}
```
### Using Objects and Methods
This example illustrates creating an object, adding fields and methods, and using inheritance:

```
func main() {
  person = @;  // Creating a new object
  person.name = "Jane";
  person.introduce = lambda() {
    print("Hello, my name is ", this.name);
  };

  // Creating another object that inherits from person
  employee = @;
  employee.proto = person;
  employee.name = "John";
  employee.job = "Developer";
  employee.introduce = lambda() {
    print("Hello, my name is ", this.name, " and I am a ", this.job);
  };

  person.introduce();  // Outputs: Hello, my name is Jane
  employee.introduce();  // Outputs: Hello, my name is John and I am a Developer
}
```
### First-Class Functions and Closures
This example shows how functions can be treated as first-class citizens and demonstrates closure functionality:

```
func createAdder(x) {
  return lambda(y) { return x + y; };
}

func main() {
  addFive = createAdder(5);
  print(addFive(3));  // Outputs: 8
}
```
### While Loop and Control Structures
This example uses a while loop and if statements to demonstrate control structures:

```
func main() {
  i = 10;
  while (i > 0) {
    print(i);
    i = i - 1;
    if (i == 5) {
      print("Halfway there!");
    }
  }
}
```
These examples provide a foundation for new users to start writing programs in Brewin#, offering a glimpse into the language's capabilities and syntax.
## Credit
This was my implementation for the Programming Language course at UCLA with Professor Carey Nachenberg, so credits to him for the specifications and the idea of the language
