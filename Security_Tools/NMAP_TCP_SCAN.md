# $\color{#FF69B4}{\text{NMAP TCP SCAN TEST}}$

Hello! This is my first official documentation of one of the Mosse Cybersecurity Institute's activities. Although it is not my first time completing these assignments, I've made a Github dedicated to these projects to prove my participation. 

Today, we are doing the Perform a TCP port scan using Nmap activity. 

The requirements are as follows:  Important
Research what flags do before using them
Nmap will return "open|filtered" when it is unable to determine whether a port is open or filtered. This exercise requires you to identify "open" ports!
2. Prepare the target machine
Start a Linux virtual machine that will serve as the target for the TCP port scan
Start the "apache2" service and the "ssh" service on the target virtual machine
2.1. Validation
Verify that the services are running on the default ports (22 and 80)
Validate that you can detect the "open" port(s) using Nmap and the loopback address (127.0.0.1)
3. Perform TCP Scans
Start another Linux virtual machine with Nmap installed, which will act as the attacker machine
Use Nmap's TCP Connect Scan ("-sT") against the target machine to identify open ports
Use Nmap's TCP SYN Scan ("-sS") against the target machine to identify open ports using SYN packets
Use Nmap's Service Detection ("-sV") against the target machine to identify the services running on open ports
Use Nmap's OS Detection ("-A") against the target machine to identify the operating system running on the target system
Use Nmap's scan option to scan all TCP ports ("-p-") against the target machine to identify all open ports
3.1. Validation
For each of the scans performed using the attacker machine, ensure that Nmap successfully discovers port 22 (SSH) and port 80 (HTTP) as "open" on the target machine


# $\color{#FF69B4}{\text{HERE IS MY WORK AND THOUGHT PROCESS}}$

Determine this:
What ports are open? 
What services are running? 
What OS is this system using? 
How different scanning techniques discover info.

How I will create this lab: 

Two Linux virtual machines, one representing the attacker, one representing the target/victim. 

Attacker VM will use NMAP
TARGET VM (REMEMBER THIS) We will use Port 22 and 80 | SSH, 
# $\color{#FF69B4}{\text{...AND APACHE}}$
Remember, Port 80 is HTTP
Port 22 is SSH

NMAP IS THE SECURITY TOOL USED TO SCAN THE TARGET 

apache2	The Apache HTTP web server.
openssh-server	The server software that accepts SSH connections
nmap	The network scanning tool.
systemctl — A Linux command used to manage system services.
ss - socket stats
Flag	Meaning
ss	Socket Statistics
-t	Display TCP sockets.
-u	Display UDP sockets.
-l	Display listening sockets.
-n	Display numerical IP addresses and port numbers.
-p	Display the processes associated with sockets.

I typed sudo ss -tulnp, thats very interesting!

Adapter 1 — NAT	Allows the VM to access the internet to download software.
Adapter 2 — Host-only	Allows communication between your lab machines and physical host.


-br	Displays information in a brief format


### $\color Interface	Purpose{#FF69B4}{\text{Target machine prep done}}$

lo	Loopback interface.
enp0s3	Often the first virtual Ethernet adapter (NAT).
enp0s8	Often the second virtual Ethernet adapter (host-only).
/24	The first 24 bits identify the network; equivalent to subnet mask 255.255.255.0.
UP	The network interface is enabled.



