# DNZ / VLAN / Firewalls / Attacks

**The DMZ**

* The Demilitarized  Zone \(DMZ\) is a private network that sits between a private LAN and the public internet.
* Used to expose web-servers and other servers to the public internet without exposing the private LAN to the internet.
* If a machine on the DMZ becomes compromised the attacker will not have access to the LAN.

For security reasons, you would not want to open up port 80 \(http\) directly into the LAN. Instead the web-server is placed in the DMZ with port 80 open from the outside to the DMZ only.![](https://www.evernote.com/shard/s342/res/2bf841ab-ea51-8831-07fa-45ed31e2f8a0)  
**Honeypot & Honeynet**

* Honeypot - a host that is exposed or partially exposed to the internet to invite attacks while monitoring and collecting information.
* Honeynet - an entire network that is made to seem like a live production network with weak security that invites attacks for monitoring purposes.

  
**Testing Lab**

* It's important to have a testing lab or testing environment that is separated from the production network.
* A testing lab is useful for:
  * Testing patches and updates before deploying to the production network.
  * Test new/different hardware and software setups.
  * Test fixes to complex problems.
  * Train others on lab equipment without interfering with the production network.

  
**VLANs**

* VLANs are incredible tool for segmenting networks.
* Different VLANs can be created for different areas of the network such as the main network, guest network, and DMZ.
* Can apply security on a per-VLAN basis with things like ACLs applied to each VLAN gateway.

![](https://www.evernote.com/shard/s342/res/b0795e07-5ed1-41e1-f8ee-1cfc64fa17b8)

**Network Segmentation**

**Intrusion Detection System \(IDS\)**

\*\*\*\*![](https://www.evernote.com/shard/s342/res/5f7413f7-695e-6d2a-cbaa-140f387d6556)  
HIDS - Host-based Intrusion Detection \(on computer\).NIDS - Network-based Intrusion Detection \(on Network\).  
![](https://www.evernote.com/shard/s342/res/da4120b1-2ccb-ec85-aacc-7f9401e269c3)  
  
IDS and IPS work from inside the network to catch attacks and breaches that make it through the firewall.

* Firewalls filter traffic on the edge.

IDS detects attackers and network anomalies and sends alerts via email, text, etc.

* HIDS - Host Based, on host computer.
* NIDS - Network-based, on network.

IPS actively defends the network by stopping attacks and also performs IDS functions such as alerting.

**What is a Firewall?**

* A Firewall filters \(permits or denies\) traffic based on a set of criteria.
* Goal: control traffic that enters and leaves the network.
* Rules are created for inbound and outbound connections.
* Network-based Firewall \(physical hardware on the edge of the network\)
* Host-based Firewall \(software on a computer\).

![](https://www.evernote.com/shard/s342/res/8b815668-3557-4492-2f43-2a4d84b897e1)  
  
**Network Firewalls**

![](https://www.evernote.com/shard/s342/res/00603470-5b64-5959-da83-5e266af26ec6)

\*\*\*\*![](https://www.evernote.com/shard/s342/res/26d6d5a5-c3b3-dbb3-e914-9e3a3968aee2)

* Network firewalls are usually routers also, but can also just be an in-line filter.
* Network firewalls are usually capable of NAT since they are internet facing devices.
* Routers don't have to be firewalls, but some can have firewall features enabled.
* Dedicated Network firewalls can provide multiple security services.
* Firewalling, VPN services, anti-malware, content filtering, etc.
* This is called Unified Threat Management \(UTM\)
  * a single hardware or software installation provides multiple security functions.

![](https://www.evernote.com/shard/s342/res/b4dd7277-f06f-dbc8-239d-054f0749d81c)  
  
**ACLs, Stateless & Stateful**  
ACL \(Access Control List\): Used on routers and firewalls to create a list of rules for permitting and denying traffic. ACLs can define the protocol such as IP, source network, destination network, and the TCP/UDP port number for matching traffic.

* Stateless Firewall: employs only ACLs to control inbound and outbound traffic.
* Stateful Firewall: keeps track of the connections and can allow return traffic as long as it was first generated from inside the network.

![](https://www.evernote.com/shard/s342/res/adad05c5-1e29-755d-b755-4caec797ef6f)  
  
**Deep-Packet Inspection**  
Advanced firewalls are capable of inspecting the content of Packets. This allows a firewall to determine the context of the connection \(what it is really doing\).

* Application Aware Firewall
* Context Aware Firewall
* This means the firewall can understand what services and applications the packets are fore.
* This is how services such as network-based anti-malware are possible, but it also allows us to have even more control over what happens in our networks.
* Decisions can be made based on what is deep inside the packets rather than just where it's coming from and where it's going to.

  
**VPN -** Virtual Private Network  
****Provides a private network connection between two endpoints .

* Normally incorporates encryption to protect the VPN tunnel.
* Two main types of VPN.
  * Host to Site aka Remote VPN
  * Site to Site VPN

![](https://www.evernote.com/shard/s342/res/fa79503e-0ea5-8fa1-96a5-659c7034931b)  
VPN Concentrator: A device that is dedicated to handling large amounts of VPN connections. Most of the time the Firewall also acts as the VPN Concentrator, but it could also be a separate device.  
**VPN Protocols & Encryption**

* PPTP \(Point to Point Tunneling Protocol\): Uses PP
* P for authentication and modified GRE for the tunnel. No inherent encryption, unsecure, mostly obsolete.
* GRE Tunnel \(Generic Routing Encapsulation\): Used with routers to create a generic tunnel. In combination with IPSec creates an encrypted VPN tunnel.
* IPSec \(Internet Protocol Security\): Provides a method for authentication and negotiation of crypto keys. Uses Internet Key Exchange \(IKE\) to negotiate the key and ISAKMP for key exchange.
  * Authentication Algorithms: HMAC-MD5, HMAC-SHA-1
    * [https://en.wikipedia.org/wiki/HMAC](https://en.wikipedia.org/wiki/HMAC)
  * Encryption Algorithms: DES, 3DES, Blowfish, AES
* SSL VPN \(Secure Sockets Layer\): Uses SSL to establish VPN connectivity. For host to site VPNs a web browser can be used to connect the VPN which is easier for the VPN users.

**Attacks and Threats**  
**Malware**Software written specifically to harm and infect a host system including viruses, worms, trojans, spyware, adware, ransomware, etc.  
Compromised SystemA host, server, network node, or other computer system that has been infected with malware or otherwise successfully attacked and exploited.  
Many attacks are performed by compromising computers with malware that is designed to perform a specific type of attack.**Denial of Service Attack** \(DoS\)

* Floods the target with traffic.
* Distributed DoS \(DDoS\)
* Botnet, zombie computers.
* Coordinated attack.
* Target cannot handle the traffic.

![](https://www.evernote.com/shard/s342/res/a225fc3a-67d6-c3c3-b6f9-4c3557a964bd)  
**Smurf Attack**

* Floods the target with a spoofed ICMP.
* Attacker sends an IP directed broadcast ping to large networks with a spoofed IP source of the target victim - the ICMP replies all go to the target causing a DDoS.
* A type of reflective/amplified DoS.
* Most modern routers have directed broadcast turned off by default.

![](https://www.evernote.com/shard/s342/res/2f354df8-9423-777a-7e2b-3a98773fff7f)  
**VLAN Hopping**

* A Malicious user on one VLAN gains access to traffic on another VLAN that it shouldn't have access to.
* Either acts a trunking switch \(switch spoofing\) or double tags its frames with two VLANs.
* Can also exploit Voice over IP ports as they use a data VLAN and voice VLAN. An attacker can use similar techniques on a VoIP port to gain access to the Voice VLAN.

![](https://www.evernote.com/shard/s342/res/f61f894d-999d-e1fd-8fad-416f7d4bf08c)  
**Man-In-The-Middle \(MITM\)**

* An attacker causes traffic between two endpoints to be sent through to the attacker.
* Attacker can then intercept and manipulate the data.
* This could be on a local private LAN with a malicious user on or via the public internet.
* There are many types of MITM attacks. 

![](https://www.evernote.com/shard/s342/res/8c7d914e-2ce4-748d-d061-f4faa1d12ad3)  
**ARP Poisoning**

* A malicious user poisons the ARP cache of devices communicating with each other so that their layer 2 Frames will be redirected to a machine used to intercept the communication.
* A type of MITM attack.

