# Networking Basics

**What is a 'Network'?**

* A network is a way to get 'stuff' between 2 or more 'things'.
* Goal: Basic understanding of common modern networking technology and terminology.
* Examples:
  * Analog:
    * Snail mail.
    * Phone system.
    * Conversations.
    * Railroad systems.
    * Highways and roads.
  * Digital:
    * Routers & switches.
    * Clients & servers.
  * Applications:
    * Email/messaging.
    * Database.
    * Web.

**Protocol Concepts**

* Protocols are a set of rules.
* What do you want to do? \(Application\)
* Where are you going? \(Addressing\)
* How did you get there? \(Media Types\)
* Did you get there? \(Acknowledgements, Error Checking\)

**Computer Networking Models**

* Models, also called protocol stacks, represented in layers, help to understand where things go right or wrong.

![OSI Model: The 7 Layers of Network Architecture &#x2013; BMC Blogs](https://blogs.bmc.com/wp-content/uploads/2018/06/osi-model-7-layers-1.png)

![Network Services: TCP/IP and the OSI Model](https://3.bp.blogspot.com/-0nh6-bv5qUg/UpOpaFpAVhI/AAAAAAAADds/Y8z1p7dGWVc/w1200-h630-p-k-no-nu/Network+_FIGURE+3+.+1+A+comparison+of+the+seven-layer+OSI+model,+the+four-layer+DoD+model,+and.png)

**Physical Layer \(Layer 1\)**

* Cat 5 \(5e, 6\) twisted pair copper wire.
* Fiber \(multi-mode or single-mode\) coaxial copper \(thick and thin-net\).
* Cable modem, plain phone \(DSL\), microwaves \(wireless ethernet\), etc.
* WiFi, IEEE 802.11

**Data Link \(Layer 2\)**

* The MAC address, or sometimes ethernet address, physical address, adaptor address, hardware address, etc.
* It's a 12 digit \(48 bit\) hexadecimal address that is unique to that ethernet adaptor and no other in the world. It can be written as 00:30:65:83:fc:0a, 0030.6583.fc0a, 03065:84fc0a, or 00-30-65-83-fc-0a, but they all mean the same thing.
* The first 6 digits are the vendor code, \(003565 belongs to Apple\), the last 6 are the individual interface's own. Like a car's VIN.
  * [http://coffer.com/mac\_find](http://coffer.com/mac_find)
* Finding MAC address:
  * Open a command prompt \(Windows\) or Terminal \(Linux, OSX\).
  * Type Ifconfig /all \(Windows\) or ipconfig \(Linux, OSX\).
  * On phones it's found in the settings under "About Phone".

**Network Layer \(Layer 3\)**

* The Internet Protocol \(IP\) is the Network layer protocol used on the internet.
* ARP: Address Resolution Protocol. Turns an IP number into an ethernet number. Asks IPs for MAC addresses.
* **IP Addressing**
  * IPv4 address consists of 4 'octets' such as 171.64.20.23
  * Each 'octet' consists of numbers between 0 and 255 \(or OO and FF in hex\).
  * It works like the phone system with area codes to the left, then a prefix, but are more flexible. On campus, your computer will know that 171.64 means "UNO" while it will figure out that "20" means "Pine Hall" and will learn that "23" means the computer called "networking". It does this via subnet masking \(in this case, 255.255.255.0\).
  * IPv6 uses 128-bit address, theoretically allowing 2128, or approximately 3.4x1038 addresses.
    * Example: fd1a:c35:241:0:ac05:9a33:b74:3b15
* **IP: Domain Name Resolution \(DNS\)**
  * Since most people find it easier to remember names instead of numbers, IP numbers can and almost always are associated with names.
  * Your computer, however, needs a number, so the Domain Name System \(DNS\) exists to make everyone happy.
  * A name, such as networking.bellevue.edu, tells you the first \(or top\) level domain \(.com, .edu, .net, etc\), the second level domain \(google, cybrary, nexgent, etc\) and the actual hosts' name \(www, networking, learn, etc\).
    * If you want the number for a host name within a site, you'd ask one of the DNS servers to give it to you.
    * If you need to go outside the site, you'd ask the servers to figure out which other servers should get your request, send it to them, and then you'd get a reply back from the original DNS server queried.
      * Host -&gt; DNS -&gt; Outside DNS -&gt; DNS -&gt; Host.

**Transport Layer \(Layer 4\)**

* The protocols of the layer provide host-to-host communication services for applications.
* Uses in-coming and out-going ports to/from a server.
  * Examples:
    * Port 80 - HTTP
    * Port 443 - HTTPS
* Major Types:
  * Transmission Control Protocol \(TCP\) is connection-oriented and provides error checking.
  * User Datagram Protocol \(UDP\) is connectionless, used for streaming.

**Application Layer \(Layer 7\)**

* Interfaces with the operating system and other applications and communicates data between files, messages, and other network activities.
  * Email \(SMTP\)
  * Web \(HTTP/HTTPS\)
  * File Transfer \(FTP, Telnet\)
  * Time \(NTP\)

**Port Knocking** [{source}](https://en.wikipedia.org/wiki/Port_knocking)

* A method of externally opening ports on a firewall by generating a connection attempt on a set of pre-specified closed ports. 
* Once a correct sequence of connection attempts is received, the firewall rules are dynamically modified to allow the host which sent the connection attempts to connect over the specified port\(s\). 

