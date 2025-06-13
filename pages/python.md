- python documentation
  collapsed:: true
	- https://pyton.org
	- https://docs.python.org/3/
	- is interpreted language
	- is dynamically typed language
	- indentation is important in python (white space, tabs before statements)
- devops
  collapsed:: true
	- installation
	  collapsed:: true
		- py --version
	- ide: vscode, vscode extensions: pylance, python, python debuuger, pycharm
	- google colab
	- github codespaces
	- python interpreter
		- REPL - Read Evaluate Print Loop
	- python cli
	  collapsed:: true
		- python3
		- `exit()` or `Ctrl + Z`
- variables
  collapsed:: true
	- x = 10
	- x, y, z = (10, 20, 30) this is tuple
	- swaping of values
		- (x, y) = (y, x)
	- list
		- Lists are Easy, Powerful & Flexible
			- Ordered
			- Hetrogenous
			- Mutable
			- Size can be changed
			- Nestable
		- x = [1, 2, 3] this is list
		- y = x
		- y.append(4)
		- y and x will have [1, 2, 3, 4]
		- mixed_list = [1, "Hello", 0.5, True]
		- slice_list[3] = 5
		- mixed_list.append([2, 3])
			- ```
			  [1, 'Hello', 0.5, True, [2, 3]]
			  ```
		- mixed_list.extend([2, 3])
			- ```
			  [1, 'Hello', 0.5, True, 2, 3]
			  ```
		- mixed_list.insert(2, 'world')
			- ```
			  [1, 'Hello', 'world', 0.5, True, 2, 3]
			  ```
		- mixed_list.remove('world')
			- ```
			  [1, 'Hello', 0.5, True, 2, 3]
			  ```
		- pop
			- int_list = [1, 2, 7, 4, 9, 11, 11]
			- `int_list.pop()` will return `11` and `int_list` changed to `[1, 2, 7, 4, 9, 11]`
		- index
			- mixed_list = [1, 'Hello', 0.5, True, 2, 3]
			- mixed_list.index('Hello') returns `1`
		- count
			- int_list = [1, 2, 7, 4, 9, 11, 11, True]
			- int_list.count(11)
			- Note:: in a list `1`, `Ture` and `0`, `False` will be treated as same `count()`
		- reverse
			- int_list.reverse()
		- sort
			- int_list.sort()
			- note:: only can be performed on integer list only. otherwise it will throw error
		- sum(int_list)
		- len(int_list)
		- min(int_list)
		- max(int_list)
		- queue FIFO
			- name_queue = ['gnr', 'src']
			- name_queue.insert(0, 'ksm')
			- name_queue.remove(0, 'ksm')
		- for performing queue FIFO
			- from collections import deque
			- name_queue2 = deque(['ksm', 'gnr', 'src'])
			- name_queue2.append('rs')
		- combined_list = int_list + mixed_list
		- nested_list = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
			- nested_list[0]
			- [1, 2, 3]
			- nested_list[0][1]
			- 2
		- slice
			- [start:stop:step] start index included, stop index not included
			- note: if step `-1` then it will return in reverse order
		- copy
			- list1 = [1, 2, 7, 4, 9]
			- list2 = list1.copy()
			- note:: in nested list, copy creates shallow copy means any changes to a list will effect others also. so it is advisable to create shallow copy.
			- import copy
			- list4 = copy.deepcopy(list1)
		- list function
			- x = list('hello')
				- ```
				  ['h', 'e', 'l', 'l', 'o']
				  ```
- comments
  collapsed:: true
	- starts with `#` (short cut `ctrl` + `/`)
- data types
  collapsed:: true
	- numeric
	  collapsed:: true
		- int
		- float
	- string
	  collapsed:: true
		- string literal are surrounded by doble quotes ("") `"cat"`
		- new line character `\n`
		- concatenation `+`
	- boolean
	  collapsed:: true
		- True or False
	- compound
	  collapsed:: true
		- sequence
		  collapsed:: true
			- lists []
			  collapsed:: true
				- lists are mutable
				- mylist = [0, 1, "two", 3.2, false]
				- append `+`
					- mylist + another_list
				- access by index
					- mylist[2]
				- slice
					- mylist[1:4:2]
						- starting, ending (not inclusive), step
					- reverse the sequence
						- mylist[::-1]
				- Strings are also sequece but unmutable
			- tuples ()
				- tuples are immutable
				- mytuple = (0, 1, 2, "three")
			- set {}
			  collapsed:: true
				- contains only unique values
			- sets, tuples don't support indexing
			- membership with `in` operator
			  collapsed:: true
				- ```
				  print(1 in mylist)
				  print(1 in mytuple)
				  print(1 in myset)
				  ```
		- dictionary
		  collapsed:: true
			- key-value data structure
			- keys have to be immutable datatypes like strings, numbers
			- key in a dictionary has to be unique in the dictionary
			- dictionaries are accessed via keys
			- set the dictionary data by creating a new key
			- accessing non-existent with `[]`will give KeyError, better version is with `in` operator will return `True` or `False`
			- to get all keys use `keys()` function
			- to get all values use `values()` function
			- to iterate over the members of dictionary use `items()` function to get member as tuple.
	- Mapping Type
	- None Type
	- Binary Types
	- Custom Types
	- exercise
	  collapsed:: true
		- type(12)
		- isinstance(12, int)
		- 5 + 1.0 = 6.0 (int + float = float)
		- int(6.0) converts float to int
		- float(6) converts int to float
		- type(True) bool (boolean)
- arithmetic operations
  collapsed:: true
	- 10 + 5
	- 10 - 5
	- 10 * 5
	- 10 / 3 = 3.33333
	- 10 // 3 = 3 (floor division)
	- 10 ** 3 = 1000 (exponential)
	- 2 + 3 * 5 ** 2 = 77
	- 100 % 75 = 25 (modulus % to get the reminder)
	- operator precedence
	  collapsed:: true
		- parenthesis (), exponentiation **, (* , /), (+, -) left to right
		- and, or
		- (2 > 1) or (10 < 8) and (not True)
- conditional and logical operators
  collapsed:: true
	- indentation is important, python uses white space indentation to group together sets of statements for execution identified after `:`
	- `>`, `<`, `>=`, `<=`, `==`, `!=`
	- not True is False
	- not False is True
	- and
		- (2 > 1) and (10 > 11)
	- or
		- (2 > 1) or (10 > 11)
	- 22 == 20 + 2 (first arithmetic followed by logical)
	- result = "x is less than y" if (x < y) else "x is greater than or equal to y"
- loops
  collapsed:: true
	- while
		- used to read data continuously from data source
		- ```
		  answer = input("Should I stop?")
		  while answer != "yes":
		    print(answer)
		    answer = input("Should I stop?")
		  ```
		- developer should make sure to have loop terminating statement
	- for
		- ```
		  days = ["Mon", "Tue", "Wed", "Thu", "Fri", "Sat", "Sun"]
		  for d in days:
		    print(d)
		  ```
		- use `for` over `while` for a collection
	- `break`
		- `break` statement used to break out of the loop
		- ```
		  days = ["Mon", "Tue", "Wed", "Thu", "Fri", "Sat", "Sun"]
		  for d in days:
		    if (d == "Wed"):
		      break
		    print(d)
		  ```
	- `continue`
		- `continue` statement used to break current iteration and continue with next iteration in the loop
		- ```
		  days = ["Mon", "Tue", "Wed", "Thu", "Fri", "Sat", "Sun"]
		  for d in days:
		    if (d == "Wed"):
		      continue
		    print(d)
		  ```
	- using the `enumerate()` function to get an index and an item. return a tuple using the function.
		- ```
		  for i, d in enumerate(days):
		    print(i, d)
		  ```
- function
  collapsed:: true
	- larger programs are organised into reusable blocks of code known as functions.
	- if a function is executed it will give return
	  collapsed:: true
		- function definition
		  collapsed:: true
			- ```
			  def my_function(x):
			      return 0
			  ```
		- function calling
		  collapsed:: true
			- ```
			  my_function(5) == 0
			  ```
	- example
	  collapsed:: true
		- `print()`
		- ```
		  def hello_func():
		    print("hello world!")
		    name = input("What is your name? ")
		    print("Nice to meet you,", name)
		  
		  hello_func()
		  ```
	- function that returns a value
	  collapsed:: true
		- ```
		  # function that returns a value
		  def cube(x):
		    return x*x*x
		  
		  result = cube(3)
		  print(result)
		  ```
	- function with default parameter
	  collapsed:: true
		- ```
		  # function with default value for an parameter
		  def hello_func(greeting, name=None):
		    print("hello world!")
		    if(name == None):
		      name = input("what is your name? ")
		    print(greeting, name)
		  
		  hello_func("nice to meet you.", "Joe")
		  hello_func("nice to meet you.")
		  ```
	- named parameters allows to feed parameters without remembering order
	  collapsed:: true
		- ```
		  hello_func(name="Joe", greeting="nice to meet you.")
		  ```
	- function with variable number of parameters
	  collapsed:: true
		- ```
		  def multi_add(start, *args):
		    result = start
		    for x in args:
		      result = result + x
		    return result
		  
		  print(multi_add(10, 4, 5, 6, 7))
		  ```
		- var arg should come as the last parameter
	- core library
	  collapsed:: true
		- ```
		  # LinkedIn Learning Python course by Joe Marini
		  # Example file for using built-in functions
		  #
		  
		  mystring = "The quick, brown fox jumped over the lazy dog!"
		  mynumbers = [1,3,5,6,9,12,14,17,20,30]
		  
		  # the len() function calculates the length of a sequence
		  print(len(mystring))
		  print(len(mynumbers))
		  
		  # the max() and min() functions will find the largest and smallest value in a sequence
		  print(max(mystring))
		  print(min(mynumbers))
		  
		  # the str() function will return a string version of an object
		  prefix = "result: "
		  result = 5
		  print(prefix + str(result))
		  
		  # range(start, stop, step) will create a range of numbers 
		  # You can use ranges along with loops 
		  for i in range(5, 15, 2):
		    print(i)
		  
		  for i in range(5, len(mystring), 2):
		    print(mystring[i])
		  
		  # string interpolation
		  # the print function itself is pretty flexible - you can embed variables directly in it
		  greeting = "Hello!"
		  count = 10
		  
		  print(f"{greeting} you are vistor number {count}")
		  ```
- `pass` is null operation
- errors
  collapsed:: true
	- syntax error
	- indentation error
- classes
  collapsed:: true
	- encapsulating functionality and data together and reused as complete module in other projects
	-
	-
- modules
	- library module can be imported
	- math library
	  collapsed:: true
		- ```
		  import math
		  
		  math.log(2.7182)
		  math.log(100, 10)
		  math.exp(10)
		  math.sqrt(64)
		  math.pi
		  math.floor(2.5) round down
		  math.ceil(2.1) round up
		  abs(-30)
		  round(233.234, 1) #(default decimal places is 0)
		  ```
	- tabulate
		- https://pypi.org/project/tabulate
- resources
  collapsed:: true
	- Thonny
	- videos
		- Udemy_100_Days_of_Code_The_Complete_Python_Pro_Bootcamp_2024_8
		- linked in object oriented programming python
	- books
		- learn python