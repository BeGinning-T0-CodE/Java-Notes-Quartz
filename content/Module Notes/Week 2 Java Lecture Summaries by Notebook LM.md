Week 2 Lecture 1

Here is a bullet-point summary of the lecture on Java:

- **Introduction to "Hello World" Programs**
    
    - The "Hello World" program, popularised by Kernighan and Ritchie for the C language, is an iconic starting point for learning a new programming language.
    - Successfully writing, saving, compiling, and running "Hello World" signifies overcoming the first major hurdle in programming mechanics.
    - It serves as a symbolic challenge to gauge the ease or difficulty of programming in a given language.
- **"Hello World" Comparison: Python vs. C vs. Java**
    
    - **Python:** The simplest "Hello World" program is a single `print` statement, making it very attractive for beginners due to its low syntactic barrier.
    - **C:** More complicated, requiring the inclusion of the standard input/output library (`#include <stdio.h>`), the definition of a `main` function, using `printf`, and explicitly adding a newline character (`\n`).
    - **Java:** Appears "quite scary" initially, with the `print` statement (`System.out.println("hello world")`) being buried inside a function definition, which is further enclosed within a class.
- **Deconstructing Java's "Hello World" Program Syntax**
    
    - **Class Definition:**
        - Java is designed as a bottom-up object-oriented programming language, where functions are defined in the context of objects, not as free-floating entities.
        - Therefore, every function in Java must reside inside a class.
        - The class must be declared `public` to allow the function inside it to be executed from outside.
    - **`main` Function:**
        - Unlike Python, where code can be executed statement by statement from top to bottom, C and Java require all executable code to be within a function.
        - A convention is needed to specify where execution begins; C established the `main` function for this purpose, which Java inherits.
    - **`main` Function Signature (`public static void main(String[] args)`):**
        - `void`: Indicates that the `main` function does not return any value, similar to Python's `None` type for values that do not exist.
        - `String[] args`: Allows command-line arguments to be passed to the program as an array of strings.
        - `public`: The `main` function must be `public` so it can be executed from outside the class.
        - `static`: This modifier is crucial because `main` is the program's starting point, and no object exists yet to invoke it. `static` allows the function to be called without creating an instance (object) of its class, similar to standalone functions in Python or mathematical functions in libraries.
    - **`System.out.println("hello world")` Breakdown:**
        - The `print` statement must live within a class; in this case, it's part of the `System` class.
        - `System.out`: `out` is a `static` stream object (like a pipe to the screen) within the `System` class, to which data is written.
        - `println` vs. `print`: Java offers `println` which automatically adds a newline character after printing, and `print` which does not (contrasting with Python's default newline or C's explicit `\n`).
    - **Punctuation and Code Blocks:**
        - Unlike Python, which uses colons and indentation to define code blocks, Java (and most other languages) use explicit opening and closing braces (`{}`) to delimit blocks of code for classes, functions, loops, or conditional statements.
        - Every statement in Java must end with a semicolon (`;`).
        - Indentation and new lines in Java are for readability and style; they are not syntactically enforced by the compiler, unlike in Python where layout is crucial. This design choice aims to prevent subtle bugs related to inconsistent indentation.
- **Java Execution Model and Portability**
    
    - A Java program is a collection of classes, and each class must be stored in a separate `.java` file whose name exactly matches the class name.
    - **"Write Once, Run Anywhere" (Portability):**
        - Unlike C or C++, which compile code for specific machine architectures, Java compiles code into **bytecode** for an abstract **Java Virtual Machine (JVM)**.
        - The JVM is then implemented for different operating systems and hardware architectures, providing a uniform execution environment and consistent behaviour regardless of the underlying machine.
        - This portability was a key selling point, especially with the rise of the internet.
    - **Compilation and Execution Steps:**
        - The `javac` compiler translates `.java` source files into bytecode, which is stored in `.class` files (e.g., `HelloWorld.class`). The `.class` extension merely indicates bytecode and is unrelated to the object-oriented concept of a class.
        - The `java` interpreter runs these `.class` bytecode files on the JVM.
        - When using `javac`, the file extension (`.java`) must be provided (e.g., `javac helloworld.java`), but when using `java`, the `.class` extension is omitted (e.g., `java helloworld`).
        - The `javac` compiler is smart enough to automatically follow dependencies between classes and compile all necessary `.java` files, so a programmer only needs to explicitly compile the class containing the `main` function.
- **Reasons for Java's Verbose Syntax ("Baggage")**
    
    - The perceived "heaviness" of Java's syntax is a direct result of its core design principles.
    - It is a purely object-oriented language that strictly enforces the distinction between public interfaces and private implementations.
    - Java aims to ensure disciplined programming through compiler enforcement rather than relying solely on programmer discipline, necessitating modifiers like `public`, `private`, and `static`.
    - It requires explicit declaration of functions and variables in advance, which helps prevent programmer mistakes and aids the compiler in managing storage and values.
    - Its design prioritises code portability through the JVM and bytecode, allowing code to run consistently across various architectures.

