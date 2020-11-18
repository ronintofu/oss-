# Module 3 - Full Stack Network Security

### LAN &  WAN SECURITY

**Access Controls -** [https://learn.nexgent.com/modules/cyber-security-specialist-module3/sections/cyber-security-specialist-module3-section2/lessons/cyber-security-specialist-module3-accesscontrols](https://learn.nexgent.com/modules/cyber-security-specialist-module3/sections/cyber-security-specialist-module3-section2/lessons/cyber-security-specialist-module3-accesscontrols)

**The Problem**

* Viruses, worms, and botnets are often spread by unknowing victims. These victims may be your own network users.

![](https://www.evernote.com/shard/s342/res/61695447-17b2-92c4-40e5-4ed681be688d)

* Network today is not the same.
* There are a lot more users and a lot more network traffic, as well as BYOD \(bring your own devices\).

**What is a Network Access Control?**

* A NAC system can deny network access to non-compliant devices, place them in a quarantined area, or give them only restricted access to computing resources, thus keeping insecure nodes from infecting the network.
* NAC enables three key capabilities to secure IoT devices:
  * Network visibility to see every device and user as they join the network.
  * Network control to limit where devices can go on the network.
  * Automated response to speed the reaction time to events.
* Network access control allows you to identify who, what where, when, and how an end-user or device is accessing your network.
  * Who is the end-user and are they a known user inside of your active directory?
  * What is the end-user or device \(IoT\) trying to access on your network?
  * Where are they connecting to the WiFi? In their office, the cafeteria, hotel room, etc?
  * When are your end-users or IoT devices accessing the network?
  * How your end-users are accessing your network \(smartphones, laptops, tablets, etc\) as well as what IoT devices/systems are accessing your network \(security cameras, vending machines, HVAC, scanners, printers, POS systems, etc\).

![](https://www.evernote.com/shard/s342/res/a0101a60-4da6-c33c-d4b0-fe90a54fd7ac)  
**Assign**

* Once NAC system properly identified who or what \(or both\) is trying to access the network NAC can then assign the correct corresponding role for that user/device or group of users/devices.
* These assigned roles come with pre-determined sets of policies that control their access on the network \(RBAC\)

![](https://www.evernote.com/shard/s342/res/3279a1a1-2ed7-4ba7-c368-2107f7fa30b9)  
**Enforce**

* NAC use organization's network infrastructure to enforce security policy compliance on all devices that attempt to gain access.
* NAC appliance to authenticate, authorize, evaluate, and remediate wired, wireless, and remote users before they can access the network.
* Enforcement comes down to creating accurate policies that provide the correct user or device with the access it needs.
* Enforce security policies by blocking, isolating, and repairing non-compliant machines.

![](https://www.evernote.com/shard/s342/res/4ec9bfc8-a9c1-c6cb-d037-49937b1471a9)![](https://www.evernote.com/shard/s342/res/2288669c-9a50-16d2-e32f-3995f4ddb842)  
  


**Firewall**

**What is a Network Firewall?**

* A firewall is a network security device that provides network security by filter incoming and outgoing network traffic based on a set of user-defined rules.
* They establish a barrier between secured and controlled internal networks that can be trusted and untrusted outside networks, such as the Internet.
* A firewall can be hardware, software, or both.

**Firewall Control**

* Service Control
  * Determines the types of Internet services that can be accessed, inbound or outbound.
* Direction Control
  * Determines the direction in which particular service requests are allowed to flow.
* User Control
  * Controls access to a service according to which user is attempting to access it.
* Behavior Control
  * Controls how particular services are used \(e.g. filter e-mail\).

**Firewall Rules**

* Firewall works by filtering incoming network data based on configured rules to permit or deny traffic.
* Firewall rules can be based on:
  * Source IP Address
  * Destination IP Address
  * Protocols
  * Ports
  * Application
  * Action

![](https://www.evernote.com/shard/s342/res/ac25aa38-90d1-8d21-663b-b4ce2ce37b4a)  
**Firewall Types**

* Stateless Firewall
  * Firewalls filter packets that attempt to enter or leave a network and either accept or reject them depending on the predefined set of ACL rules.
  * Based on information in packet header source, destination IP, port, IP protocol, and interface.
* Stateful Firewall
  * Stateful firewall allows or blocks traffic based on state, port, and protocol.
  * It monitors all activity from the opening of a connection until it is closed.
  * Filtering decisions are made based on both administrator-defined rules as well as context, which refers to using information from previous connections and packets belonging to the same connection.

![](https://www.evernote.com/shard/s342/res/39737042-18f2-1a89-1942-86dae75847a3)

* Next-Generation Firewalls \(NGFW\)
  * Combine traditional firewall technology with additional functionality, such as encrypted traffic inspection \(SSL Decryption\), IPS, anti-virus, anti-malware, content filtering, deep packet inspection, threat prevention, and URL filtering.
* Host-Based Firewall
  * A host-based firewall is a piece of firewall software that runs on an individual computer or device connected to a network.
  * Protect single host machine only.
* Cloud Firewall
  * Hosted in the cloud.

![](https://www.evernote.com/shard/s342/res/5772a99c-b0c3-3c79-1693-ce27dcf06c1c)![](https://www.evernote.com/shard/s342/res/971238d5-9f69-2033-2c7d-8195ad7aefaf)  
**Firewall Deployment Options**

* Software/Host Firewall
* Hardware/Network Firewall
* Cloud Firewall
  * A firewall that is hosted in the cloud.
  * Cloud based firewalls form a virtual barrier around cloud platforms, infrastructure, and applications, just as traditional firewalls form a barrier around an organization's internal network.

**Proxy Server** - [https://learn.nexgent.com/modules/cyber-security-specialist-module3/sections/cyber-security-specialist-module3-section2/lessons/cyber-security-specialist-module3-proxyservers](https://learn.nexgent.com/modules/cyber-security-specialist-module3/sections/cyber-security-specialist-module3-section2/lessons/cyber-security-specialist-module3-proxyservers)

**Proxy Server Overview**

* An intermediary server between the client and the internet.
* A server that sits between a client application, such as a web browser, and a real server.
* All computers on the local network go through it before accessing information in the Internet.
* Proxy server hide, conceal, and make network ID anonymous by hiding real IP address.
  * The proxy server IP is logged instead of yours.

![](https://www.evernote.com/shard/s342/res/6c024522-9dea-6616-b184-a5b8389ded1d)  
**Purpose of Proxy Servers**

* Security
  * Since the proxy server hides the identity of the user, it protects from spam and hacker attacks.
* Improved Performance
  * Acts as a cache server.
  * Bandwidth control.
* Filter Requests
  * Prevent access to some web sites.
  * Prevent access to some protocols.
* Logging
  * Single point of access, control, and logging.

**Types of Proxy Servers**

* HTTP Proxy Server
  * Provides for the caching of web pages and files which allows you to access them faster.
  * HTTP proxy will search for the website address in the cache. If the website address is located, it will return the website to you immediately as opposed to you having to wait for it to download.
* SSL Proxy Server
  * Secure Socket Layer
  * Connected between the client and the server to provide SSL support.
  * Prevents hackers from attacking the network and intercepting  personal or financial information which is being transmitted over the Internet.
* FTP Proxy Server
  * File Transfer Protocol
  * Used in many different applications while uploading data to a server.
  * Offers enhanced security for uploading files to another server.
* Anonymous Proxy
  * Provides privacy while browsing the Internet by hiding your IP address.
  * Capable of eliminating cookies which track web browsing activity.
  * Support FTP, HTTP, and HTTPS protocols.

**Security Advantages of a Proxy Server**

* Hide your IP address.
* Filter requests.
* Performance.
* Protection
* Business Locations

![](https://www.evernote.com/shard/s342/res/f9eb9c8d-ee9e-d25b-89a3-7e56f50eb726)  
**Disadvantages of Proxy Servers**

* Limited visibility.
* Data or identity theft.
  * Due to the proxy not being set up properly by the provider.
* Lack of integration.
* Protocol limitations.

**Honeypots & Honeynets** - [https://learn.nexgent.com/modules/cyber-security-specialist-module3/sections/cyber-security-specialist-module3-section2/lessons/cyber-security-specialist-module3-honepots](https://learn.nexgent.com/modules/cyber-security-specialist-module3/sections/cyber-security-specialist-module3-section2/lessons/cyber-security-specialist-module3-honepots)

**What is a Honeypot?**

* A honeypot is a faked vulnerable system used for the purpose of being attacked, probed, exploited, and compromised.
* A honeypot system is filled with fabricated information to make it resemble a real system on the network.

**Benefits of Honeypots**

* Attack Analysis
  * Find out reasons and strategies as to why and how you are attacked.
  * To identify new vulnerabilities and risks of various operating systems, environments, and programs which are not thoroughly identified at the moment.
* Risk Mitigation
  * Lure an attacker away from the real production systems.
* Evidence
  * Once the attacker is identified, all data captured may be used in a legal procedure.
* IDS-Like Functionality
  * Since no legitimate traffic should take place to or from the honeypot, any attempt to communicate with a honeypot likely a probe, scan, or attack.
  * To capture new viruses or worms for future study.

![](https://www.evernote.com/shard/s342/res/ef0e2f3d-a662-3dca-268f-8d8aa76ec6af)  
**Common Attacks that are Mitigated**

* Brute Force Attack
* DoS
* Command Injection
* Local File Inclusion
* Remote File Inclusion
* SQL Injection

**Honeypot Tools**

* BackOfficer Friendly
* Specter

**Virtual Private Networks** - [https://learn.nexgent.com/modules/cyber-security-specialist-module3/sections/cyber-security-specialist-module3-section2/lessons/cyber-security-specialist-module3-vpn](https://learn.nexgent.com/modules/cyber-security-specialist-module3/sections/cyber-security-specialist-module3-section2/lessons/cyber-security-specialist-module3-vpn)

**What is a VPN?**

* Virtual Private Network
* Establish a secure connection over an insecure network, such as the Internet.
* Creates an encrypted connection, know as a VPN tunnel, and all Internet traffic and communication is passed through this secure tunnel.
* Any VPN is not secure, you need to add security to create secure VPNs.
* Great alternative to private WAN connections since Internet access is a cheaper solution and is widely accessible.

**VPN Features**

* Confidentiality
  * preventing anyone from reading your data. This is implemented with encryption.
* Authentication
  * Verifying that the peer device or remote user that is sending VPN traffic is a legitimate device or user.
* Data Integrity
  * Verifies that the VPN packet wasn't changed during transit.
* Anti-Replay
  * Preventing someone from capturing traffic and resending it, trying to appears as a legitimate device/user.

**VPN Types**

1. Site-to-Site VPN
   * When two or more sites that want to securely connect and communicate using the Internet.
   * VPNs traditionally use  a collection of VPN technologies called IPSec.

![](https://www.evernote.com/shard/s342/res/b0fb9d44-3954-9484-2ee4-372ae76083fa)

1. Remote-Access VPN
   * Permits a user to connect to a private network and access all its services and resources remotely.
   * Secures connections for remote users, such as mobile users or telecommuters, to corporate LANs over shared service provider networks.
   * The user installs a VPN client on his/her computer, laptop, smartphone, or tablet.
   * Remote-access VPNs can use IPSec or Secure Socket Layer \(SSL\) technologies for their VPN.

![](https://www.evernote.com/shard/s342/res/6f68545f-3141-6e9c-8db0-21ce82ab3b8d)  
**VPN Protocol**

* Internet Protocol Security \(IPSec\)
  * Used to secure Internet communication across an IP network.
  * Secures Internet Protocol communication by authenticating the session and encrypts each data packet during the connection.
  * Operates in two modes, Transport mode and Tunneling mode, to protect data transferred between two different networks.
    * Transport Mode encrypts the message.
    * Tunneling Mode encrypts the entire packet.
  * Uses two basic security protocols -
    * Authentication Header \(AH\)
    * Encapsulating Security Payload \(ESP\)
* PPTP
  * Point-to-Point Tunneling Protocol
  * Old VPN that uses PPP and GRE - insecure, no inherent encryption, and should not be used anymore.
* L2TP
  * Layer 2 Tunneling Protocol is a tunneling protocol that is often combined with another VPN security protocol like IPSec to establish a highly secure VPN connection.
  * A VPN protocol that tunnels layer two traffic, does not offer any encryption so should be used together with IPSec.
* SSL VPN
  * Uses SSL \(HTTPS\) to create a secure connection with a web browser.
  * When you surf the web using HTTP, everything is clear text. For secure connections, we use HTTPS.

**Common VPN Attacks**

* Session Hijacking
* MitM
* Spoofing
* Virus or Malware
* DDoS

**IPSec** - [https://learn.nexgent.com/modules/cyber-security-specialist-module3/sections/cyber-security-specialist-module3-section2/lessons/cyber-security-specialist-module3-ipsec](https://learn.nexgent.com/modules/cyber-security-specialist-module3/sections/cyber-security-specialist-module3-section2/lessons/cyber-security-specialist-module3-ipsec)

**IPSec VPN Overview**

* IP protocol itself doesn't have any security features at all.
* IPSec is developed by the Internet Engineering Task Force \(IETF\) which is  a set of security protocols and algorithms used to secure IP data at the network layer.
* IPSec is deployed when it comes to the implementation of a VPN.
* Secures IP communication by authenticating the session and encrypts each data packet during the connection.
* It is a common method for creating a virtual, encrypted link over the unsecured Internet.

![](https://www.evernote.com/shard/s342/res/c1f42291-b9af-7d8f-77e3-ccf97fa539c0)  
**IPSec Goals**

* Confidentiality
  * Provided through encryption, changing clear text into cipher text.
* Data Integrity
  * Provided through hashing to verify that data has not been manipulated during its transit across the network.
* Authentication
  * The sender and receiver will authenticate each other to make sure that we are really talking with the device we intended to via PSK or RSA digital certificates.
* Anti-Replay
  * By using sequence numbers, IPSec will not transmit any duplicate packets.

**Internet Key Exchange \(IKE\) Protocol**

* IPSec uses IKE protocol to negotiate and establish secured site-to-site or remote access VPN between two peers.
* There are two versions of IKE:
  * IKEv1 - 1998
  * IKEv2 - 2005
* IKE uses two phases:
  * **IKE Phase 1**
    * Not going to be used to forward user packet but rather only to protect the management traffic.
    * Packets such as keepalive messages are sent across the IKE Phase 1 tunnel between VPN peer devices.
    * The main purpose of IKE Phase 1 is to establish a secure tunnel that we can use for IKE Phase 2.
    * In this phase, an ISAKMP \(Internet Security Association and Key Management Protocol\) session is established.
    * The collection of parameters that the two devices will use is called a Security Association \(SA\).
    * Phase 1 has two modes:
      * Aggressive mode \(3 messages\).
      * Main mode \(6 messages\).
    * Five parameters need to be agreed to between the two VPN devices for the IKE Phase 1 tunnel to succeed.
      * Hashing: MD5 or SHA
      * Encryption: DES, 3DES, or AES.
      * Diffie-Hellman \(DH\) group: Group 1 till 20.
      * Authentication: Pre-shared key or digital certificates.
      * Lifetime: How long does the IKE Phase 1 tunnel stand up? The shorter the lifetime, the more secure it is.
  * **IKE Phase 2**
    * IKE Phase 2 tunnel, also known as the IPSec Tunnel, will be used to protect and send user data.
    * Just like with Phase 1, VPN peer devices will negotiate about a number of parameters.
      * IPSec Protocol: Do we use AH or ESP?
      * Encapsulation Mode: Transport or tunnel mode?
      * Encryption: What encryption algorithm do we use? DES, 3DES, or AES?
      * Authentication: What authentication algorithm do we use? MD5 or SHA?
      * Lifetime: How long is the IKE Phase 2 tunnel valid? When the tunnel is about to expire, we will refresh the keying material.
    * There is only one mode to build the IKE Phase 2 tunnel which is called quick mode.
    * Each IKE Phase has its SAs: ISAKMP SA \(phase 1\) and IPSec SA \(Phase 2\).

![](https://www.evernote.com/shard/s342/res/5affdfe4-aa91-d939-0384-78508e619f6a)  
**IPSec Modes**

* Tunnel Mode
  * IPSec tunnel mode is the default mode in Cisco.
  * The entire original IP packet is protected.
  * The original IP datagram is encapsulated with an AH \(provides no confidentiality by encryption\) or ESP \(provides encryption\) header and an additional IP header.
  * The IP addresses of the newly added outer IP header are that of the VPN Gateways.
  * IPSec Tunnel mode is most widely used to create site-to-site IPSec VPN.
* Transport Mode
  * Only the data payload of the IP datagram is secured by the IPSec.
  * IP header is the original header and IPSec inserts its header between the IP header and the upper level headers.
  * IPSec Transport mode can be used when encrypting traffic between two hosts or between a host and a VPN gateway.
  * The data is encrypted and authenticated if Encapsulating Security Payload \(ESP\) is used, or just authenticated if Authentication Header \(AH\) is used.

![](https://www.evernote.com/shard/s342/res/b70cb49d-bc04-8411-83d6-e1ba216d2c76)  
**IPSec Protocol**

* Authentication Header
  * Provides source authentication and data integrity.
  * Protects against replay attacks and protects against DoS attacks.
  * No protection for confidentiality.

![](https://www.evernote.com/shard/s342/res/8aeaa3b0-5a64-42eb-b13d-34c905ca2115)

* Encapsulation Security Payload
  * Provides all that AH offers but also provides data confidentiality via encryption.
  * Uses symmetric key encryption.

![](https://www.evernote.com/shard/s342/res/df5f2646-8661-4389-59b4-eeb9c725d7bf)  
**Building IPSec VPN**

1. Define interesting traffic that should be protected.
2. Perform IKE Phase 1 - Negotiate the security policy.
3. Perform IKE Phase 2 - Negotiate SA.
4. Transfer Data - Encrypt interesting traffic and send it to peer devices.
5. Tear down the tunnel.

![](https://www.evernote.com/shard/s342/res/712607be-f844-ecd9-7275-02732dd886d7)

**Wireless Network Security** - [https://learn.nexgent.com/modules/cyber-security-specialist-module3/sections/cyber-security-specialist-module3-section3/lessons/cyber-security-module3-wirelessnetwork](https://learn.nexgent.com/modules/cyber-security-specialist-module3/sections/cyber-security-specialist-module3-section3/lessons/cyber-security-module3-wirelessnetwork)

**Wireless Network**

* Wireless networks are computer networks that are not connected by cables of any kind.
* Use radio waves to connect devices to the Internet, the business network, an dapplications.

**802.11 and the OSI Model**  
![](https://www.evernote.com/shard/s342/res/f784aa24-0868-17de-6e29-67c09c0f86d3)  
**Wireless Topologies**

* WPAN \(Wireless Personal Area Network\)
  *  Exists within a relatively small area and connects electronic devices such as computers, printers, scanners, and fax.
* WLAN \(Wireless Local Area Network\)
  * Based on IEEE 802.11 standard and are referred to as "Wi-Fi" networks.
* WMAN \(Wireless Metropolitan Area Network\)
  * Wireless network that covers a large geographic area such as a city or campus.

**Wireless Network Security**

* Primarily protects wireless network from unauthorized and malicious access attempts.
* Following are the wireless security protocols:
  * WEP \(Wired Equivalent Privacy\)
  * WPA \(Wi-Fi Protected Access\)
  * WPA2 "" "" v2.

**WEP**

* Developed for wireless networks and approved as a Wi-Fi security standard in September 1999.
* WEP was supposed to offer the same security level as wired networks.
* Has well-known security flaws, is difficult to configured, and is easily broken.
* Officially abandoned by the Wi-Fi Alliance in 2004.

**WPA**

* Ratified by the WiFi Alliance in 2003 as a response to the insecurities that were discovered in WEO.
* Most modern WPA applications use a pre-shared key \(PSK\), most often referred to as WPA Personal, and the Temporal Key Integrity Protocol \(TKIP\) for encryption.
* WPA Enterprise uses an authentication server for key and certificate generation.

**WPA2**

* Implements AES.
  * Approved by the U.S. government for encrypting information classified as 'top secret'.
* WPA and WPA2 can further be classified as follows:
  * **Personal \(Pre-Shared Key \[PSK\]\)**: A unique key is shared with each client in the network.
    * Users use this key to securely log into the network.
    * The key remains the same until it is changed by authorized personnel.
  * **Enterprise**: More secure than Personal. Every client automatically receives a unique encryption key after securely logging onto the network. This key is automatically updated at regular intervals. WPA uses TKIP and WPA2 uses the AES algorithm.

![](https://www.evernote.com/shard/s342/res/f7102ee6-00e9-3512-ef9f-18474508f822)  
**Common Wireless Attacks**

* Piggybacking - [https://en.wikipedia.org/wiki/Piggybacking\_\(Internet\_access\)](https://en.wikipedia.org/wiki/Piggybacking_%28Internet_access%29)
* Wardriving - [https://en.wikipedia.org/wiki/Wardriving](https://en.wikipedia.org/wiki/Wardriving)
* Wireless Sniffing - [https://en.wikipedia.org/wiki/Sniffing\_attack](https://en.wikipedia.org/wiki/Sniffing_attack)
* Unauthorized Computer Access
* Shoulder Surfing
  * Glancing over your shoulder as you type.
* Theft of Mobile Devices

**Wireless Risk Mitigation**

* Change default passwords.
* Restrict access.
* Encrypt the data on your network.
* Install a firewall.
* Keep access point software up to date.

**Virtualization & Cloud Security** - [https://learn.nexgent.com/modules/cyber-security-specialist-module3/sections/cyber-security-specialist-module3-section4/lessons/cyber-security-specialist-module3-iot](https://learn.nexgent.com/modules/cyber-security-specialist-module3/sections/cyber-security-specialist-module3-section4/lessons/cyber-security-specialist-module3-iot)

**What is IoT?**

* The Internet of Things \(IoT\) is a network of smart devices that connect to each other in order to exchange data via the internet without human intervention.

**The IoT Market Trend**

* The global IoT market is expected to grow to 212 billion USD by the end of 2019.
* Technology reached 100 billion USD in market revenue for the first time in 2017.
* The forecast suggests this figure will grow to around 1.6 trillion by 2025.

**Cybersecurity Challenges with IoT**

* Firmware vulnerabilities.
* Insecure web interface \(this is how users interact with the device\).
* Insufficient authentication.
* Lack of encryption.
* Insufficient security configuration.

**Types of IoT Attacks**

* DoS
  * Denial-of-Sleep as well, keeps it from shutting down and drains the battery to shut down.
* MitM
* Device Spoofing
* Malware \(usually loaded due to lack of software updates\).
* Application-based attacks.
* Physical intrusion.

**Security of IoT Devices**

* Patch and software management.
* Strong authentication.
* Encryption and secure protocols.
* Network segmentation.
* NAC.
* Identity management.
* IoT device data collection.
* Employee training.

