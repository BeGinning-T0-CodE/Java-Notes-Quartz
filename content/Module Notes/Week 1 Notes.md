
# Week 1 code Walk-through

![](Pasted%20image%2020250616235041.png)

![](Pasted%20image%2020250616235514.png)

Running this java file using javac is going to create a byte-code file or something
![](Pasted%20image%2020250616235213.png)

![](Pasted%20image%2020250616235256.png)

![](Pasted%20image%2020250616235317.png)

Now we can run this byte-code file using JVM and then we'll see the output

![](Pasted%20image%2020250616235412.png)



> “If your Java environment has multiple versions installed or your classpath isn't set up correctly, you may run into runtime errors. Using `java -cp . ClassName` helps Java find your class in the current directory and avoid such issues.”
To not get that error you use this -cp . command

![](Pasted%20image%2020250616235646.png)

-cp stands for class path
. stands for current working directory




![](Pasted%20image%2020250617000151.png)

![](Pasted%20image%2020250617000242.png)

![](Pasted%20image%2020250617000413.png)
![](Pasted%20image%2020250617000559.png)

![](Pasted%20image%2020250617000707.png)
![](Pasted%20image%2020250617000807.png)

![](Pasted%20image%2020250617001051.png)
![](Pasted%20image%2020250617001129.png)
![](Pasted%20image%2020250617001142.png)

![](Pasted%20image%2020250617001407.png)
![](Pasted%20image%2020250617001441.png)
![](Pasted%20image%2020250617001538.png)

![](Pasted%20image%2020250617001621.png)![](Pasted%20image%2020250617001753.png)
![](Pasted%20image%2020250617001844.png)
![](Pasted%20image%2020250617001909.png)
![](Pasted%20image%2020250617002102.png)
![](Pasted%20image%2020250617002143.png)
![](Pasted%20image%2020250617002212.png)
![](Pasted%20image%2020250617002236.png)



### Dynamic vs. Static Typing


## From Notebook LM

Week 1 of the "Programming Concepts using Java" course provides a comprehensive introduction to fundamental programming concepts, setting the stage for understanding Java in particular. The lectures cover a wide range of topics, from the basic definition of programming languages to advanced concepts in object-oriented design and memory management.

Here's a breakdown of what Week 1 is about:

- **Introduction to Programming Languages**
    
    - A programming language is defined as a medium for communicating computational instructions.
    - Initially, programming languages were directly connected to computer architecture, involving direct manipulation of memory locations and registers, which was described as tedious and error-prone.
    - The evolution of languages introduced **abstraction** to match computational thinking, incorporating ideas like assigning values to named variables, conditional execution, iteration, functions (including recursion), and aggregate data structures such as arrays, lists, and dictionaries.
    - The concept of **compilers and interpreters** is introduced as tools that translate "high-level" programming languages into "low-level" machine language, enabling expressiveness at the cost of some fine-grained control over hardware mapping, though this often leads to fewer errors.
- **Styles of Programming: Imperative vs. Declarative**
    
    - **Imperative programming** focuses on "how to compute," providing step-by-step instructions on what needs to be done, often using intermediate variables and explicit iteration. Examples include Python functions `sumlist` and `sumsquareeven` where computations are clearly step-by-step.
    - **Declarative programming** focuses on "what the computation should produce," often exploiting inductive structure and typically avoiding intermediate variables, sometimes through a combination of small transformations (functional programming). This style can help identify natural units of reusable code.
- **The Role of Types**
    
    - Types are essential for **interpreting binary data** stored in memory consistently, viewing bit sequences as integers, floats, or characters, and defining allowed values and operations.
    - Types also help in **naming concepts and structuring computation** at a higher level, making code more transparent, readable, and easier to maintain (e.g., `Point` vs. `(Float,Float)`, banking application types).
    - A significant advantage of types is **catching bugs early** (e.g., incorrect expression evaluation or assignment), analogous to dimension mismatch in science.
    - The distinction between **Dynamic Typing** (type determined at runtime by current value, like Python) and **Static Typing** (type associated in advance, like Java/C/C++) is discussed. Static typing aids **static analysis**, allowing compilers to detect type errors at compile-time, saving cost and effort, and enabling optimisations. The **Halting Problem** is mentioned as a fundamental limitation on compiler correctness checking.
- **Memory Management**
    
    - This section explains how variables are stored during program execution, differentiating between their **scope** (when a variable is available for use) and **lifetime** (how long the storage remains allocated). A "hole in scope" scenario is described where storage is alive but not accessible.
    - The **memory stack** is introduced as the mechanism for managing local variables of functions, using **activation records** that are pushed on function call and popped on exit. Control and return value links are explained for stack navigation and result storage.
    - **Passing arguments to functions** is detailed, including **call by value** (copying the value) and **call by reference** (parameter points to same location as argument, enabling side-effects).
    - The **heap** is presented as a separate storage area for dynamically created data that needs to persist after a function exits (e.g., nodes in a linked list), conceptually allocated from the "opposite" end of memory from the stack.
    - Methods for **managing heap storage** are discussed: **manual memory management** (e.g., `malloc`/`free` in C, prone to memory leaks and invalid assignments) versus **automatic garbage collection** (e.g., Java, Python, which check and clean up dead storage like mark-and-sweep, offering convenience at the cost of potential performance penalties).
- **Abstraction and Modularity**
    
    - **Stepwise refinement** is introduced as a top-down approach to solving complex tasks by breaking them into manageable subtasks, which can be coded by different people.
    - **Data refinement** is highlighted, where changes in data representation can have cascading impacts on functions that operate on that data (e.g., banking application needing transaction history).
    - **Modular software development** involves defining components with clear **interfaces** (what's visible) and **specifications** (behaviour). This allows building prototypes, validating designs, and improving components independently while preserving their interface and specification.
    - Programming languages support abstraction through **control abstraction** (functions/procedures) and **data abstraction** (Abstract Data Types - ADTs), where internal representation is hidden behind a public interface.
- **Object-Oriented Programming (OOP) Concepts, Classes, and Objects**
    
    - **Objects** are presented as similar to abstract data types, encapsulating hidden data with public operations (methods/messages). They provide a uniform way to combine data and functionality, ranging from simple counters to entire file systems.
    - The **history of OOP** traces back to Simula in the 1960s, a simulation language that introduced objects to handle event-based simulations with diverse event types and generic simulation operations.
    - Key distinguishing features of OOP are:
        - **Abstraction**: Public interface, private implementation.
        - **Subtyping**: Arranging types in a hierarchy where a subtype is a specialization that can be used wherever its parent type is needed, ensuring interface compatibility.
        - **Dynamic Lookup**: How a method acts (its implementation) is determined at runtime based on the object's actual type, not just its declared static type. This differs from static overloading.
        - **Inheritance**: Reusing implementations from parent types (e.g., Manager inheriting from Employee). The philosophical difference between subtyping (interface relationship) and inheritance (implementation relationship) is highlighted using the Deque/Stack/Queue example.
    - **Classes** are defined as templates for abstract data types, specifying how data is stored (instance variables) and how public functions manipulate that data, while **objects** are concrete instances of these templates.
    - **Constructors** are special functions (e.g., `__init__` in Python) implicitly called to set up instance variables when an object is created.
    - Examples with Python's `Point` class demonstrate adding methods (`translate`, `odistance`) and changing internal implementation (Cartesian to Polar coordinates) while maintaining the public interface.
    - **Python's limitations** in enforcing abstraction are discussed, specifically its allowance of direct access to instance variables (breaking abstraction) and potential inconsistencies in subtyping/inheritance due to a lack of privacy mechanisms or strong type declarations. This highlights the need for **strong declarations** (type and visibility) to enforce privacy and enable static type checking.
- **Course Focus**
    
    - The course will **explore these concepts using Java as the illustrative language**. Java is described as an imperative, object-oriented language that incorporates most features of interest. The course will also discuss design decisions and compromises made in programming languages to help understand why many languages exist and new ones are still being created. Additional topics to be covered include exception handling, concurrency, and event-driven programming.
