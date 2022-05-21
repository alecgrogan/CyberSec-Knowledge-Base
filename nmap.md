# NMAP



## Port Scanning

> nmap sS TCP SYN scan TARGET-IP
The most basic of these scans is the sS TCP SYN scan, and this gives most users all the information they need. It scans thousands of ports per second, and because it doesn’t complete a TCP connection it does not arouse suspicion.

> nmap sT TCP connect scan TARGET-IP
The main alternative to this type of scan is the TCP Connect scan, which actively queries each host, and requests a response. This type of scan takes longer than a SYN scan, but can return more reliable information.

> nmap sU UDP scans TARGET-IP
The UDP scan works in a similar way to the TCP connect scan but uses UDP packets to scan DNS, SNMP, and DHCP ports. These are the ports most frequently targeted by hackers, and so this type of scan is a useful tool for checking for vulnerabilities.

> nmap sY SCTP INIT scan TARGET-IP
The SCTP INIT scan covers a different set of services: SS7 and SIGTRAN. This type of scan can also be used to avoid suspicion when scanning an external network because it doesn’t complete the full SCTP process.

> nmap sN TCP NULL TARGET-IP
The TOP NULL scan is also a very crafty scanning technique. It uses a loophole in the TCP system that can reveal the status of ports without directly querying them, which means that you can see their status even where they are protected by a firewall.

### Sources
https://www.varonis.com/blog/nmap-commands
