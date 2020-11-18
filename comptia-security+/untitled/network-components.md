# Network Components

**Load Balancers**

* Scheduling: distributing load.
  * Round-robin - taking turns using a circular pattern.
  * Affinity \(AKA 'sticky session'\) - requests sent to a specific application.
  * Least connections.
  * Random.
* Active/Active: servers work together.
* Active/Passive: all traffic is sent to the active server.
  * The secondary server remains on standby until the load on the primary server reaches a critical point. 
* Virtual IPs \(VIPs\): at least one physical server assigned, but more than one virtual IP address assigned.

**Access Points**

* A centralized access controller \(AC\) is capable of providing management, configuration, encryption, and policy settings for WLAN access points.
  * Fat - intelligent access points.
  * Fit - scaled fat.
  * Thin - intelligent antennas \(only transmit/receive\).
  * Controller-based vs standalone.

**Network Address Translation \(NAT\)** - [{source}](https://www.geeksforgeeks.org/network-address-translation-nat/)

* Allows multiple devices to access the internet through a single public address. 
  * Needs to translate private IP address to a public IP address to achieve this.
* NAT is a process in which one or more local IP address is translated into one or more Global IP address and vice versa in order to provide internet access tot he local hosts. 
* From a security standpoint, NAT hides internal IP addresses from the public network. 

**Spanning Tree Protocol \(STP\)** - [{source}](https://www.dummies.com/programming/networking/cisco/spanning-tree-protocol-stp-introduction/)

* The primary loop protection on an ethernet network. 
* Helps mitigate the risk of L2 switches in the network suffering from a DoS style attack caused by staff incorrectly cabling network connections between switches. 
* STP passes data back and forth to find out how the switches are organized on the network and then takes all the information it gathers and uses it to create a logical tree. 
* Defines exactly how all the network switches are interconnected. 

![](../../.gitbook/assets/image%20%2818%29.png)

**Antennas**

* _Directional antennas_ can limit the area that is covered by the antenna. 
* Antenna placement should be as far away from exterior walls as possible. 
  * Otherwise, the signal will go outside the building. 
* Types of Antennas
  * _Omni_ - a multi-directional antenna that radiates radio wave power uniformly in all directions in one plane with a radiation pattern shaped like a doughnut. 
  * _Yagi_ - a directional antenna with high gain and narrow radiation pattern. [{source}](http://www.antenna-theory.com/antennas/travelling/yagi.php)
  * _Sector_ - a directional antenna with a circle measured in degrees of arc radiation pattern. 
  * _Dipole_ - the earliest, simplest, and most widely used antenna with a radiation pattern shaped like a doughnut. [{source}](https://www.electronics-notes.com/articles/antennas-propagation/dipole-antenna/dipole-antenna-aerial.php)

