<br>

Useful but forgettable 

<br>

**Meta**

https://www.tablesgenerator.com/markdown_tables

Search for definition: "# WordToDefine"

<br>
<br>

# Code

<br>

**Python**
```python

#                                                   CONVENTION

b.a() # usually modifies values and returns None
a(Input) # returns calculated values
b.a # returns stored value


#                                                   NUMERICAL

x * y # mul
x ** y # exp
x % y # mod
x ** 0.5 # sqrt
import math 
math.sqrt(64)
math.log(64,2) 
True + 10 # 11 through implicit conversion
not 48 # 0 through implicit conversion


#                                                   BASE

int(Num, Base) # revert to base 10 
binary = bin(10) # '0b1010'
1-bit # NOT
bit^1 # NOT
not bit # NOT
& # AND      
| # OR      
^ # XOR ( only either ) 
decimal << int # SHIFT left
decimal >> int # SHIFT right
hexadecimal = hex(10) # '0xa'


#                                                   TYPES

dir(type) # find type methods

float
	Float = 5.0
	
	# Methods
	bool( Num % 1 ) # test if float has decimals
	def ceil(x): return int(x+bool(x%1)) # round up without importing

int 
	Int = 2

list
	# ordered, iterable
	List = [1]

	# Methods

	List.append(Element)
	List.insert(index,Element)
	List.extend(Iterable)
	List = zip(List) # [1,2],[3,4] > [(1, 3), (2, 4)]

	from numpy import prod; prod(NumList)
	from math import prod; prod(NumList)

	*Iterable # *["a","b"] == "a","b"
	
str 
	# ordered, immutable, iterable
	string = "123" 
	string = f"This is an F string which easy add values like {x} into"

	# Methods

	eval("1+2") # 3

	ord(Character) # unicode integer
	ord(Char) - ord('a') + 1 # lower case alphabetic position
	ord(Char) - ord('A') + 1 # upper case alphabetic position

	string.istitle() # is title capitalization
	string.isupper()
	string.islower()
	string.isalpha() # is all letters
	string.isnumeric() # is all numbers
	string.isalnum() # is alpha numeric 
	string.upper() # changes all letters in string to upper case
	string.lower() # changes all letters in string to lower case

tuple
	# ordered, immutable
	Tuple = (1,)

	x,_,z = ('x',2,'z') # _ avoids assigning  
	x,*_,z = ('x',2,2,3,2,'z') # *_ is any number of values 

	# https://www.youtube.com/watch?v=GfxJYp9_nJA
	from collections import namedtuple
	rgb = namedtuple('color', ['red','green','blue'])
	offWhite = rgb(183, 185, 167)
	print(offWhite.red)

set
	# unique elements, unordered, iterable
	Set = set(List) = {1}

	# Methods
	.union(Iterable)
	.difference(Iterable, Iterable, ...) # in set and not other iterables
	.symmetric_difference(Iterable, Iterable, ...) # values not shared
	.intersection(Set2, Set3, ...)  # using & is cleaner
	.add(Element)
	.update(Iterable)
	.discard(Element)
	.remove(Element) # throws error if not present

	dict 
		# unique elements, unordered, iterable
		Dictionary = {}
		Dictionary = {1:None} 
		Dictionary = {x:i for i:x in enumerate(Iterable)}

		from collections import Counter
		Dictionary = Counter(Iterable)
		Dictionary.most_common(n_most_common) 

		from collections import defaultdict 
		Dictionary = defaultdict(int)

		# Methods

		dic["key"] = 31
		dic["key2"] +=1
		dic.popitem()

		Dictionary.keys()
		Dictionary.values()
		Dictionary.items()

#                                                   METHODS

Type + Type # string list int float
del Dict_or_List[Location] # dict list
Pop = Iterable.pop() # list set dict

# string list
Iterable = sorted(Iterable) 
Iterable.sort() 
Iterable.sort(reverse=True)
Iterable[0:2]
Iterable[::n] # every nth item
Iterable[::-1] # reverse iterable
Iterable.index(element)

# generators string list set dict
reversed(Iterable)
max(Iterable) 
min(Iterable)
sum(Iterable)


#                                                  CONTROL FLOW 



if Condition: Code ...
if Condition: return # doesn't need else after

while Condition: print("while")
for i in range(5, 10): print(i) # Use start
for i, x in enumerate([13,5,29]): print(i, x) # Use enumerate (i before x)
for i in range(len(Iterables)-1,-1,-1): print(Iterables[i]) # Use different steps
for a,b in zip(listA,listB): print(a,b) # use zip for multiple lists

	# Methods
	break 
	continue # next i


#                                                  FUNCTIONAL

def Bool_function(Element): return Element>5
list(map(Bool_function, Iterable)) 
list(map(lambda Element: Element>5, Iterable)) 


#                                                   SHORTHAND

x = y = 1
x, y = 9, 3
Iterable[1], Iterable[0] = Iterable[0], Iterable[1] # no temp
x += y # works for all operators
x = x//y # x = int( x/y )
Assigned = True if Bool else False  # one line if else
"repeat "*3 # 'repeat repeat repeat '
[0]*3 # [0,0,0]


#                                                   OOP

class Animal():
    def __init__(self, Age, ):
        self.Age = Age

    def birthDay(self):
        self.Age += 1

class Human(Animal):
	def __init__(self, Age):
    	super().__init__(Age) # Alternative to below
		# Animal.__init_(self)

Tom = Human(20) # instance
Tom.birthDay()
print(Tom.Age)


#                                                  	MEMOIZATION

from functools import cache, lrucache     

@lrucache(maxsize=2)
def fib(n):
	if n <= 1: return n
	return fib(n-1)+fib(n-2)

@cache
def expensive_computation(n):
	...


#                                                  MISC

float('inf') # infinity without importing
sorted( arr, key=lambda Num: (abs(Num), Num, ...) ) # sort with multiple conditions in the same iterable
[x for _, x in sorted(zip(Y, X), key=lambda pair: pair[0])] # sort based on other iterables
sorted(List)[:n_largest] # better than repeated min and max
"".join(Str_Iterable) # ["a","b"] --> "ab"
plus_plus = lambda x: x+1 # lambda just defines a function; plus_plus(2) = 3
__main__ # magic methods   
1_000 # _ makes large numbers easier to read
In = input("optional message")
@decorator 

```

<br>
<br>
<br>
<br>
<br>


**c++**
```c++

// Hello world

#include<iostream>
int main() {
    std::cout << "Hello world";
}
/*
    before the name of the function is the returned type
    main() returns an int as returning 0 signals no errors
    newer compilers return 0 from main implicitly
*/

// VERSION -----------------------------------

int main() {
	if (__cplusplus == 201703L) std::cout << "C++17\n";
	else if (__cplusplus == 201402L) std::cout << "C++14\n";
	else if (__cplusplus == 201103L) std::cout << "C++11\n";
	else if (__cplusplus == 199711L) std::cout << "C++98\n";
	else 							 std::cout << "pre-standard C++\n";
}

// TYPES -----------------------------------

int main() {
    short bytes = 5
    int integers[bytes] = {1, 3, 5} 
	auto AnyType;
}

#include<vector>
int main() {
    vector<int> = {1,2,3}
    vector<vector<int>> = {{1,3}{2,4}}
}

#include <string> 
int main() {
    const char* name = "John Smith"; // save static string
	std::string name = "John Smith"; // save static string	
	std::short = name.length(); // number of characters
	std::string = name.substring(0,4); // save part of a string
	std::string_view first_name(name.c_str(), 4); // create pointer to string
}

// POINTERS -----------------------------------

int main() {

}

// NUMERICAL -----------------------------------

#include<iostream>
#include<cmath>
int main() { 
    std::cout << sqrt(2) << std::endl; 
    std::cout << pow(2,8) << std::endl; 
    std::cout << round(-3.7) << std::endl; // closest integer
    std::cout << floor(-3.4) << std::endl; // integer towards neg inf 
    std::cout << int(-3.4) << std::endl; // integer towards zero 
    std::cout << fmax(1,3);
    std::cout << fmin(1,3);
}

// LOGIC OPS ----------------------------------- 

#include<iostream>
int main() { 
    std::cout << (true & true);  // & --> AND
    std::cout << (true | false); // | --> OR
    std::cout << (!false);       // ! --> NOT
}

// CONTROL FLOW ----------------------------------- 

if (Bool) {}

switch (value) {
    case possible_value: print("1") break
	case another_possible_value: print("2") break
}

for (i=0;i<Int;i++) {} // sep with ;
while (Condition) {}

// overloading function to support multiple types
int plusFuncInt(int x, int y) { return x + y; }
double plusFuncDouble(double x, double y) { return x + y; }

// S H O R T  H A N D -----------------------------------

int one, two; // declare variables with shared type 
y += x 
y++ // y+=1
x-- // x-=1

// INPUT  -----------------------------------

#include<iostream>
int main() { 
    std::cin >> character;
    std::cout << character;

    getline(cin, string)
    std::cout << string;
}

// -----------------------------------
```

<br>
<br>
<br>
<br>
<br>

**Java**
```Java
// Hello world
class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!"); 
    }
}

for (i=0;i<Int;i++) {} // sep with ;
while (Condition) {}

```

<br>
<br>
<br>
<br>
<br>

**Javascript**
```Javascript
console.log('Hello World');

```

<br>
<br>
<br>
<br>
<br>

**Swift**
```swift
// test
@main
Bool
```

<br>
<br>
<br>
<br>
<br>

**Bash**
```console
	*not caps sensitive*
	https://www.youtube.com/watch?v=41LdR8kuLDs

	PWD —> print working directory
	LS —> list directories
	CD —> change directory
	.. —> previous directory

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
```
https://learngitbranching.js.org/
https://www.youtube.com/watch?v=mJ-qvsxPHpY

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

checkout <Commit hash> 
	change commit position
	add n~ to move to the parent n times 

branch <new branch name>
	(doesn't checkout)
checkout -b <new branch name>	

merge <chain> 
	merge checkout and specified chain into new commit
rebase <chain>
	checked out chain is moved onto specified

reset <head> 
	moves head to new position to effectively remove a commit
revert
	creates a commit that reverses the previous commit

GITHUB

git push origin <branch name>
git pull origin <branch name>

REMOVE GITHUB HISTORY
git checkout --orphan latest_branch
git add -A
git commit -am "rm history"
git branch -D main
git branch -m main
git push -f origin main
```

<br>
<br>
<br>
<br>
<br>

**SQL**
```SQL
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

-- W R I T E

	INSERT INTO tbl (clm1, clm2, ...) VALUES (val1, val2...); 
	UPDATE tbl SET cml = val, … WHERE cond;
	DELETE FROM tbl WHERE cond;
```

<br>
<br>
<br>
<br>
<br>

**Vim**

	i —> insert mode

	esc key -> command mode

		MOVE

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
		f *character* —> skips to next character

		DELETE

		n dd  —> delete n lines
        D -> delete to end of line
		diw —> delete inner word
		:dt —> delete until the character next typed is found

		UNDO REDO

		u —> undo
		ctrl r (not command) —>  redo 

		COPY PASTE

		yy —> yank current line
		n yy —> yank the next n lines
		yt {}—> yank (copy) blocks of code
		p —> paste

		SEARCH AND REPLACE

		/ term —> highlights terms 
		:%s/toReplace/replaceWith/g —> replace globally
		
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
https://www.youtube.com/watch?v=X_6LLmj4_5I 

	 n
	 Σ i^3 = n^2 (n+1)^2 / 4
	i=1
( Sum of integers squared )


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

**Lagrange's three square theorem** 

https://leetcode.com/problems/perfect-squares/discuss/765682/Python3-math-and-dp

Any natural number can be represented as the sum of three integer squares, if n is not of the form 4^k(8m+7) for integers k and m

IE 

    if n / ( 4**int(math.log(n,4)) ) % 8 == 7
		n = a^2 + b^2 + c^2

remember not to disqualify multiples of only one factor <br>
And for factors to a power, that there could be any number

**Two square theorem** 

An integer greater than one can be written as a sum of two squares, if and only if,
its prime decomposition contains no prime congruent to 3 modulo 4 raised to an odd power. ( Just use brute force checking for this at O( √n ) rather than the theorem )

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

# Computer science (CS)

<br>


## **Algorithm analysis**

<br>

## Complexity

A function describing algorithm resource use dependent on the number of inputs, with a specific input.

This measure is better than running tests, because

- it is hardware independent
- it creates a continuous comparable functions, rather than error prone data points
- it can compare run times with inputs numbers that might not be feasible to test 

Depending on specific inputs to the algorithm this complexity can be best or worst case, AVERAGE CASE

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

<br><br>

## **Algorithms**
In mathematics and computer science, an algorithm is a finite sequence of well-defined, computer-implementable instructions, typically to solve a class of problems or to perform a computation.

<br>

## Greedy algorithm
Algorithms which always take the best short term solution, which in many cases will still results in the global minimum

<br>

## Linear search

Searching one after another until an match is found

<br>

## Binary search

A recurrent search algorithm that works on sorted sets by halving sorted elements with  < >  comparison operators. Implemented with a [Binary search tree](#Binary-search-tree).

<br>

# Depth & Breadth first search

Depth uses a [Stack](#Stack), where the search starts from the newest node, and so goes deep.
Breadth uses a [Queue](#Queue), where the search starts from the unearthed node found first, and so goes broad, one link away from the origin at a time.

<br>

## Minimum spanning tree algorithms
Algorithms to find
a subset of edges in a graph, which connect all nodes with the minimum weighted distance.

**Prim's Algorithm**
From a random starting node, while not all nodes have been reached, pick the shortest connection from any of the joined nodes which leads to a new node. 
https://www.youtube.com/watch?v=cplfcGZmX7I

**Kruskal's Algorithm**
From a minimum weighed edge, while not all nodes have been joined, pick the smallest weighted connection that connects to one or two new nodes.
https://www.youtube.com/watch?v=71UQH7Pr9kU&list=PL9xmBV_5YoZObEi3Hf6lmyW-CBfs7nkOV&index=2

<br>

## Dijkstra's algorithm

Finds the shortest path between two vertices in a graph

- The start vertex takes 0 time and you start by assuming every other vertex takes infinite time to get to it ( This is the same as saying you don't know how long it will take, but this is easier when updating to the shortest time )

- From the node you are on, travel along its paths and put the time it takes to move to each from the start which is the distance to the node you are standing on and the path you travel, updating if you find a shorter time

- Then, moving to the shortest node from the start, and repeat the last step until you are at the vertex you want to be at

The path can be kept track of by having an arrow pointing to the where the shortest path is from

<br>

## A* graph search

An improvement of [Dijkstra's algorithm](#Dijkstra's-algorithm) which takes into account general direction by taking into account the distance to the end node, alongside to the start node
Usually used on grids rather than the traditional graph

https://www.youtube.com/watch?v=-L-WgKMFuhE

<br>

## Sort

**Bubble sort** 
Items bubble to the top
**Selection sort**
Smallest items sink to the bottom

**Insertion sort**
Inserts each element into a sorted area in the list, in the right position

**Merge sort**
https://www.youtube.com/watch?v=4VqmGXwpLqc <br>
Divides and merges sorted lists


**Heap sort**
https://www.youtube.com/watch?v=k72DtCnY4MU <br>
Creates a max or min [heap](#heap) and extracts values


**Quick Sort**
https://www.youtube.com/watch?v=Hoixgm4-P4M <br>
Like binary search, this algorithm splits everything up


<br><br>

## **Data structures and types**

<br>

## Ordered and unordered 
Ordered means the data is sorted in some way, including by placement.

<br>

## Immutable	
Cannot be changed

<br>

## 	Data structure
A data structure is a particular way of organizing data in a computer so that it can be used effectively.

<br>

## Implicit data structure
A [Data structure](#Data-structure) which uses positioning as a way to carry information about a values position in the underlying representation. 
Formally, an implicit data structure is one with constant O(1) space overhead 
An example is a list representing a binary tree.

<br>

## Data type
An attribute of data which tells a compiler how to interpret and process it.

## 	Abstract Data type
A data model which provides only a limited interface to the underlying implemented [Data structure](#Data-structure).
https://en.wikipedia.org/wiki/Abstract_data_type

<br>

## List
[Abstract data type](#Abstract-data-type) <br>
Sequential elements represented by sequential memory addresses

<br>

## Graph
[Abstract data type](#Abstract-data-type) <br>
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
A [Tree](#tree) with at most two edges connected to each node. <br>

Full > Each node has 2 or no children. <br>
Complete > Nodes are filled in top to bottom, left to right. <br>
Perfect > Full and complete.  <br>

<br>

## Binary Search Tree 
A BST is a [Binary Tree](#Binary-Tree) where each node is greater than its left child and less then its right.

https://www.youtube.com/watch?v=LU4fGD-fgJQ <br>
A tree is balanced if the maximum difference between the number of subtree child nodes is 1 or 0. 


|        | unsorted array | sorted array | linked list | balanced BST |
|--------|----------------|--------------|-------------|--------------|
| Read   | O(n)           | O(log n)     | O(n)        | O(log n)     |
| Write  | O(1)           | O(n)         | O(1)        | O(log n)     |
| Remove | O(n)           | O(n)         | O(n)        | O(log n)     |

<br>

## Red black Tree
https://www.youtube.com/watch?v=qvZGUFHWChY <br>
A balanced [Binary search tree](#Binary-search-tree) with a guaranteed height of O ( log n ) for n nodes.

- A node is either red or black
- The root node is black 
- Nil nodes are black 
-  If a node is red, its children are black
-  All paths from Root to Nil contain the same number of black nodes 

<br>

## Stack
[Abstract data type](#Abstract-data-type) <br>
Last in First out <br>
Implemented include using a [Linked list](#linked-list). )

<br>

## Queue
[Abstract Data Types](#Abstract-Data-Types) <br>
First in First out. <br>
Implemented include using a [Linked list](#linked-list). 

<br>

## Priority queue
[Abstract data type](#Abstract-data-type) <br>
important first out <br>
Implemented include using a [heap](#heap)

<br>

## Double ended queue
[Abstract data type](#Abstract-data-type) <br>
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
A running sum [Arrays](#Array) or Lists of floats or integers in a corresponding list, which allows for the sum of values from index a to b in that list to be achieved in constant times

O(N) to update

https://en.wikipedia.org/wiki/Prefix_sum
In a flat array of numbers, you can either store the elements, or the prefix sums. In the first case, computing prefix sums requires linear time; in the second case, updating the array elements requires linear time (in both cases, the other operation can be performed in constant time).

<br>

## Array
[Implicit data structure](#Implicit-data-structure) <br>
Sequential elements in memory with a single data type and which can represent multidimensional data by storing extra data on the shape of the array.

<br>

## Linked List
[Data structure](#Data-structure) <br>
Sequential elements represented by value pointer pairs, where pointers point to the next value in the list 

Variations
- singly linked lists have one way directed pointers
- doubly linked lists have two way directed pointers.
- circular linked list, tail next points to head 
- Skip list, multiple links to allow for O(log n) read


<br>

## Heap 
[Data structure](#Data-structure) <br>
https://www.youtube.com/watch?v=AE5I0xACpZs <br>
A complete [Binary Tree](#Binary-Tree) stored as an array where for max heaps, no child is greater than its parent.

For Insertion new nodes are placed in the next available position, and then swapped with their parents until they are less in value than them, retaining the node value requirement

For deletion you delete the root, 
and move it down by swapping it with the greatest child element greater than itself.

A min heap is the reverse of this

<br>

## Dictionary
[Hash](#Hash) <br>
Also called hash tables. <br>
A key is hashed and the using modulus the remainder of the a division by the length of the array becomes an array index where the value is stored.
Allows for O( 1 ) retrieval time.

Some of the ways of addressing collisions include

Open addressing > placing an item at a position different than the hash <br>

	Linear probing > The value goes to the next available position in the set length array

Closed addressing 

	Linked list collisions > If there is a collision, then the array index will be set as the first link in a linked list.

<br>

## Prefix sum
A running sum [Arrays](#Array) or Lists of floats or integers in a corresponding list, which allows for the sum of values from index a to b in that list to be achieved in constant times

O(N) to update

https://en.wikipedia.org/wiki/Prefix_sum
In a flat array of numbers, you can either store the elements, or the prefix sums. In the first case, computing prefix sums requires linear time; in the second case, updating the array elements requires linear time (in both cases, the other operation can be performed in constant time).

<br>

## Fenwick tree
[Binary tree](#Binary-tree) <br>
Also called a Binary indexed Tree

https://en.wikipedia.org/wiki/Fenwick_tree
https://www.youtube.com/watch?v=v_wj_mOAlig

It allows both updating and prefix sums in O( log n ) time.

13 = 2^3 + 2^2 + 2^0 <br>
SUM_TO(13) = SUM_RANGE(1,8) + SUM_RANGE(9,12) + SUM_RANGE(13,13)


<br><br>

## **Paradigms**
https://www.youtube.com/watch?v=aoE-92Ac4zE

<br>

## Object Oriented Programming
OOP is writing code around the idea of object properties and actions.

Encapsulation > Creating a sealed class which controls reading and writing variables and calling functions for intended use

Inheritance > How a class that is a subset of another class avoids writing duplicated shared methods, IE class Developer(Human): ...

Polymorphism > "Many forms", The ability of an object to identify as more than one class

Abstraction > A simplification of a mental model IE going from logic gates to an adder circuit

Static methods > Don't require a class instance

Class methods > Operate on every instance of a class 

Abstract class > A class only used for child classes to inherit from, and which is not instantiated.

<br>

## Functional
Create Pure functions where the output should only depend on its inputs and not effect outside variables. This allows for parallelization, as functions can run at the same time without affecting each other.

https://www.youtube.com/watch?v=dAPL7MQGjyM

<br>

## Declarative
Code which focuses on the end product rather than how it is created. A description rather than a recipe.

<br>

## Imperative
Describing the steps

<br>

## Procedural programming
Steps, one after the other in logical order.

## Logic
TODO
Prolog <br>
https://en.wikipedia.org /wiki/Prolog
https://www.youtube.com/watch?v=xP0q3WOBRks


<br><br>

## **Programming language**
A human readable syntax used to write code which is converted to machine readable code to run.

<br>

## Source code
Human readable which represents machine code

<br>

## Byte code
Compressed [Source code](#Source-code) which can be optimized for a specific machine before being executed

<br>

## Machine Code
Binary that can execute on a computer’s physical processor without further translation.

<br>

## Interpreter
Interpreting a [Programming language](#Programming-language) is executed code with each line.

<br>

## Compiler
A Compiler converts the [Programming language](#Programming-language)  Human to OS machine code as a whole and  then executed

<br>

## AOT
[Compiler](#Compiler) <br>
Ahead Of Time compilers convert from human to machine readable before run time are the most common and intuitive compiler implementation.

<br>

## JIT
A Just in time [Compiler](#Compiler) converts from human readable code to byte code for distribution, and then is converted to machine code with each computer for better optimization.

<br>

## Explicit conversion
When a type is converted explicitly in code.
<br>

	int( "1234" )

## Implicit conversion
When a type is converted by the compiler without explicit instruction in code. This conversion retains information and so the new type takes more memory than the previous type. 
<br>

	2+"3" = "23"

<br>

## Strong or Weak typing
A continuous spectrum that compares how flexible (weak) or rigid (strong) programming languages are using implicit conversion.

<br>

## Dynamic / Static typed languages
Dynamic typed programming languages check for types during run time, "on the fly". Static languages check for types when they compile, and so are faster in run time.

<br>

## Call stack 
https://en.wikipedia.org/wiki/Call_stack <br>
A [Stack](#Stack) implemented to store values in the order a program will use them.

<br>

## Literal
A fixed value which is assigned to variables or printed, and whose type is defined in syntax.

<br>

## Primitive data types
Primitives data types are built into the language, and are not imported or added on

<br>

## Operator
https://en.wikipedia.org/wiki/Operator_(computer_programming) <br>
Operators inbuilt constructs which behave like functions, but differ syntactically ( add(x,y) and x+y ) or semantically 


<br><br>

## **High level**

<br>

## Application
Code directly applicable to the user.

<br>

## OS 
Operating System <br>
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


<br><br>

## **Cryptography**

<br>

## Hashing 
A hash maps any input of varied size to an, ideally always, unique value.

A hash function such as SHA256 will take a key and output a hash code.
Over the range of possible hash codes, hash functions are designed to spread these out to avoid collisions, but at the same time the function is not random and the same key will always result in the same hash code being deterministic.

<br>

## Encryption
https://www.youtube.com/watch?v=GSIDS_lvRv4 <br>
https://www.youtube.com/watch?v=vsXMMT2CqqE <br>
A process that converts text into nonsensical cipher-text, which can only be decrypted by people with a numerical key, for use in sending information when communications can be intercepted.

<br>

## Symmetric Encryption
Where the message is encrypted and decrypted with the same key, and so needs to be transferred between parties. The key needs to be securely shared, but this method is faster than [Asymmetric Encryption](#Asymmetric-Encryption)

<br>

## Asymmetric Encryption
Also called Public key Encryption 

https://www.youtube.com/watch?v=AQDCe585Lnc <br>
https://www.youtube.com/watch?v=vsXMMT2CqqE <br>

Everybody has a public and private key.

Messages encrypted with your recipients public  key can be decrypted by them only.

Messages encrypted with your private key can be decrypted by anyone, but only sent by you.

Messages can be encrypted multiple times, and so use both of these properties to secure a message and verify a sender.

<br><br>

## **Blockchain**

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


<br><br>

## **Devops**

<br>

## Containers
A container is a software package that consists of all the dependencies required to run an application 

Docker is software for distributing software in the same environment it was made in, to avoid configuration issues, and has replaced using  [[Virtual machines]], by  only creating the parts of the OS that an application, not the user, interacts with.

https://stackoverflow.com/questions/30632386/is-docker-a-solution-for-making-application-cross-platform

<br>

## Container orchestration
A way to scale and maintain [Containers](#Containers) automatically

<br>

## Microservices
Splitting up cloud services between [Containers](#Containers) to them scale for their different workloads
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


<br><br>

## **Databases**

<br>

## Primary keys
The index of a unique rows in a database to describe an entry

<br>

## Relation databases
A database design to to avoid redundant and old data

IE A customer ID in a sales table describes the location in another table of up to date customer information

This avoids duplicates of data that can change, like for example, a customers address which could change between sales

<br>

## Foreign keys
A primary key in a foreign table, to create linked data

<br><br>

## **AI / ML**

## RNN
Recurrent neural network

## LSTM

## GRU

## Transformer

## CNN
Convolution neural network


## Auto encoder

## Hopfield net

## Perceptron

## Boltzmann machine

## Syn flow

<br><br>

## **Misc**

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

## recursion
A function calling itself

<br>

## Dynamic programming
- 1 Recursion
- 2 Memoize (not memorize)

	Store what values you have already computed

- 3 Top down Bottom up
	
**Bottom up**  Base case and work up

**Top Down** Memoization and Recursion to work down

<br>

## P vs NP
https://www.youtube.com/watch?v=u2DLlNQiPB4

<br>

## Premature optimization
Optimizing that delays finishing a working product, as when the optimization... 

- will become deleted code as the program changes, and will go unused in the program 
- won't be a bottleneck to needed performance, and will go unnoticed by the user
- makes it slower to write more code, and will be a hindrance to development

## Invariant 
Something that doesn't vary and which is always true.

## Loop Invariant 
A loop invariant is a statement about program variables that is true before and after each iteration of a loop.