- tutorials
	- [[pluralsight - getting started in C language]]
- youtube
	- https://www.youtube.com/@dr-Jonas-Birch
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
					- sleep(2) -> freezes runtime for a brief period
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
- resources
	- https://cs.brown.edu/courses/csci0300/2021/schedule.html
	- https://beej.us/guide/