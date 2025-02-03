- jdk installation
	- sdk install java 17.0.7.fx-zulu
	- sdk default java 17.0.7.fx-zulu
	- set environment variable for your account
		- variable: `JAVA_HOME` value: `E:\tools\sdkman\candidates\java\current`
		- add `%JAVA_HOME%\bin` to `PATH`
- [[jshell]]
- standard version
	- operators
	  collapsed:: true
		- `+`: add two values
		- `-`: subtracts two values
		- `*`: multiplies two values
		- `/`: divide two values
			- for integers without reminders
			- for floating numbers it produces a floating number
		- `%`: gives the reminder for integers
		- equality operator & relational operators
			- |==|equal to|
			  |!=|not equal to|
			  |>|greater than|
			  |>=|greater than or equal to|
			  |<|lesser than|
			  |<=|lesser than or equal to|
		- conditional operators
			- equality & relational operators can be combined with conditional operators:
				- && means AND
				- || means OR
	- variables
	  collapsed:: true
		- variable is a container which holds a value, text or object
		- each variable gets a `name`
		- java is strongly typed.
		- every variable needs a type before anything stored in it
		- |int|32 bit (4 bytes)|-2,147,483,648 to 2,147,483,647|
		  |byte|8 bit|-128 to +127|
		  |short|16 bit|-32,768 to 32,767|
		  |long|64 bit|-9,223,372,036,854,775,808 to 9,223,372,036,854,775,807|
		  |double (floating double numbers)|64 bit|4.9E-324 to 1.8E+308|
		  |float (floating numbers with simple precision)|32 bit|1.4E-45 to 3.4E+38|
		- ```
		  // step 1: variable definition
		  int number;
		  
		  // step 2: assign 
		  number = 43;
		  
		  // both steps can be combined like this
		  // int number = 43;
		  ```
		- LATER byte implementation is a type of ring
		  :LOGBOOK:
		  CLOCK: [2025-02-02 Sun 13:55:00]--[2025-02-02 Sun 13:55:01] =>  00:00:01
		  :END:
		- Strings
			- text values like "hello world!"
			- Strings are sequences of characters
			- they are written in double quotation marks like this: "hello world!"
			- the values can be concatenated with plus sign:
				- String h = "hello " + "world!" ;
			- String is non-primitive variable type. it is an object/class.
		- char
			- for characters like 'j' or ASCII values like 74 which is for 'j'
		- boolean
			- logical values true or false
			- boolean b = true;
			- boolean b = i == 1;
	- compound assignment
	  collapsed:: true
		- `+=` assigns the result of the addition
			- a += b is same as a = a + b
		- `-=` assigns the result of subtraction
		- `*=` assigns the result of multiplication
		- `/=` assigns the result of division
		- `%=` assigns the remainder of division
		- `bitwise AND` `&=` assigns the result of bitwise AND
			- a &= b is same as a = a & b which is same as a = a && b
		- `bitwise OR` `|=` assigns the result of bitwise OR
	- unary operations
	  collapsed:: true
		- |i++|post increment|
		  |++i|pre increment|
		  |i--|post decrement|
		  |--i|pre decrement|
		  |!|Negation NOT|
- [[maven]]
	- installation
		- sdk install maven 3.9.8
	- set environment variable for your account
		- variable: `MVN_HOME` value: `E:\tools\sdkman\candidates\maven\current`
		- add `%MVN_HOME%\bin` to `PATH`