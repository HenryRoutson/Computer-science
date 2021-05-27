<br>

Useful but forgettable 

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
	.reomove(Element) # throws error if not present

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
True if Bool else False  # one line if else
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


#                                                   MISC

float('inf') # infinity without importing
sorted( arr, key=lambda Num: (abs(Num), Num, ...) ) # sort with multiple conditions in the same iterable
[x for _, x in sorted(zip(Y, X), key=lambda pair: pair[0])] # sort based on other iterables
sorted(List)[:n_largest] # better than repeated min and max
"".join(Str_Iterable) # ["a","b"] --> "ab"
plus_plus = lambda x: x+1 # lambda just defines a function; plus_plus(2) = 3
__main__ # magic methods   
1_000 # _ makes large numbers easier to read
In = input("optional message")

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
```
	
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
```

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

# CS topics

<br>

## **Concepts**

<br><br>

## Complexity

A function describing algorithm resource use dependent on the number of inputs, with a specific input.

This measure is better than running tests, because
- it is hardware independent
- it creates a continuous comparable functions, rather than error prone data points
- it can compare run times with inputs numbers that might not be feasible to test 

Depending on specific inputs to the algorithm this complexity can be best or worst case, AVERAGE CASE

<br><br>

## Asymptotic analysis
*Sometimes called Asymptotic bounding*

An analysis of [Complexity](#**complexity**) graphs and what functions can be anymptotic to them.

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

<br><br>

## Best, worst and average case

Depending on the inputs to a function, the complexity of an algorithm can change, such as when a sorting algorithm has to sort an already sorted list.

<br><br>

## Application
Code directly applicable to the user.

<br><br>

## OS 

Code to run other 1st or 3rd party applications. 
With multiple applications it consequentially needs the ability to switch between them, and manage shared resource use if they run at the same time. 
With 3rd party applications it likely enforces proper hardware use and provide common services to 3rd party developers.

<br><br>

## Abstract Data Type
A data type which provides only an interface to the abstraction, and not the underlying Data structure it is based on which could be different depending on implimentation.

<br><br>

## Literal
A fixed value which is assigned to variables or printed, and whos type is defined in sytax.

<br><br>

## Primitive data types
Primitives data types are built into the language, and are not imported or added on

<br><br><br>

## **Data structures**

<br>

**Properties**

<br>

## Ordered and unordered 
Ordered means the data structure is sorted in some way, including by placement.

<br>

## Immutable	
Cannot be changed

<br><br>

**Basis Structures**

<br>

## Graph
A set of nodes possibly joined with edges

<br><br>

## Tree
An acyclic [Graph](#graph) where all nodes are connected to a root leading out to leaf nodes.

<br><br>

## Binary Tree
A [Tree](#tree) with at most two edges connected to each node.

<br><br>

**Functional structures**

<br><br>

## Array
Sequential elements in memory with a single data type and which can represent multidimensional data by storing extra data on the shape of the array.

<br><br>

## List
Sequential elements represented by sequential memory adresses

## Linked List
Sequential elements represented by value pointer pairs, where pointers point to the next value in the list

<br><br>

## Stack
Last in First out

## Queue
First in First out. <br>
[Abstract Data Types](#Abstract-Data-Types) implimented using .

<br><br>

## Segment Tree 
A [Binary Tree](#binary-tree) for finding the minimum or maximum values in a range. A max tree is below and shows each node represents the maximum for its children.


	    9
       /  \
	   8  9
	 / |  | \
	3  8  9  0

<br><br>

## Trie 
Strings stored as [Tree](#**tree**) character paths

<br><br>

**Complexities** 

| Name          | Best | Average | worst |
| ------------- | ---- | ------- | ----- |
| [IE](#)       | n    | n^2     |       |

<br>

## **Paradigms**

**Object oriented** <br>
Static methods > Doesn't require a class instance <br>
Class methods > Operates on every instance of a class <br>