# Intro to Networking

**Intro to Networking**  
  
What is a Network?

* Two or more computers that can exchange information over a data link.

  
End Devices

* Computers
* Laptops
* Servers
* Tablets
* Phones

  
Infrastructure Devices

* Routers
  * "interstate highways" for routing traffic to the next point.
* Firewalls
  * "traffic control lights"
* Switches
  * "intersection/exit" for sending traffic out.
* Hubs
  * "side street/bypass"
* Wireless Access Points

  
Cables & Media

* Fiber Optics
* Cat 5e Cable
* Coaxial
* Phone Lines
* Wireless Radio

  
Protocols

* Internet Protocol \(IP\)
* Transmission Control Protocol \(TCP\)
* Hyper Text Transfer Protocol \(HTTP\)

  
Logical Diagram Icons

![](https://www.evernote.com/shard/s342/res/4d9b7968-64d0-6eac-cc62-728ca1403f88)  


**The Need for Computer Networks**  


* What do networks do for us?
  * Connect computers together.
  * Provide access to network services.
    * File sharing & data access.
    * Email & messaging
    * Printing & faxing
    * Phone service \(VoIP\)
    * Video streaming
    * Internet and web access
    * Wired and wireless access
  * Modern Networks
    * Support many types of traffic
    * Data, voice, and video.

  
**Basic Network Components**

\*\*\*\*![](https://www.evernote.com/shard/s342/res/708765f3-76b9-4f7d-5f7c-ebf5ee26acb4)\*\*\*\*

**Client**

* A workstation or other end user device that provides a user with access to the network.
* Could be a PC, laptop, VoIP Phone, wireless tablet, smartphone, teleconferencing endpoint, TV, etc.
* Uses the services of another computer or the shared resources of a network server.

  
**Server**

* Computer that shares its resources such as files and printers with other computers on the network.
* Email print, domain, phone, website, etc.
* Could be local or remote.

  
**Switch & Hub**

* Primary purpose is to provide wired access to the LAN. Hubs are older, replaced by switches.
* Switches are intelligent and know which devices are connected to them by learning the MAC address of each device.
* Switches send traffic only to the destination MAC address whereas Hubs flood the entire network.
* Switches are more efficient.
* Switches provide many other benefits such as loop avoidance.

  
**Wireless Access Point**

* AKA WAP, Wireless AP, AP, or Access Point
* Connects wireless network nodes to wireless or wired networks.
* Many commercial grade WAPs are specifically for wireless access only.
* Many consumer grade WAPS and commercial grade WAPS are combination devices that also act as a switch and router rolled into one.

  
**Network Media**

* Media of the network is what physically connects a device into the network.
* Media can be wired \(cables\) or wireless \(radio waves\). Wired media comes in the form of copper cables and fiber optic cables.
* Both wired and wireless media have many different standards associated with them. Some examples are distance limitations and bandwidth/speed capacities.

  
**Router**

* Device that connects separate networks.
* Intelligently forwards packets from one network to another based on network address such as IP addresses.
* Acts as a gateway to leave the LAN to another LAN or the internet.

**Network Types**

  
**LAN**

* Local area network
* Devices in a LAN are in the same \(small\) geographic area.

  
**WAN**

* Wide area network
* WAN connections provide access from the internal network to external or remote networks.
* Typically lower speed/bandwidth than LANs due to the long distances of WANs.

  
**WLAN/WWAN**

* Wireless LAN/WAN
* Wi-Fi, Satellite, Cellular, etc.

  
**MAN**

* Metropolitan Area Network
* Geographically larger than a LAN, incorporates both LANs and WANs.
* City-wide as an example.

  
**CAN**

* Campus Area Network
* Two or more LANs
* Multiple buildings
* Large capacity
* High speed
* Switched network
* College/military base

  
**SAN**

* Storage Area Network
* High speed server & storage based network
* Does not rely on a LAN or a WAN.

  
**PAN**

* Used to connect periphs.
* Short range wireless tech such as Bluetooth.

**BITS, BYTES, & ETHERNET FRAMES**

**What does data look like?**

* 1s and 0s

![](https://www.evernote.com/shard/s342/res/f631d37c-0c74-e60c-87be-11a220d65dc3)  
**bits vs Bytes**

* 8 bits in a single Byte - 00100101 \(example\)
* Network data rates are measured in bits per second.
  * the connection is 100 Megabits per second \(100Mbps\)
  * That's 100,000,000 bits per second.
* Files are measured in Bytes.
  * Such as a video being 350MB, or 350 Megabytes
    * That's 350,000,000 Bytes or 2,800,000,00 bits \(350,000,000 \* 8\)

  
**Packetized Data**

* Modern Networking Tech
* Packet Switched Networks
* Chunks of 1s and 0s \(not a steady stream\)
* Called a frame \(or a packet\)
* Contains a payload and addressing info
* Frame payload = 1500 Bytes

  
**Ethernet**

* IEEE standard 802.3 \(ieee.org\)
* A protocol "family"
* Supports many types of media and data rates
* Performs encapsulation of Frames
* Frames begin and end in the NIC \(Network Interface Card\)

  
Further reading: [https://www.sciencedirect.com/topics/engineering/ethernet-frame](https://www.sciencedirect.com/topics/engineering/ethernet-frame)  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  


