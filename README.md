# 3proxy
3proxy install script for Debian / Ubuntu VPS
======================================================
Download, make executable and run with these lines :
    
    wget --no-check-certificate https://raw.github.com/lionelmedal/3proxy/master/3proxyinstaller.sh #Download Files
    chmod +x 3proxyinstaller.sh #Grant Access
    ./3proxyinstaller.sh #Run script once on folder

After install : CHANGE USERNAME:PASSWORD
    
    nano /etc/3proxy/.proxyauth #Text edit file

Example change line inside .proxyauth
    
    johndoe:CL:johndoepassword123

You can also change the port, default is 3128

    nano /etc/3proxy/3proxy.cfg #Text edit file
    
Once you've change the username / password you can start the proxy 
(or reboot the VPS as 3proxy has been added to the init scripts and will autostart)

    /etc/init.d/3proxyinit start
    
For Uninstall Download, make executable and run with these lines :

	wget --no-check-certificate https://raw.github.com/lionelmedal/3proxy/master/3proxyuninst.sh
	chmod +x 3proxyuninst.sh
	./3proxyuninst.sh
	
Reset Squid
	
	service squid3 restart
  
**Script will run on :**
- Debian 6 32bits
- Debian 7 32bits
- Ubuntu 12.10 32bits
- Ubuntu 12.04 32bits
- Ubuntu 14.04 32bits and 64bits
