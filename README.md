Brewin# Interpreter

Overview
The Brewin Interpreter Suite is a robust interpreter capable of handling a variety of programming constructs, including functions, object-oriented programming, first-class functions, closures, and prototypal inheritance. It is designed to execute Brewin, Brewin++, and Brewin# programs, each adding layers of functionality to support more complex software development paradigms.

Functionality
Basic Language Constructs: Supports integer, string, boolean, and nil values.
Control Structures: Includes if, if/else statements, and while loops with basic error handling mechanisms.
Function Definitions: Functions can be defined with varying parameters, supporting recursion, function overloading, and closures.
Object-Oriented Features: Enables object-oriented programming without classes, allowing objects to have methods and fields, with support for prototypal inheritance.
Error Handling: Implements comprehensive error handling including specific error types like NAME_ERROR and TYPE_ERROR.
Usage
To execute a Brewin program, use one of the following commands depending on the feature set of your program:

bash
Copy code
python interpreter.py [file.brewin]
Features
Extended Operations
Supports all binary integer arithmetic operations, boolean logic operations, string manipulation, and comparisons.
Dynamic scoping is utilized for variable and function visibility, with environments that respect the call stack.
First-Class Functions and Closures
Functions are first-class citizens that can be passed as arguments, returned from other functions, or stored in variables.
Closures capture and maintain their lexical environment, allowing for powerful functional programming patterns.
Object-Oriented Programming
Introduces objects that can have both fields and methods, with the capability to add or modify these at runtime.
Supports prototypal inheritance, where objects can inherit fields and methods from a prototype object.
Known Issues/Bugs
As of the latest release, there are no critical issues known. The interpreter has been extensively tested with a variety of test cases to ensure functionality and stability.
Additional Notes
The interpreter is based on the foundational InterpreterBase class, which provides essential functionalities and should not be modified to maintain the integrity of the execution environment.
Developers are encouraged to extend the functionalities and participate in debugging and enhancing the interpreter by submitting patches and improvements.
