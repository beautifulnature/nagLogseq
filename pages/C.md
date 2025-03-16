- tools
  collapsed:: true
	- sudo apt update
	- sudo apt install gcc build-essential
	- ide
	  collapsed:: true
		- sublime-text editor
			- https://www.sublimetext.com/docs/linux_repositories.html#apt
			- $ subl
		- visual studio
		- visual studio code
		- Eclipse CDT
		- Code::Blocks
		- Code Lite
- c-language
  collapsed:: true
	- ISO 9899
	- programming langauge
	  collapsed:: true
		- compiled / interpreted
		- garbage collector
		- strongly typed or not
		- memory safe?
	- variables
	  collapsed:: true
		- variables are used for storing data during program execution
		- Data Types
			- simple or primitive types (4 integer types, 3 floating-point types, 1 char type)
			- |Data Type|Size (Byte)|Description|Range|
			  |char|1 (8 bits)|Integer or character|-128 to +127|
			  |short|2 (16 bits)|Ineger|-32768 to +32767|
			  |int|4 (16 bits)||-2^31 to +2^31-1|
			  |long|4 or 8 (32 bits)||-2^31 to +2^31-1|
			  |long long|8 (64 bits)||-2^63 to +2^63-1|
			  |float|4|Floating-point number||
			  |double|8|||
			  |long double|8 or 16|||
			- modern compilers make int 32 bits means 4 bytes.
			- `sizeof` operator returns the number of bytes that a type occupies. The type returned is `size_t`, which is an alias for an integer type. Specifier %zu (%Iu) to format this type with printf.
			- integers can also be assigned by using octal or hexadecimal notation in addition to decimal  notation.
			- By default, all integer types are signed. This can be explicitly specified by using the `signed` keyword.
			  collapsed:: true
				- |data type|range|
				  |signed char|-128 to +127|
				  |signed short|-32768 to +32767|
				  |signed int|-2^31 to +2^31-1|
				  |signed long|-2^31 to +2^31-1|
				  |signed log long|-2^63 to +2^63-1|
				- If only positive values need to be stored, can be declared as `unsigned`
					- |data type|range|
					  |unsigned char|0 to 255|
					  |unsigned short|0 to 65535|
					  |unsigned int|0 to 2^32-1|
					  |unsigned long|0 to +2^32-1|
					  |unsigned log long|0 to +2^64-1|
				- when an unsigned value is printed, the specifier %u is used for the unsigned char, short, and int types.
				- unsigned long type is specified with %lu and unsigned long long is specified with %llu
				- |abbreviations|full syntax|
				  |unsigned|unsigned int|
				  |signed|signed int|
				  |short|short int|
				  |long|long int|
			- Sized Integers
			  collapsed:: true
				- exact-width integer types can be enabled by including `stdint.h` header file
					- ```
					  #include <stdint.h>
					  
					  /* signed exact-width integers */
					  int8_t iSmall; /* 8 bits */
					  int16_t iMedium; /* 16 bits */
					  int32_t iLarge; /* 32 bits */
					  int64_t iHuge; /* 64 bits */
					  ```
				- unsigned versions of these types are available as well.
					- ```
					  /* unsigned exact-width integers */
					  uint8_t uSmall; /* 8 bits */
					  uint16_t uMedium; /* 16 bits */
					  uint32_t uLarge; /* 32 bits */
					  uint64_t uHuge; /* 64 bits */
					  ```
				- C99 prior, Microsoft C has implemented with different type names
					- ```
					  /* visual studio signed exact-width integers */
					  __int8 iSmall; /* 8 bits */
					  __int16 iMedium; /* 16 bits */
					  __int32 iLarge; /* 32 bits */
					  __int64 iHuge; /* 64 bits */
					  ```
			- Floating-Point Types
			  collapsed:: true
				- floating-point types can store real numbers with different levels of precision.
				  collapsed:: true
					- |type|precision|
					  |float|7 digits|
					  |double|15 digits|
					  |long|same as double|
				- when printing a floating-point number you can limit the decimal places
				  collapsed:: true
					- printf("%.2f", myFloat);
				- Floating-point numbers can be expressed using decimal, exponential, or hexadecimal notation.
				  collapsed:: true
					- ```
					  double fDec = 1.23;
					  double fExp = 3e2; /* 3*10^2 = 300 */
					  double fHex = 0xAp2 /* 10*2^2 = 40 */
					  ```
					- exponential (scientific) notation is used by adding E or e followed by decimal exponent.
					- hexadecimal floating-point notation uses P or p to specify binary exponent.
			- Literal Suffixes
			  collapsed:: true
				- `U` for unsigned, `L` for long, `LL` for long long type
				- ```
				  int i = 10;
				  long l = 10L;
				  unsigned long ul = 10UL;
				  ```
				- floating-point literal is treated as double. `F` or `f` suffix can be used. `l` or `L` suffix specifies `long double`
					- ```
					  float f = 1.23F;
					  double d = 1.23;
					  long double ld = 1.23L;
					  ```
				- The compiler implicitly converts literals to whichever type is necessary, so this type distinction for literals is usually not necessary.
				- If the F suffix is left out when assigning to float variable, the compiler may give a warning since the conversion from double to float involves a loss of precision.
			- Char Type
			  collapsed:: true
				- `char` type is commonly used to represent ASCII characters. Character constants are enclosed in single quotes and can be stored in a variable of `char` type.
				- `%c` used to display char
				- `%d` used to display numerical value
			- Bool Type
			  collapsed:: true
				- `_Bool` type which is a value that can only be either 1 (true) or 0 (false)
				- _Bool b = 0; /* false value */
				- standard header `stdbool.h`, `_Bool` is accessed via name `bool`. macros `true` and `false` are defined for 1 and 0.
				- there is no format specifier for bool. `%d` will print int value 1 or 0.
		- variable declaration
		  collapsed:: true
			- identifier can consist of letters, numbers, and underscores, but cannot start with a number. cannot contain spaces or special characters and must not be a reserved keyword.
			- identifier should be descriptive for readability
			- C is case-sensitive
			- variable declaration
				- data_type identifier;
			- initialisation (by `=` sign)
				- identifier = initial_value;
			- declaration and assignment can be combined
				- data_type identifier = initial_value;
			- assignment (by `=` sign) or assignment operator
				- identifier can be reassigned with a value
				- identifier = initial_value;
			- when a variable is assigned a value it then becomes defined.
			- short hand for declaring more than one variable of same type using comma operator (,)
				- int x = 1, y = 2, z;
			- a variable value can be reassigned to another variable
				- int a = x;
		- variable scope
		  collapsed:: true
			- local scope
				- only available to the function locally
			- global scope
				- declared outside of the function and available to all functions
			- ```
			  int globalVar; /* global varaible */
			  
			  int main(void){
			  	int localVar; /* local variable */
			  }
			  ```
			- global variables are automatically initialised to zero by the compiler, whereas local variables are not initialised at all. Uninitialized local variables will therefore contain whatever garbage is already present in that memory location.
				- ```
				  int globalVar; /* initialised to 0 */
				  
				  int main(void){
				  	int localVar; /* uninitialised */
				  }
				  ```
			- Using uninitailsed variables is a common programming mistake that can produce unexpected results. It is therefore a good idea to always give your local variables initial values when they are declared.
				- ```
				  int main(void){
				  	int locarVar = 0; /* initialesed to  */
				  }
				  ```
			- variables can be declared anywhere within a function's scope.
				- ```
				  int main(void){
				  	int var1;
				      /* other statements */
				      int var2;
				  }
				  ```
		- printing variables using `printf()`
		  collapsed:: true
			- format specifier must be matched by corresponding argument of the correct type
			- |Specifier|Output|
			  |%d or %i|char, short, or int|
			  |%c|char|
			  |%s|string of characters|
			  |%f|float or double|
			  |%Lf|long double|
			  |%ld|long int|
			  |%lld|long long int|
			  |%u|unsigned char, short or int|
			  |%lu|unsigned long int|
			  |%llu|unsigned long long int|
			  |%p|pointer address|
	- pre-processor
	  collapsed:: true
		- starts with `#`
		- `#include <stdio.h>` to bring in the code from libraries
		- `#define` to define constants
		- ```variables.c
		  #define DEBUG
		  
		  int main()
		  {
		  	#ifdef DEBUG
		      printf("WE ARE IN DEBUG MODE: %s:%d", __FILE__, __LINE__);
		      #endif
		  }
		  ```
		- In case of no DEBUG declarative, the above can be accomplished using gcc
			- gcc variables.c -o variables -DDEBUG
	- compilation process
	  collapsed:: true
		- preprocessor
		- compilation
		- assembling
		- linking
	- arrays
	  collapsed:: true
		- an array is a data structure used to store a collection of values that all have the same data type.
		- syntax
			- int ids[32] = {1, 2, 3};
			- int ids[] = {1, 2, 3}; /* alternative - array size can be left out to let the array size be decided by the number of values assigned */
		- arrays are zero index
		- assignment
			- ids[0] = 2;
		- accessing elements
			- ids[0];
		- multi-dimensional arrays
		  collapsed:: true
			- ```
			  int myArray[2][2] = { {0, 1}, {2, 3}};
			  int my2Array[2][2] = { 0, 1, 2, 3}; /* inside curly braces are optional. but including them is good practice to understand the code easier */
			  myArray[0][0] = 0;
			  myArray[0][1] = 1;
			  ```
		- Arrays and Pointers
		  collapsed:: true
			- An array in C can be treated as a constant pointer that points to the first element in the array.
			- array elements can referenced with pointer arithmetic.
			- by incrementing the pointer by one, you move to the next element in the array, because changes to a pointer's address are implicitly multiplied by the size of the pointer's data type.
			- ```
			  int myArray[3] = {13, 12, 31};
			  *myArray = 10; /* myArray[0] = 10; changes first element 13 and assigns 10 to it */
			  *(myArray+1) = 25; /* myArray[1] = 25; changes second element 12 and assigns 25 to it */
			  ```
			- four pointer airthmetics
				- `+`, `-`, `++`, `--`
				- ```
				  int* ptr = &myArray;
				  printf("Address of myArray[0] = %d is %p\n", *ptr, ptr);
				  ptr++;
				  printf("Address of myArray[1] = %d is %p\n", *ptr, ptr);
				  ptr++;
				  printf("Address of myArray[2] = %d is %p\n", *ptr, ptr);
				  ```
			- Array size
				- sizeof() - to determine length of an array in bytes
				- number of elements x size of data type
				- ```
				  int myArray[2] = {1, 2};
				  myArray[2] = 3; /* out of bounds */
				  ```
	- strings
	  collapsed:: true
		- Strings under the hood are array of characters. delimited by "".
		  collapsed:: true
			- char myString[] = "Hi";
		- Strings are NULL terminated, `\0`, null character, which is used to know where the string ends.
		- null character added automatically by the compiler
		  collapsed:: true
			- char myString[3] = { 'H', 'i', '\0' };
		- format strings
		  collapsed:: true
			- %s is the string formatter with printf function
		- character pointer
		  collapsed:: true
			- string pointer location is read-only block unlike char array characters in string cannot be changed.
			- ```
			  char* ptrs = "Hi";
			  printf("%s\n", ptrs);
			  ```
		- escape characters
		  collapsed:: true
			- |character|meaning|
			  |\\n|newline|
			  |\\t|horizontal tab|
			  |\\v|vertical tab|
			  |\\b|backspace|
			  |\\r|carriage return|
			  |\\0|null character|
			  |\\000|octal number(1-3 digits)|
			  |\\f|form feed|
			  |\\a|alert sound|
			  |\\'|single quote|
			  |\\"|double quote|
			  |\\\|backslash|
			  |\\?|question mark|
			  |\\xhh|hexadecimal number|
			- ```
			  char line = '\n'; /* escape code */
			  line = '\012'; /* octal notation */
			  line = '\x0A'; /* hexadecimal notation */
			  ```
			- supersede `\` to ASCII characters
		- common string operations functions are included in `string.h`
		  collapsed:: true
			- destination is large enough to hold the entire string
			- `strcat(dest, src)` string concatenation
			- strcat(s1, s2); /* append s2 to s1 */
			- strcmp(str, otherstr)
				- if all matches returns zero
			- strcpy
				- strcpy(dest, src); destination content will be replaced by source
				- strncpy(dest, src, n); // n bytes
			- strlen (excluding null char)
			- sizeof
				- to get size in bytes or to get allocated size
	- operators
	  collapsed:: true
		- numerical operator is a symbol that makes the program perform a specific mathematical or logical manipulation
		- arithmetic operators
		  collapsed:: true
			- |operation|symbol|
			  |+|addition|
			  |-|subtraction|
			  |*|multiplication|
			  |/|division|
			  |%|modulus|
			- Note: division gives incorrect result, if it operates on integers, one must be converted to float explicitly. If it operates on float no truncation happens.
			- increment and decrement opeators
				- increment (++) decrement (--)
					- x++; /* x = x + 1; */
					- x--; /* x = x - 1; */
				- x++; /* post-increment */
				- x--; /* post-decrement */
				- ++x; /* pre-increment */
				- --x; /* pre-decrement */
		- comparison operators (returns 1 or 0 i.e true or false)
		  collapsed:: true
			- |operator|symbol|
			  |equal to|==|
			  |not equal to|!=|
			  |greater than|>|
			  |less than|<|
			  |greater than or equal to|>=|
			  |less than or equal to|<=|
		- logical operators
		  collapsed:: true
			- logical operators are used together with comparison operators
			- logical and (&&) evaluates to true if both left and right sides are true.
			- logical or (||) is true if left or right side is true.
			- for inverting boolean result use logical not (!) operator.
			- for `logical and` and `logical or` the right side will not be evaluated if the result is already determined by the left side
		- bitwise operators
		  collapsed:: true
			- bitwise operators can manipulate individual bits inside an integer.
			- bitwise left shift operator (<<) moves all bits to the left with specified number of steps.
			- `bitwise and` `&`
				- x = 5 & 4; /* 101 & 100 = 100 (4) */
			- `bitwise or` `|`
				- x = 5 | 4; /* 101 | 100 = 101 (5) */
			- `bitwise xor` `^` exclusive or
				- x = 5 ^ 4; /* 101 ^ 100 = 001 (1) */
			- `bitwise leftshift` `<<`
				- x = 4 << 1; /* 100 << 1 = 1000 (8) */
			- `bitwise rightshift` `>>`
				- x = 4 >> 1; /* 100 >> 1 = 10 (2) */
			- `bitwise inver` `~`
				- x = ~4;
				- ```
				  ~00000100 = 11111011 (-5)
				  MSB - Most significant bit is 1 means -ve 0 means +ve
				  flip the bits 00000100 add 1 results 00000101 is 2^2+2^0 = 5.
				  negate the result -5
				  ```
			- bitwise operations also have combined assignment operations
				- ```
				  int x = 5; x &= 4;
				  	x = 5; x |= 4;
				      x = 5; x ^= 4;
				      x = 4; x <<= 1;
				      x = 4; x >>= 1;
				  ```
		- operator precedence
			- expressions evaluated from left to right
			- operator with lowest precedence will be evaluated first
			- |precedence|operator|
			  |1|`()``[]` `.` `->` `x++` `x--`|
			  |2|`!` `~` `++x` `--x` `(type)` `sizeof` `*` `&`|
			  |3|`*` `/` `%`|
			  |4|`+` `-`|
			  |5|`<<` `>>`|
			  |6|`<` `<=` `>` `>=`|
			  |7|`==` `!=`|
			  |8|`&`|
			  |9|`^`|
			  |10|`|`|
			  |11|`&&`|
			  |12|`||`|
			  |13|`=` `op=`|
			  |14|`,`|
			- use brackets `()` to give  better understanding
	- pointers
	  collapsed:: true
		- pointer is a variable that contains the memory address of another variable called the pointee.
		- creating pointer
			- int* p; /* pointer to an integer */
			- int *q; /* alternative syntax */
			- address-of operator `&` to retrieve the address and assign to pointer variable.
			- int i = 10;
			- p = &i; /* address of i assigned to p */
		- dereferencing pointers
			- pointer contains the memory address of the variable. referencing the pointer will retrieve this address. to obtain the actual value stored in that address, the pointer must be prefixed with an asterisk, known as the dereference operator (*).
			- \*p = 20; /* value of i changed through p */
			- if a second pointer is created and assigned the value of the first pointer, it will the get a copy of the first pointer's memory address.
				- int* p2 = p; /* copy address stored in p */
		- pointing to a pointer
			- ```
			  int  i = 10;
			  int* firstPointer = &i;
			  int** secondPointer = &firstPointer;
			  
			  printf("Address of first pointer: %p through second pointer\n", secondPointer);
			  printf("Address of i: %p through *second pointer\n", *secondPointer);
			  printf("Value of i: %d through **secon pointer", **secondPointer);
			  ```
		- Null Pointer
			- A pointer should be set to zero when it is not assigned to a valid address. such a pointer is called a _null pointer_. Doing this allows you to check whether the pointer can be safely dereferenced, because a valid pointer will never be zero.
			- The constant _NULL_ can also be used to signify a null pointer. _NULL_ is typically defined as zero in C (defined in stdio.h, stddef.h)
			- ```
			  #include <stdio.h>
			  
			  int* p = NULL; /* null pointer */
			  int* p2 = 0; /* null pointer */
			  ```
	- functions
	  collapsed:: true
		- defining functions
		  collapsed:: true
			- ```
			  /* returnType functionName(functionParameters){ */
			  		/* code block */
			          return valueOfSpecifiedReturnType;
			  /* } */
			  /* if nothing to retun use void */
			  /* if function doesn't accept any arguments use void */
			  void myFunction(void) {
			  	printf("hello world");
			  }
			  ```
		- calling functions
		  collapsed:: true
			- ```
			  int main(void){
			  	myFunction();
			  }
			  ```
		- parameters
		  collapsed:: true
			- function parameters, passing arguments
			  collapsed:: true
				- in function definition function parameters are defined within parenthesis.
				- while calling the function, arguments will passed
			- void parameter
			  collapsed:: true
				- in C, functions that leave out the `void` keyword from their parameter list are allowed to accept an unknown number of arguments.
				- if no arguments are accepted then it is must to include void in parameter list to make it parameterless function.
					- ```
					  /* accepts no arguments */
					  void foo(vod){}
					  
					  /* accepts unknown number of arguments */
					  vod bar(){}
					  ```
			- variable paramerter lists
			  collapsed:: true
				- function can be defined to accept a variable number of arguments.
				- first parameter is number of arguments, followed by argument list
				- prameter list must end with ellipsis (...)
				- int parmeter is typically incuded to let the function know the number of extra arguments that are passed to it.
				- to access arguments includ stdarg.h header file.
					- this header defines new type called `va_list`
					- 3 functions that operate on variables of this type: `va_start`, `va_arg`, `va_end`
					- ```
					  #include <stdio.h>
					  #include <stdarg.h>
					  int sum(int num, ...) {
					  	va_list args; /* variable argument list */
					  	int sum = 0, i = 0;
					  	va_start(args, num); /* initialize argument list */
					  	for (i = 0; i < num; i++) /* loop through arguments */
					  		sum += va_arg(args, int); /* get next argument */
					  	va_end(args); /* free memory */
					  	return sum;
					  }
					  	
					  int main(void) {
					  	printf("Sum of 1+2+3 = %d", sum(3,1,2,3)); /* 6 */
					  }
					  ```
			- C does not allow function overloading or default parameter values
		- return statement
		- forward declaration
		  collapsed:: true
			- function must be declared before it can be called.
				- 2 approches
				  collapsed:: true
					- placing function implementation before it is called (referenced).
					- adding declaration (forward declaration) known as prototype.
						- parameter names do not need to be included in prototype only data types are required
						- ```
						  void myFunction(int a); /* proto type */
						  /* void myFunction(int); */
						  int main(void){
						  	myFunction(0);
						  }
						  
						  void myFunction(int a){}
						  ```
		- pass by value
		  collapsed:: true
			- variables by default passed by value. this means only a copy of the value is passed to the function. therefore, changing the parameter in any way will not affect the original value.
			- ```
			  #include <stdio.h>
			  
			  void set(int i) { i = 1; }
			  
			  int main(void){
			  	int x = 0;
			      set(x); /* copy of vale of x is passed. but x can't be changed by set() function */
			      printf("%d\n", x);
			  }
			  ```
		- pass by address
		  collapsed:: true
			- alternative to pass by value is to use pointer syntax to pass the variable by address.
			- when an argument is passed by address, the parameter can be changed to replaced, and the change will affect the original variable.
			- ```
			  void set(int* i) { *i = 1; }
			  int main(void) {
			  	int x = 0;
			  	set(&x);
			  	printf("%d", x); /* "1" */
			  }
			  ```
			- arrays can be treated as pointers. they will automatically passed by address.
				- ```
				  void set(int a[]) { a[0] = 1; }
				  int main(void) {
				  	int x[] = { 0 };
				  	set(x);
				  	printf("%d", x[0]); /* "1" */
				  }
				  ```
		- return by value or address
		  collapsed:: true
			- by default a function returns by value
			- return by address, function return type is a pointer.
			- function should not return an expression or literal, it should return a variable.
			- the variable returned should never be a local variable.
			- return by address is commonly used to return an argument that has been passed to the function by address.
			- ```
			  int* byAdr(int* i) { (*i)++; return i; }
			  int main(void) {
			  	int a = 10;
			  	int *p = byAdr(&a);
			  	printf("%d", *p); /* "11" */
			  }
			  ```
		- inline functions
			- to improve performance, the programmer can recommend that the compiler inlines the calls to a specific function by using the `inline` function modifier.
			- ```
			  inline int increment(int a) { return a + 10; }
			  
			  int main(void) {
			  	int i;
			      for(i = 0; i < 100;){
			      	i = increment(i);
			          printf("%d\n", i);
			      }
			  }
			  ```
			- note that the `inline` keyword is only a recommendation. the compiler may choose to ignore this recommendation and it may also inline functions that dont have the `inline` modifier.
	- comments
	  collapsed:: true
		- comments are used to insert notes into the source code.
		- multi-line comment
			- ```
			  /* 	multi-line
			  	comment */
			  ```
		- single line comment
			- ```
			  // single-line comment
			  ```
	- whitespace
	  collapsed:: true
		- white space characters like comments, spaces, and tabs are generally ignored by the compiler.
	- conditionals
	  collapsed:: true
		- conditional statements are used to execute different code blocks based on different conditions
		- if statement
			- the if statement will execute only if the expression inside the parentheses is evaluated to true.
			- in C, this does not have to be a Boolean expression. it can be any expression that evaluates to a number, in which case 0 is false and all other numbers are true.
			- to test for other conditions, the if statement can be extended by any number of else/if clauses.
			- the if statement can have one else clause at the end, which will execute if all the previous conditions are false.
		- switch statement
			- `switch` statement checks for equality between an integer and a series of `case` labels, and then passes execution to the matching case. it may contain any number of `case` clauses, and it can end with a `default` label for handling all other cases.
			- ```
			  switch (x){
			  	case 0:
			      	printf("x is 0");
			      	break;
			      case 1:
			      	printf("x is 1");
			      	break;
			  	default:
			      	printf("x is not 0 or 1");
			          break;
			  }
			  ```
			- note that the statements after each `case` label end with the `break` keyword to skip the rest of the `switch`. if `break` is left out, execution will fall through to the next case, which can be useful if several cases need to be evaluated in the same way.
		- ternary operator(`?:`)
			- ternary operator can replace single `if/else` clause.
			- this operator takes 3 expressions. if first one is true then second expression is evaluated and returned; and if it is false, the third one is evaluated and returned.
			- x = (x < 0.5) ? 0 : 1;
	- loops
	  collapsed:: true
		- loops are used to execute a specific code block multiple times.
		- while loop
		  collapsed:: true
			- loop will continue as long as the condition remains true. condition is only checked at the start of each iteration (each loop).
				- ```
				  int i = 0;
				  while (i < 10){
				  	printf("%d\n", i);
				      i++;
				  }
				  ```
		- do-while loop
		  collapsed:: true
			- in do-while loop condition check happens after code block.
			- do-while loop ends with `;`
				- ```
				  int j = 0;
				  do {
				  	printf("%d", j);
				      j++;
				  } while (j < 10);
				  ```
		- for loop
		  collapsed:: true
			- for loop uses 3 parameters.
				- first parameter, initialises a counter and is always executed once before the loop.
				- second parameter, holds the condition and is checked before each iteration.
				- 3 parameter, contains the increment counter and is executed at the end of each iteration.
			- if first parameter contain declaration, then scope of this variable is limited to the for loop.
				- ```
				  for(int k = 0; k < 10; k++){ /* k scope limited to the loop */
				  	printf("%d\n", k);
				  }
				  ```
				- ```
				  int k;
				  for(k = 0; k < 10; k++){
				  	printf("%d\n", k);
				  }
				  ```
				- split 1st and 3rd parameter into several statements using `,` operator
					- ```
					  int k, m;
					  for (k = 0, m = 0; k < 10; k++, m--) {
					  	printf("%d", k+m); /* 000... (10x) */
					  }
					  ```
				- infinite loop
					- ```
					  for(;;){
					  	/* infinite loop */
					      /* there should be another exit condition defined */
					  }
					  ```
		- break and continue
		  collapsed:: true
			- 2 jump statements can be used inside loop
			- break ends the loop structure.
			- continue skips the rest of the current iteration and continues at the beginning of the next iteration.
				- ```
				  int i;
				  for(i = 0; i < 10; i++){
				  	if(i == 2){
				      	continue;
				      }else if(i == 5){
				      	break;
				      }
				      printf("%d\t", i);
				  }
				  ```
		- goto statement
			- 3rd jump statement, `goto` performs unconditional jump to a specified label within the same function.
			- this instruction not used due to difficulty to follow.
			- ```
			  goto myLabel;
			  /* ... */
			  myLabel: /* label declaration */
			  ```
	- typedefs
	  collapsed:: true
		- an alias of a type can be created using `typedef` keyword followed by the type and alias name. by convention, uppercase letters are commonly used.
			- ```
			  typedef unsigned char BYTE;
			  ```
		- once defined, the alias can be used as a synonym for its specified type.
			- ```
			  BYTE b; /* unsigned char */
			  ```
			- ```
			  typedef struct {int point;} score;
			  score a, b, c;
			  a.points = 10;
			  ```
	- enums
	  collapsed:: true
		- an enum is a user-defined type consisting of fixed list of named constants.
		- ```
		  enum color {RED, GREEN, BLUE};
		  
		  int main(void){
		  	enum color c = RED;
		  }
		  ```
		- enum variables may also be declared when enum is defined, by placing the variable names before semicolon. this position is known as the declaration list.
		- ```
		  enum color {RED, GREEN, BLUE} c, d;
		  printf("%d\n", c);
		  ```
		- enumerated constants are of the int type. enum will give the ordinal value starts with 0. these default values can be overridden by assigning values to the constants. values can be computed and do not have to be unique.
			- ```
			  enum color {
			  	RED = 5,
			      SCARLET = RED,
			      BLUE = RED + 2,
			  }
			  ```
		- enums in C are not typesafe because enums are essentially integers.
			- ```
			  enum Color {
			      RED,
			      GREEN,
			      BLUE
			  };
			  
			  enum Shape {
			      CIRCLE,
			      SQUARE,
			      TRIANGLE
			  };
			  
			  enum Color c = RED;
			  bool flag = (c >= TRIANGLE); // This comparison is allowed
			  ```
		- enum a way to group a set of integer constants. enum identifier is not strictly necessary and may optionally omitte.
			- enum {RED, GREEN, BLUE} c;
		- enum conversions
			- ```
			  int i = RED;
			  enum color c = (enum color) i;
			  ```
		- enum scope
			- ```
			  /* Global enum */
			  enum speed { SLOW, NORMAL, FAST };
			  
			  int main(void){
			  	/* Local enum */
			      enum color { RED, GREEN, BLUE };
			  }
			  ```
	- structs
	  collapsed:: true
		- a `struct` or structure is a user-defined type used for grouping a collection of related variables under a single name.
		- structs allow data items of different kinds to be combined.
		- structs may contain  variables, pointers, arrays or other user-defined types. may not contain functions.
		- ```.syntax
		  struct identifier{
		  	/* code block */
		  }
		  
		  /* example: */
		  struct point {
		  	int x, y;
		  }
		  ```
		- struct objects
		  collapsed:: true
			- to declare a variable of struct type, the `struct` keyword is followed by the type name and variable identifier. variables of struct type are commonly referred to as objects or instances.
			- ```
			  int main(void){
			  	struct poin p; /* object (instance) declaration */
			  }
			  ```
			- objects may also be created when the struct is defined by placing the object names before the final semicolon. This position is called the declaration list.
			- if the optional struct identifier is left out, this becomes the only way to create objects of the struct type. such a struct is called unnamed struct and provides a way for programmers to prevent any more instances of the type from being created.
			  collapsed:: true
				- ```
				  struct /* unnamed struct */
				  {
				  	int x, y;
				  } a, b; /* object declarations */
				  ```
			- it is common in C to use `typedef` when defining structures.
			  collapsed:: true
				- ```
				  typedef struct point point;
				  
				  stuct point {
				  	int x, y;
				  }
				  
				  int main(void){
				  	point p; /* struct omitted */
				  }
				  ```
			- member access
			  collapsed:: true
				- variables of a struct type are called fields or members.
				- these fields are accessed using the member of operator (.) prefixed by the object name.
				- fields of an object are by default undefined, so it is important to assign them a value before they are used.
				- ```
				  int main(void){
				  	point p;
				      p.x = 1;
				      p.y = 2;
				  }
				  ```
				- similar to an array, struct objects may also be initialize when they are declared by enclosing values in curly brackets. the values are then assigned in order based on the corresponding members of the struct. this way of assigning values to a composite type is known as aggregate initialization.
					- ```
					  struct point{
					  	int x, y;
					  } r = {1, 2}; /* assigns x and y */
					  
					  int main(void) {
					  	point p;
					  }
					  ```
		- struct pointers
		  collapsed:: true
			- a struct is a value type not a reference type
				- ```
				  int main(void){
				  	point p = { 1, 2 };
				      point r = p; /* copies field values */
				  }
				  ```
			- for large structures, it is common to use pointers when passing objects to functions for performance. the pointer must be dereferenced before the member of the operator can be used  used to access the fields. shortcut infix operator (`->`).
				- ```
				  void init_struct(point* a){
				  	(*a).x = 1;
				      (*a).y = 2;
				  }
				  
				  int main(void){
				  	point p;
				      init_struct(&p);
				      point* r = &p;
				      r->x = 3;
				      printf("%d\n", p.x);
				  }
				  ```
		- bit fileds
			- within struct type memory optimised by specifying bit length of integer fields.
			- such a field is called a bit field and its length is set by placing `:` after filed name followed by the number of bits. the length must be less than or equal to the bit length of the specified type.
			- ```
			  struct my_bits{
			  	unsigned short f1 : 1,
			      unsigned short f2 : 1;
			      unsigned short id : 10;
			  } a;
			  ```
			- Bit fields are packed as compactly as possible, while keeping in mind that the size of an object needs to be a multiple of the size of the largest type it contains.
			- in the above case the needed 12 bits will require 16 bits (2 bytes) to be reserved for the object (size of unsigned short 16 bits). if bit fields not been used, 3 shorts and the struct would occupy 48 bits.
	- union
	  collapsed:: true
		- union type is identical to struct type, except that all fields share the same memory location. therefore, the size of a union is the size of the largest field it contains.
		- ```
		  union mix {
		  	char c; /* 1 byte */
		      short s; /* 2 bytes */
		      int i; /* 4 bytes */
		  }
		  ```
		- given this memory sharing, the union type only be used to store one value at a time, because changing one field will overwrite the value of the others.
		- ```
		  int main(void){
		  	union mix m;
		      m.c = 0xFF; /* set first 8 bits to 11111111 */
		      m.s = 0; /* reset first 16 bits to 0 including the bits in the previous step */
		  }
		  ```
		- ```
		  union mix2 {
		  	char c[4]; /* 4 bytes */
		      struct { short hi, lo; } s; /* 4 bytes */
		      int i; /* 4 bytes */
		  } m;
		  
		  m.i = 0xFF00F00F;	/* 11111111	00000000	11110000	00001111 */
		  m.s.lo;				/* 11111111 00000000						 */
		  m.s.hi;				/* 						11110000	00001111 */
		  m.c[3];				/* 11111111									 */
		  m.c[2];				/* 			00000000						 */
		  m.c[1];				/* 						11110000			 */
		  m.c[0];				/* 									00001111 */
		  ```
	- type casting or type conversion
	  collapsed:: true
		- converting an expression from one type to another is known as type casting or type conversion. this can be done either implicitly by the compiler or explicitly with code.
		- implicit conversions
			- an implicit conversion is performed automatically by the compiler when an expression needs to be converted into one of its compatible types.
			- implicit conversions of primitive types are 2 kinds: promotion and demotion.
				- promotion occurs when an expression gets implicitly converted into a larger type.
				- demotion occurs when converting an expression to a smaller type.
				-
	- storage classes
	- constants
	- preprocessor
	- memory management
	- input handling
	- headers
	- strings and numbers
- resources
	- books
		- modern-c-quick-syntax-reference-2nd
		- Jens Gustedt - Modern C-Manning Publications (2019)
		- Dan Gookin - Tiny C Projects-Manning (2022)
		- Yale N. Patt_ Sanjay J. Patel - Introduction to Computing Systems_ From Bits & Gates to C & Beyond-McGraw-Hill Education (2003)
		- Jens Gustedt - Modern C-Manning Publications (2019)
	- web
		- https://cs.brown.edu/courses/csci0300/2021/schedule.html
		- https://beej.us/guide/
		- http://www.cplusplus.com/reference/clibrary/
	- videos
		- youtube
			- https://www.youtube.com/@dr-Jonas-Birch
			  collapsed:: true
				- notes
					- `c` is modular language
					- `c` has only few built in functions /commands
					- `libc` library contains `stdin.h` `stdio.h`
					- `functions`
					  collapsed:: true
						- `main` function where program starts
						- `printf` function to print message to standard outuput i.e., screen
						  collapsed:: true
							- special / non-printing
							  collapsed:: true
								- `\n`: new line character
						- `scanf` function to get input from user
						  collapsed:: true
							- `%s` for string of characters
							- `%31s` for string of characters size restricted to 31
							- `%d` - integer (int)
							- `%f` - float number
						- `strncpy(birch.title, "doctor", 7)` to copy string into variable
						- custom functions
						  collapsed:: true
							- ```
							  int custom_fun(int arg1, int arg2){
							  	return arg1 + arg2;
							  }
							  ```
						- random values
						  collapsed:: true
							- pseudo random functions i.e. mathematical algorithms that is mimicing true randomness
							- rand();
							- srand();
							- srand(getpid());
						- `sleep`
						  collapsed:: true
							- sleep(2) -> freezes runtime for a brief period
						- `fork()`
						  collapsed:: true
							- creates 2 instances of the program to run the programs parallelly
							- x = fork();
						- `ncurses`
						  collapsed:: true
							- based on window -> entire screen
							- there can be number of screens can be initiated
							- `initscr()` -> initiate screen
							- each screen can have specific functions
							- `printw()`
							- `refresh()`
							- letter = getch()
							- ```
							  char letter;
							  
							  initscr(); // initiate screen
							  printw("press any key"); // print function of ncurses
							  refresh(); // to view the fresh screen
							  
							  letter = getch(); // getchar fuction of ncurses
							  clear();
							  
							  printw("you pushed: %c", letter);
							  refresh();
							  
							  getch();
							  endwin();
							  ```
							- compile with library ncurses
								- gcc ncurses.c -lncurses -o ncurses
							- getyx(stdscn, y, x);
							- move(y, x);
							- keypad(stdscr, TRUE);
							- noecho();
						- `malloc`
							- dynamic memory
							- x = malloc(32);
							- free(x) // at the end of program
						- `getchar()` -> to get character from standard input
						- `memset(x, 0, sizeof(int));`
						- `strcmp(searchstr, str)`
						- `select()`
					- variables
					  collapsed:: true
						- char name[32]
						- datatype variable_name size_of_variable
					- data-types
					  collapsed:: true
						- `char` - characters, letters
						- `int` - number without decimal
						- `float` - number with decimal
					- debugging
					  collapsed:: true
						- errors: it won't compile
						- warning: it will be compiled but expected behaviour is unsure.
						- sudo apt install ltrace strace
						- `ltrace` for library calls
							- ltrace -f books1.c
						- `strace` for sys calls
					- while loops
					  collapsed:: true
						- ```
						  while (condition check){
						  	//body
						  }
						  ```
						- ```
						  int x = 0;
						  while (x == 0){
						  	printf("do you want to quit? press 1\n");
						      scanf("%d", &x)
						  }
						  ```
					- if statements
					  collapsed:: true
						- ```
						  if(condition check){
						  	// body
						  }
						  ```
						- ```
						  if(speed > 100){
						  	printf("you are driving too fast\n");
						  }else if(speed > 80){
						  	printf("you are driving perfectly fine\n");
						  }else{
						  	print("OK\n");
						  }
						  ```
						- `>`, `<`, `>=`, `<=`, `==`, `!=`
						- first one should start with `if` statement, as many as `else if` statements optional, only one `else`.
						- `else` statement is optional with only one `if` statement.
						- `else` is must if at least one `else if` statement used.
						- after `if`, `elseif`, `else` follows block of code in `{}`. if only one statement to execute `{}` can be omitted.
					- `break;` statement exits the loop
					- `continue;` breaks the statements below it, but continue the loop.
					- short syntax
					  collapsed:: true
						- number = number - 1;
						- number -= 1;
						- number--;
						- number = number + 1;
						- number += 1;
						- number++;
					- structures - struct
					  collapsed:: true
						- composite variable
						- struct variable is created outside of `main()` and will be used in `main()`
						- `struct` ends with `;`
						- ```
						  struct person {
						  	char title[8];
						      char lastname[32];
						  	int age;
						  };
						  ```
						- struct elements can be referenced with `dot(.)` operator like `person.title`
						- if it is struct pointer `*person` `person -> title`
					- switch
					  collapsed:: true
						- switch followed by case.
						- every case statement has break
						- end will have default statement
						- ```
						  switch input is char, int
						  switch(x){
						  	case 1:
						      	printf("apples\n");
						          break;
						      case 2:
						      	printf("pears\n");
						          break;
						      case 3:
						      	printf("bananas\n");
						          break;
						      default:
						      	printf("something else\n");
						  }
						  ```
					- pointers
					  collapsed:: true
						- is a variable stores address of the another variable
						- ```
						  int x = 10;
						  char y = 'a';
						  int *p = &x;
						  char *c = &y;
						  ```
						- dereferencing a pointer is to refer to the data
						- ```
						  printf("%d\n", *p);
						  ```
						- `&` pass by reference
						- `function pointers`
							- ```
							  void multiplication(int *target, int x, int y){
							  	*target = x * y;
							  }
							  
							  int main(){
							  	void (*fp)(*int, int, int);
							  	fp = multiplication;
							      (fp)(&result, a, b)
							  }
							  ```
					- for loops
					  collapsed:: true
						- ```
						  for(initiation; condition; increment){
						  	// body of the loop 
						  }
						  ```
					- assert(condition) if assert condition is true the rest of the program executes otherwise it will exits the program
					- `#define` we can also define our own shortcuts alias or macro at the top of the program
					  collapsed:: true
						- ```
						  #define F fflush(stdout)
						  ```
					- FILE *fd
					  collapsed:: true
						- File descriptor
						- fopen("test.text", "a");
						- fprint(fd, "%d\", x);
						- fclose(fd);
					- typefef struct s_book Book;
					  collapsed:: true
						- shortens the typing now `Book` can be used in place of `struct s_book`
					-
		- tutorials
			- [[pluralsight - getting started in C language]]