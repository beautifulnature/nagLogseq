- proxy settings
	- ```~/.bashrc
	  # Set HTTP proxy
	  export http_proxy="http://intgw-hyd.bhel.in:8080"
	  export HTTP_PROXY="http://intgw-hyd.bhel.in:8080"
	  
	  # Set HTTPS proxy
	  export https_proxy="http://intgw-hyd.bhel.in:8080"
	  export HTTPS_PROXY="http://intgw-hyd.bhel.in:8080"
	  
	  # Exclude localhost and internal IP addresses from proxy
	  export no_proxy="localhost,127.0.0.1,192.168.0.0/16,10.*,*.bhel.in"
	  export NO_PROXY="localhost,127.0.0.1,192.168.0.0/16,10.*,*.bhel.in"
	  ```
- apt proxy settings
	- ```/etc/apt/apt.conf.d/proxy
	  echo 'Acquire::http::Proxy "http://6014755:Bhel%40202512@intgw-hyd.bhel.in:8080";' | sudo tee /etc/apt/apt.conf.d/proxy
	  echo 'Acquire::https::Proxy "http://6014755:Bhel%40202512@intgw-hyd.bhel.in:8080";' | sudo tee -a /etc/apt/apt.conf.d/proxy
	  ```
- snap proxy settings
	- ```proxy
	  sudo snap set system proxy.http="http://6014755:Bhel%40202512@intgw-hyd.bhel.in:8080"
	  sudo snap set system proxy.https="http://6014755:Bhel%40202512@intgw-hyd.bhel.in:8080"
	  ```
	- ```unset-proxy
	  sudo snap set system proxy.http=""
	  sudo snap set system proxy.https=""
	  ```
	- ```/var/lib/snapd/config/proxy.conf
	  <defaultProxy useDefaultCredentials="true">
	  	<proxy autoDetect="false" proxyaddress="http://6014755:Bhel%40202512@intgw-hyd.bhel.in:8080" bypassonlocal="false" usesystemdefault="false" />
	  </defaultProxy> 
	  ```
- node
	- sudo apt install nodejs
	- sudo apt install npm