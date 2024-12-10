- proxy
	- cntlm
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
	- apt proxy settings - like this can be configured
		- ```/etc/apt/apt.conf.d/proxy.conf
		  echo 'Acquire::http::Proxy "http://6014755:Bhel%24202512@intgw-hyd.bhel.in:8080";' | sudo tee /etc/apt/apt.conf.d/proxy
		  echo 'Acquire::https::Proxy "http://6014755:Bhel%24202512@intgw-hyd.bhel.in:8080";' | sudo tee -a /etc/apt/apt.conf.d/proxy
		  ```
	- proxy settings - like this can be configured
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
	- snap proxy settings - like this can be configured
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