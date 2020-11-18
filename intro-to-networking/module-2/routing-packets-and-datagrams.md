# Routing Packets and Datagrams



**Routing Packets and Datagrams**

* The data unit of IP can be called a "datagram" or "packet".
* Based on assistance from the TCP stack.
* UDP+IP = Datagram \(connection-less\).
* TCP+IP = Packet \(connection-oriented\).
* Most often referred to as a "packet" rather than a datagram.
* The router doesn't care if it's a datagram or packet and will route either way.

![](https://www.evernote.com/shard/s342/res/ab365325-02ed-0946-501d-d2d7ee0253e5)

* * Router is called the "Default Gateway" when a computer needs to go to it to get to another network \(like the internet\), not from the internet to the Computer.
    * "The gateway to get to other networks."
  * Specializes in routing packets from one network to another, so it has multiple IP addresses.
    * Router has multiple IP addresses/MAC addresses \(for the different routing sides\).
  * Frame gets IP address info \(source/destination\) at Sender \(IP 192.168.100.2\)
  * Frame goes to switch \(Network 192.168.100.0\)
    * Switch sees next destination MAC address as CC-CC-CC-CC-CC-CC router and sends it there.
  * Router analyzes frame header \(addressing info\) and see's the frame is intended for it.
    * Checks packet and sees the destination is for IP 10.10.10.2
    * Repacks into frame \(counts as new frame\)
      * Changes the MAC address header to BB-BB-BB-BB-BB-BB.
    * Sends it out into the network.
  * Network 10.10.10.0 switch receives the frame and sends it to BB-BB-BB-BB-BB-BB.
  * BB-BB-BB-BB-BB-BB unpacks frame/packet and reads the data.

