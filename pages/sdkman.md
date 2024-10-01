- installation on windows
	- step-1: install git-bash
		- install git bash
		- download zip package from [https://gnuwin32.sourceforge.net/packages/zip.htm](https://gnuwin32.sourceforge.net/packages/zip.htm)
		- copy `zip.exe` and `zip32z64.dll` to `C:\Users\6014755\AppData\Local\Programs\Git\mingw64\bin`
		- check for `which unzip` and `which zip` at git-bash
	- step-2 install sdkman
		- ```
		  $ curl -s "https://get.sdkman.io" | bash
		  ```
		- add to `.bashrc`
		  ```
		  export SDKMAN_DIR="/e/tools/sdkman/"
		  [[ -s "/e/tools/sdkman//bin/sdkman-init.sh" ]] && source "/e/tools/sdkman//bin/sdkman-init.sh"
		  ```
	- verify sdk version
- usage
	- sdk list java
	- sdk offline enable
	- sdk offline disable
	- sdk install java 17.0.7.fx-zulu
	- sdk uninstall java 17.0.7.fx-zulu
	- sdk use java 17.0.7.fx-zulu (for current terminal session)
	- sdk default java 17.0.7.fx-zulu (for changing permanently)