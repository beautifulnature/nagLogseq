- proxy
	- cntlm
	  collapsed:: true
		- sudo apt install cntlm
		- generate password hashes
			- sudo cntlm -H -u 6014755 -d BHEL
		- sudo nano /etc/cntlm.conf
			- ```
			  # Your proxy server address
			  Proxy intgw-hyd.bhel.in:8080
			  
			  # Your NTLM credentials
			  Username 6014755
			  Domain BHEL  # Replace with your actual domain name
			  
			  # Passwords should be hashed for security
			  # You can generate these hashes using the command: cntlm -H
			  # Then copy the relevant hashes into this configuration
			  PassLM          F88627137AF9F7BA05EDCA1ABFF86472
			  PassNT          BC10EDA78B60D964F31D7C60266BA277
			  PassNTLMv2      B828BB12D24FC1E9AED4EA914E16D023    # Only for user '6014755', domain 'BHEL'
			  
			  # Listen on this port for local applications
			  Listen 3128
			  
			  # Optional: NoProxy settings for local addresses
			  NoProxy localhost, 127.0.0.1
			  ```
		- sudo service cntlm restart
		- sudo service cntlm status
	- proxy settings
	  collapsed:: true
		- new way
		  collapsed:: true
			- make entry `proxyon()` `proxyoff()` in `~\.bashrc`
			  collapsed:: true
				- ```~/.bashrc
				  # Function to enable proxy
				  function proxyon() {
				      export http_proxy='http://localhost:3128'
				      export https_proxy='http://localhost:3128'
				      export no_proxy='localhost,127.0.0.1,::1'
				      echo 'Acquire::http::Proxy "http://localhost:3128";' | sudo tee /etc/apt/apt.conf.d/proxy
				      echo "Proxy enabled."
				  }
				  
				  # Function to disable proxy
				  function proxyoff() {
				      unset http_proxy
				      unset https_proxy
				      unset no_proxy
				      sudo rm -f /etc/apt/apt.conf.d/proxy
				      echo "Proxy disabled."
				  }
				  ```
			- source ~/.bashrc
			- proxyon at cli
			- proxyoff at cli
		- without cntlm
		  collapsed:: true
			- ```~/.bashrc
			  # Set HTTP proxy
			  export http_proxy="http::Proxy "http://6014755:Bhel%24202512@intgw-hyd.bhel.in:8080"
			  export HTTP_PROXY="http::Proxy "http://6014755:Bhel%24202512@intgw-hyd.bhel.in:8080"
			  
			  # Set HTTPS proxy
			  export https_proxy="http::Proxy "http://6014755:Bhel%24202512@intgw-hyd.bhel.in:8080"
			  export HTTPS_PROXY="http::Proxy "http://6014755:Bhel%24202512@intgw-hyd.bhel.in:8080"
			  
			  # Exclude localhost and internal IP addresses from proxy
			  export no_proxy="localhost,127.0.0.1,192.168.0.0/16,10.*,*.bhel.in"
			  export NO_PROXY="localhost,127.0.0.1,192.168.0.0/16,10.*,*.bhel.in"
			  ```
		- with cntlm
		  collapsed:: true
			- ```
			  export http_proxy="http://localhost:3128"
			  export https_proxy="http://localhost:3128"
			  ```
	- apt proxy settings
	  collapsed:: true
		- without cntlm
		  collapsed:: true
			- ```/etc/apt/apt.conf.d/proxy.conf
			  echo 'Acquire::http::Proxy "http://6014755:Bhel%24202512@intgw-hyd.bhel.in:8080";' | sudo tee /etc/apt/apt.conf.d/proxy
			  echo 'Acquire::https::Proxy "http://6014755:Bhel%24202512@intgw-hyd.bhel.in:8080";' | sudo tee -a /etc/apt/apt.conf.d/proxy
			  ```
		- with cntlm
		  collapsed:: true
			- ```
			  Acquire::http::Proxy "http://localhost:3128/";
			  Acquire::https::Proxy "http://localhost:3128/";
			  ```
- node
  collapsed:: true
	- sudo apt install nodejs
	- sudo apt install npm
- man 5 rand
  collapsed:: true
	- man for manual
	- 1 for build-in commands for linux shell
	- 2 for system calls - core kernel functions
	- 3 for library function
	- 5 for configuration files
- unix
  collapsed:: true
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
- [[bash]]
- resources
	- video
		- Udemy_Learn_Linux_in_6_Days_and_Level_Up_Your_Career_2024_5