# CS Notes

# Programming

**Memory** The location where instructions and data are stored on the computer

**Algorithm** A sequence of steps that can be followed to complete a task. The sequence must always terminate

**Syntax** The rules of how words are used within a given language

**Memory address** A specific location in memory where instructions or data are stored

**Pointer** A data item that identifies a particular element in a data structure

**Array** A set of related items stored under a single identifier

**Element** A single item within a set or list

**Record** A single line of a text file

**Subroutine/Procedure/Subprogram/Routine** A name block of code designed to carry out a specific task

**Function** A subroutine that returns a value

**Exception handling** The process of dealing with events that cause the current subroutine to stop

**Procedural programming languages** Languages where the programmer specifies the steps that must be carried out in order to achieve a result

**Imperative programming languages** Languages based on giving the computer commands or procedures to follow

**Hierarchy chart** A diagram that shows the design of a system from the top down

**Structure chart** Similar to a hierarchy chart with the addition of showing how data is passed around the system

**Top-down approach** A design process in which you start at the top of the process and work down into smaller and smaller sub-processes

**Modular design** A method of system design that breaks a whole system down into smaller units, or modules

## Encapsulation

Encapsulation is the concept of keeping the data and code within the same object.

**Method** The code or routines contained within a class

**Properties** The defining features of an object or a class in terms of its data

A class defines properties, methods and how they will behave.
An object is an instance of a class, containing its methods and the data defined in the class.

## Inheritance

**Inheritance** The concept that properties and methods in one class can be shared with a subclass

### Class diagrams for inheritance

**Class diagrams** A way of representing the relationship between classes

Class diagrams are hierarchical in structure, with the base class at the top and sub-classes beneath.
- The subclass inherits the properties and method of the base class
- Arrows are used to show the direction of inheritance
- Each class is represented with a box made up of three sections to include the class name, properties, and methods

## Instantiation

**Instantiation** The process of creating an object from a class.

## Polymorphism and overriding

**Polymorphism** The ability of different types of data to be manipulated with the same method

Polymorphism allows a method to be redefined, overridden, to work with the changes made to the sub-class.

## Abstract, virtual, and static methods

Static methods can be used without an instance of the class being instantiated

Virtual methods are defined in the base class but can be overridden by the method in the sub-class where it is used.

Abstract methods are not supplied in the base class, but must be provided in the subclass

## Aggregation

Aggregation is a method of creating new objects that contain existing object, based on the way in which objects are related.

All of the objects exist in their own right, but their is a relationship between them.

## Composition aggregation

**Composition aggregation** Creating an object that contains objects, and will cease to exist if the containing object is destroyed

## Association aggregation

**Association aggregation** Creating an object that contains other objects, which can continue to exist even if the containing object is destroyed

## Design principles

- **Encapsulate what varies**: Properties and methods are subdivided into as many classes as needed to reflect the real-life scenario

- **Favour composition over inheritance**: This refers to the way in which classes and objects are instantiated. Composition is less error prone and enables simpler maintenance

- **Program to interfaces, not implementation**:Interface methods are widely used. When a class is created that adheres to the methods in the interface, it can be seen as an implementation of the interface. Programs can be written based on interfaces rather than each individual implementation of a class. If a class needs to be amended, this can be done with reference to the interface, meaning that there will be little or no impact on the other classes in the program

# Data structures

## Data structures and abstract data types

**Data structure** A common format for storing large volumes of related data, which is an implementation of an abstract data type

**Abstract data type** A conceptual model of how data can be stored and the operations can be carried out on the data

**File** A collection of related data

### Binary files

Binary files contain binary codes and usually some header information

### Static and dynamic data structures

**Static data structure** A method of storing data where the amount of data stored is fixed

**Dynamic data structure** A method of storing data where the amount of data stored will vary as the program is being run

**Heap** A pool of unused memory that can be allocated to a dynamic data structure

**Stack** A data structure where the last item added is the first item removed

**Queue** A data structure where the last item added is the first item removed

| Static | Dynamic |
| --- | --- |
| Inefficient as memory is allocated that may not be needed | Efficient as the amount of memory varies as needed |
| Fast access to each item of data as the memory location is fixed when the program is written | Slower access as the memory location is allocated at run-time |
| Memory addresses allocated will be contiguous so quicker to access | Memory addresses allocated may be fragmented, resulting in slower access |
| Structures are a fixed size, making them more predictable to work with | Structures vary in size so there needs to be a mechanism for knowing the size of the current structure |
The relationship between different elements of data does not change | The relationship between different elements of data will change as the program is run |


## Stacks and queues

### Stacks

**Stack** A last in first out structure

The stack pointer stores where the stop of the stack is.

#### Pushing to a stack

``` python
if stack_pointer < stack.size:
    stack_pointer += 1
    stack_array[stack_pointer] = data_item
else:
    error("Stack full")
```

#### Popping from the stack

``` python 
if stack_pointer > 0:
    data_item = stack_array[stack_pointer]
    stack_pointer -= 1
else:
    error("The stack is empty")
```

#### Stack frames

**Stack frame** A collection of data about a subroutine call

**Call stack** A type of stack used to store information about active subroutines and functions within a program

**Interrupt** A signal sent by a device or program to the processor requesting its attention

**Recursion** The process of a subroutine calling itself

### Queues

**Queue** A first in first out structure

**Linear queue** A first in first out structure organised as a line of data

**Circular queue** A first in first out structure implemented as a ring where the front and rear pointers can wrap around from the end to the start of the array

**Priority queue** A variant of a first in first out structure where some data types may leave out of sequence if they have a higher priority than other data items

## Graphs and trees

**Graph** A mathematical structure that models the relationship between pairs of objects

**Graph theory** The underlying mathematical principles behind the use of graphs

**Arc** A join or relationship between two nodes, also known as an edge

**Vertex/Vertices** An object in a graph, also known as a node

**Weighted graph** A graph that has a data value labelled on each edge

**Undirected graph** A graph when the relationship between the vertices is two way 

**Directed graph** A graph when the relationship between the vertices is one way

**Latency** The time delay that occurs when transmitting data between devices

### Adjacency lists and matrices

**Adjacency list** A data structure that stores a list of nodes with their adjacent values

A weighted graph may be stored in an adjacency list by writing each adjacency of a pair of the adjacent node and the weight of the edge

**Adjacency matrix** A data structure set up as a two dimensional array that shows whether there is an edge between each node

| Adjacency list | Adjacency matrix |
| --- | --- |
| Only stores data where there is an edge, requiring less memory | Stores a value for every combination, requiring more memory |
| The list must be parsed to identify whether particular adjacencies exist | Adjacencies can be identified more quickly as every combination is stored |
| Where there are not many edges, a sparse graph, this method would be more suitable | Where there are many edges, a dense graph, this method would be more suitable

### Trees

**Tree** A data structure similar to a graph, containing no loops

**Node** An object in a graph

**Edge** A join of relationship between nodes

**Root** The starting node in a rooted data structure from which all other nodes branch off

**Parent** A type of node in a tree, where there are further nodes below it

**Leaf** A node that does not have any other nodes beneath it

#### Binary search tree

**Binary search tree** A tree where each node can only have up to two child nodes attached to it

##### Binary tree implementation

This implementation uses three arrays:
- The first stores the data
- The second stores the left pointers
- The right stores the right pointers

## Hash tables and dictionaries

**Hash table** A data structure that stores key value pairs based on an index calculated from an algorithm

### Hash tables

**Hashing algorithm** An algorithm that creates a unique index from given items of key data

**Cache** A high speed temporary area of memory

Features and problems for a hashing algorithm:
- Numeric value needs to be generated from the data to perform the calculation
- Unique indices must be generated. Non-unique indices are collisions which must be coped with
- The indices must be uniformly distributed to avoid clustering
- The algorithm must be capable of producing the necessary number of unique indices
- The algorithm must balance efficiency and complexity

**Collision** When a hashing algorithm produces the same index for two or more different keys

**Clustering** When a hashing algorithm produces indices that are not randomly distributed

**Load factor** The ratio of the number of indices available to how many there are in total

**Index** The location where values will be stored, calculated from the key

**Chaining** A technique for generating a unique index when there is a collision by adding the key value to a list stored at the same index

**Rehashing** The process of running the hashing algorithm again when a collision occurs

### Dictionaries

**Dictionary** A data structure that maps keys to data

**Associative array** A two dimensional structure containing key value pairs of data


## Vectors

Vectors can be represented as values stored in a list.

Vectors can also be represented as a function.
A function maps an input to an output.
F:S -> R
F is the function that creates the vector
S is the complete set of values that the function can be applied to 
R is the potential outputs of the function

**Magnitude** The size of the vector
**Direction** The direction of the vector
**Components** The values within a vector

### Vector addition

Vectors are added by adding the respective components of the vectors

### Scalar vector multiplication

**Scalar** A real value used to multiply a vector to scale the vector

### Dot product

**Dot product** The process of combining two vectors to calculate a single number.

A.B = A<sub>x</sub>B<sub>x</sub>+ A<sub>y</sub>B<sub>y</sub>

### Convex combinations

**Convex hull** A spatial representation of the vector space between two vectors

**Convex combination** A method of multiplying vectors that produces a resulting vector within the convex hull

**Vector space** A collection of elements that can be formed by adding or multiplying vectors together

Performing a convex combination is either multiplying one vector by either a scalar or another vector

D = αAB + βAC

Where AB and AC are the two vectors.

α and β represent the real numbers that each vector will be multiplied by.

α and β must both be greater than or equal to 0, and αβ must equal 1. D will then fall within the vector space.
*Surely if either is 0, then αβ != 1?*

### Uses of the dot product

Given two vectors u and v, it is possible to generate parity using bitwise AND and XOR operations.

Where u = [1,1,1,1] and v = [1,0,1,1], the dot product would be u.v = 1.
This is calculated by performing arithmetic over GF(2) where GF has two elements 0 and 1.
This calculation finds the parity bit for even t parity.
The first vector will always be [1,1,1,1].

uv. = [1,1,1,1].[1,0,1,1] 
    = 1 AND 1 XOR 1 AND 0 XOR 1 AND 1 XOR 1 AND 1
    = 1 XOR 0 XOR 1 XOR 1
    = 1
    
Arithmetic over GF(2) can be summarised in two small tables.
Multiplication can be achieved by the bitwise AND operation, and addition can be achieved by the bitwise XOR operation.


# Algorithms

## Graph and tree traversal

**Implementation** Creating code to produce a programmed solution

**Depth first** A method for traversing a graph that starts at a chosen node and explores as far as possible along each branch away from the starting node before backtracking

**Breadth first** A method for traversing a graph that explores nodes closest to the starting node first before progressively exploring nodes that are further away

Method for depth first traversal

| Explanation | Current node | Visited nodes  |
| --- | --- | --- |
| Selected the node to start [A] | A | |
| Mark node a as visited. Choose a node that is connected to A [B] and recursively call the search routine to explore this node | A | A |
| Mark Node B as visited. Choose a node that is connected to B and has not been visited [C] (recurse) | B | A, B |
| As above with C. Choosing D | C | A, B, C |
| As above with D. Choosing E | D | A, B, C, D |
| Mark node E as visited. All connecting nodes have been visited, so unwind recursion. There are no nodes left to visit so terminate | E | A, B, C, D, E |

In pseudocode

``` python 
def traverse(node n):
    visited.add(n)
    # Do something with the node
    for node in n.neighbours:
        if node not in visited:
            traverse(n)
```

Method for breadth first traversal

| Explanation | Contents of queue |
| --- | --- |
| Add the initial node to the queue | A |
| Add all adjacent nodes which are not already fully explored to the queue | A, B |
| Remove A from the queue as it is fully explored | B |
| Add all nodes that are adjacent to B and not already fully explored to the queue | B, C, E |
| Remove B from the queue as fully explored | C, E |
| Add all the nodes that are adjacent to C and not already fully explored to the queue | C, E, D |
| Remove C from the queue as it is already fully explored | E, D |
| Add all nodes that are adjacent to E and not already fully explored to the queue | E, D |
| Remove E from the queue as fully explored | D |
| Remove D from the queue as fully explored. Terminate as queue empty | |

*Book says remove E and then shows the queue as containing only E*

**Binary tree** A structure where each node can only have up to two child nodes attached to it

**Pre-order** A method of traversing a tree by visiting the root, traversing the left subtree, and traversing the right subtree

**In-order** A method of traversing a tree by traversing the left subtree, visiting the root, and traversing the right subtree

**Post-order** A method of traversing a tree by traversing the left subtree, traversing the right subtree, and visiting the root

**Traversal** The process of reading data from a tree or graph by visiting all of the nodes

**Binary search** A technique for searching sorted data that splits the dataset in half repeatedly until the search data is found

## Dijkstra's shortest path algorithm

**Single source** The shortest path is calculated from a single starting point

## Reverse Polish notation

**Infix** Expressions written with operators within operands

**Polish/Prefix notation** Expressions with operators before operands

**Reverse Polish/Postfix notation** Expressions with operators after operands

### Evaluating postfix expressions

- Create a stack
- For each element:
    - If the element is an operand, push it onto the stack
    - If the element is an operator, pop twice to get A and B respectively. Calculate B O A and push it to the stack

Example 4 3 * 6 2 * /

| Step | Stack |
| --- | --- |
| Push 4 | 4 |
| Push 3 | 4, 3 |
| Evaluate 4 * 3 | 12 | 
| Push 6 | 12, 6 |
| Push 2 | 12, 6, 2 |
| Evaluate 6 * 2 | 12, 12 |
| Evaluate 12 / 12 | 1 |

**In order traversal** A method of extracting data from a binary tree that will result in an infix expression

**Post-order traversal** A method of extracting data from a binary tree that will result in postfix expressions

**Pre-order traversal** A method of extracting data from a binary tree that will result in prefix expressions

### Conversion of infix to postfix

- Create an empty stack for keeping op

### Applications of postfix

Some languages are specifically designed to be stack-oriented and would therefore be ideally suited to this application.
In these cases, the interpreter or compiler checks all of the syntax with reference to the postfix notation of each expression.

## Sorting algorithms

### Bubble sort

**Bubble sort** A technique for putting data in order by repeatedly stepping through an array, comparing adjacent elements and swapping them if necessary until the array is in order

1. Iterate through each element
    1. Iterate through each element
    2. If the outer element is greater, swap them 
2. When no swap is made in inner loop break

In each iteration, the largest element will be moved to the end.

Enhanced bubble sort decreases the size of the inner loop by 1 each time, as the last element is now correct.

### Merge sort

**Merge sort** A technique for putting data in order by splitting lists into single elements and then merging them back together

#### Splitting procedure

Split the array into halves, and repeat on each sub-array until the arrays can no longer be divided into integer parts.

#### Merging procedure

Assume that the lists to be merged are already sorted

Compare the first element of each list, adding the new number to the merged list.
Repeat the process, comparing the first element in each list and placing the lowest item in the merged list

# Computational thinking

## Abstraction and automation

**Problem solving** The process of finding a solution to real-life problems

**Automation** Creating a computer model of a real-life situation and putting it into action

**Logical reasoning** The process of using a given set of facts to determine whether new facts are true or false

*a fact is "a thing that is known or proved to be true." so the definition above is crap*

### Abstraction

The concept of abstraction is to reduce problems to their essential features.
This allows a problem to be viewed from a high level, concentrating on the key aspects of designing a solution whilst ignoring the detail.

Once a solution has been identified for the current problem, a feature of abstraction is that the abstraction from one problem can be applied to another similar problem which shares the same common features.

#### Representational abstraction

**Representational abstraction** The process of removing unnecessary details so that only information that is required to solve the problem remains

This is the process of removing unnecessary details until it is possible to represent the problem in a way that can be solved.

#### Abstraction by generalisation or categorisation

**Abstraction by generalisation or categorisation** The concept of reducing problems by putting similar aspects of a problem into hierarchical categories


This process involves identifying common characteristics of representations so that more general representations can be developed.

**Procedural abstraction** The concept that all solutions can be broken down into a series of procedures or subroutines

At the design stage it is sufficient for the programmer to work out what each procedure will do without defining how it will do it.
The procedure may in turn call other procedures although it does not need to know how these work in order to call them.
This is the basis for top down design.
Other considerations include what event will trigger the procedure, how procedures will link together, including any possible side effects, and how errors will be handled.

**Functional abstraction** Breaking down a complex problem into a series of reusable functions

Similar to procedural abstraction, functional abstraction focuses on common functions that can be used to solve problems.
Functions are a feature of procedural languages. Functions can be created for any common procedure and functions can be built on top of other functions producing higher levels of abstraction.
All the program needs is for the parameters to be input into the function in order to generate a result.
Using functions reduces complexity as the function only needs to be written once.

**Problem abstraction** The process of reducing a problem down to its simplest components until the underlying processing requirements that solve the problem are identified

For example, satnavs use vectors and a variation of Dijkstra's algorithm, neither of which were developed specifically for the satnav, but both of which have been adopted to create the required solution.

**Data abstraction** Hiding how data is represented so that it is easier to build a new kind of data object (e.g. building a stack from an array)

#### Information hiding

**Information hiding** The process of hiding all details of an object that do not contribute to its essential characteristics

An example is where a GUI is used.
The complexity of the calculations used to generate the displayed information is hidden. If the method of route calculation was changed, it would not necessarily affect the interface. Information hiding separates the user interface from the actual implementation of the program.


#### Composition and decomposition

**Composition** Building up a whole system from smaller units

**Decomposition** Breaking down a large task into a series of subtasks

## Finite state machines

**Finite state machine** Any device that stores its current status and whose status can change as the result of an input

### State transition diagrams

**State transition diagram** A visual representation of a finite state machine using circles and algorithms

**Accepting state** The state that identifies whether an input has been accepted

**State transition table** A tabular representation of a finite state machine, showing inputs, current state, and next state

### Finite state machines with outputs

**Mealy machine** A finite state machine which outputs data

**Shift cipher** A simple substitution cipher where the letters are coded by moving a certain amount forwards or backwards in the alphabet

## Turing machines

**Turing machine** A theoretical model of computation

A Turing machine has an infinitely long tape divided into cells, as well as a read write head 

- Each cell contains a symbol, which can be blank
- The read write head can either read what is in the cell or write into the cell. It can also erase the current contents of the cell
- The tape can move left or right one cell at a time so that every cell is accessible by the read write head
- The machine can halt at any point if it enters a halting state or the entire input has been processed

Turing machines require:
- A start state
- A halting state
- An alphabet that lists acceptable symbols
- A transition function indicating what should be written at each cell and whether to move left or right based on the input read

### Universal Turing machine

**Universal Turing machine** A machine that can simulate a Turing machine by reading a description of the machin along with the input of its own tape

Rather than defining each individual process within a single machine, the universal machine takes two inputs:
- A description of all the individual Turing machines required to perform the calculations
- All the inputs required for the calculations

## Regular and context free languages

**Regular expression** Notation that contains a string of characters that can be matched to the contents of a set

| Regular expression | Meaning | Strings produced |
| --- | --- | --- |
| `a|b|c` | a or b or c | a, b, c |
| `abc` | a and b and c | abc |
| `a*bc` | zero or more a followed by b and c | bc, abc, aabc, aaabc |
| `(a|b)c` | a or b and c | ac, bc |
| `a+bc` | one or more a and b and c | abc, aabc, aaabc |
| `ab?c` | a and either zero or one b and c | ac, abc | 

### Searching strings

| Expression | Definition | Example |
| --- | --- | --- |
| `.` | Any character | .ole would match mole, hole, ect |
| `[]` | Matches to a single character within the brackets | `[mh]ole` would match to mole and hole, but not vole |
| `[^]` | Matches to any character except those in the brackets | `[^m]ole` would match to hole and vole, but not mole |
| `*` | Matches the preceding characters zero or more times | `m*ole` would match ole, mole, mmole etc | 

### Context free languages

**Context free language** An unambiguous way of describing the syntax of a language useful where the language is complex

Regular expressions map directly to state transition diagrams.
However, there are situations where the grammar used within a language is too complex to be defined by regular expressions.

the key problem with regular expressions is that they only work when matching or counting other symbols in a string where there is a finite limit.

Consider a binary palindrome. It is not possible to create a regular expression that describes the syntax as there is no regular expression that can describe how each letter is used.

When the counting and matching is infinite, a context free language is needed.
Context free languages can also support notation for recursion and are sometimes a clearer way of defining syntax even where regular expressions can be used.

### Backus-Naur form (BNF)

**Backus-Naur Form** A form of notation for describing the syntax used by a programming language

BNF produces a set of acceptable strings, which effectively describe the rules of the language.
It uses a set of rules that define the language in the format:

```
<S> ::= <alternative1> | <alternative2> | <alternative3>

<alternative1> ::= <alternative2> | <alternative4> 

<alternative4> ::= terminal
```

BNF works by replacing the symbol on the left with the symbols on the right until the string is defined.
The idea is to keep going until you reach a terminal, which is a rule that cannot be broken down any further.

In the example above:
- Each symbol or element is enclosed within chevrons
- The `::=` symbol means 'is replace with' and defines the rule for the symbol
- Each symbol needs to be split down further until you reach a terminal 

To define integers a BNF expression may look like this:

```
<integer> ::= <digit> | <digit> <integer>
<digit> :: = 0|1|2|3|4|5|6|7|8|9
```

This defines an integer as either a digit or a digit followed by another integer.
A digit is defined as the number 0 to 9 and this is a terminal as there is no further rule needed to define digits.

This expression would be recursive as the integer is defined in terms of itself.

Consider customer details held in a database:

```
<customerdetails> ::= <name> <address>
<name> ::= <title> <firstname> <lastname>
<address> ::= <housenumber> <streetname> <town> <country> <postcode>
...
<housenumber> ::= <integer>
// integer as above
```

This shows how BNF can produce simple rules which can be written as:
- Customer dtails must be made up of name and address
- Name must be made up of title, first name, and last name
- Address must be made up of house number, street name, town, country, and postcode
- House number must be made up of an integer

This is only a partial BNF definition and could be continued to further split down the name into a series of acceptable characters, or the postcode into a series of letters and numbers.

### Syntax diagrams

BNF expressions, or any kind of context free language, can be represented as a syntax diagram.

- An oval shape represents a terminal element
- A rectangular shape represents a non-terminal element and will therefore have another syntax diagram that breaks it down into more detail
- A rectangular shape with an arrowed path around it represents a non-terminal element that may be used more than once

**Syntax diagram** A method of visualising rules written in a context-free language

Syntax diagrams are modular so there are likely to be many syntax diagrams required to represent a whole language.
Each has an entry point and exit point to identify the start and end of each particular part.

## Maths for regular expressions

### Sets

A set is a collection of unordered values where each value appears only once in the set.
The values in the set are sometimes referred to as elements, objects, or members.

$\mathbb{N} = \{0, 1, 2, 3, 4, 5, ...\} \text{ The natural numbers}$

$\mathbb{Z} = \{..., -3, -2, -1, 0, 1, 2, 3, ..,\} \text{ The integers}$

**Natural number** A positive integer including zero

**Set building** The process of creating sets by describing them using notation rather than listing the elements

$A = \{x | x \in \mathbb{N} \land x \geq 1\}$

- $A$ is the name of the sets
- The braces $\{\}$ represent the contents of the set
- $x$ represents the actual values of the set, defined after the pipe $|$
- The pipe means such, meaning that the equation after defines the values of $x$
- $\in$ means "is a member of"
- $\mathbb{N}$ is the natural numbers
- $\land$ means "and"
- $x \geq 1$ means that $x$ must satisfy this inequality to be part of the set

**Member** A value or element that belongs to a set

#### The binary set

The binary set is usually denoted $\Sigma = \{0, 1\}$

This shows that the elements of the set of binary values are $0$ or $1$.
to build a set of all binary strings containing two bits, you would use $\Sigma^2$ where the ${}^2$ indicates two bits.

$\Sigma^2 = \{00, 01, 01, 10, 11\}$

In some cases the number of elements may be infinite.

$A = \{0^n 1^n | n \geq 1 \}$ would produce the set $\{01, 0011, 000111, ... \}$ representing all binary strings with an equal number of 0s and 1s, with the 0s preceding the 1s.

#### Representing a set in a programming language

Many programming languages have built in set-building routines.

- In Python `a = set([0, 1, 2, 3])` produces a set, as does `a = set(x**2 for x in [1, 2, 3])`
- In Haskell `[0..100]` produces a list containing the values 0 to 100, and `[x*2 | x <- [0..100]]` produces a list of the doubles of these numbers
- In C# `IEnumerable<int> numbers = Enumerable.Range(0, 9)` produces the integers 0 to 9. `var events = from num in numbers where num%2 == 0 select num;` would then extract the even numbers

#### The empty set

The empty set is represented as either $\{\}$ or $\emptyset$

**Empty set** The set that contains no values

#### Finite and infinite sets

When a set is finite, it has cardinality which means that it can be counted using natural numbers.
It can also be referred to as a countable set.

The cardinality of the set is the number of elements in the set.

**Countably infinite set** Sets where the elements can be put into a one-to-one correspondence with the set of natural numbers

**Cartesian product $A\times B$** Combining the elements of two or more sets to create a set of ordered pairs

**Union $A\cup B$** When two sets are joined and all of the elements of both sets are included in the joined set

**Intersection $A\cap B$** Describes which elements are common to both sets when the two sets are joined

**Difference $A\ominus B$ or $A \Delta B$** Describes which elements differ when two sets are joined together

#### Subsets

Where all the elements of one set are also contained within another set, it is said to be a subset. 

**Subset**  set where the elements of one are entirely contained within the other. This can include two sets that are exactly the same

**Proper subset** Where one st is wholly contained within another and the other set has additional elements

## Big O notation and classification of algorithms

### Functions

**Function** Relates each element of a set with the element of another set

**Domain** All the values that may be input to a mathematical function

**Codomain** All the values that may be output from a mathematical function

### Big O notation

This notation is used to classify the time and space complexity of an algorithm.
It considers the worst-case scenario.

**Constant time** Where the time taken to run an algorithm does not vary with the input size

**Linear time** When the time taken to run an algorithm increases in direct proportion with the input size

**Exponential time** When the time taken to run an algorithm increases as an exponential function of the number of inputs

**Logarithmic time** Where the time taken to run an algorithm increases or decreases in line with a logarithm

### Tractable and intractable problems

**Tractable problem** A problem that can be solved in an acceptable amount of time

**Intractable problem** A problem that cannot be solved in an acceptable time frame

**Heuristic** A method for producing a 'rule of thumb' to produce an acceptable solution to intractable problems

### Unsolvable problems

**Unsolvable problem** a problem that it has been proved cannot be solved on a computer

**Halting problem** An example of an unsolvable problem where it is impossible to write a program that can work out whether another problem will halt given a particular input


# Data representation

## Number systems


**Natural numbers** A positive integer including zero

**Integer** Any whole positive or negative number including zero

**Rational numbers** Any number that can be expressed as a ratio of integers

**Irrational number** A number that cannot be represented as a fraction or ratio as the decimal form will contain an infinite number of values

**Real numbers** Any positive or negative number with or without a fractional part

**Ordinal number** A number used to identify position relative to other numbers

**Cardinal number** A number that identifies the size of something

**Well ordered set** A group of related numbers with a defined order

Ordinal numbers are used to identify the position of data within an ordered set.



## Number bases

**Number base** The number of digits available within a particular number system

**Bit** A single binary digit from a binary number

**Byte** A group of bits, usually 8

**Unit** The grouping together of bits or bytes to form larger blocks of measurement

## The binary number system

### Adding unsigned binary integers

**Unsigned binary** Binary that represents positive numbers only

To add two numbers together in binary, first line up the numbers.
Add the columns starting from the right hand side, carrying 11 to the next column,

### Multiplying unsigned binary integers

To multiply in binary, you multiple the first number be each of the digits of the second number in turn, starting from the right hand side.
This means that you are multiplying each each digit by 0 or 1. 
You then do the same for the ntext digit, shifting your answers to the left as you would in decimal multiplication.

You can then carry out a binary addition to find the final answer.

```
  11011 * 
     11
------------
  11011 (1 * 11011)
 110110 (1 * 110110)
------------
1010001
------------
 1111
```

### Two's complement

**Two's complement** A method of working with signed binary values

Two's complement is a method used to represent signed integers in binary form. This means that it can be used to represent positive and negative integers.

The first digit in a two's complement integer has a negative value, and all of the other digits have positive values.

#### Adding and subtracting using two's complement

Adding numbers together using two's complement is the same as adding numbers together in decimal. You add up the total and carry values across to the next column.

In order to carry out subtractions, the method used is to convert the number to be subtracted to a negative value, and then to add it.

### Fixed point numbers

In order to represent real decimal numbers, fixed point representation can be used. In the same way that decimal has a decimal point, binary has a binary point. The numbers after the binary point represent fractions.

**Fixed point** Where the decimal/binary point is fixed within a number

The binary point is not actually stored in the 8 bit code, its position is fixed by the programmer.

### Floating point numbers

**Floating point** Where the decimal/binary point can move within a number

In floating point, the binary point can be moved depending on the number that you are trying to represent. It 'floats' left to right rather than being in a fixed position.
Floating point extends the fixed point technique.

A floating point number is made up of two parts, the mantissa and the exponent.
In binary, the exponent and mantissa are used to allow the binary point to float. They are each two's complement values.

To calculate the value of a floating point value, we first calculate the value of the mantissa and then multiply it by 2 to the power of the exponent.

This is equivalent to finding the value of the exponent, 'floating' the binary point to n places to the right if the exponent is n, and n places to the left if the exponent is -n, before evaluating the binary as a fixed point value.

### Underflow and overflow

**Overflow** When a number is too large to be represented with the number of bits allocated

**Underflow** When a number is too small to be represented with the number of bits allocated

### Normalisation and precision

**Normalisation** A process for adjusting numbers onto a common scale

**Precision** How close a value is to the true value

In order to be normalised, the first bit of the mantissa, after the binary point, should always be 1 for positive integers, or 0 for negative numbers and the bit before the binary point should be the opposite.

A normalised positive floating point number must start 0.1 and a normalised negative floating point number must start 1.0

#### Example

Consider the number 108. The 8 bit binary equivalent of which is 01101100.

- The normalised mantissa would be 0.1101100
- The binary point will have to be moved seven places to the right to convert it back to the original number
- The exponent is therefore 7
- The two's complement value for 7 is 0111
- Therefore the normalised representation of 108 is 0.11011000111

### Rounding errors

When working with decimal numbers, we are used to the idea of rounding numbers up or down. As a consequence, we will get rounding errors.

A similar phenomenon occurs with binary representation. If you attempt to convert 0.1 into binary you will find that you get a recurring number, so it is not possible to exactly represent it.

If you try to represent 1.95 with 8 bits and a fixed point 1.1111010 gives 1.953125 while 1.1111001 gives 1.943125. With 8 bits the nearest value is 0.003125 out. 
Extending the number of bits would allow for an answer closer to 1.95

### Absolute and relative errors

There are two main methods for calculating the degree of error in number that we use within a program.
The absolute error is the actual numerical difference between the answer and the approximation.

The relative error is the absolute error divided by the true value.

## Coding systems

**Character code** A binary representation of a particular letter, number, or special character

### ASCII and Unicode

The ASCII (American Standard Code for Information Interchange) was agreed upon. 7 bits of each byte are used to represent 128 characters, while the 8th bit can be used for checking.

ASCII has limitations:
- 256 characters are not sufficient to represent all of the possible characters, numbers, and symbols
- It was initially developed in English and therefore did not represent all of the other languages and scripts in the world
- Widespread use of the web made it more important to have a universal international coding system
- The range of platforms and programs has increased dramatically with more developers from around the world using a much wider range of characters


**Unicode** A standard binary coding system that has superseded ASCII

Unicode is being constantly developed and updated to include more languages and characters from around the world.

### Error checking and correction

**Parity bit** A method of checking binary coudes by counting the number of 0s or 1s in the code

#### Even and odd parity

One method for detecting errors is to count the number of ones in each byte before the data is sent to see whether there is an even or odd number. At the receiving end the code can be checked to see whether the number is still odd or even.

- Even parity: The number of 1s in the code are counted. The parity bit is set to make the total number of 1s even
- Odd parity: The number of 1s in the code are counted. The parity bit is set to make the total number of 0s odd

#### Majority voting

**Majority voting** A method of checking for errors by producing the same data several times and checking it is the same each time

When the data is checked, you would expect to see patterns of three bits.
When there is a discrepancy, you can use majority voting to see which bit occurs most frequently.

This principle can be applied on a larger scale. The Columbia space shuttle had at least four computers processing the same data and checking each other's results.

#### Check digits

**Check digit** A digit added to the end of binary data to check the data is accurate

Check digits are a common way of checking data, often when they are being entered into a computer.
For example, check digits are used on the barcodes printed on goods at a supermarket.
Like a parity bit, a check digit is a value that is added to the end of a number to try to ensure that the number is not corrupted.

The check digit is created by taking the digits that make up the number itself and using them in some way to create a single digit. The simplest, but most error prone is to add the digits of the number together and keep on adding the digits until you have only a single digit remaining.

The problem with this system is that if two numbers are transposed, the check digits will be the same. In order to overcome this, each number in the pattern is given a weighting. A common method for calculating a check digit is konw as module 11.

```
Original number 2 3 0 4 5
Weighting       6 5 4 3 2
Multiply        12 15 0 12 10
Add             12+15+0+12+10 = 49
Divide by 11 49/11 = 4R5
Subtract the remainder from 11 11 - 5 = 6
The check digit is 6 -> 230456
```

### Bit mapped graphics

**Bit mapped graphic** An image made up of individual pixels

**Pixel** An individual picture element

**Colour depth** The number of bits or bytes allocated to represent the colour of a pixel in a bit-mapped graphic

Bitmaps may also contain metadata. Metadata is normally found at the beginning of the file in a header

### Vector graphics

Vector graphics are created using objects and coordinates. A vector is a measure of quantity and direction.
To rescale a vector image requires an adjustment of the coordinates. Therefore, the graphics are being controlled mathematically rather than being completely regenerated as with a bit map.
An image created on the screen will be made up of lines and the scale and position of the lines will be adjusted as the screen display changes to create an image

**Vector graphic** An image made up of objects and coordinates

Vector graphics have numerous advantages
- Vector graphics can be scaled perfectly 
- Two and three dimensional animations can be created using vector graphics
- Less data is used for simple images


### Analogue and digital signals

Analogue data are data that are infinitely variable and are often represented in the form of a wave.

Digital data are often represented as discrete waves.

#### Analogue to digital conversions

The problem arises when we need to input analogue data into the computer or when we want to output digital data from the computer in analogue form.
In order to do this, a converter is need.

One example of an analogue to digital converter (ADC) is a microphone. The microphone inputs sound in the form of changes in air pressure and then converts them into electrical signals.

Another example is a MIDI device for an acoustic guitar. This device fits beneath the strings on the guitar and when the strings are played they generate an analogue sound wave.
The sound waves are picked up and converted to digital form.

MIDI uses event messages to control various properties of the sound.
These messages are typically encoded in binary and provide communication between MIDI devices or between MIDI device and the processor.
For a MIDI keyboard, an event message may contain data on:
- When to play a note
- When to stop playing the note
- Timing a note to play with other notes or sounds
- Timing a note to play with other MIDI enabled devices
- What pitch a note is
- How loud to play the note
- What effect to use when playing the note

MIDI files have numerous advantages over other digital audio formats:
- MIDI files tend to be much smaller. This means that they require less memory and also load faster
- MIDI files are completely editable as individual instruments can be selected and modified
- MIDI supports a very wide range of instruments providing more choices for music production
- MIDI files can produce a very high quality and authentic reproduction of the instrument

### Sound sampling and synthesis

Sampling is the process of converting analogue sound waves into digital form to create what is commonly known as digitised or digital sound.
This is sometimes referred to as analogue to digital conversion.
An analogue sound wave is infinitely variable so in order to store this digitally, a series of reads at fixed intervals are taken from the wave in order to create the discrete data values that are defining a feature of binary data.
These reading are then stored as binary codes.
This is called sampling because you do not record every single change in amplitude of the waveform.

#### Sampling an analogue wave

The amplitude of the wave is only recorded at the point where each sample is taken. Other variations in the amplitude are not recorded.
Therefore, to create an exact replica of the analogue sound would require a sample to be taken every time the amplitude of the wave changed even by a small amount.
However, the human ear doesn't notice very small changes, so sound can be faithfully created with fewer samples.
Taking more samples allow more accurate reproduction of the original analogue sound.

### Data compression

**Compression** The process of reducing the number of bits required to represent data

Compression is the process of encoding with fewer bits, so that the files take up less memory

#### Lossless compression

**Run length encoding** A method of compressing data by eliminating repeated data

**Dictionary based encoding** A method of compressing text files

Lossless compression maintains all of the original data.

#### Lossy compression

There are cases where lossless compression still results in a large file as there is a limit to how small it can get, while still maintaining accuracy.

JPEG compression works by breaking an image into blocks of 8x8 pixels. In each block, the data is converted into frequencies. Some frequencies are considered more important than others.

In a high frequency image the human eye will not notice slight changes to large blocks of similar colours, however it will notice changes in areas with high contrast. These contrasting areas must be maintained.


## Encryption

Encryption is the process of scrambling data so that it cannot be understood by a third party unless they know the encryption method and key used. 
Decryption is the process of turning the scrambled data back into data that can be understood. Data is encrypted before it is transmitted and decrypted when it is received.

**Encryption** The process of turning plaintext into scrambled ciphertext, which can only be understood if it is decrypted

**Decryption** The process of deciphering encrypted data or messages

**Plaintext** Data in human-readable form

**Ciphertext** Data that has been encrypted

**Caeser cipher** A substitution cipher where one character of plaintext is substituted for another, which becomes the ciphertext

**Vernam cipher** A method of encryption that uses a one time pad to create ciphertext that is mathematically impossible to decrypt without the key

**Transposition cipher** A method of encryption where the characters are rearranged to form an anagram

**Key** THe data that is used to encrypt and decrypt the data

**Substitution cipher** A method of encryption where one character is substituted for another to create ciphertext

**Polyalphabetic** Using more than one alphabet

### Frequency analysis

**Frequency analysis** The study of how often different letters or phrases are used

The Caesar cipher can be easily broken as certain letters are more frequently used than others and certain combinations of letters are also common.

### Transposition cipher

The letters of the message are transposed or rearranged to form an anagram. You must rearrange the letters according to a set pattern to make it possible to decrypt the message. One way of doing this is the railfence method where the message is split across several lines.

**Railfence cipher** A type of transposition cipher that encodes the message by splitting it over rows

**Route cipher** A type of transposition cipher that encodes the message by placing it into a grid

### Vernam cipher

The Vernam cipher is an example of a class of encryption techniques known as one-time pad techniques. The key that is used is a sequence of letters that should be as long as the plaintext that is being encoded. The key can be recorded on a pad, although in the Vernam case the key was written on a punched tape for input into the telex device.

**One time pad** A key that is only used once to decrypt a message and is then discarded

**Baudot code** A 5 digit character code that predates ASCII and Unicode

To encrypt a message, each character in the plaintext is combined with the character at the corresponding position in the key by converting the corresponding plaintext and key characters into a binary code, and using a logical XOR on these binary representations.

The ciphertext can be decrypted  using the same operation with the same key.

### Computational security

**Computational security** A concept of how secure data encryption is

**Computational hardness** The degree of difficulty in cracking a cipher

Computational security means that cryptographers need to be aware of the ways in which their encryption could be cracked.

- Identifying commonly used techniques such as substitution or transposition, and the patterns that they create
- Reverse engineering. The process of going step by step to work out how something has been put together
- Dictionary attacks. The process of using a dictionary that contains common words and phrases. After each attempt to decrypt the text is made, the text can be compared to the dictionary to see if it matches
- Brute force. Similar to a dictionary attack, but it takes much longer as it considers every permutation of characters that can be created

# Computer systems

## Hardware and software

**Hardware** A generic term for the physical parts of the computer, both internal and external

**Software** A generic term for any program that can be run on a computer

### Hardware

External components (peripherals) are the components of the hardware such as the monitor, keyboard, mouse, and printer. The external components are used either to input or output data. Some storage devices are also external, such as flash drives.

### Software

#### Application software

Application software refers to all of the programs that the user uses in order to complete a particular task.

**Application software** Programs that perform specific tasks that would need doing even if computers did not exist. e.g. text editing

#### System software

System software covers a range of programs that are concerned with the technical aspects of setting up and running the computer.

There are four main types of system software:

##### Utility programs

This covers software that is written to carry out certain housekeeping tasks on the computer.
They are normally supplied with the operating system and include

**Utility programs** Programs that perform specific common tasks related to running the computer e.g. zipping files

#### Library programs

Library programs are utility programs in that they are written to carry out common tasks. The word library indicates that there will be a number of software tools available to the users of the system.

**Library programs** Code, data, and resources that can be called by other programs

Whereas some utility programs are non-essential, library programs tend to be critical for the applications for which they were built.

## Classification of programming languages and translation

**Translators** Software that converts programming language instructions into machine code

**Compiler** A program that translates a high-level language into machine code by translating all of the code

**Assembler** A program that translates a program written in assembly language into machine code

**Interpreter** A program for translating a high-level language by reading each statement in the source code and immediately performing the action

**Operating system software** A suite of programs designed to control the operations of the computer

**Virtual machine** The concept that all of the complexities of using a computer are hidden from the user and other software by the operating system

### Operating system software

The operating system carries out many tasks, such as:
- Controlling the start-up configuration of the computer
- Recognising that a mouse button has been pressed and deciding what action to take
- Sending signals to the hard disk controller, telling it what program to transfer to memory
- Deciding which sections of memory to allocate to the program you are intending to use and manages memory to ensure all of the programs you want to run are allocated the space they need
- Attempting to cope with errors as and when they occur
- Making sure the computer shuts down properly
- Controlling print queues
- Managing the users on a network

### Resource management

**Resource management** How an operating system manages hardware and software to optimise the performance of the computer

**Processor** A device that carries out computation on data by following instructions, in order to produce an output

**Scheduling** A technique to ensure that different users or different programs are able to work on the same computer system at the same time

The simplest way that an operating system can schedule access to the processor is to allocate each task a time slice. This means that each task is given an equal amount of processor time.
Time slicing is a crude system because a praticular task might not need all or even any of its alloted time slice with the processor.

### Managing input output devices

The operating system controls the way in which the various input and output devices are allocated, controlled, and used by the programs that are using them, such as:
- Allocating print jobs to printers
- Rendering the windows, frames, and dialog boxes to the screen
- Controlling the read-write access to the hard disk

Accessing some devices is a relatively slow process compared to the speed at which the processor can handle requests. At the same time there are likely to be competing request where several processes are waiting for the same device. Rather than waiting for each process to end before it can continue, the OS can effectively create a queue of commands that are waiting for the device and then handle each request in sequence or based on a priority.

Every input/output device has a device driver, which is a piece of software that enables the device to communicate with the OS. Device drivers are often built in to the OS or installed when new devices are attached. When the OS starts up it loads the various driver for all of the input/output devices it detects.

### Memory management

**Memory management** How the operating system uses RAM to optimise the performance of the computer

The operating system controls the use of main memory by creating a memory map, which shows which blocks of memory have been allocated to each astk. Tis way an operating system can control more than one task in the RAM at any one time.
The amount of memory needed by each task is dependent on the size of the program itself, the variables that will be needed and any files that might be generated by the task, but it is up to the operating system to decide how much space can be allocated.

#### Virtual memory and paging

In some cases, the application or file being accessed is too large to fit in RAM. In this case a process called virtual memory can be used.
This involves using secondary storage such as a hard disk to store code or files that would normally be held in RAM. The operating system then uses part of the hard disk as if it is part of the RAM.
An alternative method is to hold a kernel or central block of the code in RAM. Other sections of code known as pages are loaded from the secondary storage as and when they are needed. Using this method allows very large applications to run in a small section of RAM. This in turn frees up memory for other applications to use.

### File management

**File management** How an operating system stores and retrieves files




## Boolean algebra

**Boolean expression** An expression made up of Boolean operations

### Simplifying boolean expressions

| Identity name | AND Form | OR Form
| --- | --- | --- | 
| Identity | $A.1 = A$ | $A+0 = A$ |
| Null/Dominance | $A.0 = 0$ | $A+1 = 1$ |
| Idempotence | $A.A = A$ | $A+A = A$ |
| Inverse | $A.\overline{A} = 0$ | $A+\overline{A} = 1$ |
| Commutative | $A.B = B.A$ | $A+B = B+A$ |
| Associative | $(A.B).C = A.(B.C)$ | $(A+B)+C = A+(B+C)$ |
| Absorption | $A.(A+B) = A$ | $A+A.B = A$ |

### De Morgan's Law

$\overline{A.B} = \overline{A} + \overline{B}$

$\overline{A+B} = \overline{A}.\overline{B}$


## Logic gates

**Logic gate** An electronic component used to perform boolean operations

# Computer organisation and architecture

## Internal hardware of a computer

### Processor

**Processor** A device that carries out computation on data by following instructions, in order to produce an output

### Main memory

Main memory is used to store data and instructions. 

**Main memory** Stores data and instructions that will be used by the processor

**Fetch-execute cycle** The continuous process carried out by the processor when running programs

**Random Access Memory** Stores data and can be read and written from

**Chip** An electronic component contained within a thin slice of silicon

RAM is temporary storage space that can be accessed very quickly. 
RAM is volatile, meaning that whatever is stored on it will be lost once power is lost.

**Read only memory** Stores data and can be read from, but not written to (unless programmable ROM)

ROM is non-volatile, and is usually writeable.

### Addressable memory

Memory is made up of millions of addressable cells and the various instructions and data that make up a program will be stored across a number of cells. Each address can be uniquely identified.

### Buses

Buses are groups of parallel microscopic wires that connect the processor to the various input and output controllers being used by the computer.

**Bus** Microscopic parallel wires that transmit data between internal components

#### Data bus

**Data bus** A bus used to transfer data between the processor and memory

**IO controller** A component which controls the flow of information between the processor and the IO devices

The data bus connects the registers to each other and to memory. The amount of data that can be passed along the bus depends on how many wires are in the bus.

**Word length** The number of bits that can be addressed, transferred, or manipulated as one unit

**Address bus** A bus used to specify a physical address in memory so that the data bus can access it

#### Address bus

The address bus is unidirectional, from the processor into memory. The address bus is used by the processor and carries the memory address of the next instruction or data item. The address bus is therefore used to access anything that is stored in memory, not just instructions.

The size of the address bus is also measured in bits and represents the amount of memory that is addressable. An 8 bit bus would give only 256 directly addressable memory cells.

**Addressable memory** The concept that data and instructions are stored in memory using discrete addresses

**Control bus** A bus used to control the flow of data between the processor and other parts of the computer

#### Control bus

A bi-directional bus which sends control signals to the registers, the data and address buses.
Data buses are sending data to and from memory while address buses send only to memory.

The control bus is used to ensure that the correct data is travelling to the right place at the right time. This involves synchronisation of signals and the control of access to the data and address buses which are being shared by a number of devices.

#### IO controllers

The processor also receives and sends instructions and data to the various input and output devices connected to the computer.
Controllers consist of their own circuitry that handle the data folowing between the processor and the device.
Every device will have its own controller which allows new devices to be connected to the processor at any time.

A key feature of an IO controller is that it will translate signals from the device into the format required by the processor. There are many different devices and many different types of processor and it is the IO controller that provides the flexibility to add new devices without having to redesign the processor.

Another important feature is that the IO devices themselves respond relatively slowly compared to the processor. Therefore the IO controller is used to buffer data being sent between the processor and the device.

### Von Neumann and Harvard architectures

**Von Neumman architecture** A technique for building a processor where data and instructions are stored in the same memory and accessed via buses

**Harvard architecture** A technique for building a processor that uses separate buses and memory for data and instructions

The advantage of the Harvard architecture is that instructions and data are handled more quickly as they do not have to share the same bus. 
The Harvard architecture is widely used on embedded systems such as mobile phones, burglar alarms, etc, where there is a specific use, rather than being used within general purpose PCs.

Many such devices use digital signal processing. The idea of DSP is to take continuous real world data such as audio or video and then to compress it to enable faster processing. Chips that are optimised for DSP tend to have much lower power requirements.


## The stored program concept and processor components

**Stored program concept** The idea that instructions and data are stored together in memory

**Fetch-execute cycle** The continuous process carried out by the processor when running programs

- Fetch- The processor fetches the program's ntext instruction from memory. THe instruction will be stored at a memory address and will contain the instruction
- Decode- The processor works out what the binary code at that address means
- Execute- The processor carries out the instruction which may involve reading, writing, or performing a calculation

![fdsf](http://i.imgur.com/clPcpJN.png)

### The control unit

**Control unit** Part of the processor that manages the execution of instructions

The control unit supervises the fetch-execute cycle. The control unit also makes sure that all the data is being processed and routed correctly.

### Arithmetic logic unit

**Arithmetic Logic Unit** Part of the processor that processes and manipulates data

The arithmetic logic unit carries out both arithmetic and logic.
The ALU is sent an operation code and the operands.

### The clock 

All computers have an internal clock which generates a signal that is used to synchronise the operation of the processor and the movement of data around the other components of the computer

**Clock** A device that generates a signal used to synchronise the components of a computer

### Registers

The control unit needs somewhere to store details of the operation being dealt with by the fetch-execute cycle, and the ALU needs somewhere to put the results of any operation it carries out.

**Register** A small section of temporary storage that is part of the processor

**Status register** Keeps track of the various functions of the computer, such as if the result of the last calculation was positive or negative

**Interrupt register** Stores details of incoming interrupts

**Current instruction register** Stores the instructions that the CPU is currently decoding or executing

**Program counter** Stores the address of the next instruction to be read from main memory

**Memory buffer register** Stores data that is either written to or copied from the CPU

**Memory data register** Another name for the memory buffer register

**Memory address register** Stores the location of the address that data is either written to or copied from by the processor

A register must be large enough to hold an instruction.
Some registers are general purpose while others are used for a specific purpose.

The status register keeps track of the status, such as if an overflow occurred during an arithmetic register.

The interrupt register is another type of status register, it stores details of any signals that have been received by the processor from other components attached to it.

### The fetch-decode-execute cycle

- Fetch: The program counter holds the address of the next instruction. The processor sends this address along the address bus to main memory. The contents of the memory location at that address are sent via the data bus to the current instruction register and the program counter is incremented. The details of addresses are initially loaded into the memory address register and the data is initially loaded into the memory buffer register. Some instructions need to load a number of words, so they may need to be fetched as successive parts of a single instruction.
- Execute: THe processor then takes the instruction from the current instruction register and decides what to do with it by referring to the instruction set.This might be to send the contents of the memory buffer register to the arithmetic logic unit. Once the instruction that has just been taken from memory has been decoded, the processor carries out the instruction. It then goes back to the top of the cycle and fetches the next instruction. The results of any calculations are written either to a register or a memory location.

### Factors affecting processor performance

- Clock speed: It indicates how fast each instruction will be executed
- Bus width: The processor needs to optimise the use of the clock pulse. One way of doing this is to increase the bus width.
- Word length: Related to the data bus width. Computer systems with a greater word length can process more data at once
- Multiple core: Several processors can be used to increase performance. The term core is used to define the components that enable instructions to be fetched and executed
- Cache: Caching is a technique where instructions and data that are needed frequently are placed into a temporary area of memory separate from main memory. The cache can be accessed much more quickly than main memory

### Interrupts

**Interrupt** A signal sent by a device or program to the processor requesting its attention

An additional step is added to the fetch-execute cycle. Between the completion of one execution and the start of the next a check is made to see if the interrupt register contains a new interrupt.

If an interrupt has occured the processor will stop whatever it is doing to service the interrupt. This is done using the interrupt service routine.


The contents of the registers are placed onto the system stack. Once the interrupt has been processed the CPU will retrieve the values from the stack and place them in the correct registers.

**Interrupt service routine** A routine to handle a particular type of interrupt

**Priorities** A method for assigning importance to interrupts in order to process them in the right order

#### Priorities

Sometimes the interrupt routine may be interrupted.
In this case the processor will either place details of its current task on the stack or it will assess the priority of the interrupts and decide which one needs to be serviced first. Assigning different interrupts priority levels means that the most important signals are dealt with first.

| Level | Type | Possible causes |
| --- | --- | --- |
| 1 | Hardware failure | Power failure |
| 2 | Reset interrupt | Some computers have a reset button which resets the computer to its start-up position |
| 3 | Program error | The current application is about to crash, so the OS will attempt to recover |
| 4 | Timer | A timer interrupt is used as part of the time slicing process in a multitasking environment |
| 4 | IO | Incoming data from a keyboard or mouse etc |

#### Vectored interrupt mechanism

Once the values of the registers have been pushed to the stack, the processor can handle the interrupt. This is done using a technique called vectored interrupt mechanism.

**Vectored interrupt mechanism** A method of handling interrupts by pointing to the first memory address of the instructions needed


Each interrupt has an associated section of code that tells the processor how to deal with that particular interrupt.
When the processor receives an interrupt it needs to know how to find that code. every type of interrupt has an associated memory address known as a vector.
The vector points to the starting address of the code associated with each interrupt.

When an interrupt occurs, the processor identifies what kind of interrupt it is, then finds its associated interrupt vector. It then jumps to the address specified by the vector, from where it runs the interrupt service routine.

## The processor instruction set and addressing modes


**Instruction set** the patterns of 0s and 1s that a particular processor recognises as commands, along with their associated meanings

**Opcode** An operation code or instructions used in assembly language

**Operand** A value or memory address that forms part of an assembly language instruction

**Addressing mode** The way in which the operand is interpreted

**Assembly language** A way of programming using mnemonics

**Mnemonics** Short codes that are used as instructions when programming

### Immediate and direct addressing

**Immediate addressing** When the operand is the data to be used

**Direct addressing** When the operand is the memory address or register number to load information from

### Types of opcodes

**Data transfer operations** Operations within an instruction set that move data around between the registers and memory

**Arithmetic operations** Operations within an instruction set that perform basic maths

**Shift instructions** Operations within an instruction set that move bits within a register

**Logical operations** Operations within an instruction set that move the bits around within the operand

**Branch operations** Operations within an instruction set that allow you to move from one part of the program to the other



## External hardware devices

### Digital camera

**Digital camera** A device for creating images of photographs, which can be printed or transferred onto a computer to be manipulated and stored

- When a photograph is taken the shutter opens and lets light in through the lens
- The light is focused onto a sensor, which is usually either a charge coupled device or a complementary metal oxide semiconductor
- The sensors are made up of millions of transistors, each of which stores the data for one or more pixels
- As the light hits the sensor it is converted into electrons and the amount of charge is recorded for each pixel
- With light, all colours can be created from red, green, and blue. Therefore the camera will either have three different sensors, or use three different filters
- The data are typically stored on removable storage devices, usually referred to as flash memory
- Data are usually stored in compressed files
- RAW files can also be generated, which are uncompressed and therefore contain all of the data from the original photograph
- This digital data can be decoded and manipulated using specialised software

**RGB filter** red, green, and blue filters that light passes through in order to create all other colours

**Compression** The process of reducing the size of a file

**Resolution** The number of pixels used to create an image

### Barcode reader

**Barcode reader** A device that uses lasers or LEDS to read the black and white lines of a barcode

- A light, usually an LED or laser is passed over an image
- Some form of light sensor is used to measure the intensity of light being reflected. This is converted into a current effectively generating a waveform. this could be achieved using a photodiode or a CCD sensor in the same way as the digital camera
- White areas reflect most light and black areas least
- The waveform is analogue and therefore needs to be converted into digital form using an analogue to digital converter
- The signal is decoded into a form that can then be interpreted by software

There are many different types of barcode. 
The most common is the universal product code which uses a series of black and white lines of four different widths that are encoded to represent the values 1 to 4. The numbers are below for a manual override and include a check digit.

Barcodes are used primarily for inputting product details at the point of sale.

More recently, the same technology has been applied to codes that are made up of blocks of black and white symbols rather than lines. One example is a QR code which can be used to encode a wider range of information than a barcode.

### Radio frequency identification

**Radio frequency identification** A microscopic device that stores data and transmits it using radio waves. Usually used in tags to track items

- The tag, which can be microscopically small, contains a chip, which contains the data about the item and a modem to modulate and demodulate the radio signals
- The tag also contains an antennae to send and receive signals
- Tags can be either active, which means that they have their own power source, or passive, which means that they will pick up electromagnetic power when they are in range of an RFID reader
- Signals and therefore data can be transmitted in both directions using radio frequencies. This may be over a short or long distance depending on what the tags are being used for and how they are powered. The typical range of RFID tags is between 1 and 100 metres
- Tags may be used to simply track the physical location of the tagged item or the item may transmit data back

Example use cases
- Tracking individuals, particularly vulnerable adults
- Use in electronic passports
- In credit and debit cards to make contactless payments
- In transport and distribution to track shipments and deliveries
- On high value items, such as artwork in museums or equipment in hospitals

### Laser printer

**Laser printer** A device that uses lasers and toner to create mono and colour prints

- A rotating drum inside the printer is coated in a chemical which holds an electric charge
- The laser beam is reflected onto the drum and where the light hits the drum is discharged, effectively creating an image on the drum
- As the drum rotates it picks up toner on the charged parts of the drum
- Paper is passed over the drum and by giving the paper the opposite charge, the toner is transferred to the paper
- The paper is heat treated to fuse the toner onto the paper

To achieve colour printing, four different coloured toners are used, and the process of transferring the toner to the drum is repeated for each colour. In some printers, a transfer belt is used to hold the four-colour image and therefore transfer it just once from the belt to the paper. 
When printing, four colours are needed: cyan, magenta, yellow, and black.

### Magnetic hard disk

**Hard disk** A secondary storage device made up of metallic disks that stores data magnetically

Hard disks spin at speeds between 3600 and 15000 rpm as a series of heads read from and write to the disks. The heads to not actually touch the disks but float slightly above it by virtue of the speed at which the disk spins.

The surface of the disk is organised into concentric tracks and each track is split into sectors each of which can be individually addressed by the operating system. Because the head assembly can read any one of several disks, a cylinder reference is also used to identify which of the disks in the stack is being addressed.

Each sector has the same capacity and a large file will be stored over a number of sectors. The operating system groups sectors together into clusters to make storage easier to manage.

### Optical disk

Optical disk is a generic term for all variations of CD, DVD, and Blu-Ray that use laser technology to read and write data. 
An optical disk is made up of one single spiral track that starts in the middle and works its way to the edge of the CD. The laser will read the data that are contained within this track by reading the pits and lands in combination with a sensor that measures how much light is reflected.

For read-only optical disks, when data is written it is encoded as a series of pits or lands within the track. A protective layer is then put over the surface to prevent any corruption of the data.

For writeable optical disks, rather than using pits and lands, the disk is coated with a translucent photosensitive dye. When writing to the disk, the laser will alter the state of a dye spot that is coated onto the surface making it opaque.
A write laser alters the density of the dye, and a read laster interprets the different densities to create binary patterns.

### Solid state disk

High speed access to memory is achieved using memory cards made up of semiconductors.
Solid state drives use NAND memory and data is organised into blocks in a similar way to a traditional hard disk, with a controller managing the blocks of data.

**Controller**  A device which manages access to and organises data into blocks

**Block** The concept of storing data in set groups of bits and bytes of a fixed length

**Floating gate transistor** A non-volatile transistor that stores data without a power source

A gloating gate transistor is able to trap and store charge. 
It contains two gates, a floating gate and a control gate.
A thin layer of oxide is placed between the two gates, effectively trapping the charge inside the floating gate even when the power is turned off.

| | Hard disk | Solid state | Optical disk | Blu-Ray (OD) |
| --- | --- | --- | --- | --- |
| Typical capacity | High (1 TB) | Medium (500 GB) | Low (0.9-1.7 GB) | Low (25-50 GB) |
| Relative cost | Medium | High | Low | Low |
| Power consumption | High | Low | High | High |
| Speed of access | Medium | High | Low | Low |
| Latency | High | Low | Very high | High |
| Fragmentation | | None | | |
| Reliability | Good | Very good | Fair | Fair |
| Physical size | Large | Small | Small | Small |


# Moral, ethical, legal, and cultural issues

**Ethical issues** Factors that define the set of moral values by which society functions

## Use and misuse of data

Most organisations collect data on an ongoing basis and much of these data are personal.
this presents a number of issues:

- Personal privacy: A lot of data are stored online as a matter of routine and as individuals we may not have explicitly consented to them being collected and used
- Data security: Much of the data are stored online or on networks connected to the Internet. How can we be sure they are safe from unauthorised users?
- Misuse of data: Data collected for one purpose are used for a different purpose. In many cases data are sold on to other organisations.
- 'Big Brother': Many people have concerns that personal data are being used by government to monitor individuals and that this is a breach of our basic human rights
- Online profile: Every time you do anything online, such as using social media, that data may stay online for years and contribute to what people know about you
- Profiling: Large organisations often accumulate data in order to build up a profile of individuals. this could have a negative impact on an individual

### Banking- the benefits of technology

Around 30 years ago, if you wanted to carry out any banking transaction you had to do it in the limited time that a bank was open. the invention of cash machines in the 1980s was a revolution that allowed customers constant access to their money. the invention of online banking in the 1990s meant that almost all transactions could be done at any time, including paying bills, setting up direct debits, and moving money from one account to another.

### Banking- The threat of technology

According to some sources there are as many as 250,000 phishing attacks per year.
Some customers have lost hundreds of thousand of pounds in individual attacks that use sophisticated software to emulate online banking websites.

### Other moral and social issues

**Unauthorised access** Where computer systems or data are used by people who are not the intended users

- Unauthorised use of software: Some people believe that software is too expensive and that software companies are exploitative. Therefore, downloading or copying software is morally defendable
- Inappropriate behaviour: There is evidence that people's behaviour changes when they are online. In the worst cases this can lead to online abuse which may spread into the real world
- Inappropriate content: There are large volumes of content on the Internet which many people consider to be inapprorpriate. This content may not be illegal, but there is conecrn about what effect it has on society
- Freedom of speech: Some people believe that they should be able to say whatever they want, even if that offends other people. the Internet gives almost everyone the ability to do that. It therefore raises the issue of whether there should be some code that all internet users should adhere to when expressing their views
- Unemployment: A broader social issue relates to the impact that new technology has on people's working lives. Many businesses such as retail and banking no longer need to emply as many people in their stores and branches. On the other hand, they may create more jobs in IT for employees working in their online businesses
- Access to the internet: It is difficult to know how many people have access to the Internet. Are those who do not have access disadvantaged?

**Moral issues** Factors that define how an individual acts and behaves

**Code of conduct** A voluntary set of rules that defines the way in which individuals and organisations will behave

The British Computer Society has produced a code of conduct and a code of ethics that guide individuals and organisations on the use of computer systems. 

The main principles are that members should:
- Always operate in the public interest
- Have a duty to the organisation that they work for, or the college that they attend
- Have a duty to the profession
- Maintain professional competence and integrity

## Legal issues

**Legal issues** Factors that have been made into laws by the government

Legislators who enforce these laws have two main issues:
- Geographical limitations: Most UK laws only apply in the UK. With the global nature of the Internet it can be difficult to prove where a particular offence took place. Also, if the perpetrator breaks a UK law but they are based in another country, it can be difficult to prosecute them
- Constant change: most acts are introduced in response to current events. As technology develops so rapidly, laws often become out of date quite quickly

### Data Protection Act

The Data Protection Act was introduced in 1984. it has since been updated to reflect the enormous changes in the use of information.
It places controls on organisations and individuals that store personal data electronically.

The definition of personal data is any data on an individual where the person (known as the data subject) is alive and can be individually identified.

The Act states that any person or organisation storing personal data must register with the Information Commissioner, an independent organisation set up by the government to oversee Data Protection and Freedom of Information.

the Information Commissioner's mission is:

"We shall develop respect for the private lives of individuals and encourage the openness and accountability of public authorities.
- by promoting good information handling practice and enforcing data protection and freedom of information legislation; and
- by seeking to influence national and international thinking on privacy and information access issues."

There are eight main principles behind the data Protection Act. Anyone processing data must comply with these eight enforcable principles of good practice.

Data must be:
- Fairly and lawfully processed
- Processed for limited purposes
- Adequate, relevant, and not excessive
- Accurate
- Not kept longer than necessary
- Processed in accordance with the data subject's rights
- Secure
- Not transferred to countries without adequate data protection

Another feature of the Act is that data subjects have the right to know what data are stored about them by any particular individual or organization.
These are known as subject access rights. If this information is incorrect then the data subject has the right to have it corrected. The organisation must be given notice and may charge a small fee to the data subject.

### Freedom of information act

The Freedom of Information Act extends the subject access rights of the Data Protection Act and gives general rights to access of information held by public authorities such as hospitals, doctors, dentists, the police, schools and colleges. Both Acts are overseen by the Information Commisioner.

The Act gives individuals access to both personal and non-personal data held by public authorities. the idea behind the Act was to provide more openness between the public and government agencies. Therefore, the agencies are obliged to give the public access to information and to respond to individual requests for information. Much of t

### Computer Misuse Act

**Data misuse** Using data for purposes other than for which it was collected

The Computer Misuse Act contains three specific offences related to computer usage:
- Unauthorised access to computer programs or data: This includes some forms of hacking including breaking through password protection and firewalls, decrypting files, or stealing another user's identity
- Unauthorised access with further criminal intent: An extension of the first offence where there is a clear intention to carry out a further criminal act such as an act of fraud or a copyright breach
- Unauthorised modification of computer material: This includes falsifying bank details or exam grades, spreading viruses designed to corrupt data and programs and interfering with system files

The Act was introduced before the widespread use of the Internet, which has lead to some problems with enforcement.

### Regulation of Investigatory Powers Act

The RIP Act was introduced to clarify the powers that government agencies have when investigating crime or suspected crime. It is not specific to the world of computing but was introduced partly to take account of changes in communication technology and the widespread use of the Internet.

There are five main parts to the Act.
Part 1 relates to the interception of communications, including electronic data.
Part 3 covers the investigation of electronic data protected by encryption.

It gives law enforcement agencies the right to intercept communications where there is suspicion of criminal activity. They also have the right to decipher these data if they are encrypted even if this means that the user must tell the police how to decrypt the data.

It also allows employers to monitor the computer activity of their employees during work time.

### Copyright, Designs, and Patents Act

This Act gives rights to the creators of certain kinds of material allowing them control over the way in which the material is used. The law covers the copying, adapting, and renting of materials.

**Copyright** The legal ownership that applies to software, music, films, and other content

Copyright applies to all works, regardless of the format. Consequently, work produced on the Internet is also covered by copyright. It is illegal to produce pirate copies of software or run more versions on a network than have been paid for.
It is an offence to adapt existing versions of software without permission. It is also an offence to download music or films without the permission of the copyright holder.

In computing, two techniques are used to protect copyright:
- Digital Rights Management: This uses access control software to limit the way in which users can control, use, copy, print, or edit digital content that they have bought
- Licensing: normally used for software, this provides users with a paper based or digital proof that they have purchased software legally and details what they are allowed to do with the software

### Other relevant acts

- The Official secrets Act prevents the disclosure of government data relating to national security
- The Defamation Act prevents people from making untrue statements about other which will lead to their reputation being damaged
- The Obscence Publications Act and the Protection of Children Act prevent people from disseminating pornograhic or violent images
- the Health and Safety Regulations provides regulation on the correct use of screens and is a specific addition to the Health and Safety at Work Act
- The Equality Act makes it illegal to discriminate against anyone on the grounds of sex, sexual orientation, ethnicity, religion, disability, or age

## Cultural issues

**Cultural issues** Factors that have an impact on the ways in which we function as a society

There are elements of computer use that have a cultural impact in that they can change our attitudes, beliefs, and actions:
- Over use of data: There are fears that we are becoming completely dependent on data. Many decisions about the way in which the country is run are based on data analysis
- Invasive technologies: A lot of data are collected without our consent, such as satellite images
- Over reliance on computers: What happens when computer systems fail?
- Over reliance on technology companies: Two thirds of all Internet searches are done through Google. Wikipedia often appears on the front page of search results. This gives these two organisations a great influence over the information we access
- 'Big Brother' culture: With the increasing use of CCTV, the desire for national identity cards, and the monitoring of emails and mobile phone calls, some people believe that we are heading towards a society where everything is watched
- Globalisation: As we become more connected to other cultures, we are more likely to be influenced by them



# Communication and networking

## Communication

**Serial transmission** Data is transmitted one bit at a time down a single wire

**Parallel transmission** Data is transmitted several bits at a time using multiple wires

**Bandwidth** A measure of the capacity of the channel down which the data is being sent

**Bit rate** The rate at which data is actually being transmitted

**Baud rate** One baud represents one electronic state change per second. An electronic state change could encode multiple bits

**Latency** The time delay that ocfurs when transmitting data between devices

### Synchronous and asynchronous data transmission

In synchronous transmission, the two devices will synchronise their transmission signals. The computer sending the data will control the transmission rate to be in time with the device or computer receiving the signal. If two devices are not synchronised then data could be lost during transmission.

Once the devices are synchronised, data can be sent without any need for further information.

Asynchronous  transmission does not require the permanent synchronisation of the sender's and receiver's system clocks. Instead, it synchronises only for the duration of the transmission by sending additional bits of information called start and stop bits.

**Asynchronous data transmission** Data is transmitted between two devices that do not share a common clock signal

**Start bit** A bit used to indicate the start of a unit of data in asynchronous data transmission

**Stop bit** A bit used to indicate the end of a unit of data in asynchronous data transmission

**Parity bit** A method of checking binary codes by counting the number of 0s and 1s in the code

- The start bit causes the receiver to synchronise its clock to the same rate as the sender
- Both devices have already agreed on how many bits of data will follow, whether parity is used, and how many stop bits there will be
- The stop bit(s) indicate that the data has arrived so the processor on the receiver's device can now handle those bits. The stop bit also also allows the receiver to identify when the next start bit arrives
- If there is more data then another start bit will be sent and the cycle will continue
- The sender's device sends data as soon as it is available rather than waiting for the clock pulse or a synchronisation signal from the receiver

**Synchronous data transmission** Data is transmitted where the pulse of the clock of the sending and receiving devices are in time with each other

### Protocols

**Protocols** Sets of rules

**TCP/IP** A set of protocols for all TCP/IP transmissions

**HTTP** The protocol to define the identification, request, and transfer of multimedia content over the internet

**FTP** The protocol for handling file uploads and downloads

TCP/IP:

The Transmission Control Protocol/Internet Protocol is actually two protocols that are usually referred to as one and relate to the set of rules that govern the transmission of data around the Internet. Data sent around the Internet are split into packets. TCP/IP handles the routing and re-assembly of these data packets.

HTTP:
The Hypertext Transfer Protocol is the set of rules governing the exchange of the different types of file that make up displayable web pages.

FTP:
The File Transfer Protocol is similar to HTTP in that it provides the rules for the transfer of files on the Internet. FTP is commonly used when downloading files or uploading web pages to a server.



## Networks

**Network** Devices that are connected together to share data and resources

**Network adapter/Network Interface Card** A card that enables devices to connect to a network

**Network topology** The conceptual layout of a network

**Local Area Network** A network over a small geographical distance, usually a single site and organisation

**Wide Area Network** A network spread over a large geographical distance

Modern routers are actually a number of devices merged together into a single device:
- Receives every packet of data being transmitted, reads the header and forwards it to its destination
- Acts as a firewall, preventing certain packets from being forwarded
- Acts as an switch, creating a connection between two devices on a network
- Provides a wireless access point transmitting a WIFI signal
- Acts as a modem to convert digital signals to analogue so that they can be transmitted down standard telephone cables

### Star topology

**Star topology** A way of connecting devices to a network where each device has a dedicated cable to a central computer or switch

Software may be stored centrally on the server and can be installed, upgraded, and maintained via the server. The server will also contain an operating system that controls the users' access to the system and also includes various administration functions such as managing the print queue.

| Advantages | Disadvantages |
| --- | --- |
| Fast connection speed as each client has a cable | Expensive to set up due to cabling |
| Will not slow down when many users are online | If the cable fails, the client may not be able to receive data |
| Fault finding is simpler as individual faults are easier to trace | Difficult to install as multiple cables are needed, especially across multiple buildings |
| Relatively secure as each connection is unique | The server can get congested as all communications must pass through it |
| New clients can be added without affecting the other clients | |
| If one cable or client fails, then only that client is affected | |

### Bus topology

**Bus topology** A network layout that uses one main data cable as a backbone to transmit data

| Advantages | Disadvantages |
| --- | --- |
| Only one main cable required | Less secure as data are transmitted down one cable |
| Easier to install than a star | Transmission times get slower when more users are on the network |
| Easy to add new clients | One cable affects all users |
| | Less reliable and more difficult to find faults |

**Physical topology** The way in which devices in a network are physically connected

**Logical topology** The conceptual way in data is transmitted around a network

### Client-server networks

In the star and bus topologies, the diagram shows a main server. Although the clients have local resources in terms of processing power, and storage capacity, they are controlled by the server. This emans that when new software is installed, it can be installed on the server and distributed.

The client may request
- Access to a printer
- Providing a secure Internet connection
- Access to email
- Access to applications
- Access to files

This is the most common way of constructing a LAN with a large number of uses.

**Client-server** A network methodology where one computer has the main processing power and storage and the other coputers act as client requesting services from the server

### Peer to peer networks

**Peer-to-peer** A network methodology where all devices in a network share resources between them rather than having a server

This is more common among smaller networks or for certain applications such as file-sharing. Peer-to-peer networks can be created without the need for a special network operating system.

### Wireless networks

**Wireless Wide Area Network** A WAN that does not use cables, but sends data using radio waves

**Media Access Control Adress** A unique code that identifies a particular device on a network

**WiFi** A standard method for connecting devices wirelessly to a network and to the Internet

**Wireless Local Area Network** A LAN that does not use cables, but connects using radio waves

All devices on a network have a MAC address. This is encoded into the network interface card and is in the format of six groups of two hex digits.
The first half of the MAC address is the manufacturer code and the second half is the unique device code allocated by that manufacturer.

Different communication devices are needed to create a wireless network, depending on the geographical coverage.

### Protocols

There are a set of standards and protocols for wireless communications and WiFi to ensure that all devices are able to connect with each other and transmit and receive data. A protocol called Carrier Sense Multiple Access with Collision Avoidance (CSMA/CA) was developed to enable the various devices to transmit at high speeds without interfering with each other.

When data are sent around the networks, they are sent in frames with all the frames being re-assembled at the receiving end. Any device on the network may attempt to send frames. These frames can be picked up by any nodes or devices within range.
Before each frame is sent, the devices use the CSMA/CA protocol to see whether the transmission medium is idle or whether another device is using it. If the transmission media is idle, the data are sent.
Otherwise, each device will wait a random amount of time before trying again.

On receipt of the data, an acknoledgement is sent back to the sending device to confirm that the data have been received and not corrupted. If this is not received, again it will wait a random amount of time before resending.

An optional extension to the protocol is a system called Request to Send/Clear to Send (RTS/CTS), which works between the nodes on a network. The RTS sends a message to the receiving node or access point and if a CTS message is received, it knows that the node is idle and that the data frame can be sent.

**Request to Send/Clear to Send** A protocol to ensure data does not collide when being transmitted on wireless networks

**Service Set Identiffier (SSID)** A locally unique 32-character code that identifies a device on a wireless network

As alll of the data are being sent through radio waves rather than cables, each device needs a way of ensuring that it is connecting to the correct network. The standard method of doing this is to use the SSID in the header of each packet of data being sent.

Each code is locally unique to the particular WLAN that is being used, and therefore acts as an identifier allowing that frame of data to be transmitted.
The network interface card must also be programmed with the same ID so that the device can connect to the WLAN in the first place.

### Network security

Wireless technology can be less secure than a wired system. This is because the signals are asier to intercept.
There are a number of steps that can be taken to increase the level of security on a wireless network:
- Change the SSID from the default value and hide it from transmission
- Ensure that all devices are WiFi Protected Access compliant
- Use strong encryption
- Create a white list of MAC addresses that are known to be trustworthy

**WiFi Protected Access** A protocol for encrypting data and ensuring security on Wifi Networks

## The Internet

**Internet** A global network of networks

### Uniform resource locator

A URL is the full address used to find files on the Internet.

The contentds of the file that a URL locates will vary depending on the Internet protocol being used. When HTTP is used, it finds an index.html file.

**Uniform resource locator** A method for identifying the location of resources on the Internet

The address is made of several parts:
- The protocol being used
- The domain name
- The filename to locate the specific file needed

#### Domain name

**Domain name** The recognisable name of a domain on the Internet

The domain name identifies organisations or groups on the Internet.
- co indicates a company
- com indicates a commercial organisation
- gov indicates a government
- ac indicates an academic institution
- sch indicates a school
- org indicats a non commercial organisation
- net indicates a company providing Internet services
- A two letter country code such as "uk" indicates the country

#### IP Address

**Internet Protocol (IP) address** A unique number that identifies devices on a network

Every domain name is mapped to a number. A domain name server is used to translate the domain name to an IP address.

**Domain name server (DNS)** A server that contains domain names and associated IP addresses

Some IP addresses are classed as private or non-routable addresses. Typically these are the IP addresses used by devices on a private network.
The IP address is needed in order to route data around the network, however it does not need to be made public as that device is not diretly connected to the Internet. It is hidden behind a router or firewall. Non-routable addresses only have to be unique within the LAN and therefore do not need to be alloacted on a global basis.

When connection to the Internet is required, the device will be connected to a router or proxy server in order to connect. In this case the IP address of that router or server needs to be a public or routable address in which case it becomes a unique address that is registered under the domain name system.

### Ports

**Port** Used to identify a particular process or application on a network

**POP3** A protocol for receiving emails

The port is a 16 bit number attached to the IP address. By addressing that port, a process or application will be accessed on the client.

When a client sends a request to the server using a well-knon port, the server needs to respond back to a client port and not the well known port on the client side. Therefore a source port must be sent as part of the client request.

**Secure shell (SSH) protocol** A protocol for remote access to computers

### Network Address Translation

The system that is used to match private IP addresses to public ones is called Network Address Translation.
This has two main advantages:
- A unique IP address is not needed for every device on a network, only on the router or server that is physicallly connected. This means that only the public address needs to be registered with the DNS system
- There is an increased level of security as the private IP address is not being broadcast over the Internet, making that device more secure from unauthorised access

**Domain name server (DNS) system** A system of connected domain name servers that provides the IP addresses of every website on the internet

The router will track connections and maintain a list of mappings between private IP addresses and port numbers and the corresponding public address. It does this by adding entries to a translation table which act as a look-up between the internal IP address and the external IP address.

The following is a common way that NAT can work when a workstation on the internal network wants to load data from a server on the Internet:
- The workstation on the internal network sends a packet to the server on the Internet to request some data, including its own internal IP address and port number in the packet so that the server knows where to return the data to
- The router replaces the internal IP address and port number in the packet with its external IP address and a port number that it generates. This port number will be unique to this communication, within a certain time frame
- The router stores the mapping information from the internal IP address and port number to external port number in the translation table
- Data sent back from the server will be received by the router which will look up the port number in the translation table to identify which machine on the intrnal network sent the request to the server
- The router's IP address in the packet will be replaced with the originating workstation's IP address and port number, as read from the translation table
- The reply packet can then be sent on to the originating workstation
- Where the translation table does not contain a match to a port number in a packet received from a computer on the Internet, the packet is dropped because it is not a packet sent in response to a request from within the network and may be a security issue
- The internal IP address and port are never made public on the external network

### Port Forwarding

Port forwarding is commonly used when a server inside a private network, with a non-routable IP address, is to be used to provide services to clients on the Internet. As the server has non-routable IP address, it cannot be accessed directly from the Internet.
Therefore, the client on the Internet must use the public IP address of the router that connects the private network with the server on it to initiate a connection. This router can be programmed so that request sent to a particular port number are forwarded to a device with a specific IP address within the network.

**Port forwarding** A method of routing data through additional ports

### Sockets

A network socket is an endpoint of a communication flow across a computer network. Sockets are created in software not hardware. A TCP/IP socket is made up from the combination of an IP address and port number.

**Socket** An endpoint of a communication flow across a computer network

Sockets can be created at any time to enable a network connection to be established to or from a computer.
For example Client A is being used on a LAN with a local IP adress 192.168.233.100 and wishes to request a web page from server B which has IP address 192.168.233.2. As a web page is being requested, port 80 on the server will be used so Client A will send its request to 192.168.233.2:80.

In the request, Client A will include its own IP address and port number that has been temporarily generated for this communication. The client will listen on this port number for a reply.
The transport layer of the TCP/IP stack uses the port number to direct packets to the correct application

### Subnet masking

IP addresses are split into a network identifier and a host identifier.
The network may be a local network, or it could be a remote network and the device could be a computer or printer etc.

**Subnet masking** A method of dividing a network into multiple smaller networks

Addresses are split up this way to make networks easier to manager and to make the routing of data more efficient.

When a computer on a network sends data to another computer, it needs to identify whether it is on the same subnet as the other computer. If it is, it can send data to it directly. If it is not, it will send data to the relevant router or gateway, which will in turn send the data on to the correct subnet and computer.

**Gateway** A node on a network that acts as a connection point to another network with different protocols

A gateway may be used to connect two different company networks together.

The gateway carries out all of the protocol conversion required to enable the two networks to work together.

To identify whether the destination computer is on the same subnet, the sending computer needs to look at the network portion of the destination IP address to see if it is the same as its own.

To do this a subnet mask is used, which uses the bitwise logical AND to eliminate the irrelevant bits.

```
01111000.10110000.10000110.00100000 Full IP of sending computer
11111111.11111111.11111111.00000000 AND Subnet mask
01110000.10110000.10000110.00000000 Network ID of sending computer

01111000.10110000.10000110.01001011 Full IP address of destination
11111111.11111111.11111111.00000000 AND Subnet mask
01110000.10110000.10000110.00000000 = Network ID of destination computer
```

As the sending computer and destination computer have the same network ID, the data can be sent directly. Otherwise the data would be sent to a router that would forward the transmission to the subnet that the destination computer is on.

### IPV4 and IPV6

The original 32 bit code is not enough to provide a sufficient number of permutations for the number of devices present on the Internet. Consequently, IPV6 was created, which uses 128 bits represented as eight groups of four hex numbers.

### Dynamic Host Configuration Protocol

IP addresses are defined as either static or dynamic. Static IP addresses are ones that are assigned and then never change. Dynamic IP addresses are allocated every time a device connects to a network.

**Dynamic Host Configuration Protocol (DCHP)** A set of rules for allocating locally unique IP addresses to devices as they connect to a network

A dedicated DHCP server is used on the network and handles the requests by managing the pool of available IP addresses, usually within a defined range of numbers depending on how the network is physically configured.

### Domain name server

Once allocated, the domain names of websites are mapped to unique IP addresses and this information is stored in databases on large servers.

There are hundreds of DNSs in use around the world, all of which are connected to each other. 

#### Internet registries

The organisation that oversees the allocation of domain names and IP addresses is called ICANN, the Internet Corporation for Assigned Names and Numbers.
They have a department called the Internet Assigned Numbers Authority (IANA) who manage five further organisations called Regional Internet Registries. Each of these has a defined region of the world and therefore a defined set of IP addresses that they are responsible for allocating.

**Internet registries** Organisations who allocate and administer domain names and IP addresses

**Regional Internet Registries** Organisations that allocate and administer domain names and IP addresses in different parts of the world

### Routing and gateways

Any transmission will be routed through a number of nodes before a connection is established between the sender and the reveiver. The router is used to send the data to the appropriate node on the network. It knows where to send it as each piece of data is sent as a packet, and it will read the header information in each packet of data being sent.

**Packet** A block of data being transmitted

Data packets are often transmitted between networks as well as around them. Sometimes the networks will be dissimilar in that they use different protocols. A gateway must be used to convert between the two protocols.

Routing finds the optimum route between the sender and the receiver, which may be made up of many nodes. At each stage of the routing process, the data packets are sent to the next router in the path, often with reference to a routing table. The routing table stores information on the possible routes that each data packet may take between nodes on its path from sender to receiver.

**Routing** The process of directing packets of data between networks

### Packet switching

One of the methods used to send data across networks is called packet switching. Data sent over the Internet is broken down into smaller chunks called packets. Each packet will also contain additional information including a packet sequence number, a source and destination address, and a checksum

### Packet switching

One of the methods used to send data across networks is called packet switching. Data sent over the Internet is broken down into smaller chunks called packets. Each packet will also contain additional information including a packet sequence number, a source and destination address, and a checksum. Packets of data are normally made up of a header, body, and footer.

**Packet switching** A method for transmitting packetes of data via the quickest route on a network

| Part | Contents |
| --- | --- |
| Header | MAC address of sender and receiver<br>The sender and receiver IP address<br>Protocol in use<br>Packet number or sequence number
| Body | The actual data |
| Footer | A checksum |

The checksum is used to identify any errors. It could be generated by adding the values in the packet.

Each packet can take a different route to its destination as it can be reassembled at the other end regardless of the sequence in which the packets are receieved. The packets are routed via the least congested and therefore quickest route. Data are transferred quicker using this method and are more secure as the packets take different routes.



## Internet security


### Firewall

**Firewall** Hardware or software for protecting against unauthorised access to a network

An organisation that has a LAN will have a number of computers linked together, which will all have access to internal information.
The LAn may also allow users to acces the Internet, and this is a vulnerability. 

One method of creating a firewall is packet filtering. It uses two network interface cards, one for the LAN and one for the Internet. When data packets are received through the Internet NIC, they can be examined before being passed around internally via the LAN NIC. Firewall stoftware is used to examine the packets to ensure that they do not contain any unauthorised data. At a basic level, the header of each packet can be examined to check that it has come from a recognised source.

**Packet filtering**  atechnique for examining the contents of packets on a network and rejecting them if they do not conform to certain rules

 Firewall software may also facilitate logging of all data so that it can be traced.
 This allows automatic warnings to be generated.
 
 A more sophisticated firewall may examine the contents of each data packet.
 This is called stateful inspection and also involves the firewall examining where each data packet has come from. It keeps track of all open communication channels and therefore knows the context of each packet it receieves.
 
 **Stateful inspection** A technique for examining the contents of packets on a network and rejecting them if they do not form part of a recognised communication
 
### Proxy server

One security mesaure that can be used is a proxy server. By routing through a proxy server, there is no direct connection between the computer on the LAN and the Internet. Instead, all requests get passed through a proxy server and can be evaluated to ensrue that they cme from a legitimate source or to filter  users so that they only have access to specific websites.

### Private/Public key encryption

**Symmetric encryption** Where both the sender and receiver use the same key to encrypt and decrypt the data

The problem with symmetric encryption is that the the receiver must know the key. This is an inherent weakness with this system as if the key is intercepted is would be possible work out what it is, therefore making all further communications vulnerable.

**Asymmetric encryption** Where public and private key are used to encrypt and decrypt data

**Private key** A code used to encrypt/decrypt data that is only known by one user but is mathematically linked to a corresponding public key

**Public key** A code used to encrypt/decrypt data that can be made public and is linked to a corresponding private key

Suppose there are two computers A and B:
- A will have a private key known only to A
- A will also have a public key, mathematically related to the private key. Anyone can access it
- B will also have a private key and a related public key
- For A to send a secure message to B, A will first encrypt the message using B's public key
- As the private and public keys are related, the message can only be decrypted by B using B's private key
- As no-one else knows B's private key, even if the message were intercepted, it could not be decrypted

### Digital certificates and signatures

**Digital certificate** A method of ensuring that an encrypted message is from a trusted source as they have a certificate from a Certification Authority

**Certification Authority** A trusted organisation that provides digitaol certificates and signatures

Digital certificates, sometimes referred to as Secure Socket Layer certificates, were introduced to encourage people to do business on the Inernet, as many consumers were concerned about fraud.

Websites using digital certificates usually advertise the fact prominently on the site using the logo of the Certification Authority.

A digital signature is another method of ensuring the authenticity of the sender. 

**Digital signature** A method of ensuring that an encrypted message is from a trusted source, as they have a unique, encrypted signature verified by a Certification Authority.

Suppose A wants to send b a message with a digital signature:
- A hashes the message
- The hash is encrypted with A's private key
- The encrypted hash is appened to the message
- The message is encrypted using B's public key
- The encrypted message is sent to B
- B decrypts the message with B's private key
- B decrypts the hash with A's public key to get the original hash
- The decrypted message is hashed again, reproducing the message digest
- The message has not been tampered with if the decrypted message digest is the same as the reproduced digest

### Trojan

**Trojan** Malware that is hidden within another file on your computer

the distingushing feature of a Trojan is that it is hidden away inside another file and that it is not always obvious that a computer is infected.

The Trojan does not replicate itself in the same way as other malware, and can therefore remain undetected.

The Flam malware, is being classed as a new generation of superbug that is part Torjan, part worm, and part virus. It is quite large at 20MB. Once it has installed itself it has the capability to monitor network traffic, access data and programs, take screenshots, record converstaions, and monitor keystrokes.

### Viruses

**Virus** A generic term for malware where the program attaches itself to another file in order to infect a computer

The defining feature of a virus is that it replicates itself and can therefore cause extensive damage to  networks.

### Worms

**Worm** Malware or a type of virus that replicates itself and spreads around a computer system. It does not need to be attached to another file in order to infect a computer

### Protecting against malware

Users can attempt to protect their computers:
- Use anti virus software and other anti malware software, and keep it up ot date
- Keep the operating system up to date
- Use a firewall
- Do not open attachments or click on pop-ups
- Operate a white list of trusted sites
- Ensure sites use HTTPS, digital signatures, and certificates
- Use paswords on programs and files
- Encrypt data files

Programmers can:
- Select a programming language with built in security features
- Use recognised encryption techniques for all data stored within the pgoram
- Set administrative rights as part of the program and carefully control access and permission rights for different users
- Don't load up lots of Internet services unless they are needed
- Thoroughly test the code, specifically for known security issues
- Keep code up to date
- Never trust the user

System administrators can:
- Ensure that requests are coming from recognised sources
- Use a network firewall and use the packet filtering and sateful inspection techniques
- use encryption techniques and ensure digital certificates and signatures are used and are up to date
- Keep anti-virus software up to date
- Update the network operating system regularly




## Transmission Control Protocol and Internet Protocol

TPC/IP is made up of four main layers

| | 
| --- | 
| Application layer |
| Transport layer |
| Internet layer |
| Link layer |

- Layer 4- Application layer: The application layer ahndles the Domain Name System and a series of other protocols such as FTP, HTTP, HTTPS, POP£, ect. For example, incoming and outgoing data are converted from one format to another
- Layer 3- transport layer: this contains most of the configuration and coordination associated with the transmission that ensures that all the packets have arrived and that there are no errors in the packets. it also handles the way in which connections are made to create a path for data to travel between nodes. The sender and receiver are identified and the communication is set up, coordinated and terminated. Network resources are identified to ensure that they are sufficient for the communication to take place
- Layer 2- network or Internet layer: Defines the IP addresses of devices that send and receive data and handles the creation and routing of packets being sent and receieved
- Layer 1- Link layer: Provides synchronisation of devices so that the receiving device can manage the flow of data being received. It identifies what network topoloy is being used and controls the physical signals that transmit the strings of bits around the network. it also controls physical characteristics such as data transmission rates and the physical connections in a nework. On wireless networks it handles the CSMA/CA protocol

![Image](http://ebooks.dynamic-learning.co.uk/prod_content/extracted_books/9781471839559/OEBPS/images/348-2.jpg)

The highest level is closer to the user in that the processes are usually handled using either the operating system or application software. The lower layers are handled using a combination of hardware and software including the physical or wireless connections between devices. It is referred to as a stack because of the way in which the request from the client passes down through the layers of the protocol and then back up through the layers of the server side. This means that the last action that takes place in the Link layer on the client computer becomes the first action in the Link layer on the server.

### Hypertext Transfer Protocol (HTTP) and Secure HTTP (HTTPS)

**HTTP** A protocol for transmitting and displaying web pages

**Client-server model** A way of implementing a connection between computers where one computer makes use of resources of another computer

**HTTPS** An encrypted HTTP protcol

Hypertext refers to the fact that web pages will have hyperliks to other files.

### File Transfer Protocol (FTP)

**FTP** A protocol for handling file uploads and downloads

File transfer can be anonymous or non-anonymous depending on whether you need to identify yourself before the download.

### Secure Shell (SSH) Protocol

**Secure Shell (SSH) Protocol** A protocol for remote access to computers

SSH is used to improve the security  of remotely controlling a computer.
It does this partially by creating a secure network of nodes through which the access is made available. Public key encryption is used and login details are normally required.

### Simple Mail Transfer Protocol (SMTP) and Post Office Protocol (POP3)

**SMTP** A protocol for sending emails

**POP3** A protocol for receiving emails

Where the data cannot be sent, SMTP uses a queuing system to hold the email and attempts to send it at a later time. After a set number of times, it will send a message back to the sender notifying them of the delivery failure.

POP3 is used to check for incoming mail on port 110.

### Email and web servers

**Email server** A dedicated server for handling email

**Web server** A dedicated server for handling web content

- Email server: This machine typically has a large storage capacity for storing a database of all the network users and their email addresses. Specific software on the server is used to handle the storage and transmission of emails, allowing users to access their emails regardless of what other services are available
- Web server: This server hosts a website and handles traffic from users to the site.  Data stored on a web server may be in various formats, including text, scripts, and multimedia content. Web servers will make use of various protocols to ensure that all of these data are correctly handled and formatted

### Web browsers

**Web browser** An application for viewing web pages

When a web page is loaded, a request is made to the DNS, which translates the URL to an IP address. The IP address is then used to access the web page host. The host then serves the web page to the browser on the client. 
When a web page is loaded, the browser may cache it allowing it to br reloaded without having to make repeated requests.

## The client-server model

In a small network, there may be a single server where all of the programs and data are stored.
It is more likely however, that there will be several servers on a network serving hundreds of clients.

- File server: Contains any type of file, including programs
- Web server: Used to serve web pages on an Intranet
- Proxy server: Each client is provided with a gateway to the Internet through the server
- Print server: All client print requests are sent to the same server where they are prioritised, buffered, and then printed
- Database server: Used to store the contents of databases and access the data for individual clients
- Application server: Used to execute all of the procedures need to run applications

### Application Program Interface (API)

**Application Program Interface (API)** A set of subroutines that enable one program to interface with another program

An API defines the way in which programs can work together. 
One of these is the websocket protocol, which creates a connection between the client and the server. The client first sends a handshaking request to the server. In response the server creates a full duplex connection on a single socket. This allows simultaneous exchange of data in both directions enabling the client and server to communicate on an ongoing basis without the need to constantly refresh.

**Websocket protocol** A protocol that creates a persistent connection between two computers on a network to enable real-time collaboration

**Message** The name given to a packet of data being transmitted using the websocket protocol

### CRUD and REST

The four main processes required with databases can be defined with the CRUD acronym:
- C: Create
- R: Retreive
- U: Update
- D: Delete

It also refers to the way in which data is actually displayed and reported on via the user interface. All databases conform to the CRUD principle however they are designed.

**REST (Representational State Transfer)** A methodology for implementing a networked database

REST is a deisgn methodology for networked database applications. It uses the HTTP protocol to carry out each of the four CRUD operations.

| CRUD | SQL | HTTP |
| --- | --- | --- |
| Create | INSERT | POST |
| Retreive | SELECT | GET |
| Update | UPDATE | PUT |
| Delete | DELETE | DELETE |

![REST](http://ebooks.dynamic-learning.co.uk/prod_content/extracted_books/9781471839559/OEBPS/images/356-3.jpg)


The REST model
- The client makes a request to the server
- The service requested is the database identified by its URL, which uniquely identifies the resource on the server and contains the database query
- The API is run from the serve and accessed by the browser to coordinate processes between client and server applications
- HTML files are used to ensure data is displayed in the correct format on the client side
- Requests and data are transferred using HTTP
- JSON (JavaScript Online Notation) or XML (Extensible Markup Language) are used to return the results of the query

### JSON and XML

**JSON (JavaScript Online Notation)** A standard method for transmitting data

**XML (Extensible Markup Language)** A method of defining data formats for data that will be transmitted around a network

JSON is a data format originally created as part of JavaScript, but now available as a standalone format. It is defined as human-readable and is made up of an object and values.

JSON is a compact code that is very easy to understand and implement. It is also easy for computers to parse as each object and value is clearly define and described on each line.

XML is a markup language that defines how data is encoded. 

#### JSON vs XML

| | JSON | XML |
| --- | --- | --- |
| Readability | Very easy to read as it is defined as objects and values | More difficult to read as it contains tags |
| Size | Less data used | Requires more code than JSON |
| Parsing | Quicker than XML as data is clearly defined | Slower than JSON as data has to be extracted from tags
| Creation | Easier to create as syntax is simpler | More knowledge required for creation |
| Extendibility | Limited range of data types | Complete freedom over data types used |

### Thin vs thick clients

**Thin client** A network where one computer contains the majority of resources, processing power, and storage capacity

**Thick client** A network where resources, processing power, and storage capacity are distributed between the server and clients

**Terminal** A computer that has little or no processing power or storage capacity and is used as a client in a thin client network

#### Thin client model

| Advantages | Disadvantages |
| --- | --- |
| Easier and cheaper to set up new clients | Clients are dependent on the server |
| The server can be configured to distribute all required resources | Can slow down with heavy use |
| Changes need only be implemented in one place | May require greater bandwidth to cope with client requests |
| Easier for network manager to control clients | Powerful servers are expensive (Initial cost) |
| Greater security as clients have fewer rights | |

#### Thick client model 

| Advantages | Disadvantages |
| --- | --- |
| Reduced pressure on the server leading to greater uptime | Reduced security if clients can download software and access the Internet directly |
| Clients can store programs and data locally, giving them more control | More difficult to manage and update as new hardware and software must be installed on each machine |
| Fewer servers and lower bandwidth can be used | Data is more likely to be lost on the client side |
| Suitable for tablets and movile phones that require more processing and storage to be done server side | Can be difficult to ensure data integrity when many clients are working with local data |



# Databases 

**Relational database** A method of creating a database using tables of related data, with relationships between the tables

**Table** A method for implementing an entity and attributes as a group of related data 

## Entities

**Entity** An object about which data is stored

**Attribute** A characteristic or piece of information about an entity, which would be stored as a field in a relational database

### Entity relationship diagrams

**Entity relationship diagram** A visual method of describing relationships between entities

The name of the entity is shown in the box with the lines indicating the nature of the relationship.
Labels are usually added above the lines to clarify the relationship.

When creating a relational database, you should replace any many to many relationships with one to many relationships using an entity in between.

## Primary key and entity identifier

**Primary key** An attribute that can be used to uniquely identify every record within a table

**Entity identifier** An attribute which can uniquely identify each instance of an entity

- Use a unique attribute: Sometimes there is an attribute that is already unique, such as national insurance numbers
- Create a unique attribute: A unique code or identifier could be created for each entity. Some relational programs have an autonumber which automatically creates the number
- Use a composite key- Two or more attributes could be used in combination. For example name and address, although it is still possible that this process could create duplicates

## Foreign key

**Foreign key** An attribute in a table that is a primary key in another table and is used to link tables together

## Normalisation

**Normalisation** The process of ensuring that a relational database is structured efficiently

- Redundant data occurs when the same field is unnecessarily duplicated in two or more tables. For example, many different customers may download the same movie. If all the movie details were stored every time it was downloaded, much of the data would be redundant as we only need to store the details once and then link those details to each customer who downloaded it
- Storing the same data multiple times can also lead to the problem of data inconsistency, for example we might store the same customer's details several times but the telephone number stored might differ
- Storing data at an atomic level means that they cannot be further decomposed. For example, a table may contain an attribute called *Address* that stores the full address of the customer. At an atomic level this could be decomposed into several attributes, for example *HouseNumber*, *Street*, *Town*, *Country*, etc.

When a database is constructed according to these rules it is said to be in normal form.

there are various levels of normal form and the level that a programmer needs to go to depends on the complexity of the database.

### First normal form

First normal form is achieved by ensuring that a table does not containing repeating attributes or repeating groups and that all of the data in the table is atomic.

| CustomerID | CustomerName | Address | Date | MovieID | Title | Genre | Format | FileType |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | John Smith | 1 street 1 | 19/03/15 <br>19/03/15 | 1 <br>2 | The Hangover<br>22 Jump Street | Comedy<br>Comedy | LowRes<br>LowRes<br> | MPEG-2<br>MPEG2 |
| 2 | Mary Jones | 2 street 2 | 19/03/15<br>19/03/15<br>19/03/15 | 3<br>4<br>2 | The Hunger Games<br>Robocop<br>22 Jump Street | Sci-Fi<br>Sci-Fi<br>Comedy | HiRes<br>HiRes<br>LowRes | MPEG-4<br>MPEG-4<br>MPEG-2 |

- This is not first normal form because there are repeating groups, which are shown in the *Date* and *MovieID*, *Title*, *Genre*, *Format*, and *FileType*. A repeating group of values is stored in a particular row/column intersection in a database table instead of a single value.
- To satisfy first normal form, the repeating groups should be replaced by creating one record for each download 

| CustomerID | CustomerName | Address | Date | MovieID | Title | Genre | Format | FileType |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | John Smith | 1 street 1 | 19/03/15 | 1 | The Hangover | Comedy | LowRes | MPEG-2 |
| 1 | John Smith | 1 street 1 | 19/03/15 | 1 | 22 Jump Street | Comedy | LowRes | MPEG-2 |
| 2 | Mary Jones | 2 street 2 | 19/03/15 | 1 | The Hunger Games | Sci-Fi | HiRes | MPEG-4 |

etc

- If a customer downloads more than one movie there will be multiple records for the same customer.
- Each download can now be uniquely identified with a composite key made up of *CustomerID* and *MovieID*, so this could be made into the primary key. It is possible that one customer could download the same movie again, in which case this primary key would not be adequate.


### Second normal form

Second normal form is achieved by ensuring the database is in first normal form and then removing attributes that depend upon part but not all of the primary key by creating additional tables.

The non-key attributes are all the other attributes apart from the primary key.
For example *Address*, *DateOfDownload*, *Genre*, *FileType* are non-key attributes. To be in second normal form, any non-key attributes that depend upon part but not all of the primary key should be removed to another table.
For example, the *Address* of the customer is dependent on the *CustomerID*, but not on the *MovieID*.
Similarly, the *Genre* is dependent on the *MovieID* but not on the *CustomerID*. S, both *Address* and *Genre* are examples of attributes that depend on part but not all of the primary key.
This means that separate tables are needed to store the customer data and the movie data.

| CustomerID | CustomerName | Address | Date | MovieID |
| --- | --- | --- | --- | --- |
| 1 | John Smith | 1 street 1 | 19/03/15 | 1 |
| 1 | John Smith | 1 street 1 | 19/03/15 | 2 |
| 2 | Mary Jones | 2 street 2 | 19/03/15 | 3 |
 etc
 
 Movie table:
 | MovieID | Title | Genre | Format | FileType |
 | --- | --- | --- | --- | --- | 
 | 1 | The Hangover | Comedy | LowRes | MPEG-2 |
 | 2 | 22 Jump Street | Comedy | LowRes | MPEG-2 |
 | 3 | The Hunger Games | Sci-Fi | HiRes | MPEG-4 |
 etc
 
 When we split the initial table into two tables, we keep the *MovieID* attribute as a foreign key.
 Every non-key attribute in the movie table depends on the whole of its primary key, so this table is now in second normal form
 
 The customer download table is still a problem as the primary key for this table would be a composite key made up of the *CustomerID* and *MovieID*.
 Together these two fields form a primary key as they would be unique to each record, because we have assumed that a particular customer will only download the same movie once.
 The table is not in second normal form because it contains attributes that depend upon part, but not all of the primary key.
 For example *CustomerName* depends on *CustomerID* but not *MovieID*.
 
 The solution is to split the table into a customer table and a download table.
 
 Customer table:
 | CustomerID | CustomerName | Address |
 | --- | --- | --- | 
 | 1 | John Smith | 1 street 1 |
 | 2 | Mary Jones | 2 street 2 |
 etc
 
 Download table:
 
 | CustomerID | MovieID | Date |
 | --- | --- | --- |
 | 1 | 1 | 19/03/15 |
 | 1 | 2 | 19/03/15 |
 | 2 | 3 | 19/03/15 |
 etc
 
 The customer table now has the *CustomerID* as the primary key. The two other attributes depend on the whole of the primary key. This table is now in second normal form.
 
 The only attribute in the download table depends on both of the keys.

### Third normal form

Third normal form is achieved by ensuring the database is in second normal and then removing non-key attributes that depend upon other non-key attributes by creating additional tables.

In the movie table, it can be noted that *FileType* depends upon the *Format*.
Therefore, the non-key attribute *FileType* depends upon the non-key attribute *Format* so we can split the information off from the movie information to create two new tables.

 Movie table:
 | MovieID | Title | Genre | Format | 
 | --- | --- | --- | --- |
 | 1 | The Hangover | Comedy | LowRes |
 | 2 | 22 Jump Street | Comedy | LowRes |
 | 3 | The Hunger Games | Sci-Fi | HiRes |
 etc

Format table:
| Format | FileType |
| --- | --- | 
| LowRes | MPEG-2 |
| HiRes | MPEG-4 |

Both of these tables are now in third normal form.
- Movie table: All of the non-key attributes are directly dependent on the primary key
- Format table: There is only one non-key attribute so the table must be in third normal form
- Customer table: The *address* and *name* attributes both depend on the *CustomerID* and not on each other
- Download table: There is only one non-key attribute so the table must be in third normal form 


# Structured Query Language

*SQL* A specialised language that is used for managing relational databases. Its functions allow users to define tables, insert, update, and delete data and to carry out queries on data to produce and output subsets of the main data. 

Data types:
| Type | Explanation |
| --- | --- |
| Character(n) | Character string with fixed length (n) | 
| Varchar(n) | Character string variable length with maximum length (n) |
| Boolean | True or false |
| Int | An integer value |
| Decimal(p, s) | A decimal number with a number of digits before and after the decimal point |
| Real | Any number to 7 decimal places |
| Date | In the format day, month, year |
| Time | In the format hour, minutes, seconds |

## Entering and updating data

To enter data, the name of the table and column are required.

```SQL
INSERT INTO Customer (CustomerID, Name, Address)
VALUES ("1", "John Smith", "1 street 1");
```

This will create a row of data in the Customer table entering the details.
An alternative syntax can be used where every field is being entered:

```SQL
INSERT INTO Customer 
VALUES ("1", "John Smith", "1 street 1");
```

To update data, the table and column must be specified, and the item to update must be identified.

```SQL
UPDATE Customer
SET Address = "some new address"
WHERE CustomerID = "1";
```

## Deleting data

Deleting data is similar to updating data, in that it uses a where clause to specify which items are to be deleted.

```SQL
DELETE FROM Customer

WHERE CustomerID = "1";
```

Wildcards can also be used to match all records

```SQL
DELETE * FROM Customer;
```

```SQL
DELETE FROM Customer;
```

## Querying data

**Query** A search or sort carried out on data that retrieves the answer to a question

```SQL
SELECT CustomerName, CustomerAddress
FROM Customer
WHERE CustomerName = "John Smith"
ORDER BY CustomerName Desc;

```

*SELECT* Identifies the columns which are to be extracted. Where the columns are from more than one table and if the field is used in more than one table it is necessary to include the name of the table followed by a full stop and the name of the column.

*FROM* Indicates the table or tables that are needed to extract the data. In the case that is more than one table, the tables should be in a comma separated list.

*WHERE* Indicates the condition which must be met. If there are no conditions the *WHERE* statement can be excluded.

## Client server databases

**Client-Server database** An implementation of a database where the database is put into a server and various users can access it from their workstations. The processing will take place on the server

**Database management system** Software that enables the management of all aspects of a database including adding, updating, and querying data

### Issues with concurrent access on shared databases

One common problem with a database that is accessible to a number of users is what to do if a number of users are attempting to access the same data at the same time. As long as they are only reading the data, this is not a problem, but as soon as a user wants to write the data there will be a problem.

**Record locks** One solution to these problems is to lock the data. As soon as a user with write access takes an item of data a lock is put on that data item so that no other user can save to that location, and the second person will not be able to save their version of the data without acknowledging that the data may have been altered by another user.

**Serialisation** This is the process of only allowing transactions on a particular database to take place one at a time. If another transaction is taking place on a record while a user attempts to read the data, serialisation ensures that the transactions take place one after each other in the correct order.

**Timestamp ordering** Every transaction that takes place on the database will have a read and a write timestamp that indicates the last time that the record was written to or read from. To ensure serialisation, the timestamp can be used as a method of sequencing the transactions. to avoid concurrency issues where two transactions are taking place on the same record at the same time, the DBMS can use the timestamp to identify the last action that took place and it will us a protocol to decide whether to execute the current transaction or not based on the timestamp.

**Commitment ordering** This system looks at each command it has been asked to execute on the database in terms of when it was made but also whether it should take precedence over other commands. This depends on the nature of the command and what the impact of it is on the database. For example, where a command from one user could cause deadlock, it would be blocked until the dependent action was completed.

# Big data

**Big data** A generic term for large or complex datasets that are difficult to store and analyse

Uses of big data:

- Scientific research: This data may be readings from weather sensors, data collected from telescopic observations, biological results of experiments or global statistics on health issues

- Retail: Online retailers use data to improve the performance of their business. Sales data allows trends to be spotted

- Banking: The banking sector has to keep transaction data secure and have an audit trail of every single transaction to prevent against loss and fraud

- Government: The NHS records every single patient appointment and operation.

- Mobile networks: There are an estimated 4.6 billion mobile phone contracts around the world.

## H1N1 and Google

Google set up their own big data project called Google Flu Trends, which analysed real-time data of searches being made relating to flu. By matching the geographical location of searches, it would be possible to predict areas where flu is prevalent or spreading on a daily basis.

## Structured and unstructured data

Most databases work on the model that the data will fall into columns and rows.

### Structured data

This data can be defined using traditional database techniques using fields and records. It is possible to give each data item a field name and type.

**Structured data** Data that fits into a standard database structure of fields and records

### Unstructured data

This data cannot be defined in columns and rows. This might include multimedia data, web pages, and the contents of emails, documents, or presentations.
It is important to note that although each of these types of data have their own structure, they do not fit easily into the standard database structure therefore making it difficult to analyse the contents of the data

**Unstructured data** Data that does not fit into a standard database structure of fields and records

## Machine learning techniques

Qualitative data is much harder to analyse and is most likely to be unstructured.
Techniques collectively known as machine learning are used to automate the process of analysing qualitative data.

In the context of written feedback on a product, a machine could learn to look for patterns of words within a text in determining the nature of the feedback. In order to do this it would need to be programmed with words or phrases to look for.

A more advanced system would be where the computer is able to develop its own knowledge based on the data that it is manipulating. This is particularly valuable in the context of big data as there may be patterns and correlations that exist within the data that are not immediately obvious.
One technique, called predictive analysis, is widely used in the financial and insurance sectors to predict risk.

### CAIS
The Credit Account Information Sharing database stores over 400 million records of credit transactions, from bank loans to overdrafts. This information is used by banks and other lenders to determine whether a customer has a good or bad credit history and to identify the level of risk associated with that customer.

## Issues with big data

- Datasets are so large that they are too difficult to store and analyse
- Unstructured data can be very difficult to analyse in an automated way
- Specialised software is needed to manage and then extract meaningful information about the data
- Massive storage and processing power is needed, requiring supercomputers or large dedicated networks
- Data are constantly changing so it is difficult to keep track of every change
- Finding a correlation in a dataset does not necessarily mean that the solution has been found
- There is an issue with concurrency where several users are working on the data at the same time

## Modelling big data

**Modelling** Recreating a real-life situation on a computer

**Graph schema (database)** A method of defining a database in terms of nodes, edges, and properties

**Node** In database modelling, a node is an entity

**Properties** In database modelling, it is items of information stored within each entity

**Edge** In database graph schema, it refers to the link and relationship between two nodes

## Distributed processing

**Distributed processing** The principle of spreading large and complex tasks over a number of computers or servers

**Distributed program** A program specifically written to be used in a distributed processing environment

### Functional programming for distributed programs

**Variable** A data item whose value will change as the program is run

**Mutable** Changeable

**State** Refers to the state that the variables are in

**Side effects** The fact that the value contained within a variable will change as the program is run, which has implications for other parts of the program

**Imperative language** A language based on giving the computer commands or procedures to follow

**Object-oriented langauge** A programming paradigm that encapsulates instructions and data together into objects

**Function** A subtroutine that returns a value

**Concurrence** The concept of two users trying to access the same data item at the same time

# Functional programming

The functional programming paradigm is an example of a declarative programming language where all the algorithms call functions. This means that the lines of code look and behave like mathematical functions, requiring an input and producing an output.

There is one main function, which in turns calls further functions in order to achieve a specific task. 

**Functional programming paradigm** A language where each line of code is made up of calls to a function, which in turn may be made up of other functions, or result in a value

**Declarative programming languages** Languages that declare or specify what properties a result should have

**Procedural programming languages** Languages where the programmer specifies the steps that must be carried out in order to achieve a result

In functional programming:
- Program requirements may be better defined as a series of abstractions based on functions rather than a more complex series of steps
- Broader abstractions can lead to fewer errors during implementation
- functions can be applied at any level of data abstraction making them highly re-usable within a program
- Functional code is easier to test and debug as each function cannot have any side effects
- There are no concurrency issues as data is modified by two threads at the same time
- In multi processor environments the sequence that functions are evaluated in is not critical

## Function types

A function type refers to the way in which the expression is created. All functions are of type $A \to B$ where it is defined with an argument type $(A)$ and a result type $(B)$


## First class objects and higher order functions

**First class object** Any object that can be used as an argument or result of a function call

**Higher order function** A function that takes a function as its inputs or creates a function as its output

A function which can accept another function as an argument is a higher order function.
The three most common of which are map, fold, and filter.

## Function application

**Function application** The process of calculating the result of a function by passing it some data to produce a result

## Partial function application

**Partial application** The process of applying a function creating an intermediate function by fixing some of the arguments to the function

## Function composition

**Function composition** Combining two or more functions together to create more complex functions

## Higher order functions

**Map function** A function that generates an output list from an input list by applying a function to each element in the input list

**Filter function** A method of creating a subset based on specified criteria

**Reduce or fold function** A method of reducing a list to a single element by combining the elements using a function

## List processing


**Head** the first element in a list

**Tail** Every element in a list after the head




# Aspects of software development

## Analysis

**Analysis** The first stage of system development where the problem is identified, researched, and alternative solutions are proposed

# From the book

### Defining the problem

Having identified that there is a problem with an existing system or perhaps seeing a new area that needs developing, it is very important to keep an open mind and concentrate on getting gto grips with what the problem involves rather than looking for possible solutions.
This involves identifying the scope of a problem and being realistic about how much of the problem a new system can solve.
Any constraining factors may be identified here.

If you are creating a solution for someone else, it is important that you agree the specification and the scope of the work before you start. 
In general, the more you can involve the end users, the less likely you are to do something they do not want.

### Prompts for a new system

There are many reasons for creating a new computer system.
Many of these are based on the ever-increasing demands that are made of existing system and the ever-changing advances in computer technology.

- Some existing systems simply cannot cope with the increased volume of data that they are being asked to handle. For example, the way in which a bank maintains its data has changed beyond all recognition in the last 20 years, and banks have spent millions of pounds updating their systems
- New technology has meant that existing systems soon become outdated. For example, at one time it took a lot of time and effort to book a holiday. Now it can all be done in real time with the flights you want booked in minutes
- The current system may be inflexible or inefficient. For example, the number of people flying is increasing every year and this has placed pressure on the airport immigration authorities. Computer-readable passports allow immigration staff far greater control and instant access to details of the person in front of them
- New technology has created new opportunities. You have only to look at the way the use of the Internet has exploded to realise how many new opportunities such as e-commerce and e-banking there are. Other developments such as computer control and GPS have created other totally new fields. For example, cards are becoming increasingly automated. Current technology enables cars to park themselves
- Commercial reasons. Many new systems are created in order to generate demand from customers. There isn't necessarily a need for a new system but companies introduce them because customers will buy them
- New platforms and operating systems. Businesses create new systems to take full advantage of new platforms and operating systems. For example, thousands of new apps have been created for iOS and Android devices
- Increased processing power. As processing power increases, new software is written to take advantage of it. Some applications that are processor intensive may become feasible with the advent of faster processors.
- Increased network power. Many applications are developed to take advantage of ever increasing connectivity. For example, many of the leading applications written over the last few years have been based on social media

## Methods of gathering information

If the problem that you care going to tackle is based on an existing system then it may be worthwhile investigating how it currently works, though there are times when a completely fresh approach to a problem might lead to a better solution.
Asking for opinions about a possible new system is a good idea too.
there are several ways in which you can gather data about an existing system:
- Interview people who are involved with the current system. This will probably include the systems administrator, the people actually using the system, and their customers or clients. Although this can be a time-consuming process, talking to people who are actually using the existing system will give valuable first-hand knowledge and you can follow up on any comments that they might make. A drawback is that each person you talk to may give you a very personal view of the system
- Unless they are carefully structured the data collected from an interview can be hard to make use of. Asking someone to to fill in a carefully designed questionnaire or carrying out a survey will allow you to carry out a more accurate analysis of the responses, but these tend to restrict the data you gather to definite, closed answers. Questionnaires allow you to gather a lot of data relatively quickly
- Although it can be very time consuming, observation of current practices will help to identify problem areas. It is objective rather than subjective and you may spot something that everyone else has missed
- Examination of the current system including the files, paperwork and processes used will help to identify the data requirements of the new system. It will also help with the creation of the HCI of the new system. This process will also help you to see the overall scope of the problem

## Feasibility study

**Feasibility study** An analysis of whether it is possible or desirable to create a system

A feasibility study is a preliminary report to the person that asked for the new system in the first place. It will identify possible solutions and suggest the best way forward. The report will indicate how practical a solution is in terms of time and other resources, such as the availability of suitable software and hardware and the abilities of the end user to cope with the proposed method of solution.

Possible solutions might include doing nothing, having bespoke software written for you, writing software yourself or buying an existing package and tailoring it to your needs.

## Design

Before work can start on the actual creation of the solution, the availability of appropriate hardware and software should be assessed. The choice of hardware will be driven by the users' needs and by the way in which data will be manipulated and stored. Work will begin on the file structures and algorithms that are to be used.

Most big projects are far too large to be considered as one complete problem.
The best solution is often to break them down into smaller modules.
Each module will be self contained, and the programmer will test it on its own. This approach will allow more than one person to work on the solution. Often the view a user has of the system will need to be defined so that all the modules have the same 'feel'.

The process of looking at a big problem and breaking it down into smaller problems is top-down design.
The benefits of this approach are similar to the modular design system mentioned above, though there is the potential problem of getting too engrossed in small details such as the fine tuning of the interface.
It makes more sense to solve the overall problem first before considering screen layouts.

**Design** The second state of system development where the algorithms, data, and interface are designed

**Top-down design** Related to the modular approach, this starts with the main system at the top and breaks it down into smaller and smaller units like a tree

**Modular design** A method of system design that breaks a whole system down into smaller units or modules

## Data flow diagram

**Data flow diagram** A visual method of showing how data passes around the system

- A rectangle represents an external entity such as a user document
- A double ended silo shape represents validation
- An open ended rectangle with a segmented area represents storage
- An arrow represents the flow of data

## Describing algorithms

At this state, a description f the algorithms that will be used should be included. These will not be fully formed lines of code as it is only the design stage. For example, if search or sort algorithms are needed, they can be identified at this stage.

It may be appropriate to work the algorithms into pseudo-code that reflects the programming language being used. For example, if a functional programming language is being used, the main functions should be identified.
If a relational database is being used, them main SQL statements should be identified.

## Data dictionary 

**Data dictionary** A list of all the data being used in the system including name, length, data type, and validation

Details of the data to be stored, including the data type, length, title, and any validation checks, will be stored in a data dictionary.
this can be seen as a database about the database. It holds background details but not the data itself.

## Variables tables and data structures

It is important to decide what variables a program will need and what purpose they will serve. Some programming languages will only let the programmer use variables that have been declared. Declaring variables at the start of the program allows the programmer much tighter control of their program. The programmer will need to decide about certain characteristics of each variable, type, length, name, and whether the variable is local or global.

**Variables table** A list of all the variables that a program will use, including names and data types

## Volumetrics

The volume of data that a system will be asked to handle both now and in the future will have a bearing on how the programmer decides to store and handle the data. They will need to consider the throughput of data. How many transactions the system will need to cope with in a given time span, and also how much the data the system will need to store at any one time. This will affect the storage media that is used, and it will also be a consideration when backup strategies are being decided.
The programmer will also need to consider how many users will be will be allowed to access the files and programs at one time.

It is important to realise that the databases that most students see in their time at school or college are generally small. Even a pupil database in a school with 1200 pupils is very small compared to the high street banks which have millions of customers each with hundreds of fields of data stored about them.
The computers used by the DVLA store details of well over 20 million cars which means the planning needed for this project is very different to planning how the secretary of a swimming club will store their data.

## The human computer interface

The human computer interface is the term given to any form of communication between a computer and its user. For the majority of us this might seem limited to the computer screen with its familiar graphical user interface, but it can also include the layout of buttons on a mobile phone or house alarm system and the way information is presented on a tablet or smart phone or the flight controls of a new aircraft.

There are a number of aspects that need to be considered when designing an effective HCI:
- Ease of use: There is no point creating sophisticated software if the functions are hidden behind a series of screens and button presses. A good HCI will feel intuitive
- Target audience: What suits a child might not necessarily suit an adult so it is important that the programmer is aware of who the end user is going to be
- Technology: There is little point in creating a screen layout that works comfortably on a 21 inch screen if the target audience mostly use tablets and smartphones
- Ergonomics: The interface should be 'comfortable' to use. This is important if the user is likely to be sitting with the interface for a long period of time, for example, an airplane pilot or tele-sales operative

## Implementation

This stage is when the application is actually written creating the fully working system using the appropriate tools identified in the feasibility study, The process of implementing a system is based on the design, and the programmer(s)b will need to be fully aware of the requirements set out in the design. It is important to note that man systems are modular and that the different modules do not all have to be written at the same time. For example, some parts of the system may still be at the design stage while other parts are being implemented. In some cases one module is dependent on another one. In other cases, the design of one part of the system may change as a result of the implementation of another part.

**Implementation** The third stage of development where the actual code and data structures are created

It is important to realise that systems development has to be a responsive process and that the developer may need to respond to issues as they arise throughout the development process.

## Prototypes

Creating a solution to a problem can be very costly both in terms of finance and time. There is little point in presenting the end user with a completed project if they are going to ask you to alter various details. In this case it would be a good idea to produce a prototype.

**Prototype** A stripped down version of a whole system built at the design stage to test whether the concept works

The functionality of a prototype may vary depending on the nature of the project. For example, the human-computer interface may be very well developed in the prototype and quite closely reflect the finished system. However, the functionality behind it may be incomplete.

At this stage the user is asked to comment on the product so far, and the will check to make sure all the major functions work as expected.

## Testing


It is important that the system is tested to make sure it performs as expected. There are a number of test strategies that can be used and it is important to understand that any testing plant must include tests that are carried out as the code is written and not just at the end.

Test data are data that generates a known result, and test data will be need to be devised that tests every aspect of the solution from the expected responses to the extremes that humans can subject a computer program to.

As individual units or modules are completed they are teste to ensure they carry out the functions they contain. As the project proceeds, modules can be fitted together and at this stage integration testing takes place.
This process makes sure that the modules work together. A lot of these procedures make use of test data.

Typically, three types of test data are used:
- Normal: Data that the system is expected to handle as they are within the acceptable range
- Boundary: Data that are on the extremes of the acceptable range. This means testing the minimum and maximum values and those that are just inside and just outside the range
- Erroneous: Data that are clearly incorrect and therefore you would expect the program to catch the error

**Testing** The fourth stage of system development that includes a range of tests using a variety of data

## Development testing

Blackbox testing involves entering test data into a routine or procedure and checking the resulting output against the expected output

**Development testing** Testing that takes place during the development of the program

**Black box testing** Using test data to test for an expected outcome

**White box testing** Checks all pathways through the code, looking inside it and potentially adding extra commands to check what is happening

**Unit testing** Testing carried out on just one module or component of the whole system

White box testing involves testing every aspect of a routine or procedure. Whilst black box testing is concerned with testing the data handling, white box testing considers all the other processes that are involved- for example, how the program reacts if it fails to find a suitable printer. White box testing checks all pathways through the code, looking inside it and potentially adding extra commands.

Unit testing makes sure each unit carries out the function it has been designed for. It incorporates both black box and white box testing.

Once all units have been tested, they are put together to form bigger sections. Integration testing is the process of making sure that the different modules have been tested as individual units will work together.

## System testing

System testing involves testing the system as a complete unit rather than as individual modules and making sure that it satisfies the specification agreed with the user.

**System testing** A range of tests carried out on the system once it has been completed

Alpha testing is carried out on the finished system. This involves creating test data in-house. This test data will try to cover all the possible eventualities, so they will allow the system to be tested under normal conditions. 
The benefits of this process are that any problems that are found can be rectified before true live data are used by the end user. Another benefit of using a known set of test data is that if necessary the system can be stopped and restarted.

Some program developers will release an early or beta version of their new program to their potential users. At this stage the software is bound to have 'bugs' in it and the users are expected to send details of the problems they have encountered back to the programmers for them to resolve.

The benefits of this system are that passing your software to a number of people that have not been involved with the development will mean the testers will all use the system in slightly different ways and so highlight faults that might not have been found by normal means.

Although the developers will test the system they have developed as thoroughly as possible, it is the end users that need to be satisfied that the solution does what they wanted it to.
Acceptance testing is carried out by the intended user. They enter their own live data and make sure the system matches the specification that was agreed with the program writers.

Some problems may only come to light some time after the system has been implemented by the user. These might include issues involving the volume of data the system is asked to cope with. Problems such as these will be resolved as part of the systems maintenance.

## Evaluation

The final stage of the system development is evaluation. The solution that has been created was designed to match the specification that was agreed with the user. An evaluation compares the actual outcome with this specification. it should also contain suggestions for future improvements. it is these improvements and refinements that start off the whole cycle all over again. Evaluation may take place over an extended period of time. In fact, many systems are constantly being evaluated. There may be several criteria used to evaluate a system.

**Evaluation** The final stage of system development where the system is judged according to certain criteria

- Functionality: Does it do what it is supposed to?
- Ease of use: this is not the same as 'easy to use' but it means that the level of complexity is appropriate to the user
- Ease of implementation: How easy was it to transfer from the old system to the new system?
- Reliability: A measure of how much the system is 'up' or 'down'
- Performance: Does the system meet its performance criteria, which might relate. e.g. the speed of operation or the amount of data it can handle
- Cost effectiveness: Refers to how much it costs to implement the solution and whether the cost is justified
- Ease of maintenance and adaptability: How easy is it to fix faults or add new modules?
- Longevity: How future-proof is the system?



