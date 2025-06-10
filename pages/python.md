- devops
	- installation
		- py --version
	- ide: vscode, vscode extensions: pylance, python, python debuuger
	- google colab
	- github codespaces
	- python interpreter
		- REPL - Read Evaluate Print Loop
	- python cli
		- python3
		- `exit()` or `Ctrl + Z`
- python
	- is interpreted language
	- is dynamically typed language
- Data Types
	- numeric
	  collapsed:: true
		- int
		- float
	- string
	  collapsed:: true
		- "cat"
	- boolean
		- True or False
	- compound
		- sequence
			- lists []
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
				- contains only unique values
				- do not
		- dictionary
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
- Arithmetic operations
  collapsed:: true
	- 10 + 5
	- 10 - 5
	- 10 * 5
	- 10 / 3 = 3.33333
	- 10 // 3 = 3 (floor division)
	- 10 ** 3 = 1000 (exponential)
	- 2 + 3 * 5 ** 2 = 77
	- 100 % 75 = 25 (modulus % to get the reminder)
- python core library math functions
  collapsed:: true
	- abs(-30)
	  id:: 67249246-4ff5-4d0a-9cfc-66602d8a8295
	- round(233.234, 1) (default decimal places is 0)
- math library
  collapsed:: true
	- import math
	- math.log(2.7182)
	- math.log(100, 10)
	- math.exp(10)
	- math.sqrt(64)
	- math.pi
	- math.floor(2.5) round down
	- math.ceil(2.1) round up
- logical operators
  collapsed:: true
	- `>`, `<`, `>=`, `<=`, `==`, `!=`
	- not True is False
	- not False is True
	- and
		- (2 > 1) and (10 > 11)
	- or
		- (2 > 1) or (10 > 11)
	- 22 == 20 + 2 (first arithmetic followed by logical)
- operator precedence
  collapsed:: true
	- parenthesis (), exponentiation **, (* , /), (+, -) left to right
	- and, or
	- (2 > 1) or (10 < 8) and (not True)
- `pass` is null operation
- if a function is executed it will give return
  collapsed:: true
	- function definition
	  def my_function(x):
	      return 0
	- function calling
	  my_function(5) == 0
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
- python
  collapsed:: true
	- indentation is important in python (white space, tabs before statements)
- IDE: pycharm
- keyword
- function
  collapsed:: true
	- print()
- data types
  collapsed:: true
	- Strings
		- string literal are surrounded by doble quotes ("")
		- new line character `\n`
		- concatenation `+`
- errors
  collapsed:: true
	- syntax error
	- indentation error
- comments
  collapsed:: true
	- starts with `#` (short cut `ctrl` + `/`)
- resources
	- Thonny
	- videos
		- Udemy_100_Days_of_Code_The_Complete_Python_Pro_Bootcamp_2024_8
	- books
		- learn python