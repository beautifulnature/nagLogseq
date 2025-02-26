- tutorials
	- [[pluralsight - getting started in C language]]
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
- resources
	- https://cs.brown.edu/courses/csci0300/2021/schedule.html
	- https://beej.us/guide/
	- http://www.cplusplus.com/reference/clibrary/
- tools
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
	- Strings
		- Strings under the hood are array of characters. delimited by "".
			- char myString[] = "Hi";
		- Strings are NULL terminated, `\0`, null character, which is used to know where the string ends.
		- null character added automatically by the compiler
			- char myString[3] = { 'H', 'i', '\0' };
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
	- Operators
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
	- format strings
	- Comments
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
	- Whitespace
	  collapsed:: true
		- white space characters like comments, spaces, and tabs are generally ignored by the compiler.
- Yale N. Patt_ Sanjay J. Patel - Introduction to Computing Systems_ From Bits & Gates to C & Beyond-McGraw-Hill Education (2003)
- Jens Gustedt - Modern C-Manning Publications (2019)