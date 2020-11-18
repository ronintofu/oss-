# Intro to IP Routing

  
**Internet Protocol \(IP\)**

* IPv4, part of the TCP/IP Protocol Stack
  * Transmission Control Protocol \(TCP\) / Internet Protocol \(IP\)
* Provides a logical addressing schema for networks.
* Labels datagrams with IP source and IP destination.
* Relays \(or routes\) traffic across network boundaries.
* Connection-less, best effort

![](https://www.evernote.com/shard/s342/res/53291b93-7e7b-735f-9bed-d7714c801ffd)

* Each network here can have 1 IP address being broadcast across the entire topology.

![](https://www.evernote.com/shard/s342/res/9ca36f3d-777a-dfa8-92a1-b685f1f8114e)  
**A Brief History of IP**

* Vint Cerf and Bob Kahn
  * "A protocol for Packet Network Intercommunication"
  * Creators of TCP/IP protocol suite.
  * 1974 - Introduced by DARPA
  * 81 - IPv4 became official through IETF \(Internet Engineering Task Force\)
    * as described in RFC791: [https://tools.ietf.org/html/rfc791](https://tools.ietf.org/html/rfc791)
  * 82 - TCP/IP Becomes the standard for military networks.
  * Early to late 80s - TCP/IP written for most systems
  * 95 - TCP/IP included natively in Windows 95.

  
![](https://www.evernote.com/shard/s342/res/8ec46110-e89c-16ba-f7d0-c5db35613636)![](https://www.evernote.com/shard/s342/res/5ac0735d-e893-b627-3a7c-ed41baefc18c)  
  
**The IP Address**

* IPv4: 32 bits in length, represented in decimal format.
  * Example: 192.168.100.1
  * 4 binary Octets: 11000000.10101000.01100100.00000001
* Assigned to each endpoint on a network.
* Identifies that a device is part of particular broadcast domain \(or network\). This is called a Network ID or Subnet ID.

![](https://www.evernote.com/shard/s342/res/fa75cb58-4b0b-aa3e-bcc7-2170578b8856)  
**Private vs Public**

* RFC 1918, IPv4 Ranges for use in private networks.
  * [https://tools.ietf.org/html/rfc1918](https://tools.ietf.org/html/rfc1918)
  * Class A - \(Last three octets can change\) 10.0.0.0/8
  * Class B - \(Last two octets can change\) 172.16.0.0/12
  * Class C - \(Last octet can change\) 192.168.0.0/16
* Public addresses are used on the internet.

![](https://www.evernote.com/shard/s342/res/20a09dbe-2d85-b019-8046-23ebeadd9e38)  
**NAT** - Network Address Translation

* Transfers whomever is trying to access public \(72.55.109.45\) to the internal network \(192.168.100.1\)

Tobiah's explanation:

* ISP gives you public IP.
* ISP has registered with IANA - Internet Authority for Numbers Assigned
  * They pay to own a set of IP addresses.
  * They can hand them out at their leisure, charge for them \(comes with your internet access\).
* They give you a router that has a NAT function.
  * It has a NAT table.
* They say the Private is equal to the Public in that NAT table.
  * This happens in PAT - Port Address Translation
* If they want to send something to you, they send it to your public IP address/port and that directs, through the NAT table into your Private IP address.
* This is part of the Source/Destination in the packet/frame.

  
  
Windows: nslookupMac/Linux: netstat  
  
  
  
  
  
  
  
  
  
  
  
  
  


