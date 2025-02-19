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
- tools
	- sudo apt update
	- sudo apt install gcc build-essential
	- sublime-text editor
		- https://www.sublimetext.com/docs/linux_repositories.html#apt
	- $ subl
- c-language
	- ISO 9899
	- programming langauge
		- compiled / interpreted
		- garbage collector
		- strongly typed or not
		- memory safe?
	- variables
		- variable declaration
			- type name = initial_value;
			- name should be descriptive for readability
		- int
		- float
		- char
	- variable scope
		- local scope
			- only available to the function locally
		- global scope
			- declared outside of the function and available to all functions
	- pre-processor
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
		- preprocessor
		- compilation
		- assembling
		- linking
	- arrays
		- syntax
			- int ids[] = {1, 2, 3};
			- int ids[32] = {1, 2, 3};
		- arrays are zero index
		- accessing elements
			- ids[0];
	- Strings
		- Strings under the hood are array of characters
		- Strings are NULL terminated
		- strcopy(dest, src);
		- strncopy(dest, src, n); // n bytes
		- strcmp(str, otherstr)
	- functions
	- format strings