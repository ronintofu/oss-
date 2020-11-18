# ARP, DHCP, IP Addressing

**ARP, Gratuitous ARP, and RARP**

* ARP - Address Resolution Protocol
  * RFC 826 [https://tools.ietf.org/htmk/rfc826](https://tools.ietf.org/htmk/rfc826)
* Used to resolve IP addresses into MAC addresses.
* For network communication to happen, computers need to know both the IP address and the MAC address of the destination.
* ARP is used to find out a MAC address when the IP address of the destination in known.

![](https://www.evernote.com/shard/s342/res/5b85b4c2-4f23-e834-c3c8-39bf1b2ba59f)Similar to an NMAP \(not TCP/UDP\) scan. This isn't a connection, it's more a discovery/scan/echo.**ARP Cache**

* A table of all known IP address to MAC address mappings:
  * WIN/MAC/Linux Command: "arp -a"
  * Cisco IOS \(router or switch\): "show arp"
* The ARP cache includes static and dynamically learned entries.
* Before sending network communication computers reference the ARP cache.
* If no MAC address is present then an ARP Request is sent to determine the MAC address.
* After the ARP is completed the ARP cache is updated.

**Gratuitous ARP**

* An ARP announcement to update other hosts ARP tables without the need for an ARP Request.
* Sometimes performed during the computer operating system startup process.
* Helps to update the network faster when there was a recent change to a hosts IP address.

  
**RARP**

* Reverse Address Resolution Protocol
  * RFC 903 [https://tools.ietf.org/html/rfc903](https://tools.ietf.org/html/rfc903)
* Was used to resolve MAC addresses into IP addresses and required servers on every network.
* RARP has been deprecated and its processes have been replaced by BOOTP and Dynamic Host Configuration Protocol \(DHCP\) which provide better and more services than RARP.
* DHCP is used primarily to automatically assign IP addresses to hosts on a network.

  
![](https://www.evernote.com/shard/s342/res/4b763007-d697-654d-875a-e4eda38448ff)![](https://www.evernote.com/shard/s342/res/c9f512f1-9a33-4a1d-c3b0-d72b03e8dc6c)

Total of 4 packets being sent out/thrown out at 10.10.10.200 since it's not 10.10.10.55  
**IP Address Assignment**

\*\*\*\*![](https://www.evernote.com/shard/s342/res/3323a4f3-7eee-cf6d-6a3b-b7e993524b25)

DNS - Domain Name Services  
**How Are IP Addresses Assigned?**  


* Values:
  * IP address
  * Subnet Mask
  * Default Gateway
  * DNS Server
* Static:
  * Manually touch each computer.
  * Manually document each assigned IP
  * Difficult to manage and maintain
  * More secure in comparison with DHCP
  * Used mostly on servers, routers, and switches where the IP address should never change.
* Dynamic:
  * IP address assignment is auto.
  * IP addresses are assigned quickly.
  * DHCP server keeps records of all assigned IPs,
  * Best for hosts, phones, and other network nodes that don't need a dedicated IP address
  * Can assign additional options such as TFTP server used with VoIP \(option 150\)
  * IP address will expire.

![](https://www.evernote.com/shard/s342/res/97da89fd-4983-5b86-5b69-17eedb296bbb)  
  
**DHCP**Dynamic Host Configuration Protocol

* Predecessor was called BOOTP
  * DHCP still uses BOOTP, but does much more.
* DHCP can run on servers, routers, and even switches.
* Home routers have DHCP built in.
* There should be only 1 DHCP server in a broadcast domain.
* With DHCP relay the DHCP server can be in a different broadcast domain.
* A rogue DHCP server can cause network access problems for any hosts using DHCP

![](https://www.evernote.com/shard/s342/res/52ce43d4-c6cb-da53-8d26-c7bcce123630)  
  
**APIPA**Automatic Private IP Addressing

* Self-assigns an automatic IP address from a specific network ID: 169.254.0.0/16
* Used when a device does not have a static IP address assigned and also has no DHCP server available.
* Is not routable outside the local broadcast domain.
* Also called link-local address autoconfiguration.

![](https://www.evernote.com/shard/s342/res/ea902f7b-e472-8566-f95a-320433c0a6b1)![](https://www.evernote.com/shard/s342/res/8467fe29-adcf-c98f-eac3-8cdaca67f6b1)  
**DHCP Relay**

* Router is configured with helper address to relay DHCP client requests and forward them to the DHCP server.

![](https://www.evernote.com/shard/s342/res/7a70cc66-f645-adc6-6f75-d1f7d06c4d26)  
**DHCP Config:**

1. Router\(config\)\#ip dhcp excluded-address 10.10.10.10 10.10.10.50
2. Router\(config\)\#ip dhcp pool NexGenT
3. Router\(dhcp-config\)\#network 10.10.10.0 255.255.255.0
4. Router\(dhcp-config\)\#default-router 10.10.10.1
5. Router\(dhcp-config\)\#dns-server 10.10.10.1
6. Identifying the IP pool.
7. Naming the IP pool.
8. setting the network
9. setting the default route
10. setting the dns server

**DHCP Verification**

* show ip dhcp binding
* show ip dhcp conflict
* show ip dhcp pool
* clear ip dhcp binding \*
* Windows Command Prompt:
  * ipconfig /all
  * ipconfig /release
  * ipconfig /renew

  
**RECAP**  


* IP addresses can be assigned statically or dynamically.
* AT a minimum we use the following IP settings:
  * IP address
  * Subnet mask
  * Default gateway
  * DNS
* DHCP is for dynamically assigned IP addresses.
* A DHCP server is needed for DHCP to function
* APIPA network: 129.254.0.0/16

