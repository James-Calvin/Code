# Code Language Design Document

## Introduction

### Purpose

This document outlines the design and specifications of the Code programming language, which is intended to facilitate the creation of interactive applications
and games with 2D graphics.

### Overview

Code is a statically typed, object-oriented programming language with a syntax similar to C#. It emphasizes readability, simplicity, and rapid development.

## Language Goals

### Primary Goals

- Simplify 2D game development.
- Ensure readability and maintainability.
- Support object-oriented programming.

### Secondary Goals

- Facilitate rapid prototyping.
- Provide robust error handling.
- Encourage community contributions.

## Requirements

### Functional Requirements

- **FR-001**: The language shall use clear and consistent syntax to improve readability and maintainability.
- **FR-002**: The language shall avoid abbreviations and acronyms in reserved words. Full words like `function`, `class`, `integer`, `string` shall be used.
- **FR-003**: The language shall support primitive types such as `integer`, `float`, `boolean`, `character`, and `string`.
- **FR-004**: The language shall support composite types such as arrays, lists, dictionaries, and tuples.
- **FR-005**: The language shall support type inference to reduce verbosity while remaining statically typed.
- **FR-006**: The language shall support immutable data types and variables.
- **FR-007**: The language shall support classes and objects for defining and instantiating complex data types.
- **FR-008**: The language shall support inheritance and polymorphism for creating hierarchical relationships between classes.
- **FR-009**: The language shall support encapsulation with access modifiers (`public`, `private`, `protected`).
- **FR-010**: The language shall support interfaces and abstract classes to define contracts and abstract behavior.
- **FR-011**: The language shall support properties and methods within classes.
- **FR-012**: The language shall support constructors and destructors for initialization and cleanup.
- **FR-013**: The language shall provide a simple syntax for defining and invoking functions.
- **FR-014**: The language shall treat functions as first-class citizens, allowing them to be passed as arguments and returned - from other functions.
- **FR-015**: The language shall support lambda expressions for inline anonymous functions.
- **FR-016**: The language shall support function and method overloading.
- **FR-017**: The language shall support conditional statements such as `if`, `else if`, and `else`.
- **FR-018**: The language shall support looping constructs such as `for`, `foreach`, `while`, and `do while`.
- **FR-019**: The language shall support enhanced pattern matching for complex conditional logic.
- **FR-020**: The language shall provide try-catch-finally blocks for error handling.
- **FR-021**: The language shall allow the definition of custom exception types.
- **FR-022**: The language shall support coroutines for handling asynchronous programming.
- **FR-023**: The language shall provide built-in support for multi-threading and synchronization primitives.
- **FR-024**: The language shall provide automatic memory management through garbage collection.
- **FR-025**: The language shall ensure memory safety with managed pointers.
- **FR-026**: The language shall have a built-in graphics library for 2D graphics, including drawing shapes, handling sprites, and managing animations.
- **FR-027**: The language shall provide a standard game loop - framework.
- **FR-028**: The language shall support built-in handling for keyboard, mouse, and game controller input.
- **FR-029**: The language shall support basic sound and music playback.
- **FR-030**: The language shall include a simple API for collision detection between game objects.
- **FR-031**: The language shall provide a basic 2D physics engine for realistic movement and interactions.
- **FR-032**: The language shall include a Read-Eval-Print Loop (REPL) for interactive programming.
- **FR-033**: The language shall have a comprehensive standard library with modules for common tasks such as file I/O, networking, and data structures.
- **FR-034**: The language shall provide a built-in package manager for managing dependencies and libraries.
- **FR-035**: The language shall support an integrated development environment (IDE) with features like syntax highlighting, code completion, debugging, and project management.
- **FR-036**: The language shall support both interpreted execution for rapid development and a compiler for optimized performance.
- **FR-037**: The language shall be cross-platform, supporting major operating systems.

### Nonfunctional Requirements

- **NFR-001**: The language shall be designed to execute efficiently, with optimizations for performance-critical applications such as game development.
- **NFR-002**: The language's garbage collection mechanism shall minimize pauses to ensure smooth execution of graphics and game applications.
- **NFR-003**: The language shall be easy to learn for beginners, with a gentle learning curve.
- **NFR-004**: The language’s syntax and features shall promote code readability and maintainability.
- **NFR-005**: The development environment shall provide helpful error messages and debugging tools to assist developers.
- **NFR-006**: The language shall ensure memory safety to prevent common programming errors such as null pointer dereferences and buffer overflows.
- **NFR-007**: The language shall provide robust error handling mechanisms to maintain application stability.
- **NFR-008**: The language shall have comprehensive documentation, including a language reference, tutorials, and example code.
- **NFR-009**: The language shall foster a strong community with forums, libraries, and frameworks to support developers.
- **NFR-010**: The language shall support the development of both small-scale and large-scale applications.
- **NFR-011**: The language and its runtime shall efficiently handle increasing workloads and larger code bases.
- **NFR-012**: The language shall provide mechanisms for interoperability with other languages and systems, allowing for integration with existing code bases and libraries.
- **NFR-013**: The language shall include features to help developers write secure code, such as safe handling of input and prevention of common vulnerabilities.
- **NFR-014**: The language shall be portable across different platforms, ensuring that code can be easily transferred and run on various operating systems without modification.

## Syntax and Semantics

### Basic Syntax

Code uses a syntax similar to C#, with some simplifications to enhance readability and ease of use.

### Data Types

- `Integer`: Represents whole numbers.
- `Float`: Represents floating-point numbers.
- `Boolean`: Represents true/false values.
- `Character`: Represents single characters.
- `String`: Represents sequences of characters.
- `Record`: Represents structured data.
- `Vector`: Represents 2D or 3D vectors.
- `UnitInterval`: Represents numbers in the range [0,1].
- `Color`: Represents colors.

### Variables and Constants

Variables are declared using the `let` keyword. Constants are declared using the `constant` keyword. Variables can be suffixed with `?` to denote the variable is nullable.

```code
let x = 10
constant PI = 3.14159
let y? = null
```

### Control Flow

- **If Statement**: Conditional execution of code blocks.
- **For Loop**: Iterative execution of code blocks.
- **Foreach Loop**: Iterative execution for each element within an iterable.
- **While Loop**: Repeated execution of code blocks based on a condition.
- **Do While Loop**: Executes the block once before checking the condition.
- **Break and Continue**: Control loop execution.
- **Match Statement**: Pattern matching for complex conditions.

```code
if x > 5 {
    // Do something
} else {
    // Do something else
}

for let i = 0; i < 10; i += 1 {
    // Loop body
}

while x < 10 {
    // Loop body
}

do {
    // Loop body
} while x < 10
```

### Functions

Functions are declared using the `function` keyword.

```code
function add(a, b) {
    return a + b
}
```

### Classes and Objects

Classes support encapsulation, inheritance, and polymorphism.

```code
class Person {
    public string name
    public integer age

    constructor(string name, integer age) {
        self.name = name
        self.age = age
    }

    public function greet() {
        println("Hello, my name is " + self.name)
    }
}

class Student extends Person {
    public integer grade

    constructor(string name, integer age, integer grade) {
        super(name, age)
        self.grade = grade
    }
}
```

### Operators

- Arithmetic: `+`, `-`, `*`, `/`
- Assignment: `=`
- Comparison: `==`, `!=`, `<`, `<=`, `>`, `>=`
- Logical: `&&`, `||`, `!`
- Compound Assignment: `+=`, `-=`, `*=`, `/=`
- Unary Negation: `-`

### Comments

- Single-line comments: `//` or `#`
- Multi-line comments: `/* ... */`
- Markdown comments: `/~~ ... ~~`

```code
// This is a single-line comment
# This is another single-line comment

/*
This is a
multi-line comment
*/

/~~
This is a markdown comment
~~/
```

### Literals

- **Integer**: A sequence of digits, with optional negative sign.
  - Examples: `42`, `-1`, `0`
- **Float**: A sequence of digits with a decimal point, with optional negative sign.
  - Examples: `3.14`, `-0.001`, `2.0`
- **Boolean**: `true` or `false`
- **Character**: A single character enclosed in single quotes.
  - Examples: `'a'`, `'1'`, `'\n'`
- **String**: A sequence of characters enclosed in double quotes.
  - Examples: `"Hello, World!"`, `"123"`, `"This is a string"`

## Standard Library

### Overview

The standard library provides a comprehensive set of functions and data structures to support common programming tasks.

### Console

Functions for input and output.

```code
Console.WriteLine("Hello, World!")
Console.ReadLine()
```

### Math

Common mathematical functions.

```code
let result = Math.sqrt(16)
let angle = Math.PI / 2
```

### Collections

Data structures like lists and dictionaries.

```code
let list = List()
list.add(1)
list.add(2)
list.remove(1)
```

### Utilities

Helper functions and utilities.

```code
let now = DateTime.now()
let guid = Guid.new()
```

## Language Implementation

### Lexer

The lexer is responsible for tokenizing the input source code. It converts a stream of characters into a stream of tokens.

### Parser

The parser converts the stream of tokens into an abstract syntax tree (AST), representing the hierarchical structure of the source code.

### AST (Abstract Syntax Tree)

The AST represents the syntactic structure of the source code. Each node in the tree corresponds to a construct occurring in the source code.

### Interpreter/Compiler

The interpreter or compiler traverses the AST to execute the program or generate machine code.

### Error Handling

Strategies for handling different types of errors:

- **Lexical Errors**: Detected during tokenization.
- **Syntax Errors**: Detected during parsing.
- **Runtime Errors**: Detected during execution.

## Use Cases

- **2D Game Development**: Rapidly prototype and develop 2D games.
- **Educational Projects**: Teach programming concepts with a simple and readable syntax.
- **Interactive Applications**: Create interactive applications with robust input/output support.
