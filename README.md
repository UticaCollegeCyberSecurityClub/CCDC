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





# Work cited
- https://hackertarget.com/tcpdump-examples/
