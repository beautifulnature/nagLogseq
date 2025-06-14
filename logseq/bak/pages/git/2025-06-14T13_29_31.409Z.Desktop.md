- git config
	- git config --global core.autocrlf true -> to handle line endings LF to CRLF when check out and CRLF to LF when commiting
	- git proxy settings
		- ```proxy
		  git config --global http.proxy http://6014755:Bhel%40202512@intgw-hyd.bhel.in:8080
		  git config --global https.proxy https://6014755:Bhel%40202512@intgw-hyd.bhel.in:8080
		  ```
- git init . -> creates an empty git repository
- git add * -> add all the files to git staging
- git commit -m "create website skeleton" -> checks in the files to version control with a commit message
- git status -> to check the git status
- git branch
	- git branch -> to list branches in local
	- git branch -r -> to list branches at remote
	- git branch -a -> to list branches in local & remote
	- git branch -v -> current branch with commit message
	- git checkout -b new-branch -> git checkout of present branch to new-branch if available otherwise creates new-branch
	- git switch -c new-branch -> similar to above
	- git branch new-branch -> creates new-branch but not switch
	- git checkout new-branch -> git checksout to new-branch