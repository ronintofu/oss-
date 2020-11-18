# TCP/UDP/Real World TCP/Port Forwarding

**TCP** - Transmission Control Protocol

![](https://www.evernote.com/shard/s342/res/7fe91b27-818c-c081-9170-2eb1d49ee32a)

* The data unit is called a Segment.
* Favors safety over speed.
  * Making sure the data gets there in order, free of errors.
* Used for reliable communication.
* Connection-oriented protocol, 3-way handshake.
* Sequence \# and Acknowledgement \#
  * Uses these as sending traffic to keep track of the data.

![](https://www.evernote.com/shard/s342/res/733d940b-6d2c-8f63-b9c3-efa08ac5c55d)                                                          
TCP Header

* Ordered \(stream of segments arrive ordered\).
* Error detection & correction.
* Flow control.
  * Sliding window:
    * if one computer is sending traffic to another, TCP figures out if they're sending too much traffic and closes the window, or if they can handle more, it opens it up wider for more traffic to come.
* Congestion control.
  * If the session detects congestion, TCP will make changes to that to adjust for it.
* Complex and heavyweight \(a lot of processes associated with connection\).
* Examples of TCP connection:
  * HTTP
  * FTP
  * eMail \(Port 25\)

  
**Connection Establishment of TCP**

1. Source host sends SYN to destination host.
2. Destination host sends SYN ACK back to host.
3. Source host sends ACK to destination host.

Connection established at this point.

![](https://www.evernote.com/shard/s342/res/ed91e904-212c-2fa1-ed58-6845da4e2a54)  
**Connection Termination of TCP**Two ways:

1. Termination via automatic time-out.
2. Manually closing:
   * Host sends FIN to destination.
   * Destination host sends, FIN **and** FIN ACK back to source host.
   * Source host returns ACK to destination host.

Session terminated at this point.

![](https://www.evernote.com/shard/s342/res/96f9b670-907a-6ebb-da65-882ec9a6a0b1)  


**UDP** - User Datagram Protocol  


* Data is called a Datagram
* Favors speed over safety.
* Used when loss can be tolerated.
* Connection-less.
* Length & Checksum
  * Checks to make sure all the data is there.

![](https://www.evernote.com/shard/s342/res/5a7d9a47-f76e-3eb9-7162-7d2d00ab4aa0)

* Unreliable delivery
* Not ordered.
* No congestion control.
* Lightweight, faster than TCP.
* Examples:
  * Online games.
  * VoIP
  * TFTP \(Older form of FTP\)

**Real-World TCP**  


* Win/Mac/Linux
  * "netstat" switches: -a, -b, -n, -o, -r
  * "netstat ?" to show various applicable flags.
* Scan a network for IP addresses and open ports.
  * Angry IP Scanner
  * Nmap
* Check active TCP sessions on Cisco router IOS
  * "show tcp brief"

**RECAP**

* TCP is connection-oriented and allows host computers to know when packets are lost.
* UDP is connection-less and favors speed over safety or reliability.
* TCP uses a 3-way handshake to set up a TCP session.
* TCP uses a sequence number and acknowledgement number to keep track of the data that is sent.
* TCP data unit is called a segment.
* UDP data unit is called a datagram.
* The netstat command lists all ports currently open on your computer and the common switches/flags are -a, -b, -n, -o, and -r.

**Port Forwarding**Any traffic arriving on a specific TCP or UDP port will be forwarded to a defined internal host and port.  
Example 1 - Port Forwarding Settings Protocol: **TCP** Source Network: **ANY** Source Port: **80** IP: **192.168.100.50** Destination Port: **80**  
![](https://www.evernote.com/shard/s342/res/e2aaf398-6d77-6326-fa9d-7398e060fed0)  
Example 2 - Port Forwarding Settings Protocol: **TCP** Source Network: **ANY** Source Port: **8080** IP: **192.168.100.50** Destination Port: **80**  
![](https://www.evernote.com/shard/s342/res/ac53f6fb-4f3b-fbd4-d855-faecdfd99308)  
**When to Use Port Forwarding?**

* There are many scenarios when you may want to forward ports to a specific host. Below are some examples:
  1. Web Server
     * Forward ports 80\(HTTP\) and 443\(HTTPS\) to the server so it will be sent any web traffic.

              2.  Mail Server

* * * If running a mail server such as MS Exchange it will need to be forwarded traffic coming inbound on port 25\(SMTP\)

      3.  IP Camera

* * * Use a random port number above 1024 such as 9000 or 15000 and forward that to the camera on internal port 80. That way we aren't using up the web port \(80\) and we are also adding just a bit of security by using a non-standard port.

![](https://www.evernote.com/shard/s342/res/baf4c945-95fe-d6c7-ddc2-e27da728417a)

