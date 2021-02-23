# CCDC

### Services

### Zesus web server
- Zesus is also https://en.wikipedia.org/wiki/Zeus_Web_Server
- Default port: 9090
-  Has a bunch of vulnerablities ( to list a few as of 2/20/2021 ): 
    - CVE-2010-0359
    - CVE-2010-0362
    - CVE-2010-0363
- https://www.cvedetails.com/vulnerability-list/vendor_id-10515/product_id-18788/Zeus-Zeus-Web-Server.html
- https://www.exploit-db.com/exploits/22692



### Red Team Activity
- Red team used ICMP reverse shell to access our boxes. We could of detected the shells by using tcpdump. 
- TCPDUMP manpage
    - https://www.tcpdump.org/manpages/tcpdump.1.html
### This command could be used to capture all ICMP traffic
```
sudo tcpdump -n icmp
```
The following command will show ICMP Packets that are not ECHO/REPLY

```
sudo tcpdump 'icmp[icmptype] != icmp-echo and icmp[icmptype] != icmp-echoreply'
```



### NMAP


Host discovery is used to find other devices in a network. This will give you a better idea what is 
on the network. 
```
nmap -sL 192.168.0.1
```
The -O command can be used to get information about the operating system. 
```
nmap -O 192.168.0.1
```

NMAP also has an agurment that allows the user to get information about the services versions. 
This could be useful if that service has a public vulnerability. 
```
nmap -sV 192.168.0.1
```

```
nmap 192.168.0.*
```
The command above will make NMAP scan all through the following IP range, 192.168.0.0-192.168.0.255. 
The "*" acts as a wild card. 

Another example of usage is:
```
nmap 192.168.*.*
```


# Work cited
- https://hackertarget.com/tcpdump-examples
- https://nmap.org/book/man-version-detection.html
