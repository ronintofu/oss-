# Network Architecture

**Security Zones / Topologies**

* Each zone on a network is separated based on organizational role or level of security.
* For example:
  * Secure Zone - These are the most sensitive systems, with mission-critical data.
  * General Work Zone - These are standard workstations and servers, with typical business data and functionality.
  * Low Security Zone - These are computers, network segments, and systems that have no highly sensitive information, and the breach of these systems would have minimal impact.
* Types:
  * DMZ - Demilitarized Zones
    * A network segment located between the protected \(internal\) and unprotected \(public\) networks.
    * Provides a buffer zone / defense-in-depth.
    * Usually set up using firewalls.
    * Contains hardened systems that need to reach each network segment.
      * email
      * web
      * DNS servers
  * Extranet
    * A private network that uses Internet tech and the public telecom system to securely share part of a business's info or operations with suppliers, vendors, partners, customers, or other businesses.
  * Intranet
    * Websites or apps that are only accessible within the org's network.
  * Wireless Segmentation
    * Separating wireless access on an internal network.
    * Creating a buffer between wireless and wired networks.
    * Separating guest wireless access from internal networks.
    * Controlled by 801.1x - Port based access control.
    * MAC filtering - restricting access based on the device's NIC address \(MAC\).
  * Guest

**Security Device Placement**

* Where should security devices be on a corporate network?
  * Firewalls / UTM \(border\)
  * IDS / IPS \(border or internal segments\)
  * VPN
  * Proxies \(external\)
  * Load Balancers
  * SIEM - log collection / correlation
    * _Correlation Engine_ - A software application that programmatically understands relationships. 
      * Used in systems management tools to aggregate, normalize, and analyze event log data using predictive analytics and fuzzy logic to alert the systems admin when there is a problem. 
      * _Applications that examine relationships between entries in firewall logs to understand possible attacks._
      * [https://whatis.techtarget.com/definition/correlation-engine\#:~:text=A%20correlation%20engine%20is%20a,when%20there%20is%20a%20problem.](https://whatis.techtarget.com/definition/correlation-engine#:~:text=A%20correlation%20engine%20is%20a,when%20there%20is%20a%20problem.)
  * DDoS Mitigation \(Border Router\)

**Firewalls, Proxies, IDS/IPS, UTM**

* Firewall Functions:
  * Packet Filter
  * Proxy Firewall
  * Stateful Packet Inspection
* Dual-Homed Firewall - 2 NICs
* NAT - Network Address Translation
* _Dual-Homed Firewall_
  * Has two network interfaces.
    * One connects to the public network.
    * One connects to the private network.
  * The forwarding and routing function should be disabled on the firewall to ensure the network segregation.

![](../../.gitbook/assets/image%20%2810%29.png)

**Segregation, Segmentation, & Isolation**

* Dividing a network into zones based on business or security needs.
* Example: Accounting on a different network segment from manufacturing.
* Logical \(VLAN\)
  * A network of computers that behave as if they are connected to the same wire even though they may actually be physically located on different segments of a LAN.
* Virtualization
  * Virtualized servers and workstations - easier to separate.
  * You should not allow internet browsing on a virtualization host. 
    * This can present possible security breaches through the introduction of spyware or malware.  
* Air Gaps
  * Physical separation.

**VPN / Tunneling**

* A private network connection through an unsecured, public network.
* Use to connect LANs
* Remote devices appear as if they are local.
* Methods:
  * Site-to-Site - Connect LANs across the internet.
  * Remote Access - Connect users or devices to a corporate network.
  * Remote Access Server \(RAS\)

**SDN - Software Defined Network**

* The entire network is virtualized.
* Allows for easier network segmentation.
* Allows admins to place virtualized security devices anywhere.
* The SDN architecture is:
  * Directly Programmable
  * Agile
  * Centrally Managed
  * Programmatically Configured
  * Open Standards-Based and Vender-Neutral

**Honeypots / Honeynets**

* Use:
  * Systems or networks exposed to capture malicious activity.
  * Gather investigation evidence.
  * Study attack strategies.
* Separated from any business network. 
* [http://www.honeyd.org](http://www.honeyd.org)/

**Fibre Channel** - [{source}](https://www.geeksforgeeks.org/fundamentals-of-fibre-channel/)

* A high-speed network technology used to connect server to data storage area network. 
* It handles high performance of disk storage for apps on many corporate networks. 
* Supports data backup and replication. 
* Topology:
  * Point-to-Point
  * Fibre Channel Arbitrated Loop
  * Switched Fabric Topology

