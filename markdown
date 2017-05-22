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

**Subroutine|Procedure|Subprogram|Routine** A name block of code designed to carry out a specific task

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



# Communication and networking

## Communication

## Networks

## The Internet

## Internet security

## Transmission Control Protocol and Internet Protocol

## The client-server model

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



