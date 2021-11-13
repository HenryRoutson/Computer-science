w

*Useful but forgettable* 

<br>

**Meta**

https://www.tablesgenerator.com/markdown_tables

Note that markdown links cant have capitals  
[Link with lower](#code)  
[Link with upper](#Code)  

<br>

When writing code, don't write scalable code straight away, but write code for a small part of the program and get that working first

<br>

Search "???" for unsure  

<br>
<br>

# Code

### **Shared syntax**  

<br>

###  Increment and decrement operators

	pre
	x++ and x--

	post
	++x and ++x

<br>

### Augmented assignment  
https://en.wikipedia.org/wiki/Augmented_assignment  

	+=, -=, %= ...

<br>

###  Control flow brackets
	... (...) {...}
```c
if ( i>100 ) {...} // i>100 is a Boolean

switch ( i ) {                  // i, a and b are values
	case a: ... break;
	case b: ... break;
}

for (int i=0; i<100; i++) {...}

while ( i>100 ) {...}
```

<br>

### Iterable bracket indexing

```c
"string"[1]
```

<br>

### Standard mathematical syntax

```python
x * y # mul  
x / y # division
x % y # mod  
```

<br>
<br>
<br>
<br>

**Python**  
[Augmented assignment](#augmented-assignment)  
[Iterable bracket indexing](#iterable-bracket-indexing)
[Standard mathematical syntax](#standard-mathematical-syntax)


```python
#                                                   HELLO WORLD
print("Hello world")	

#                                                   CONVENTION

() # means something is spontaneously calculated, and possibly takes inputs
ClassInstance.Attribute # Stored
ClassInstance.Method()
Function(Input)

CONSTANT = 10
variable_name = [1,2,3,4]
def function_name(): ...
# note that variables are preserved with functions

def function():
    """Demonstrates triple double quotes
    docstrings and does nothing really."""
    pass

print(function.__doc__)

#                                                   MATHEMATICAL

x ** y # exp
x ** 0.5 # sqrt

import math 
math.log(64,2) 
True + 10 # 11 through implicit conversion
not 48 # 0 through implicit conversion


#                                                   BASE

binary = bin(10) # '0b1010'
int(Num, Base) # revert to base 10 
1-bit # NOT
not bit # NOT
& # AND     
| # OR      
^ # XOR ( only either ) 
decimal << int # SHIFT left
decimal >> int # SHIFT right
hexadecimal = hex(10) # '0xa'


#                                                   TYPES

dir(type) # find type methods

bool 
	Bool = True
	bool(Type) # if the type is the simplest / smallest, then it will eval to False
	not # to flip

	"""Evaluating bool expressions"""
	True or True and not True # Not left to right
	# 1 Conditions 
	# 2 not
	# 3 and
	# 4 or 

	
	# strings will be evaluated on dictionary order

	>  # Greater than
	>= # Greater than or equal to
	<  # Less than
	<= # Less than or equal to
	!= # not equal to

float
	Float = 5.0
	
	# Methods
	bool( Num % 1 ) # test if float has decimals
	def ceil(x): return int(x+bool(x%1)) # round up without importing

complex 

	Complex = 3+4j 
	Complex = complex(3, 4)
	Complex.real # 3
	Complex.imag # 4
	Complex.conjugate() # 3-4j
	abs(Complex) # 5

	import cmath
	Complex = complex( 1, (3**0.5) )
	cmath.polar(Complex) 

int 
	Int = 2

list
	# ordered, iterable, mutable 
	List = [1]

	# Methods

	List.append(Element)
	List.insert(index,Element)
	List.extend(Iterable)
	List = zip(List) # [1,2],[3,4] > [(1, 3), (2, 4)]

	from numpy import prod; prod(NumList)
	from math import prod; prod(NumList)

	*Iterable # *["a","b"] == "a","b"

	# Note that when using = to create a new list this is still points to and modifies the same list
	# to make a new list to avoid modifying the previous one use
	New_list = List.copy()
	
str 
	# ordered, iterable
	string = "123" 
	string = "1234" + "5678" # concatenation
	fstring = f"This is an F string which easy add values like {x} into"
	fstring = f"F strings can be formatted with rounded float for example {2**0.5:.10f}"

	# Printing
	print(1234, "567", "eight", "nine") # , adds a space
	print(str)	

	# Methods

	eval("1+2") # 3

	ord(Character) # unicode integer
	ord(Char) - ord('a') + 1 # lower case alphabetic position
	ord(Char) - ord('A') + 1 # upper case alphabetic position
	chr(ord(Character)) # chr is reverse

	# eval
	string.istitle() # is title capitalization
	string.isupper()
	string.islower()
	string.isalpha() # is all letters
	string.isnumeric() # is all numbers
	string.isalnum() # is alpha numeric 
	string.upper() # changes all letters in string to upper case
	string.lower() # changes all letters in string to lower case
	string.split() # Splits up into list based on string, leave as default to split words
	string.strip() # default is " ", removes this string at start and end of another
	
	# optimization
	"".join() # is faster than +


tuple
	# ordered 
	Tuple = (1,)

	x,_,z = ('x',2,'z') # _ avoids assigning  
	x,*_,z = ('x',2,2,3,2,'z') # *_ is any number of values 

	# https://www.youtube.com/watch?v=GfxJYp9_nJA
	from collections import namedtuple
	rgb = namedtuple('color', ['red','green','blue'])
	offWhite = rgb(183, 185, 167)
	print(offWhite.red)

set
	# unique elements, unordered, iterable, mutable
	Set = set(List) = {1}

	# Methods
	A - B # dif, A - (A ∩ B)  
	A | B # union, A U B
	A & B # intersection, A ∩ B 
	A ^ B # symmetric difference, (A U B) - (A ∩ B)

	.add(Element)
	.update(Iterable)
	.discard(Element)
	.remove(Element) # throws error if not present

	dict 
		# unique elements, unordered, iterable
		Dictionary = {}
		Dictionary = {1:None} 
		Dictionary = {x:i for i:x in enumerate(Iterable)}

		# add to dictionary
		if not Dictionary.get(Key): # index notation throws error without value
			Dictionary[key] = ...

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
Val = List.pop() # Removes last value, deletes index with argument value
Val = Set.pop() # Removes last value
Val = Dict.pop(Arg) # key arg required

# string list
Iterable = sorted(Iterable) 
Iterable.sort() 
Iterable.sort(reverse=True)
Iterable[start:end:move] # slicing
	# second comma is optional if move doesn't need to be changed
	# Defaults if values aren't entered... 
	start=0; end=len(string)+1; move=1
	# start is inclusive, end is exclusive to the character at the index
Iterable[::-1] # reverse iterable
Iterable.index(element)

# generators string list set dict
reversed(Iterable)
max(Iterable) 
min(Iterable)
sum(Iterable)

def show_index(Iterable):
  
	for i in range(len(Iterable)):
	print(i, end=" ")
	print("+")

	for i in range(len(Iterable)):
	print(Iterable[i], end=" ")
	print(type(Iterable))

	for i in range(len(Iterable)):
	print(len(Iterable)-i, end=" ")
	print("-")

#                                                  CONTROL FLOW 

DefaultArg = "squared is"
def Print_Square(Num, Another, String=DefaultArg): # default arguments need to be the last stated arguments
	print(Num, String, Num**2, Another) 

Print_Square(String="DefaultArg", Another=2, Num=1) # valid
	

Print_Square(10, String="to the power 2 is") # OR
Print_Square(10, "" ,"to the power 2 is")

	
if Condition: Code ... # evaluating a type will be implicitly converted to bool
if Condition: return # doesn't need else after

while Condition: print("while")
for i in range(5, 10): print(i) # Use start
for i, x in enumerate([13,5,29]): print(i, x) # Use enumerate (i before x)
for i in range(len(Iterables)-1,-1,-1): print(Iterables[i]) # Use different steps
for a,b in zip(listA,listB): print(a,b) # use zip for multiple lists

break # break out of for loop
continue # continue to next element or value
pass # write if nothing happens to avoid an error

# for else
for ... :
	if ... :
		break
else ... : # called if break not called
	...

(), eval, not, and, or  # order of logical operations


#                                                  FUNCTIONAL

def Bool_function(Element): return Element>5
list(map(Bool_function, Iterable)) 
list(map(lambda Element: Element>5, Iterable)) 


#                                                   SHORTHAND

x = y = 1
x, y = 9, 3
Iterable[1], Iterable[0] = Iterable[0], Iterable[1] # no temp
x = x//y # x = int( x/y )
Assigned = True if Bool else False  # one line if else
"repeat "*3 # 'repeat repeat repeat '
[0]*3 # [0,0,0]


#                                                   OOP

class Human():
    def __init__(self, Age, ):
        self.Age = Age

    def birthDay(self):
        self.Age += 1

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

#                                                  	OPERATOR OVERLOADING  

class complex:
    def __init__(self, a, b):
        self.a = a
        self.b = b
 
     # adding two objects
    def __add__(self, other):
        return self.a + other.a, self.b + other.b
 
Ob1 = complex(1, 2)
Ob2 = complex(2, 3)
Ob3 = Ob1 + Ob2
print(Ob3)


#                                                  FILES
    
# Open
open(...) # https://docs.python.org/3.6/library/functions.html#open 

with open(filename) as file_object # USE
	...

# Read
number_chars = 10 
text = file_object.read(number_chars) # optional arg
new_index = 23
file_object.seek(new_index) # change next read starting index
#OR
line_sep_list = file_object.readlines()
for line in file_object.readlines(): ... # lower max memory than storing everything at once

# JSON - able to write normal python data types
import json

with open('path_to_file/person.json') as json_file:
  Dict = json.load(json_file)

# do something

with open(File_name,'w') as File:
        File.write(json.dumps(Dict))

#                                                  LIST COMPREHENSION

[x-1 for x in List]

from collections import Counter
def mode(numlist):
    counts = Counter(numlist)
    max_count = max(counts.values())
    return list(num for num in counts if counts[num] == max_count)

["ODD" if num % 1 else "EVEN" for num in List]

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
print("Split lines "
+ "with open brackets")
help( Something )	
def var_parameters(*c) return sum(c) # multiple values get converted to a tuple

#                                                  DOC STRINGS                                          

# Google Style Python Docstrings
def manhatan(loctn_a, loctn_b):
    ''' return distance between location a and b
    
    Args: 
        loctn_a / loctn_b (tuple): locations with integer axis values
        
    Returns:
        integer: manhatan distance, 
        the sum of the positive difference between axis values
    
    '''
    return sum(abs(a - b) for a, b in zip(loctn_a, loctn_b))


```

<br>
<br>
<br>
<br>
<br>

**C**  
[Augmented assignment](#augmented-assignment)  
[Increment and decrement operators](#increment-and-decrement-operators)  
[Control flow brackets](#control-flow-brackets)

```c
// HELLO WORLD

#include <stdio.h>
int main() {
	printf("Hello World!");
	return 0;
}
/*	
    - stdio is short for standard input output 
    - the type before the name of the function is the returned type
    - int main() returning 0 signals no errors, 
    - newer compiler return 0 implicitly
*/

// TYPES

	char A = 'A';
	int Ten = 10;
	float Tenth = 0.1;
	double Half = 0.5;

// TYPE MODIFIERS

	signed or unsigned
	short or long
	

// PRINT VARIABLES

#include <stdio.h>
int main() {
	char Planet[] = "Mars";
	printf( "Hello %s!", Planet ); 
	return 0;
}
/* 
	%c char single character
	%d (%i) int signed integer
	%e (%E) float or double exponential format
	%f float or double signed decimal
	%g (%G) float or double use %f or %e as required
	%o int unsigned octal value
	%p pointer address stored in pointer
	%s array of char sequence of characters
	%u int unsigned decimal
	%x (%X) int unsigned hex value
*/

// POINTERS

#include <stdio.h>
int main() {
	int Var = 5;	
	int *Pointer = &Var;
	printf( "Address: %d \n", Pointer );
	printf( "Value: %d \n", *Pointer );
}

// TYPE CASTING / BIT MANIPULATION

#include <stdio.h>
int main() {
	for (int i=0;i<128;i++) {
		char a = (char)i;
		printf("%c", a );
	}
}

// ARRAYS
TODO below

#include <stdio.h>
int main() {
	char Variable_AnyLength[];
	char Variable_CappedLength[25];
	char *Constant = "Value";
	int GridArray[][] = 
}

// FUNCTIONS PARAMETERS


#include <stdio.h>
int main() {
    
    int Fib(int n) { 
        if (n == 0) { return 0; }
    	if (n == 1) { return 1; }
    	return Fib(n-1) + Fib(n-2);
    }

    printf("%i",Fib(4));
    return 0;
}

// INPUT

	printf( "What is your name?" );
	int chars = 25;
	char[chars] String;
	fgets(name, chars, stdin) 
	// stdin is standard input (the terminal)
	printf( name )


// LOGIC OPERATIONS

#include<iostream>
int main() { 
    std::cout << (true & true);  // & --> AND
    std::cout << (true | false); // | --> OR
    std::cout << (!false);       // ! --> NOT
}


// OVERLOADING
int plusFuncInt(int x, int y) { return x + y; }
double plusFuncDouble(double x, double y) { return x + y; }

// SHORTHAND

int one, two; // declare variables with shared type 

```

<br>

**C++**  
Inherits from c 

```c++

// Hello world

#include<iostream>
int main() {
    std::cout << "Hello world";
}

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

# Arduino
Inherits from c++

Digital pins have a binary value  
Analog pins have a float value  

```c++
// example code

int sensorValue = 0;

void setup()
{
  pinMode(A0, INPUT);
  pinMode(13, OUTPUT);
  Serial.begin(9600); 
}

void loop()
{
  // read the value from the sensor
  sensorValue = analogRead(A0);
  Serial.println(sensorValue);
  // turn the LED on
  digitalWrite(13, HIGH);
  delay(sensorValue); // wait for sensorValue milliseconds(s)
  // turn the LED off
  digitalWrite(13,LOW);
  delay(sensorValue); // wait for sensorValue milliseconds(s)
}
```

<br>
<br>
<br>
<br>
<br>

**Java**  
[Augmented assignment](#augmented-assignment)  
[Increment and decrement operators](#increment-and-decrement-operators)  
[Control flow brackets](#control-flow-brackets)  
[Iterable bracket indexing](#iterable-bracket-indexing)  

```Java
// Hello world
class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!"); 
    }
}
```

<br>
<br>
<br>
<br>
<br>

**Javascript**
[Augmented assignment](#augmented-assignment)  
[Increment and decrement operators](#increment-and-decrement-operators)  
[Control flow brackets](#control-flow-brackets)  
[Iterable bracket indexing](#iterable-bracket-indexing)  
```Javascript

// HELLO WORLD
console.log('Hello World');

// HTML modification
document.getElementById("demo").innerHTML = "Hello JavaScript";

// ASSIGNMENT

	var // variable
	let // constant which can be reassigned
	const // constant which cannot be reassigned

// FUNCTIONS
function myFunction(p1, p2) { return p1 * p2; }

// STRING MULTIPLICATION
"a".repeat(10) // no string multiplication

// objects -- link to JSON
const car = {type:"Fiat", model:"500", color:"white"};

// accessing
objectName.propertyName
objectName["propertyName"]


this
new

```

<br>
<br>
<br>
<br>
<br>

**Prolog**  
```Prolog

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

**JSON**  
JavaScript Object Notation is a language independent data format.  
 - Data is in name/value pairs  
 - Data is separated by commas ,
 - Curly braces hold objects {}
 - Square brackets hold arrays []

```JSON
{
	"business_id": "1434729",
	"postcode": "400",
	"open": true,
	"employees":[
		{"firstName":"John", "lastName":"Doe"},
		{"firstName":"Anna", "lastName":"Smith"},
		{"firstName":"Peter", "lastName":"Jones"}
		]
}
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

# Deployment

## Terraform



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

# CS concepts

<br>

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

## Algorithms
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

## Depth & Breadth first search
Depth uses a [Stack](#Stack), where the search starts from the newest node, and so goes deep.
Breadth uses a [Queue](#Queue), where the search starts from the unearthed node found first, and so goes broad, one link away from the origin at a time.

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
Finds the shortest path between two vertices in a graph  

- The start vertex takes 0 time and you start by assuming every other vertex takes infinite time to get to it ( This is the same as saying you don't know how long it will take, but this is easier when updating to the shortest time )

- From the node you are on, travel along its paths and put the time it takes to move to each from the start which is the distance to the node you are standing on and the path you travel, updating if you find a shorter time

- Then, moving to the shortest node from the start, and repeat the last step until you are at the vertex you want to be at

The path can be kept track of by having an arrow pointing to the where the shortest path is from

<br>

## A* graph search
An improvement of [Dijkstra's algorithm](#Dijkstra's-algorithm) which takes into account general direction by taking into account the distance to the end node, alongside to the start node.
Usually used on grids rather than the traditional graph.  
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
https://www.youtube.com/watch?v=4VqmGXwpLqc  
Divides and merges sorted lists

**Heap sort** https://www.youtube.com/watch?v=k72DtCnY4MU  
Creates a max or min [heap](#heap) and extracts values  

**Quick Sort** https://www.youtube.com/watch?v=Hoixgm4-P4M  
Like binary search, this algorithm splits everything up

<br>

## Ordered and unordered 
Ordered means the data is sorted in some way, including by placement.

<br>

## Immutable	
Cannot be changed
If at the programming level it looks like it has changed, then the new value is at a different address 

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

<br>

## 	Abstract Data type
A data model which provides only a limited interface to the underlying implemented [Data structure](#Data-structure).
https://en.wikipedia.org/wiki/Abstract_data_type

<br>

## List
[Abstract data type](#Abstract-data-type)  
Sequential elements represented by sequential memory addresses

<br>

## Graph
[Abstract data type](#Abstract-data-type)  
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
Full > Each node has 2 or no children.  
Complete > Nodes are filled in top to bottom, left to right.  
Perfect > Full and complete.

<br>

## Binary Search Tree 
A BST is a [Binary Tree](#Binary-Tree) where each node is greater than its left child and less then its right.

https://www.youtube.com/watch?v=LU4fGD-fgJQ  
A tree is balanced if the maximum difference between the number of subtree child nodes is 1 or 0. 

|        | unsorted array | sorted array | linked list | balanced BST |
|--------|----------------|--------------|-------------|--------------|
| Read   | O(n)           | O(log n)     | O(n)        | O(log n)     |
| Write  | O(1)           | O(n)         | O(1)        | O(log n)     |
| Remove | O(n)           | O(n)         | O(n)        | O(log n)     |

<br>

## Red black Tree
https://www.youtube.com/watch?v=qvZGUFHWChY  
A balanced [Binary search tree](#Binary-search-tree) with a guaranteed height of O ( log n ) for n nodes.  
- A node is either red or black
- The root node is black 
- Nil nodes are black 
-  If a node is red, its children are black
-  All paths from Root to Nil contain the same number of black nodes 

<br>

## Stack
[Abstract data type](#Abstract-data-type)  
Last in First out  
Implemented include using a [Linked list](#linked-list). )

<br>

## Queue
[Abstract Data Types](#Abstract-Data-Types)  
First in First out.  
Implemented include using a [Linked list](#linked-list). 

<br>

## Priority queue
[Abstract data type](#Abstract-data-type)  
important first out  
Implemented include using a [heap](#heap)

<br>

## Double ended queue
[Abstract data type](#Abstract-data-type)  
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
[Implicit data structure](#Implicit-data-structure).   
Sequential elements in memory with a single data type and which can represent multidimensional data by storing extra data on the shape of the array..
## Linked List
[Data structure](#Data-structure)  
Sequential elements represented by value pointer pairs, where pointers point to the next value in the list.  

Variations
- singly linked lists have one way directed pointers
- doubly linked lists have two way directed pointers.
- circular linked list, tail next points to head 
- Skip list, multiple links to allow for O(log n) read

<br>

## Heap 
[Data structure](#Data-structure)  
https://www.youtube.com/watch?v=AE5I0xACpZs  

A complete [Binary Tree](#Binary-Tree) stored as an array where for max heaps, no child is greater than its parent.  

For Insertion new nodes are placed in the next available position, and then swapped with their parents until they are less in value than them, retaining the node value requirement.

For deletion you delete the root, 
and move it down by swapping it with the greatest child element greater than itself.

A min heap is the reverse of this

<br>

## Dictionary
[Hash](#Hash)  
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
A running sum [Arrays](#Array) or Lists of floats or integers in a corresponding list, which allows for the sum of values from index a to b in that list to be achieved in constant times

O(N) to update

https://en.wikipedia.org/wiki/Prefix_sum
In a flat array of numbers, you can either store the elements, or the prefix sums. In the first case, computing prefix sums requires linear time; in the second case, updating the array elements requires linear time (in both cases, the other operation can be performed in constant time).

<br>

## Fenwick tree
[Binary tree](#Binary-tree)  
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
[Paradigm](#Paradigm)

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
[Paradigm](#Paradigm)  
Create Pure functions where the output should only depend on its inputs and not effect outside variables. This allows for parallelization, as functions can run at the same time without affecting each other.  

<br>

## Declarative programming 
[Paradigm](#Paradigm)  
Code which focuses on the end product rather than how it is created. A description rather than a recipe.

<br>

## Imperative
[Paradigm](#Paradigm)  
Describing the steps

<br>

## Procedural programming
[Paradigm](#Paradigm)  
Steps, one after the other in logical order.

<br>

## Logic programming
[Paradigm](#Paradigm)  
Programming based on formal logic, including languages such as Prolog.

<br>

## Programming language
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
[Compiler](#Compiler)  
Ahead Of Time compilers convert from human to machine readable before run time are the most common and intuitive compiler implementation.

<br>

## JIT
A Just in time [Compiler](#Compiler) converts from human readable code to byte code for distribution, and then is converted to machine code with each computer for better optimization.

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
A [Stack](#Stack) implemented to store values in the order a program will use them.

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

and everything under [PaaS](#PaaS)

## Faas

Function as a Service provides 

- On demand function computing

and everything under [PaaS](#PaaS)

## PaaS
Platform as a Service provides 

- Developer tools  
- Operating systems 

and everything under [IaaS](#IaaS)

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
Where the message is encrypted and decrypted with the same key, and so needs to be transferred between parties. The key needs to be securely shared, but this method is faster than [Asymmetric Encryption](#Asymmetric-Encryption)

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
Uses a [Dictionary](#Dictionary)  
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
A process of changing weights in a [Neural network](#Neural-network) based on how much each contributed to a wrong answer, which is calculated using derivatives.

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
A Recurrent neural network is a [Neural network](#Neural-network) whose outputs feed into future inputs, and which so are able to process variable size time series data.

<br>

## LSTM
A long / short term memory neural network is a [RNN](#RNN) which mitigates the [Vanishing gradient problem](#Vanishing-gradient-problem).
An LSTM has a continuous memory which is processed by the 'forget' multiplication and 'remember' addition operations. This memory always continues to the next time step, but is also duplicated to and processed by a 'relevant' multiplication operation to be added to only the next time step. Each of these operation is decided by trained neural networks and some parts of the network are normalized.

<br>

## GRU
A Gated recurrent unit is a [RNN](#RNN) which mitigates the [Vanishing gradient problem](#Vanishing-gradient-problem).
Similar to an [LSTM](#LSTM), only without the hidden state, making them simpler and faster to train, although they are both suited to different cases.

<br>

## Transformer
A Gated recurrent unit is a [RNN](#RNN) which mitigates the [Vanishing gradient problem](#Vanishing-gradient-problem) and memory loss through weighted focused as introduced in the 'Attention is all you need' paper.

<br>

## CNN
Convolutional [neural network](#Neural-network)  
To convolute is to blur, which is intuitively is mapping a number of values to less. Doing this repeatedly, with trained feature detectors, will allow machine to complete tasks including image content identification or depth perception.

<br>

## Auto encoder
Unsupervised  
An autoencoder is an architecture to train one [neural network](#Neural-network) to encode data into characteristics (a lower dimensional representation) and another to decompress the characteristics into the original data. 

<br>

## GAN
Generative Adversarial Network  
Consists of a Generative network, which creates model data from random or relevant inputs, and a Adversarial model to determine if the data which it is fed is real or generated. The Generative network is trained to minimize the certainty which the Adversarial model thinks it's data is modeled, and the Adversarial model is trained to distinguish this. This allows realistic modeled data to be created for things such as photos. A naive approach would directly train the network to model data, which would result in the average and not a realistic case.

<br>

## Hopfield net
[neural network](#Neural-network)  
A neural network which retrieves data with part of that data fed into the network.

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
- 1 [Recursion](#Recursion)
- 2 Memoize (store computed values)
- 3 Top down or Bottom up

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