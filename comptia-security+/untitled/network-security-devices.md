# Network Security Devices

**Firewalls**

* Isolate one network from another.
* A network security device that monitors incoming and outgoing network traffic and decides whether to allow or block specific traffic based on a defined set of security rules \(CISCO\).
* Hardware \(appliances\), software, or both.
* Network or host-based.

**Firewall Types**

* Packet filter.
  * Passes or blocks traffic to specific ports or IP addresses based on rules.
  * Access Control List \(ACL\) filter.
  * Little intelligence / stateless.
  * Faster than stateful inspection.
* Proxy firewall.
  * Acts an an intermediary.
  * Application proxy.
  * Web proxy.
* Stateful packet inspection.

**Stateful Inspection Firewalls**

* Intelligent.
* Analyzes data flows and traffic patterns.
* Dynamic access control decisions.
* Records are kept using a state table that tracks every communications channel;
  * Remembers where the packet came from and where the next one should come from.

**Firewall Rules**

* Configured to specify computers, programs, services, or ports/protocols.
* Order of firewall rules matters.
* Implicit Deny
  * Access or resource availability is restricted to only those that are explicitly granted access; all others are denied.
  * 'Deny any any' \(last firewall or ACL rule\).
* Explicit Deny - denied permission that is configured explicitly for that resource.
* Implicit Allow - an allowed permission that is implied for that resource based on another explicit or implicit permission.
* Explicit Allow - an allowed permission that is configured explicitly for that resource.

**Application Firewalls**

* Controls input, output, and/or access from, to, or by an application or service based on categories, rules, or heuristics.
* Deep packet inspection.
* Function at Layer 7 of the OSI model.
* Web Application Firewall \(WAF\)
  * Protects web applications from known attacks \(injection, buffer overflows, etc\)
* Often included in other firewall types \(Proxy, IDS/IPS\).

**IDS/IPS**

* Intrusion - any activity or action that attempts to undermine or compromise the confidentiality, integrity, or availability of resources.
* Intrusion Detection/Protection Systems
* Like a burglar alarm - identify unauthorized activity, access, or anomalies.
* Sensor - the IDS component that collects data from the data source and passes it to the analyzer.
* Host-based \(HIDS/HIPS\)- on individual systems.
* Network-based \(NIDS/NIPS\) - on the network borders.

**IDS vs IPS - Detection vs Prevention**

* IDS - Passive response
  * Logging
  * Notification
  * Shunning / Quarantine
* IPS - Active Response
  * Terminating process or sessions.
  * Configuration changes.
  * Deception Active Response - Attacker believes the attack is succeeding while the system monitors the activity and potentially redirects the attacker to a honeypot or logging system.

**IDS / IPS Types**

* Signature Based \(AKA Knowledge Based\)
  * Detects known vulnerabilities.
  * Rules/updates provided by vendor.
  * Reactive
* Behavior Based
  * Outside of normal bounds or established profile.
  * Anomaly based.
  * Potential for false positives.
* Heuristic Based
  * Uses algorithms to analyze the activity / network traffic.
  * High initial overhead.

**IDS / IPS Analytics**

* False Positive - Occurs when a typical or expected behavior is identified as irregular or malicious.
* False Negative - Occurs when an alert that should have been generated did not happen.

**NIDS / NIPS**

* Network Intrusion Detection / Protection Systems
* Analysis used to be separate, now combined with firewalls.
* Passive - traffic is mirrored to sensor.
* Inline - with traffic flows and prevents attacks in real time. Could cause latency.

**VPN Concentrators**

* A VPN allows remote access into a network.
  * site-to-site
  * user \(host-to-site\)
* VPN Concentrator
  * Single device to funnel all VPN access / connects VPN nodes.
  * Encrypted tunnels.
  * Centralized authentication \(RADIUS, Kerberos, Federated ID\)
* Always-on VPN
* Network security through encryption.
  * Internet Protocol Security \(IPSec\)
  * Secure Sockets Layer \(SSL\)
* Cannot be placed wherever they are needed.
  * Should be placed in the perimeter network near the gateway. 

**Internet Protocol Security \(IPSec\)**  
\[[https://www.geeksforgeeks.org/types-of-virtual-private-network-vpn-and-its-protocols/](https://www.geeksforgeeks.org/types-of-virtual-private-network-vpn-and-its-protocols/)\]  
\[[https://www.geeksforgeeks.org/ip-security-ipsec/](https://www.geeksforgeeks.org/ip-security-ipsec/)\]

* Provides authentication services and encapsulation of data through support of the Internet Key Exchange \(IKE\) protocol.
* Functions within the IP/Network Layer \(Layer 3\).
* Three services:
  * Data verification.
  * Data tampering protection.
  * Private transactions.
* Two separate \(mutually exclusive\) protocols\):
  * Authentication Header \(AH\) - authentication and integrity checking for data packets.
  * Encapsulating Security Payload \(ESP\) - encryption services.
* Transport Mode: works to encrypt the message in the data packet. 
  * Used mostly in host-to-host communications. 
* Tunneling Mode: works to encrypt the entire data packet, not just the message within the packet \(transport\). 
  * Used mostly between gateways \(Cisco routers or ASA firewalls\) or at end-station to a gateway, the gateway acting as a proxy for the hosts behind it. 
  * [http://www.firewall.cx/networking-topics/protocols/870-ipsec-modes.html\#:~:text=Tunnel%20mode%20is%20most%20commonly,for%20the%20hosts%20behind%20it.&text=Another%20example%20of%20tunnel%20mode,e.g%20ASA5510%20or%20PIX%20Firewall\).](http://www.firewall.cx/networking-topics/protocols/870-ipsec-modes.html#:~:text=Tunnel%20mode%20is%20most%20commonly,for%20the%20hosts%20behind%20it.&text=Another%20example%20of%20tunnel%20mode,e.g%20ASA5510%20or%20PIX%20Firewall%29.) 

**SSL / TLS VPN**

* SSL \(Secure Sockets Layer\)
* TLS \(Transport Layer Security\)
  * Replaces SSL
* Known as a WebVPN - remote access through a website over SSL/TLS.
* Point-to-point encrypted communications.

**VPN Tunneling**

* Full Tunnel - all requests are routed and encrypted through the VPN. More secure.
* Split Tunnel - only some \(usually incoming requests\) are routed and encrypted over the VPN.

**Unified Threat management \(UTM\) & Next Generation Firewall \(NGFW\)**

* An all-in-one firewall appliance / single interface / single vendor.
* Network IDS/IPS.
* URL filtering.
  * Block websites based on category or URL.
* Content inspection.
  * Application aware.
* Malware inspection.

**Network Access Control \(NAC\)**

* Uses a set of protocols to define and implement a policy that describes how to secure access to network nodes by devices upon initial access \(an IEEE 802.1X Standard\)
* Components:
  * Access Requestor \(AR\): The device that requests access. Assessment of the device can be self-performed or delegated to another system.
  * Policy Decision Point \(PDP\): The system that assigns a policy based on the assessment. The PDP determines access.
  * Policy Enforcement Point \(PEP\): The device that enforces the policy. This device can be a switch, firewall, or router.
* Agent vs Agentless
  * Is an agent application on the end-point?
  * Yes, for corporate -devices.
* Host Health Checks
  * "Health" of the end-point.
  * Is AV enabled?
* Dissolvable vs Permanent

**Security Information and Event Management \(SIEM\)**

* SIEM tools collect, correlate, and display data feeds that support response activities.
* Functions:
  * Log aggregation on a centralized server.
  * Centrally managing security events.
  * Correlating and normalizing events for context and alerting.
  * Reporting on data gatehred from various applications.
* Benefits:
  * Aggregation
  * Correlation
  * Automated Alerting & Triggers
  * Event Deduplication
  * Time Synchronization
  * WORM - "Write-Once, Read-Many" protection.

**Data Loss Prevention \(DLP\)**

* AKA Data Leakage Protection
* Prevent sensitive information from physically or logically leaving corporate systems.
* Designed to detect and prevent unauthorized use and transmission of confidential information.
* Network: Content-filtering \(proxy\).
* System: Application white-listing.
* Hardware: USB Blocking.
* Cloud data.

**SSL / TLS Accelerators**

* SSL Offloading - the process of shifting the burden of encrypting and decrypting traffic sent via SSL from the web server to another device.
* Accepts SSL/TLS connections from the end-point and sends the connection to the server unencrypted.
* Associated with load balancers.

**Gateways \(Mail & Media\)**

* Centralization and Routing
* Encryption
* Spam Filters
  * Inbound
  * Outbound
* Proxy Servers \(media\)

**Hardware Security Module \(HSM\)**

* Hardware-based encryption that manages digital keys, accelerates cryptographic processes, and provides strong access authentication.
* Trusted Platform Module \(TPM\) used to assist with cryptographic key generation.



