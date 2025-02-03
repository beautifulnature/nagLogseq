- man 3 rand
	- man for manual
	- 1 for build-in commands for linux shell
	- 2 for system calls - core kernel functions
	- 3 for library function
	- 5 for configuration files
- unix
	- unix was an os developed at AT&T Bell Labs in the 1960s through 1980s.
	- https://www.youtube.com/watch?v=tc4ROCJYbm0
	- GNU/Linux, MacOSX and Android are all based on ideas and specifications created by UNIX
	- https://en.wikipedia.org/wiki/File:Unix_history-simple.svg
	- time-sharing
	  collapsed:: true
		- UNIX was originally built for large mainframe computers that many people would use at the same time.
	- terminals and teleprinters
	  collapsed:: true
		- teleprinters printed program output on paper
		- terminals displayed output on a CRT monitor
		- neither device had processing power of their own
		- connected to the mainframe over cables or by telephone
		- teletype legacy: standard input and output
		  collapsed:: true
			- every program on a unix system can read input from the standard input device (stdin) and write to standard output (stdout)
			- by default, stdin comes from the keyboard and stdout gets printed to the graphical display
		- organisation
			- unix os is a collection of programs, each with a special role:
			  collapsed:: true
				- kernel
				  collapsed:: true
					- mediate access between user programs and system resources
						- CPU scheduling
						- I/O to computer hardware
						- memory
					- programs request resources by making a syscall
				- shell
				  collapsed:: true
					- a shell is a computer program that can execute other programs from text-based interface
					- In a text-based interface, you interact with a program completely from a command-line with text commands and text output
					- most modern shells are strongly influenced by the first unix shells
					- bourne again shell (bash) - brain fox 1987
				- utilities
				  collapsed:: true
					- any distribution of unix will come with dozens of other programs that perform narrow single-purpose tasks
					- the available utilities on a given system vary widely but some utilities are very common.
			- why unix still matters
			  collapsed:: true
				- portable to many kinds of hardware
				- consistent conventions
				- vast software ecosystem
				- text!
			- text interface
			  collapsed:: true
				- to remotely access a unix system, you can use the same command-line tools and interface that you use locally.
				- you can remotely access devices without a display
	- unix philosophy
		- the unix philosophy is a set of design principles for how programs relate to each other
			- each program should do one thing well
			- the output of a program can become the input of another
		- unix programming environment 1984 Brain kernighan and Rob Pike
	- commands
		- echo $SHELL
		- cat /proc/cpuinfo
		- android phone
		  collapsed:: true
			- 7 times put it in developer mode
			- adb shell
			- cd vendor
			- ls
			- cd /sdcard/
			- ls
		- list files
			- ls
			- pwd - present working directory
			- cd - change directory
				- cd .. - change to parent directory
				- cd - change directory to home directory
			- clean
			- alias
				- alias # displays all aliases
				- alias ls='ls -l' # to setup a alias
				- it will setup in the current shell only
				- you can permanently setup in ~/.bashrc
			- special directories
				- there are some special directories
				- `..` means parent directory
				- `.` means the current directory
				- `~` means home directory
			- head
				- to display file top lines