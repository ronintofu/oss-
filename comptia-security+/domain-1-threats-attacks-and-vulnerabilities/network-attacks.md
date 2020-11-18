# Network Attacks

**Hija@cking and Related Attacks**

* Clickjacking - tricking a web user into clicking a spoofed button or graphic.
* Session Hijacking \(Cookie Hijacking\) - exploiting a valid computer session, or session key, to gain unauthorized access to information or services.
* URL Hijacking / Typo Squatting - the act of registering domains that are similar to those for a known entity but based on a misspelling or typographical error.
* MAC Spoofing - The MAC address is hard-coded onto a NIC number. Many drivers allow the MAC address to be changed. A technique for changing a factory-assigned MAC address of a network interface on a networked device.

![](../../.gitbook/assets/image%20%2823%29.png)

* **IP Spoofing** - A technique used to gain unauthorized access to machines, whereby an attacker illicitly impersonates another machine by manipulating IP packets. IP Spoofing involves modifying the packet header with a forged \(spoofed\) source IP address, a checksum, and the order value.

![](../../.gitbook/assets/image%20%2819%29.png)

* **ARP Spoofing** - When an attacker sends fake ARP messages over a local area network. This results in the linking of an attacker's MAC address with the IP address of a legitimate computer or server on the network.

![](../../.gitbook/assets/image%20%2821%29.png)

* **Man-in-the-Middle Attack**
  * The attacker secretly relays and possibly alters the communication between two parties who believe they are directly communicating with each other.
  * The attacker may either observe \(confidentially attack\) or alter \(integrity attack\).
* **Denial of Service Attacks \(DoS\)**
  * Preventing access to resources by users authorized to use those resources. Attacking systems availability.
  * May accomplish:
    * Deny access to information, applications, systems, or communications.
    * Bring down a website while the communications and systems continue to operate.
    * Crash the operating system \(a simple reboot may restore the server to normal operation\).
    * Fill the communications channel of a network and prevent access by authorized users.
* **Distributed Denial of Service \(DDoS\) Attacks**
  * A DoS attack utilizing multiple compromised computer systems as sources of attack traffic.
  * Amplifies the concepts of a DoS attack by using multiple computer systems \(often through botnets\) to conduct the attack against a single organization.
* **DoS & DDoS Prevention**
  * Work with your ISP / network provider.
  * Border protections / IDS / IPS.
  * Update network appliances, OS, and applications.
  * End users' systems are UTD and deploy AV - bot protection.
* **Amplification Attacks**
  * The goal of the attacker is to get a response to their request in a greater than 1:1 ratio so that the additional bandwidth traffic works to congest and slow the responding server down.
  * The ratio achieved is known as the amplification factor, and high numbers are possible with UDP based protocols such as NTP, CharGen, and DNS.
  * Usually employed as part of a DDoS attack.
* **Domain Hijacking / DNS Poisoning / DNS Spoofing**
  * AKA Resolution Attacks
  * Poisoning: When an attacker alters the domain-name-to-IP-address mappings in a DNS system to redirect traffic to a rogue system or perform a DoS attack.
  * Spoofing: When an attacker sends false replies to a requesting system in place of a valid DNS response.
  * **Prevention**
    * Protect any internal DNS servers.
    * Use authoritative DNS sources.
* **Wireless Attacks**
  * Evil Twin - A Rogue wireless access point poses as a legitimate wireless service provider to intercept information that users transmit.
  * Rogue AP - Any wireless access point added to your network that has not been authorized.
  * Initialization Vector \(IV\) - An arbitrary number than can be used along with a secret key for data encryption. This number, also called a nonce, is employed only one time in any session. If the IV is weak, as in WEP, it may be reused.
  * Jamming- Causing interference with a wireless signal.
* **PAN Wireless Attacks**
  * Bluejacking - The sending of unsolicited messages, such as spam, over a Bluetooth connection.
  * Bluesnarfing
    * The gaining of unauthorized access through a Bluetooth connection.
    * Intercepting data through a Bluetooth connection.

