# Core Protocols



**Domain Name System**

* Broken down into multiple levels:
  * Root Domain - represented by a dot.
  * Top-level Domain.
    * .edu
    * .gov
    * .com
    * .org
    * .mil
  * Second-level Domain.
    * mit
    * lsu
    * google
    * nexgent
    * redcross
    * af
    * army
  * Host.
    * web.
    * www.
    * mail.
    * learn.
    * givingday.

![](https://www.evernote.com/shard/s342/res/bcc1b628-f684-c615-cc31-5df311fb731e)

* DNS resolves IP addresses based on Fully Qualified Domain Names \(FQDNs\)
* FQDN: Identifies the specific server or host at the domain \(the entire name all put together\).
  * [www.google.com](http://www.google.com)
  * [mail.google.com](http://mail.google.com)
  * etc.
* Root level domain: invisible.
  * www.google.com.
  * mail.google.com.
  * etc.
* With DNS we can do things like visit these websites without knowing the public IP address.
* URL: Uniform Resource Locator
  * Includes the FQDN and protocol such as http, https, and ftp.
    * [https://mail.google.com](https://mail.google.com)
    * [https://learn.nexgent.com](https://learn.nexgent.com)
    * etc.

  
**DNS Servers**

* Public DNS Server
  * A free to use DNS server on the public internet \(there are many of these\).
  * Resolves public FQDNs to IP Addresses.
  * Most ISPs have their own public DNS Server for their customers to use.
  * Public DNS server examples:
    * Google public DNS: 8.8.8.8 and 8.8.4.4
    * Hurricane Electric:L 74.82.42.42
    * Verisign: 64.6.64.6 and 64.6.65.6
    * Level3: 209.244.0.3 and 209.244.0.4
* Private DNS Server
  * Windows Server
  * Linux BIND
  * Third party DNS software for most any operating system.
  * Provides for internal hostname lookups within a private organization.
  * Public queries are forwarded out to a public DNS server.
  * Private DNS names are not part of the public Domain Name System.
  * Private DNS names are associated with an organizations private IP addresses.

![](https://www.evernote.com/shard/s342/res/f5c2cce8-1852-0f6e-1ed4-f801873384cc)

* Split Horizon DNS \(aka Split Brain\)
  * A mechanism for DNS servers to supply different results based on the source.
  * Example:
    * An organization hosting their own website with public facing DNS

**Diagram of a DNS Request**

\*\*\*\*![](https://www.evernote.com/shard/s342/res/f04ffd3d-2dd9-9a36-a863-d2dba30f01ab)![](https://www.evernote.com/shard/s342/res/4de2d0ab-bd4a-6673-dcfa-aef34f1ff11d)![](https://www.evernote.com/shard/s342/res/58d5a562-db8f-8f72-f624-781247a92c54)  


**DNS Request - Public**

\*\*\*\*![](https://www.evernote.com/shard/s342/res/beb2cd41-fb0d-fb8c-718b-9d7a12aa618a)  
  
  


**Core Protocols**

**SSH & Telnet**Command Line Access to Routers, Switches, Firewalls, and Servers

* **VTY lines** are the Virtual Terminal lines of the router or switch, used solely to control inbound Telnet connections. They are virtual, in the sense that they are a function of software - there is no hardware associated with them.

![](https://www.evernote.com/shard/s342/res/2e0bef6e-73bc-65c1-a5b3-039dd711a814)

* SSH \(Secure Shell\): TCP Port 22
  * Encrypted Session.
  * Replaces protocols like Telnet.
  * SSH v2 should be used over v1.
* Telnet: TCP Port 23
  * Clear text / plaintext.
    * Even passwords.
  * Should be disabled for best practice.

**ICMP** - Internet Control Message ProtocolCheck IP connectivity to any network node.

* Ping

![](https://www.evernote.com/shard/s342/res/e91326c8-2d9d-e65e-745f-3ff901f40183)

* Internet Control Message Protocol
  * Has no port number! Works at Layer 3.
  * Has ~40 type fields.
  * Ping uses Echo Request and Echo Reply.
  * Traceroute also uses ICMP.
  * Many organizations block ICMP on the outside \(can lead to Denial of Serves, or DoS attacks if enabled\).

  
**FTP & TFTP** - File Transfer Protocol & Trivial File Transfer ProtocolRetrieve files from an FTP Server on the network.Used to transfer files to routers, switches, firewalls, servers, & hosts.

![](https://www.evernote.com/shard/s342/res/c1969f86-b703-4cb0-3788-818fdae7e019)

FTP - File Transfer Protocol

* TCP Ports 20 & 21.
* FTP and FTP-data.
* Connection-oriented.

  
TFTP \(Trivial File Transfer Protocol\)

* UDP Port 69
* Connectionless.

  
**RECAP**

* SSH & Telnet allow for command line access to network devices.
* SSH is secure and should be used instead of Telnet.
* ICMP allows us to test IP connectivity on the network with applications like Ping & Traceroute.
* FTP & TFTP are used to transfer files across the network and over the internet as well.
* FTP uses TCP ports 20 & 21 \(connection-oriented\).
* TFTP uses UDP port 69 \(connection-less\).

