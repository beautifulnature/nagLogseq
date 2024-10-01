- proxy settings
	- inetcpl.cpl
		- `http://intgw-hyd.bhel.in:8080` `10.*;*.bhel.in`
- static ip: ncpl.cpl
	- 10.9.205.8 | 196
	  255.255.255.0
	  10.9.205.1
	  DNS
	  10.23.1.58
	  10.23.1.26
	  10.9.1.2
	  10.9.1.3
- dot files
	- follow https://github.com/nickjj/dotfiles.git
- mail settings
	- Nagaraju Gumpini
	  nagaraju@bhel.in
	  IMAP
	  mail.bhel.in
	  993
	  SSL
	  smtp.bhel.in
	  587
	  STARTLS
- ```.curlrc
  proxy="http://intgw-hyd.bhel.in:8080"
  ```
- ```.gitconfig
  [credential]
  	helper = manager
  [credential "helperselector"]
  	selected = manager
  [user]
  	name = nagaraju
  	email = heimarunag@gmail.com
  [http]
  	proxy = http://intgw-hyd.bhel.in:8080
  [https]
  	proxy = http://intgw-hyd.bhel.in:8080
  ```
- user settings:
	- ```~\.m2\settings.xml
	  <localRepository>E:\tools\maven-repo</localRepository>
	  <proxy>
	  	<id>bhel</id>
	      <active>true</active>
	      <protocol>http</protocol>
	      <host>http://intgw-hyd.bhel.in</host>
	      <port>8080</port>
	  	<username>6014755</username>
	      <password>Bhel@202512</password>
	      <nonProxyHosts>*.bhel.in|10.*.*.*</nonProxyHosts>
	  </proxy>
	  ```