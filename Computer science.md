

*Useful but forgettable*

<br>

**Meta**

https://www.tablesgenerator.com/markdown_tables

Note that markdown links cant have capitals   

Mark with TODO

[Math](#math)  
[Software](#software)  
[Hardware](#hardware)  


<br>

# Math

<br>

**Sum of Integers**  
https://youtu.be/6kvfvpatnn8?t=271

	x   x   x
	x   x   o
	x   o   o
	o   o   o

The rectangle above is equal to

        n
    2 x Σ i   
  	   i=1

which equal to length by width, or

	n(n+1)

Therefore

	 n
	 Σ i = n(n+1)/2
	i=1

<br>

**Sum of squares**  
https://www.youtube.com/watch?v=aXbT37IlyZQ

	 n
	 Σ i^2 = n(n+1)(2n+1)/6
	i=1

<br>

**Sum of cubes**  
( Sum of integers squared )
https://www.youtube.com/watch?v=X_6LLmj4_5I

	 n
	 Σ i^3 = n^2 (n+1)^2 / 4
	i=1


<br>

**Sum of odd numbers**  
https://www.youtube.com/watch?v=IJ0EQCkJCTc

	 n
	 Σ 2i-1 = n^2
	i=1

<br>

**Lagrange's four square theorem**  
https://leetcode.com/problems/perfect-squares/discuss/622567/Python-sol-by-math.-90%2B-w-Comment

Any natural number can be represented as the sum of four integer squares.

	n = a^2 + b^2 + c^2 + d^2

<br>

**Lagrange's three square theorem**  
https://leetcode.com/problems/perfect-squares/discuss/765682/Python3-math-and-dp

Any natural number can be represented as the sum of three integer squares, if n is not of the form 4^k(8m+7) for integers k and m

IE

	if n / ( 4**int(math.log(n,4)) ) % 8 == 7
		n = a^2 + b^2 + c^2

remember not to disqualify multiples of only one factor  
And for factors to a power, that there could be any number

<br>

**Two square theorem**
An integer greater than one can be written as a sum of two squares, if and only if,
its prime decomposition contains no prime congruent to 3 modulo 4 raised to an odd power. ( Just use brute force checking for this at O( √n ) rather than the theorem )

<br>

**Sum of a geometric sequence**

	 n
	 Σ r^i = (1 - r^(n+1)) / (1-r)
	i=0

1 + 3 + 9

	 2
	 Σ 3^i = (1 - 3^(2+1)) / (1-3) = -26 / -2 = 13
	i=0

<br>
<br>
<br>
<br>
<br>

# Software

**Notes for writing code**

Use git to save recent versions for large projects

Name functions starting with lower case

Name variables starting with upper case

Consider 

- Caching
- Reversing the problem

<br>
<br>

<br>
<br>


**Bash**
```console

PWD —> print working directory
LS —> list directories
CD —> change directory
. —> current directory
.. —> previous directory
... -> and so on

CLEAR —> clears terminal

MKDIR —> make directory

MV —> move or rename
TOUCH —> create file
OPEN —> open file
CAT —> concatenate, read code in terminal
RM —> remove
CP —> copy

Tab key —> autocomplete

```

<br>
<br>
<br>
<br>
<br>

**Git**

Use Git Graph in VSCode

```

git —> start of every command

status
	shows changes with added files
log
	shows commits

add <filename>
	add files to commit, none by default
	. —> all files
restore --staged <filename>
	Remove files after being added

commit -m “<message>”

```

<br>
<br>
<br>
<br>
<br>

**SQL**
```SQL
-- W R I T E

CREATE DATABASE databasename; -- create database
DROP DATABASE databasename; -- delete database
CREATE TABLE table_name ( -- create table and columns
column1 type,
column2 type constraint, -- column constraints are optional
....
);
DROP TABLE table_name; -- delete table
ALTER TABLE table_name ADD column_name datatype; -- add column to table
INSERT INTO tbl (clm1, clm2, ...) VALUES (val1, val2...); -- add a row to table
DELETE FROM tbl WHERE cond; -- delete rows from table
UPDATE tbl SET cml = val, … WHERE cond; -- update data

-- Types
-- https://en.wikipedia.org/wiki/SQL#SQL_data_types

-- Constraints
NOT NULL;
UNIQUE;
PRIMARY KEY;
FOREIGN KEY;
CHECK (inequality);
DEFAULT val;
CREATE INDEX indexName ON Table (Column);

-- R E A D

SELECT clm1, clm2 FROM tbl1;
	-- * can be used to select all columns

-- DISTINCT > a column needs a unique value to be shown
SELECT DISTINCT columns FROM tbl1;  

-- Conditions
SELECT clm1, clm2 FROM tbl1 WHERE clm1 = ‘String’;
SELECT clm1, clm2 FROM tbl1 WHERE clm1 % 2 = 1;
SELECT clm1, clm2 FROM tbl1 WHERE clm1 IN ('String','Str');
SELECT clm1, clm2 FROM tbl1 WHERE clm1 IS NULL;
SELECT clm1, clm2 FROM tbl1 WHERE clm1 IS NOT NULL;
SELECT clm1, clm2 FROM tbl1 WHERE clm1 LIKE ''; -- % > any characters, _ > char
SELECT clm1, clm2 FROM tbl1 WHERE clm1 BETWEEN num AND num;
	-- condition operators (don't need brackets)
	AND OR NOT

SELECT clm1, clm2 FROM tbl1 ORDER BY colm2 ASC; -- ascending
SELECT clm1, clm2 FROM tbl1 ORDER BY colm1 DESC; -- or descending order

SELECT MIN(clm1, clm2) FROM tbl; -- column mins
SELECT MAX(clm1, clm2) FROM tbl; -- column maximums
SELECT AVG(clm1, clm2) FROM tbl; -- column averages
SELECT SUM(clm1, clm2) FROM tbl; -- column sums

-- E X A M P L E

CREATE TABLE user_details (
	Email CHAR(25),
	Phone CHAR(12),
	Age SMALLINT
);

INSERT INTO user_details (Email, Phone, Age)
VALUES ('yes@no.com', '0123456789', 23);

SELECT * FROM user_details;

```

<br>
<br>
<br>
<br>
<br>

**Vim**

	i —> insert mode to the left of cursor
	a -> (append) insert mode the right of the cursor

	esc key -> command mode

		MOVE

		e -> end of a word
		b -> back one word
		w -> forward one word
		n —> do next command n times
		H —> top of screen
		M —> middle of screen
		L —> bottom of screen
		gg —> top of file
		G  —> bottom of file
		{ —> move up a block
		} —> move down a block
		A —> start insert mode at end of line
		I -> start insert mode at end of line
		n { }  —>  up and down blocks
		f <character> —> skips to next character
		t <character> -> skips to behind next character

		DELETE

		n dd  —> cut n lines
       		D -> delete to end of line
		diw —> delete inner word
		dt —> delete until the character next typed is found
		x -> delete cursor character

		UNDO REDO

		u —> undo
		ctrl r (not command) —>  redo

		COPY PASTE

		yy —> yank current line
		n yy —> yank the next n lines
		yt {}—> yank (copy) blocks of code
		p —> paste

		SEARCH AND REPLACE

		r<char> -> replace cursor character with new character
		/<chars> -> find characters
		/ term —> highlights terms
		:s/ <replaced> / <replace with> -> substitute 1 word on a line
		:%s/<init>/<fin>/gc —> substitute all (%) words globally (g) with confirmation (c)

		MISC

		o (lower)   —> add a new line below current and switch to insert mode
		O (capital) -> add a new line above current and switch to insert mode
		V —> visual mode, move up and down to highlight lines
			Shift < > —> indent

		FILE OPS

		:q —> quits
		:w —>writes
		:wq —> writes and quits


<br>
<br>
<br>
<br>
<br>

## Regex

	https://regexone.com/

	abc…	Letters
	123…	Digits
	\d	Any Digit
	\D	Any Non-digit character
	.	Any Character
	\.	Period
	[abc]	Only a, b, or c
	[^abc]	Not a, b, nor c
	[a-z]	Characters a to z
	[0-9]	Numbers 0 to 9
	\w	Any Alphanumeric character
	\W	Any Non-alphanumeric character
	{m}	m Repetitions
	{m,n}	m to n Repetitions
	*	Zero or more repetitions
	+	One or more repetitions
	?	Optional character
	\s	Any Whitespace
	\S	Any Non-whitespace character
	^…$	Starts and ends
	(…)	Capture Group
	(a(bc))	Capture Sub-group
	(.*)	Capture all
	(abc|def)	Matches abc or def
	\1      Back reference, matches what was in 1st capture group 
	match(?=a)    Positive lookahead, only matches if immediately followed by pattern a
	match(?=.*a)  Positive lookahead, only matches if followed by pattern a
	match(!=a)    Negative lookahead, matches if not immediately followed by pattern a
	match(!=.*a)    Negative lookahead, matches if not followed by pattern a
	(?<=a)match      Lookbehind

Apply in python
```python

import re

text = "Go ahead and watch the trailers for Avengers: Endgame, they won't give anything major away. It's amazing for a huge movie to be so self-aware of itself, as well as, the movie genres that they're overtly borrowing from."

text = text.lower()
pattern = r"[a-zA-Z']"
sub = ''

re.findall(pattern, text) # returns list of matches
re.search(pattern, text) # returns struct if in, use as bool
re.sub(pattern, sub, text) # returns string with matches swapped for sub


```

<br>
<br>
<br>
<br>
<br>

## De morgan's laws
```Python
not (a or b) # is the same as
(not a) or (not b)

not (a and b) # is the same as
(not a) and (not b)
```

## Complexity

A function describing algorithm resource use dependent on the number of inputs, with a specific input.

This measure is better than running tests, because

- it is hardware independent
- it creates a continuous comparable functions, rather than error prone data points
- it can compare run times with inputs numbers that might not be feasible to test

Depending on specific inputs to the algorithm this complexity can change.

<br>

## Asymptotic analysis
Sometimes called Asymptotic bounding

An analysis of [Complexity](#**complexity**) graphs and what functions can be asymptotic to them.

The most common functions, in higher order, are

	1 <
	  log(n) <
	 sqrt(n) <
	n <
	n log(n) <
	n^x <
	x^n <
	n!

(Remember that n is an integer, so n^2 is never smaller than n as it would be on a continuous graph)

Any complexity graph has lower, exact and upper bounding functions, and in asymptotic analysis we find functions that tightly bound the complexity graph, as a way to compare growth to other functions.

- O is upper bounding function
- Θ exists if the same function with different constants can be the lower and upper bound
- Ω is the lower bounding function  

<br>

## Best, worst and average case
Depending on the inputs to a function, the complexity of an algorithm can change, such as when a sorting algorithm has to sort an already sorted list.

<br>

## Amortized time
Average time
Amortized analysis is used for algo­rithms that have expensive opera­tions that happen only rarely. Say when appending to a list with no space, that means you need to create a new list.


<br>

## Algorithm
In mathematics and computer science, an algorithm is a finite sequence of well-defined, computer-implementable instructions, typically to solve a class of problems or to perform a computation.

<br>

## Divide and conquer
Splitting and Base case

<br> 

## Decrease and conquer
Removing and Base case

<br>

## Greedy algorithm
Algorithms which always take the best short term solution, which in many cases will still results in the global minimum

<br>

## Memoization
Storing the results of expensive function calls and returning the cached result when the same inputs occur again.

<br>

## Linear search
Searching one after another until an match is found

<br>

## Binary search
A recurrent search algorithm that works on sorted sets by halving sorted elements with  < >  comparison operators. Implemented with a [Binary search tree](#binary-search-tree).

<br>

## Depth & Breadth first search
Depth uses a [Stack](#stack), where the search starts from the newest node, and so goes deep.
Breadth uses a [Queue](#queue), where the search starts from the unearthed node found first, and so goes broad, one link away from the origin at a time.

<br>

## Minimum spanning tree algorithms
Algorithms to find
a subset of edges in a graph, which connect all nodes with the minimum weighted distance.

<br>

**Prim's Algorithm**
From a random starting node, while not all nodes have been reached, pick the shortest connection from any of the joined nodes which leads to a new node.
https://www.youtube.com/watch?v=cplfcGZmX7I

<br>

**Kruskal's Algorithm**
From a minimum weighed edge, while not all nodes have been joined, pick the smallest weighted connection that connects to one or two new nodes.
https://www.youtube.com/watch?v=71UQH7Pr9kU&list=PL9xmBV_5YoZObEi3Hf6lmyW-CBfs7nkOV&index=2

<br>

## Dijkstra's algorithm
Finds the shortest path between two vertices in a [Graph](#graph)  

- The start vertex takes 0 time and you start by assuming every other vertex takes infinite time to get to it ( This is the same as saying you don't know how long it will take, but this is easier when updating to the shortest time )

- From the node you are on, travel along its paths and put the time it takes to move to each from the start which is the distance to the node you are standing on and the path you travel, updating if you find a shorter time

- Then, moving to the shortest node from the start, and repeat the last step until you are at the vertex you want to be at

The path can be kept track of by having an arrow pointing to the where the shortest path is from

<br>

## A* graph search
An improvement of [Dijkstra's algorithm](#dijkstra's-algorithm) which takes into account general direction by taking into account the distance to the end node, alongside to the start node.
Usually used on grids rather than the traditional graph.  
https://www.youtube.com/watch?v=-L-WgKMFuhE

<br>

## Sort

**Bubble sort**
Largest Items bubble to the top  

**Selection sort**
Smallest items sink to the bottom

**Insertion sort**
Inserts each element into a sorted area in the list, in the right position  

**Merge sort**
https://www.youtube.com/watch?v=4VqmGXwpLqc  
Divides and merges sorted lists

**Heap sort** https://www.youtube.com/watch?v=k72DtCnY4MU  
Creates a max or min [heap](#heap) and extracts values  

**Quick Sort** https://www.youtube.com/watch?v=Hoixgm4-P4M  
Like binary search, this algorithm splits everything up

<br>

## 	Data structure

A data structure is a particular way of organizing data in a computer so that it can be used effectively.

<br>

## Implicit data structure
A [Data structure](#data-structure) which uses positioning as a way to carry information about a values position in the underlying representation.
Formally, an implicit data structure is one with constant O(1) space overhead
An example is a list representing a [Binary Search Tree](#binary-search-tree)

<br>

## Data type
An attribute of data which tells a compiler how to interpret and process it.

<br>

## 	Abstract Data type
A data model which provides only a limited interface to the underlying implemented [Data structure](#data-structure).
https://en.wikipedia.org/wiki/Abstract_data_type

<br>

## List
[Abstract data type](#abstract-data-type)  
Sequential elements represented by sequential memory addresses

<br>

## Graph
[Abstract data type](#abstract-data-type)  
A set of nodes possibly joined with edges

Represented in memory with...

- **Adjacency matrices** > An n^2 matrix with a boolean in each point to represent if a node points to another or itself, or both ways on an undirected graph
- **Edge sets** > A set of length e, with contains each directional edge
- **Adjacency lists** > A list of n length containing lists of which nodes a particular node points to

Properties ...

- **Directed** > Graphs with directions one or both ways between connected nodes
- **Acyclic** > No graph cycles
- **Cyclic** > Contains Graph cycles

<br>

## Tree
An acyclic [Graph](#graph) where all nodes are connected to a root leading out to leaf nodes.

<br>

## Binary Tree
A [Tree](#tree) with at most two edges connected to each node.

	Full      >  Each node has either 0 or 2 children.
	Complete  >  Nodes are filled in top to bottom, left to right.
	Perfect   >  Full and complete.

<br>

## Binary Search Tree
A BST is a [binary Tree](#binary-tree) where each node is greater than its left child and less then its right.

https://www.youtube.com/watch?v=LU4fGD-fgJQ  
A tree is balanced if the maximum difference between the number of subtree child nodes is 1 or 0.

	Binary search trees draw correctly are in order from left to right

	     4
	   /   \
	  2     6
	 / \   / \
	1   3 5   7

<br>

## Binary tree traversal
[Binary Tree](#binary-tree)

http://yt.dudzik.co/watch/?v=9Kjn_5Wc69M

Left is always before right


1: Breadth first traversal (level order)

2: Depth first traversal - including...

	Preorder  - Root Left Right > OLR
	Inorder   - Left Root Right > LOR
	Postorder - Left Right Root > LRO

	Each of these can be described by just the order placement of the root



Different orders are used for different things

- Tree copies are made using Preorder (OLR) traversal
- Reading a sorted array out of a [binary search tree](#binary-search-tree) uses Inorder traversal
- Freeing a tree uses Postorder traversal


<br>

## AVL tree
[Binary Search Tree](#binary-search-tree)

http://yt.dudzik.co/watch/?v=5C8bLQBjcDI

http://yt.dudzik.co/watch/?v=u3OVSkuOdqI


A balanced [Binary search tree](#binary-search-tree)

To keep the tree balanaces a balance factor is stored for each node where

BF(node) = HeightOf(node.right) - HeightOf(node.left)

such that HeightOf is the number of edges to the furthest leaf

For each node, the magnitude of the balance factor is kept <= 1
through a series of rotation operations

Rotations can work on either 2 or 3 nodes

Rotations are visually similar to draging the nodes as a rope around the head node as a pivot point

Left rotations go counter-clockwise

Right rotations go clockwise


	LR imbalance > 2-node left rotation on 1 ( turns into LL )
	   3
	 /
	1
	 \
	  2

	LL imbalance > 3-node right rotation on head
	    3
	   /
	  2   
	 /
	1

.

	RL imbalance > 2-node right rotation on 3 ( turns into RR )
	1
	  \
	   3
	  /
	 2


	RR imbalance > 3-node right rotation on head
	1
	 \
	  2
	   \
	    3

<br>

## Red black Tree
[Binary Search Tree](#binary-search-tree)

https://www.youtube.com/watch?v=qvZGUFHWChY  
A balanced [Binary search tree](#binary-search-tree) with a guaranteed height of O ( log n ) for n nodes.  
- A node is either red or black
- The root node is black
- Nil nodes are black
- If a node is red, its children are black
- All paths from Root to Nil contain the same number of black nodes

<br>


## 2 3 4 Tree
[Tree](#tree)

A node has either 2 3 or 4 elements

TODO

<br>


## B Tree
[Tree](#tree)

https://www.cs.usfca.edu/~galles/visualization/BTree.html

Optimized for systems that read and write large blocks of data. It is most commonly used in database and file systems.

A B-tree of order m has at most m children and m - 1 keys,
and all root nodes have to be at the same level

They have the same property as [Binary Search Trees](#binary-search-tree) where they are in order looking from left to right

	    | 2   4 |
	   /    |    \
	|1|   | 3 | | 5 6 |

If a node has too many elements, the middle value is shifted up

<br>


## B+ Tree
Derived from [B trees](#b-tree)

TODO

https://dichchankinh.com/~galles/visualization/BPlusTree.html



<br>

## Stack
[Abstract data type](#abstract-data-type)  
Last in First out  
Implemented include using a [Linked list](#linked-list). )

<br>

## Queue
[Abstract Data Types](#abstract-Data-Types)  
First in First out.  
Implemented include using a [Linked list](#linked-list).

<br>

## Priority queue
[Abstract data type](#abstract-data-type)  
important first out  
Implemented include using a [heap](#heap)

<br>

## Double ended queue
[Abstract data type](#abstract-data-type)  
Either last or first in can be first out

<br>

## Segment Tree
A [Binary Tree](#binary-tree) for finding the minimum or maximum values in a range. A max tree is below and shows each node represents the maximum for its children.


	    9
	   /  \
	   8  9
	 / |  | \
	3  8  9  0

<br>

## Trie
Strings stored as [Tree](#**tree**) character paths

<br>

## Prefix sum
A running sum [Arrays](#array) or Lists of floats or integers in a corresponding list, which allows for the sum of values from index a to b in that list to be achieved in constant times

O(N) to update

https://en.wikipedia.org/wiki/Prefix_sum
In a flat array of numbers, you can either store the elements, or the prefix sums. In the first case, computing prefix sums requires linear time; in the second case, updating the array elements requires linear time (in both cases, the other operation can be performed in constant time).

<br>

## Array
[Implicit data structure](#implicit-data-structure).   
Sequential elements in memory with a single data type and which can represent multidimensional data by storing extra data on the shape of the array..
## Linked List
[Data structure](#data-structure)  
Sequential elements represented by value pointer pairs, where pointers point to the next value in the list.  

Variations
- singly linked lists have one way directed pointers
- doubly linked lists have two way directed pointers.
- circular linked list, tail next points to head
- Skip list, multiple links to allow for O(log n) read

<br>

## Heap
[Data structure](#data-structure)  
https://www.youtube.com/watch?v=AE5I0xACpZs  

A complete [Binary Tree](#binary-Tree) stored as an array where for max heaps, no child is greater than its parent.  

For Insertion new nodes are placed in the next available position, and then swapped with their parents until they are less in value than them, retaining the node value requirement.

For deletion you delete the root,
and move it down by swapping it with the greatest child element greater than itself.

A min heap is the reverse of this

<br>

## Dictionary

[Hash](#hash)  

Also called hash tables.  
A key is hashed and the using modulus the remainder of the a division by the length of the array becomes an array index where the value is stored.
Allows for O( 1 ) retrieval time.

Some of the ways of addressing collisions include

Open addressing > placing an item at a position different than the hash

Linear probing > The value goes to the next available position in the set length array

Closed addressing

Linked list collisions > If there is a collision, then the array index will be set as the first link in a linked list.


<br>

## Prefix sum
A running sum [Arrays](#array) or Lists of floats or integers in a corresponding list, which allows for the sum of values from index a to b in that list to be achieved in constant times

O(N) to update

https://en.wikipedia.org/wiki/Prefix_sum
In a flat array of numbers, you can either store the elements, or the prefix sums. In the first case, computing prefix sums requires linear time; in the second case, updating the array elements requires linear time (in both cases, the other operation can be performed in constant time).

<br>

## Fenwick tree
[Binary tree](#binary-tree)  
Also called a Binary indexed Tree

https://en.wikipedia.org/wiki/Fenwick_tree
https://www.youtube.com/watch?v=v_wj_mOAlig

It allows both updating and prefix sums in O( log n ) time.

13 = 2^3 + 2^2 + 2^0  
SUM_TO(13) = SUM_RANGE(1,8) + SUM_RANGE(9,12) + SUM_RANGE(13,13)

<br>

## Paradigm
A style of programming

<br>

## Object Oriented Programming
[Paradigm](#paradigm)

OOP is writing code around the idea of object properties and actions.

Encapsulation > Creating a sealed class which controls reading and writing variables and calling functions for intended use

Inheritance > How a class that is a subset of another class avoids writing duplicated shared methods, IE class Developer(Human): ...

Polymorphism > "Many forms", The ability of an object to identify as more than one class

Abstraction > A simplification of a mental model IE going from logic gates to an adder circuit

Static methods > Don't require a class instance

Class methods > Operate on every instance of a class

Abstract class > A class only used for child classes to inherit from, and which is not instantiated.

<br>

## Functional programming
[Paradigm](#paradigm)  
Create Pure functions where the output should only depend on its inputs and not effect outside variables. This allows for parallelization, as functions can run at the same time without affecting each other.  

<br>

## Declarative programming
[Paradigm](#paradigm)  
Code which focuses on the end product rather than how it is created. A description rather than a recipe.

<br>

## Imperative
[Paradigm](#paradigm)  
Describing the steps

<br>

## Procedural programming
[Paradigm](#paradigm)  
Steps, one after the other in logical order.

<br>

## Logic programming
[Paradigm](#paradigm)  
Programming based on formal logic, including languages such as Prolog.

<br>

## Programming language
A human readable syntax used to write code which is converted to machine readable code to run.

<br>

## Pass by value
Copies of values are made when they are used as the inputs to a function

## Pass by reference
Pointers to values are passed as the inputs to a function, and inside of a function modifies the value if it used outside of that scope


<br>

## Source code
Human readable which represents machine code

<br>

## Byte code
Compressed [Source code](#source-code) which can be optimized for a specific machine before being executed

<br>

## Machine Code
Binary that can execute on a computer’s physical processor without further translation.

<br>

## Interpreter
Interpreting a [Programming language](#programming-language) is executed code with each line.

<br>

## Compiler
A Compiler converts the [Programming language](#programming-language)  Human to OS machine code as a whole and  then executed

<br>

## AOT
[Compiler](#compiler)  
Ahead Of Time compilers convert from human to machine readable before run time are the most common and intuitive compiler implementation.

<br>

## JIT
A Just in time [Compiler](#compiler) converts from human readable code to byte code for distribution, and then is converted to machine code with each computer for better optimization.

<br>

## Explicit conversion
When a type is converted explicitly in code.

int( "1234" )

<br>

## Implicit conversion
When a type is converted by the compiler without explicit instruction in code. This conversion retains information and so the new type takes more memory than the previous type.

2+"3" = "23"

<br>

## Strong or Weak typing
A continuous spectrum that compares how flexible (weak) or rigid (strong) programming languages are using implicit conversion.

<br>

## Dynamic / Static typed languages
Dynamic typed programming languages check for types during run time, "on the fly". Static languages check for types when they compile, and so are faster in run time.

<br>

## Call stack
https://en.wikipedia.org/wiki/Call_stack  
A [Stack](#stack) implemented to store values in the order a program will use them.

<br>

## Literal
A fixed value which is assigned to variables or printed, and whose type is defined in syntax.

<br>

## Primitive data types
Primitives data types are built into the language, and are not imported or added on

<br>

## Operator
https://en.wikipedia.org/wiki/Operator_(computer_programming)  
Operators are constructs defined within programming languages which behave generally like functions, but which differ syntactically or semantically.

Function: add(x,y)  
Operator: x + y  

**unary** One input  
**binary** Two inputs  
**ternary**  Three inputss  

<br>

## Relational operators

Constructs a True or False relation between two entities  
IE 4<8 or 4=4 or 3<1  
which evaluate to a boolean value

<br>

## Logical operators

operators which map some boolean values to other boolean values

False and (anything) automatically goes to false

<br>

## Application
Code directly applicable to the user.

<br>

## OS
Operating System  
Code to run other 1st or 3rd party applications.
With multiple applications it consequentially needs the ability to switch between them, and manage shared resource use if they run at the same time.
With 3rd party applications it likely enforces proper hardware use and provide common services to 3rd party developers.


<br>

## Kernel
Software that interfaces directly with hardware

Kernels are responsible for creating an environment for applications that abstracts from the hardware by implements standardization in networking, drivers and storage for example, and allocates limited hardware resources.

Kernel mode software is code executed with unrestricted access to hardware
User Mode software has limited hardware access, so an application can't just use all the device resources for example.

**Micro kernels** have different programs for each aspect of importance running at user level, which are all controlled by a central authority at the kernel level, which is kept to a minimal size. This has the advantage of not crashing the kernel if one aspect crashes.

**Monolithic kernels** run everything at the kernel level and have improved performance by nearly a power of magnitude, as they avoid context switching and message calls

<br>

## Virtual machines
Software that emulates dedicated hardware.

Created using Hypervisors

Bare metal (Type 1) hypervisors operate to emulate bare metal hardware for optionally multiple operating systems using portions of the resources of a single computer

Hosted (Type 2) hypervisors create an OS inside of another OS as an application, commonly called a virtual machine

<br>

## serverless

A term which describes on demand use of servers by a provider which are setup and maintained by them. Serverless is just used to describe that you don't have to use your own physical server

<br>

## SaaS

Software as a Service provides

- Application hosting

and everything under [PaaS](#paas)

## Faas

Function as a Service provides

- On demand function computing

and everything under [PaaS](#paas)

## PaaS
Platform as a Service provides

- Developer tools  
- Operating systems

and everything under [IaaS](#iaas)

Why do you need an operating system without a user, can't you just run machine code???

## IaaS

Infrastructure as a Service provides  

- Compute
- Storage
- Physical housing
- Networking and Security  

## Serverless

Where you rent a server or on demand computing from a provider, rather than buying, setting up and maintaining your own

<br>

## Daemons

From https://en.wikipedia.org/wiki/Daemon_(computing)  
Name is inspired by Maxwell's demon  
"We fancifully began to use the word daemon to describe background processes that worked tirelessly to perform system chores"  
A further characterization of the mythological symbolism is that a daemon is something that is not visible yet is always present and working its will.  

Described a background process which runs in the background without the oversight by the user

<br>

## Hash
A hash maps any input of varied size to an, ideally always, unique value.

A hash function such as SHA256 will take a key and output a hash code.
Over the range of possible hash codes, hash functions are designed to spread these out to avoid collisions, but at the same time the function is not random and the same key will always result in the same hash code being deterministic.

<br>

## Encryption
https://www.youtube.com/watch?v=GSIDS_lvRv4  
https://www.youtube.com/watch?v=vsXMMT2CqqE  
A process that converts text into nonsensical cipher-text, which can only be decrypted by people with a numerical key, for use in sending information when communications can be intercepted.

<br>

## Symmetric Encryption
Where the message is encrypted and decrypted with the same key, and so needs to be transferred between parties. The key needs to be securely shared, but this method is faster than [Asymmetric Encryption](#asymmetric-Encryption)

<br>

## Asymmetric Encryption
Also called Public key Encryption

https://www.youtube.com/watch?v=AQDCe585Lnc  
https://www.youtube.com/watch?v=vsXMMT2CqqE  

Everybody has a public and private key.

Messages encrypted with your recipients public  key can be decrypted by them only.

Messages encrypted with your private key can be decrypted by anyone, but only sent by you.

Messages can be encrypted multiple times, and so use both of these properties to secure a message and verify a sender.

<br>

## proof of work
Trust which ledger has the most computational work, which is the ledger with the most blocks verified with a rare hash property that needs to be found with trial and error search by adding numbers to a block to change the hash.
The blocks are also linked by placing the hash of the previous block at the top of the block when a new one is mined, making the chain interdependent.

A 51% attack is when a majority of computational power is being used to verify the fraudulent fork of the ledger blocks.

<br>

## Cryptocurrency

" Many cryptocurrencies, like Bitcoin, may not explicitly use sending of such secret, encrypted messages, as most of the information that involves Bitcoin transactions is public to a good extent. "

The basis for all cryptocurrencies is a distributed ledger which tracks the positive account balance of a set of users, by tracking a list of payments for which each user sending money has to sign with a digital signature.
This solves the double spending problem.

A balance is defined by the ledger, you can't change your balance without adding to the ledger and either taking or giving money to someone else.
This is in contrast to banking systems where the balance is stored as a Integer number of cents, that can easily be changed with no clear sign of wrongdoing.

But there can be willful ignorance of payments, that can divide the ledger, so we need proof of which ledger is legitimate.

https://www.youtube.com/watch?v=bBC-nXj3Ng4

<br>

## Proof of stake and deposits
Chooses a user based on their balance, to create a security deposit sum greater than the total sum exchanged in the block. The block is then forged with the users signature and the user receives fees and a reward. The user risks losing their deposit and future rights to forge blocks if the block is found to be fraudulent.

<br>

## Containers
A container is a software package that consists of all the dependencies required to run an application

Docker is software for distributing software in the same environment it was made in, to avoid configuration issues, and has replaced using  [[Virtual machines]], by  only creating the parts of the OS that an application, not the user, interacts with.

https://stackoverflow.com/questions/30632386/is-docker-a-solution-for-making-application-cross-platform

How is docker faster than virtualisation???

<br>

## Container orchestration
A way to scale and maintain [Containers](#containers) automatically

<br>

## Microservices
Splitting up cloud services between [Containers](#containers) to them scale for their different workloads
This also isolates one service from crashing others

<br>

## CI CD
Continuous Integration and Deployment or Delivery

CI > Merge continuously and avoid merge conflicts.

CD > Automatic the process from commit to testing to deployment, to save time for developers, to have up to date software, and to have change be continuous.

STEPS
- Developers commit changes to Source Control Management
- Whole application is built / compiled and tested
- Continuous delivery stops here and would wait for human action, while continuous deployment would deploy now

<br>

## Primary keys
The index of a unique rows in a database to describe an entry

<br>

## Relational databases

A database system in which any field can be a component of more than one of the database's tables.

IE

An order references a customer in another table, rather than having multiple and possible conflicting data entries in the order table, as these details can change over time.
The customer's country is specified in the customer table by again, a reference to another table.

A relational database avoids duplicating data which takes up more space and can be conflicting

<br>

## NoSQL

https://www.youtube.com/watch?v=0buKQHokLK8  
https://www.youtube.com/watch?v=W2Z7fbCLSTw

NoSQL databases are not relational

**key–value pair**  
Uses a [Dictionary](#dictionary)  
Used a a cache because you can't store on the disk ???

**wide column**  
A key-value pair database where each key can point to multiple entries or even groups  

**document**  
Just a collection of literal documents, which provides complex flexibility

[**Graph**](#graph)  
Nodes contain data and directional edges are relationships

**Search engine**  
Where results are linked to

**Multi model**  
Uses where applicable, multiple database models to get the best performance

**Column vs Row Oriented Databases**  
[Operating system blocks](#operating-system-blocks)  
https://www.youtube.com/watch?v=XNrsRVMfj1c  
Depending on if a database stores entries or columns together in blocks, the read performance can vary depending on how many blocks need to be read

<br>

## Operating system blocks
An operating system block is the minimum unit of data that the operating system can read or write.
Why are there operating system blocks???

<br>

## Foreign keys
A primary key in a foreign table, to create linked data

<br>

## AI / ML
Artificial intelligence or Machine learning is mimicking the ability of biological brains to learn.

<br>

## Neural network
A network of real or digital neurons which learn to respond to stimuli or data.

<br>

## Moravec's paradox
Moravec's paradox is the observation by artificial intelligence and robotics researchers that, contrary to traditional assumptions, reasoning requires very little computation, but sensorimotor skills require enormous computational resources

<br>

## Backpropagation
A process of changing weights in a [Neural network](#neural-network) based on how much each contributed to a wrong answer, which is calculated using derivatives.

<br>

## Vanishing and Exploding gradient problem
The product of many numbers less than one approaches 0.  
The product of many numbers more than one approaches infinity.  
As earlier weights in the network have a number of derivatives that are multiplied together to determine how the weight should be updated, the value of these weights can limit or overshoot the optimal value.

<br>

## Perceptron
Essentially a better version of y = m x + b for splitting data
https://www.desmos.com/calculator/ya2muxcbq3

<br>

## RNN
A Recurrent neural network is a [Neural network](#neural-network) whose outputs feed into future inputs, and which so are able to process variable size time series data.

<br>

## LSTM
A long / short term memory neural network is a [RNN](#rnn) which mitigates the [Vanishing gradient problem](#vanishing-gradient-problem).
An LSTM has a continuous memory which is processed by the 'forget' multiplication and 'remember' addition operations. This memory always continues to the next time step, but is also duplicated to and processed by a 'relevant' multiplication operation to be added to only the next time step. Each of these operation is decided by trained neural networks and some parts of the network are normalized.

<br>

## GRU
A Gated recurrent unit is a [RNN](#rnn) which mitigates the [Vanishing gradient problem](#vanishing-gradient-problem).
Similar to an [LSTM](#lstm), only without the hidden state, making them simpler and faster to train, although they are both suited to different cases.

<br>

## Transformer
A Gated recurrent unit is a [RNN](#rnn) which mitigates the [Vanishing gradient problem](#vanishing-gradient-problem) and memory loss through weighted focused as introduced in the 'Attention is all you need' paper.

<br>

## CNN
Convolutional [neural network](#neural-network)  
To convolute is to blur, which is intuitively is mapping a number of values to less. Doing this repeatedly, with trained feature detectors, will allow machine to complete tasks including image content identification or depth perception.

<br>

## Auto encoder
Unsupervised  
An autoencoder is an architecture to train one [neural network](#neural-network) to encode data into characteristics (a lower dimensional representation) and another to decompress the characteristics into the original data.

<br>

## GAN
Generative Adversarial Network  
Consists of a Generative network, which creates model data from random or relevant inputs, and a Adversarial model to determine if the data which it is fed is real or generated. The Generative network is trained to minimize the certainty which the Adversarial model thinks it's data is modeled, and the Adversarial model is trained to distinguish this. This allows realistic modeled data to be created for things such as photos. A naive approach would directly train the network to model data, which would result in the average and not a realistic case.

<br>

## Hopfield net
[neural network](#neural-network)  
A neural network which retrieves data with part of that data fed into the network.

<br>

## Finite State machines
A system of states and transitions
IE 
A pen nib can be in the retracted or out states and pressing a button is a transition between these
You can represent this and more complex systems with state transition diagrams

<br>

## Halting problem

Decision problem > Is there an algorithm to find conclusions from premises? Are there problems computers can't solve?

Halting > If a computer ever outputs an answer to a problem

Halting problem > Given a computer program and an input, will the program halt?

This problem is solved by using a hypothetical computer which solves the Turing problem, and changing its outputs so that as a new whole machine it creates a contradiction.

https://youtu.be/macM_MtS_w4?t=274

So if the machine halts, the yes output causes it to not halt, and if it doesn't halt the no output halts.
This means the modified and hence base computer which solves the halting problem cannot exist.

<br>

## Recursion
A function calling itself

<br>

## Dynamic programming
[Recursion](#recursion)
[Memoization](#memoization)

- 1 Recursion
- 2 Memoize (store computed values)
- 3 Top down or Bottom up

**Bottom up** > Base case and work up  
**Top Down**  > Memoization and Recursion to work down

<br>

## P vs NP
http://yt.dudzik.co/watch?v=u2DLlNQiPB4

<br>

## Premature optimization
Optimizing that delays finishing a working product, as when the optimization...

- will become deleted code as the program changes, and will go unused in the program
- won't be a bottleneck to needed performance, and will go unnoticed by the user
- makes it slower to write more code, and will be a hindrance to development

<br>

## Invariant
Something that doesn't vary and which is always true.

<br>

## Loop Invariant
A loop invariant is a statement about program variables that is true before and after each iteration of a loop.

<br>

## Function overloading
A function is defined multiple times with different input types.
Also called polymorphism

<br>

## language syntax

Arrangement and order of symbols of language

<br>

## language semantics



The meaning of the words and phrases in a language

<br>

## Expression

An expression expresses a value and so evaluates to something
For example, x=5 in python wouldn't be an expression because it wouldn't evaluate to anything, while x==5 would

<br>

## Assembly

In computer programming, assembly language, sometimes abbreviated asm, is any low-level programming language in which there is a very strong correspondence between the instructions in the language and the architecture's machine code instructions.

<br>

## Function parameters
Degrees, Range, Abs
## Function arguments
180, [-360, 360], 4

<br>

## errors  
[Programming language](#programming-language)  

Syntax > The programming language cannot interpret the code you have written

Run-time > When your code is running, it executes something that the programming language or operating system decides should raise an error, if the operation doesn't make sense or could damage hardware

Logic > Code doesn't do what it is supposed to do



<br>
<br>
<br>

# Hardware

## Sequential access memory

Where the basic method of accessing data is sequential, 
usually due to the physical design of the storage which has a single reader. Examples include

- Magnetic Tape
- CDs
- Hard disk



## RAM
Random access memory - Can be read in any order
