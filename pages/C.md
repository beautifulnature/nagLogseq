- tutorials
	- [[pluralsight - getting started in C language]]
- youtube
	- https://www.youtube.com/@dr-Jonas-Birch
		- notes
			- `c` is modular language
			- `c` has only few built in functions /commands
			- `libc` library contains `stdin.h` `stdio.h`
			- `functions`
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
				- custom functions
					- ```
					  int custom_fun(int arg1, int arg2){
					  	return arg1 + arg2;
					  }
					  ```
				- random values
					- pseudo random functions i.e. mathematical algorithms that is mimicing true randomness
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
			-