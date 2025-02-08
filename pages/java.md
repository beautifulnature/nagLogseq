- jdk installation
	- sdk install java 17.0.7.fx-zulu
	- sdk default java 17.0.7.fx-zulu
	- set environment variable for your account
		- variable: `JAVA_HOME` value: `E:\tools\sdkman\candidates\java\current`
		- add `%JAVA_HOME%\bin` to `PATH`
- [[maven]]
	- installation
		- sdk install maven 3.9.8
	- set environment variable for your account
		- variable: `MVN_HOME` value: `E:\tools\sdkman\candidates\maven\current`
		- add `%MVN_HOME%\bin` to `PATH`
- core java
	- language improvements
		- java 11 to 17
		- java 11
			- var
			- modules
		- java 17
			- jep java enhancement proposals
			- jep 358: helpful NullPointerExceptions
				- NullPointerException extremely common
				- No message, no indication what was null and why
				- After a lot of exceptions, gets optimised to simply `java.lang.NullPointerException`
					- Fast, but not useful
					- Turn off with -XX:-OmitStackTraceInFastThrow
				- java 17 shows more data about null
					- in our code, s is null
					- ```
					  String s = null'
					  System.out.println(s.length());
					  ```
						- java.lang.NullPointerException: cannot invoke "String.length()" because "s" is null at masteringjava17research/jep358_helpfule_npe.NullPointerDemo.main(NullPointerDemo.java:9)
					- we need to compile our classes with -g or -g:vars, otherwise
						- java.lang.NullPointerException: cannot invoke "String.length()" because "<local1>" is null at masteringjava17research/jep358_helpfule_npe.NullPointerDemo.main(NullPointerDemo.java:9)
					- compiling with -g or -g:vars increases class size by = 15%
					- shows even with chained elements
						- tells us exactly which local variable or field was null a.b.c.d.toString()
					- similarly with method calls
						- gives excellent information why we got a NPE
						- ```
						  Deque<String> deque = new ArrayDeque<>();
						  deque.poll().toUpperCase();
						  ```
						- cannot invoke "String.toUpperCase()" because the return value of "java.util.Deque.poll()" is null
			- jep 361: switch expressions
			- jep 378: text blocks
			- jep 394: pattern matching for instanceof
			- jep 395: records
			- jep 409: sealed classes