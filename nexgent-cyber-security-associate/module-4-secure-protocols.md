# Module 4 - Secure Protocols

**Protocols Overview**

Secure Applications - [https://learn.nexgent.com/modules/cyber-security-specialist-module4/sections/cyber-security-specialist-module4-section2/lessons/cyber-security-specialist-module4-secureapplications](https://learn.nexgent.com/modules/cyber-security-specialist-module4/sections/cyber-security-specialist-module4-section2/lessons/cyber-security-specialist-module4-secureapplications)

**What is Application Security?**

* The Process of making apps more secure by finding, fixing, and enhancing the security of apps.
* Checking for security flaws in your applications is essential as threats become more potent and prevalent.

**Why is this Important?**

* The faster in the development process you find and fix security issues, the safer your enterprise will be.
* Application security tools that integrate into your development environment make this more effective.
* These tools save time and expense by catching problems earlier.

**Application Security Tools**

* Security Testing Tools
  * Static Testing: Analyzes code at fixed points during development.
  * Dynamic Testing: Analyzes running code.
  * Interactive Testing: Combines elements of both static and dynamic testing.
  * Mobile Testing: Designed for mobile environments and can examine how attackers can leverage mobile OS and the apps running on them.
* Application Shielding Tools
  * RASP: Combination of testing and shielding. Provide a measure of protection against possible reverse-engineering attacks. Continuously monitor the app's behavior.
  * Code Obfuscation: Hackers use obfuscation methods to hide their malware, and now tools allow developers to do the same to protect their code.
  * Encryption / Anti-Tampering: Methods that can be used to keep the bad guys from gaining insights into your code.
  * Threat Detection: Examine the environment or network where your apps are running to make an assessment about potential threats / misused trust relationships.

**Challenges**

* IT has to satisfy several different business lines.
* Keep up with the evolving security and tools market.
* Anticipate business needs as enterprises dive deeper into digital products.
* Application portfolio evolves into more complex infrastructure.
* They also have to udnerstand how the SaaS services are constructed and secured.
* Finally, the responsibility for application security could be spread across several different teams within your IT operations.
* Hard to suggest one tool that will fit everyone's needs \(fragmented market\).

**Application Security Trends**

* While the number of web application vulnerabilities continues to grow, that growth is slowing.
* By far, the two most common types of web application vulnerabilities are injections and cross-site scripting.
* "Pushing left" / "Building Security In"
* Serverless.
* Bug Bounty platforms.

**Best Practices**

* Follow OWASP Top 10.
* Application Security Audit.
* Implement Proper Logging.
* Real Time Security Monitoring.
* Encrypt Everything.
* Harden Everything.
* Keep Servers up to date.
* Stay informed of the latest vulnerabilities.

TCP/IP  - [https://learn.nexgent.com/modules/cyber-security-specialist-module4/sections/cyber-security-specialist-module4-section2/lessons/cyber-security-specialist-module4-tcp](https://learn.nexgent.com/modules/cyber-security-specialist-module4/sections/cyber-security-specialist-module4-section2/lessons/cyber-security-specialist-module4-tcp)

**What is TCP/IP?**

* A suite of communication protocols used to interconnect network devices.
* Creates a connection between devices by transporting and ensuring delivery.
* TCP defines how applications can create channels of communication across a network.
* TCP also manages how a message is assembled into smaller packets before transmission, and then reassembled in the correct order at the destination.
* IP defines how to address/route each packet to make sure it reaches the correct destination.

**How Does it Work?**

* TCP/IP uses a client-server model of communication.
* The suite of protocols is defined as "stateless"
* Functionality divided into 4 layers:
  * 1. Application Layer
    * This layer sends and receives data for particular applications, such as Domain Name System \(DNS\), HypterText Transfer Protocol \(HTTP\), and Simple Mail Transfer Protocol \(SMTP\).
  * 2. Transport Layer
    * This layer provides connection-oriented or connectionless service for transporting application layer services between networks. The transport layer can optionally assure the reliability of communications. Transmission Control Protocol \(TCP\) and User Datagram Protocol \(UDP\) are commonly used transport layer protocols.
  * 3. Internet/Network Layer
    * This layer routes packets across networks. Internet Protocol \(IP\) is the fundamental network layer protocol for TCP/IP. Other commonly used prtocols at the network layer are Internet Control Message Protocol \(ICMP\) and Internet Group Management Protocol \(IGMP\).
  * 4. Physical Layer / Data Link Layer
    * This layer handles communications on the physical network components. The best-known data link layer protocol is Ethernet.

**Why is it Important?**

* The entire internet runs on this.
* Compatible with all operating systems, so it can communicate with any other system.
* The internet protocol suite is also compatible with all types of computer hardware and networks.

**Vulnerabilities**

* Common set of protocols leave them open to exploitation and attack.
  * IP/Source Routing
    * TCP and IP are separate protocols.
    * IP allows information streams to be broken up into smaller segments via IPv4/v6.
    * When information is broken up into packets, IP source generates a listing of the routes that packets must take to reach destination.
      * This listing can then be used by the recipient to send information back to the original sender.
    * At this stage, attackers can also gain access to the source path and modify the options in the route for the data packet.
      * May also read data packets.
    * This risk can be minimized by dropping/forwarding data packets which carry the source route options.
  * TCP/Reassembly
    * Predicting TCP Sequence
      * Attackers can guess the sequence of numbers that TCP assigns to a stream of data packets.
      * By knowing the next number in a transmission sequence, attackers can do a MitM attack.
  * TCP Blind Spoofing
    * Attacker guesses both the sequence number of an ongoing communication session and its port number.
    * They can then carry out an injection attack where they insert corrupted/spoofed data into the data stream.
  * SYN Flooding / Denial of Service
    * Protocol specifies that a client or server received SYN/ACK requests is required to respond to them.
    * Attackers misuse this rule by sending multiple SYN packets from a spoofed sourced address.
    * Server then sends out SYN-ACK packets to an address that does not exist.
      * This creates a backlog of half-opened sessions awaiting for replies that will never come.
      * No further fresh connections will be allowed by the server, and all requests from legitimate sources will be ignored.
  * Session Hijacking
    * Attacker captures data from packet sniffing to access an HTTP session.
    * Weak authentication between web server and clients allows control to be taken.
  * MitM
    * In unsecured sessions, data passes between sender and receiver in clear text.
    * Attacker spoofs IP address, and intercepts ongoing transmission as a man in the middle.
    * Steals valuable data & spreads misinformation towards recipients.

**Securing TCP/IP**

1. Encryption
2. Integrity
3. Authentication
4. Authorization

TLS  - [https://learn.nexgent.com/modules/cyber-security-specialist-module4/sections/cyber-security-specialist-module4-section2/lessons/cyber-security-specialist-module4-tls](https://learn.nexgent.com/modules/cyber-security-specialist-module4/sections/cyber-security-specialist-module4-section2/lessons/cyber-security-specialist-module4-tls)

**What is TLS?**

* A protocol that provides authentication, privacy, and data integrity between two devices.
* Most widely deployed security protocol used today.
* TLS is critical to securely exchange data over a network. 
  * Browsing Sessions
  * VPN Connections
  * Remote Desktops
  * VoIP
* Evolved from SSL, terms used interchangeably. TLS is far more secure and efficient. 
* Works predominantly with HTTPS but also used to secure email. 

**What Does TLS Do?**

* Solves 3 major security problems: 
  * How can we know whether the person we are talking to is really who they say they are? 
  * How can we know the data has not been tampered with? 
  * How can we prevent other people from viewing/accessing the data? 

**How Does TLS Work?**

* Handshake - This protocol is used to set up the parameters for a secure connection. 
* Application - The application protocol begins after the handshake process, and it is where data is securely transmitted between the two parties. 
* Alert - The alert protocol is used by either party in a connection to notify the other if there are any errors, stability issues, or a potential compromise. 
* Change Cipher Spec - This protocol is used by either the client or the server to modify the encryption parameters. 
* Heartbeat - This is a TLS extension that lets one side of the connection know whether its peer is still alive, and prevents firewalls from closing inactive connections. It's not a core part of TLS, so we'll be skipping it in this guide. 

![](https://www.evernote.com/shard/s342/res/c71e9ec9-c248-f4ba-fef8-aa5b86b64a43)  
**Handshakes - 3 Types**

* Basic
  * Only the server is authenticated, not the client.
* Client-Authenticated
  * The client is authenticated as well. 
  * After the server sends its certificate method, it also sends a certificate request to authenticate the client.
* Abbreviated
  * Once a handshake has already taken place, such as with a known client. 
  * Uses session ID to connect to previous parameters. 
  * Saves time and is faster.

**Handshake Breakdown: \(**[**https://www.youtube.com/watch?v=cuR05y\_2Gxc**](https://www.youtube.com/watch?v=cuR05y_2Gxc)**\)**

* Client sends the server a hello, which establishes which type of TLS and protocols will be used. The server decides on which will be used. -&gt;
* Server sends the client a hello back to the client as well as a certificate. In the cert is the public key for the server. Lastly, the server sends a Hello Done \(or finalization msg\). &lt;- &lt;- &lt;-
* Client generates a pre-master secret and sends it to the server based on the server's public key via a key-exchange msg. -&gt;
  * Server receives pre-master secret and decrypts it. 
  * Client and server now have a symmetric key based on the pre-master secret. 
* Client sends a client finished msg to server. -&gt;
* Server sends a Change Cipher Spec msg to the client. &lt;-
* Server sends a finished msg to the client. &lt;-
* &lt; - &gt; encrypted data connection.

![](https://www.evernote.com/shard/s342/res/79e6b39f-adb2-0c62-ad19-f84d7cca5383)  
**Why is it Important?**

* TLS is used to secure a large proportion of our online communications. 
* Implemented over TCP but can also be used for UDP. 
* Secures protocols such as HTTP, SMTP, FTP. 
* Used to build VPNs.

**Vulnerabilities**

* Past versions have had issues but the latest versions are considered secure \(TLS 1.2 to 1.3\).
* Renegotiation Attacks
  * TLS allows client and server to negotiate the parameters of an existing connection. 
  * Attackers can inject traffic to make it seem like it comes from a legitimate source. 
  * Attackers would not be able to read responses but can manipulate transmission. 
  * A fix for this has been proposed for the protocol. 

![](https://www.evernote.com/shard/s342/res/76b1b7fe-f027-6b09-73c5-813fd03b3ef3)

* Timing Attacks
  * Side channel attacks analyze how long it takes for an algorithm to run. 
  * That information is then used to work backwards and figure out the key. 
  * Paired with another attack to be more effective. 

![](https://www.evernote.com/shard/s342/res/9fd4e8fa-367c-6f66-3a3d-e091adab9f09)

* Downgrade Attacks
  * Trick servers into using earlier and less secure versions of TLS. 
  * Attackers use this to renegotiate the use of less secure key exchanges and ciphers. 
  * Attackers then break the key exchange mechanism and extract the keys, which allows them control of the session.

![](https://www.evernote.com/shard/s342/res/79d6e89e-2c7d-e41d-0186-fb5e6c86edee)

* Heartbleed
  * Security flaw that was introduced into OpenSSL's crypto library in 2012, but discovered in 2014. 
  * Significant global damage, due tot he popularity of OpenSSL. 
  * Buffer over-read vulnerability was introduced accidentally. 
  * This allowed extra data to be exposed. 

![](https://www.evernote.com/shard/s342/res/079dbd46-f922-c882-03d1-1d65a118bd6c)  
**Proper Use**

* While secure, configuration is key when using TLS. 
* Badly configured servers may expose data vs securing it. 
* Best way to defend against TLS attacks is to disable older protocol versions.
* Be vigilant about updates and keep an ear out about attacks.

**Protocols Applied**

**Protecting Servers**  - [https://learn.nexgent.com/modules/cyber-security-specialist-module4/sections/cyber-security-specialist-module4-section3/lessons/cyber-security-specialist-module4-protectingservers](https://learn.nexgent.com/modules/cyber-security-specialist-module4/sections/cyber-security-specialist-module4-section3/lessons/cyber-security-specialist-module4-protectingservers)

**Server Security Importance**

* Hackers are always on the lookout for server vulnerabilities. 
* 2005 had 16% of the world's population online. That number is closer to 47% now. 
* Server security is important for any organization that has a physical or virtual web server connected to the internet. 
* What makes this difficult is that they have to be accessed by outside entities and still maintain security. 
* Attacks have large financial impacts. 

**Web Server Security**

* A web server is a program that stores the content which are available for the public: 
  * Product Info
  * Pricing
  * Tech Support
  * Etc.
* Contents of the websites are stored as various files: 
  * HTML
  * ASP
  * XML
  * CSS
  * JavaScript
  * Graphics
  * etc.
* Also contain confidential business data.

**Web Server Attacks**

* Directory Traversal Attacks - Exploits bugs in the web server to gain unauthorized access to files and folders that are not in the public domain.
* Denial of Service Attacks - Web server may crash or become unavailable to the legitimate users. 
* Domain Name System Hijacking - DNS settings are changed to point to the attacker's web server. 
* Sniffing - Unencrypted data sent over the network may be intercepted and used to gain unauthorized access to the web server. 
* Phishing - Attacker impersonates the websites and directs traffic to the fake website. 
* Pharming - Compromises the DNS servers or on the user computer so that traffic is directed to a malicious site. 
* Defacement - Replaces the organization's website with a different page that contains the hacker's name, images, and may include background music and messages. 

**Web Server Vulnerabilities**

* Establish and Use a Secure Connection
  * Essential to provide a secure channel for communication such as SSH \(**port 22 by default, best practice is to change to a higher port, security through obscurity \(1024-32766**\). 
* SSH Keys for Authentication
  * Use SSH keys vs passwords, carry more bits and are uncrackable by most modern computers. 
* Secure FTP
  * Encrypts data files and authentication information. 
* Private Networks/VPNs
  * Ensures secure communication, unlike open networks which are accessible to the outside world. 

**Securing Web Server Vulnerabilities**

* Monitor Login Attempts
  * Intrusion prevention software to monitor login attempts / prevent brute force attacks. 
* Manage Users
  * Create limited user accounts and proper access control lists. 
* Password Management
  * Requirements and expiration policies.
  * No empty or default passwords. 
  * Enforce length and complexity. 
  * Enable 2FA.
* Update Software Regularly
  * Crucial step. Outdated software has already been explored for weak points and leaves it open for hackers to take advantage of. 
* Remove Unnecessary Services
  * Reduces the surface area of attack vectors. 
* Hide Server Info
  * The less info about the infrastructure, the better. 
  * Hide version numbers too!
* IDS Systems
  * Detect unauthorized activities. 
* Auditing
  * Discover unwanted changes on systems. 
* Maintain Firewall
  * Secure the server by controlling and restricting access to your system. 
* Regular Backups
  * Store encrypted backups of your critical data offsite or use a cloud solution.
* Create Multi-Server Environments
  * Eggs in different baskets. 
* Create Virtual Isolated Environments
  * Isolate execution environments/containers or VM virtualization. 

**Server Room Security**

* What is a Server Room?
  * The heart of a data center facility. 
  * Security breaches of ANY kind can result in damage to business, or killing business all together. 
* How do you keep it secure?
  * Map vulnerabilities.
  * Lock the doors.
  * Security cameras.
  * Motion sensors.
  * Secure cabinet racks.

**Secure Software Design Lifecycle**  - [https://learn.nexgent.com/modules/cyber-security-specialist-module4/sections/cyber-security-specialist-module4-section3/lessons/cyber-security-specialist-module4-securesdlc](https://learn.nexgent.com/modules/cyber-security-specialist-module4/sections/cyber-security-specialist-module4-section3/lessons/cyber-security-specialist-module4-securesdlc)

**What is SDLC?**

* Framework that defines the process used by organizations to build an application from its inception to continuous versions. 
* Process that produces the highest quality and lowest cost in the shortest time. 
* Starts by evaluating existing systems for deficiencies. 
* Defines the requirements of the new system.
* Then creates the software through the stages of design, development, testing, and deployment. 

**How does Secure SDLC Work?**

* Secure SDLC is set up by adding security related objectives to an existing development process. 
  * Write security requirements along the collection of functional requirements. 
  * Perform an architecture risk analysis during the design phase. 

**Secure SDLC Phases**

* Security Training - Small security team, doesn't scale. Level everyone else up.
  * Security 101
  * Common Issues
  * Indicators
* Start with new hires, repeat process annually \(stay up to date\). 
* Knowledge sharing. 
* Change mindset. 
* Set culture.
* Architecture Review - Start as early as possible, toughest flaws to change later on. 
  * Profiling the technology. 
  * Analyzing the attack surface. 
* Ensure it's not vulnerable by design \(foundation not being secure\). 
* Most vulnerabilities are introduced during the design phase by accident. 
  * Such as adding a feature but not understanding the ramifications. 
* "Secure by default."
* Security Requirements - Checklist meant to enforce best practices. 
  * Tailored specifically for your technology stack. 
* Typically enforced after the architecture review is done.
* Language, system, and feature specific. 
* Checklists translate well into actionable items such as tickets. 
  * Add them into sprints as you are building vs at the end. 
  * Complete while building. 
* Threat Modeling - Understand the attacker's perspective. 
  * Mapping assets. 
  * Understand what protections are in place for those assets. 
  * Different threats that would try and attack them. 
  * Understanding threat vectors. 
* Start this process after the architecture is confirmed. 
* Helps lock down easy attack paths. 

![](https://www.evernote.com/shard/s342/res/b18fe32f-c1d2-c652-b0db-bbfff638e1c7)

* Static Code Analysis - Start scanning code for obvious issues. **\*coverity\***
  * Input validation. 
  * Search field. 
* Start this as soon as code is starting to be pushed into the builds. 
* Automate this process so that it lowers the barrier and constantly checks against revisions. 
* Helps catch issues as soon as they are committed. 
* Open Source Analysis - Product is only as secure as the weakest links. 
  * Dependencies are often overlooked. 
  * Older libraries are not patched. 
    * This can cause security problems. 
* Forces you to update to known safe versions. 
* Automated process that's done as the code is being checked. 
* Helps avoid or introduce critical vulnerabilities that are introduced indirectly. 
* Dynamic Testing - Catching run-time bugs \(vs static, where it was just the code\).
  * Automated testing. 
  * Black box approach.
    * Means you don't need to understand the internal working, you're evaluating the output. 
* Start testing once you have a stable product. 
* Usually done in the staging environment. 
* Done for Quality Assurance, finds real time issues.
* Penetration Testing - Hacking your own products like an attacker would. 
* Done before product is released publicly. 
* Can be done either in staging environment or once product is pushed to production. 
* Finds the issues before the public does.  
* Should not be a high amount of results if previous steps were done properly.
* Will need multiple iterations to fine tune: 
  * Security training. 
  * Architecture review.
  * Security requirements. 
  * Threat modeling.
  * Static code analysis. 
  * Open source analysis. 
  * Dynamic Testing.
  * Penetration testing. 

![](https://www.evernote.com/shard/s342/res/e7b581d3-7d7c-740f-cb33-a22f3707fa19)

**Heartbleed Case Study** - [https://learn.nexgent.com/modules/cyber-security-specialist-module4/sections/cyber-security-specialist-module4-section4/lessons/cyber-security-specialist-module4-heartbleed](https://learn.nexgent.com/modules/cyber-security-specialist-module4/sections/cyber-security-specialist-module4-section4/lessons/cyber-security-specialist-module4-heartbleed)

**Case Study: Heartbleed**

* What is it?
  * Vulnerability in OpenSSL
* What did it do?
  * Allowed attackers to "over read" and circumvent security measures to gain information on confidential information. Allowed them to see data they were not supposed to. Exploited the "heartbeat" feature that was meant to keep a TLS connection alive. 
* How did they use it?
  * Crafted special requests that allowed attackers to receive more information than they requested. 
* How was it fixed?
  * Patch was released but not until 2 years after the bug was first implemented.
* Who did it?
  * A developer who wanted to add a new feature forgot to validate the variable containing the length in the request. The peer reviewer also missed the bug. 

Essentially, the bug was that you could send a payload of 1 byte but say it was 65,000 bytes, the server would send back 65,000 bytes. You could basically read the entire database this way. 

**Equifax Data Breach** - [https://learn.nexgent.com/modules/cyber-security-specialist-module4/sections/cyber-security-specialist-module4-section4/lessons/cyber-security-specialist-module4-equifax](https://learn.nexgent.com/modules/cyber-security-specialist-module4/sections/cyber-security-specialist-module4-section4/lessons/cyber-security-specialist-module4-equifax)

**Case Study: Equifax Data Breach**

* What is it? 
  * Consumer credit reporting agency that had a data breach of ~143 million Americans.
  * Potentially setting them all up for identity theft at any point in the future. 
* What did it do?
  * Hackers seized names, social security numbers, birthdates, addresses, and drivers license info. 
* How did they use it?
  * Equifax failed to update a software library. 
  * US-CERT had issued a warning for Apache Struts but company took no action. 
* How was it fixed?
  * Patch was used to update it. 
* Who did it?
  * Prevailing theory that it was initially started by a low-level criminal, but due to complexity, sought help from another source \(most likely a proxy for a nation state\). 

