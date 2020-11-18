# Module 6 - Tools

**PREVENTATIVE TOOLS**

**Why are preventive tools important?**

* Defense in Depth \(DiD\) \(the "castle approach"\)
  * Approach in cybersecurity in which a series of defensive mechanisms are layered in order to protect valuable data and information. 

**Intrusion Detection System**

* A system that monitors network traffic for suspicious activity and issues alerts when such activity is discovered. 
* Software application that scans a network or a system for harmful activity or policy breaching. 
* Violations are reported to an administrator or collected centrally using a SIEM \(Security Information and Event Management\) system. 
* You need to set a base line so you understand what is suspicious or abnormal in the system. 
* 2 main types of IDS: 
  * Network Intrusion Detection Systems \(NIDS\)
    * Set up at a fixed point within the network to examine traffic from all devices on the network. 
    * Does not monitor encrypted information, such as info that goes through a VPN. 
  * Host Intrusion Detection Systems \(HIDS\)
    * Monitor incoming and outgoing packet the device only and will alert the administrator if suspicious malicious activity is detected. 
* 2 types of detection: 
  * Signature Based Method
    * Detect attacks based on specific patterns such as network traffic / number of bytes / known previous attacks. 
  * Anomaly Based Method
    * Systems use machine learning to create a model of trustful activity and compare the current activity with it. 

![](https://www.evernote.com/shard/s342/res/5437b780-804e-a0fb-c87e-8665f2348faa)  
**Intrusion Prevention Systems \(IPS\)**

* Function by finding malicious activity, recording / reporting information about it, and trying to block or stop the activity from occurring. 
* Intrusion prevention systems expand on the capabilities of IDS, which serve the fundamental purpose of monitoring network / system traffic. 
* 2 predominant methods, similar to IDS \(signature and anomaly\). 
* 4 types of IPS:
  * Network Based Intrusion Prevention System \(NIPS\) 
    * Monitors the entire network.
  * Wireless Intrusion Prevention System \(WIPS\)
    * Only reviews wireless networks. 
  * Network Behavior Analysis \(NBA\)
    * Focuses on unusual traffic flows.
  * Host Based Intrusion Prevention \(HIPS\)
    * Works on a single host.

![](https://www.evernote.com/shard/s342/res/a5f0d967-110d-14ed-801b-472fda1b41ff)  
**Anti-Malware**

* Software program designed to prevent, detect, and remove malicious software. 
* 3 strategies to protect systems: 
  * Signature Based Malware Detection - an anti-**malware** approach that identifies the presence of a **malware** infection or instance by matching at least one byte code pattern of the software in question with the database of **signatures** of known malicious programs, also known as blacklists.
  * Behavior Based Detection - evaluates an object **based** on its intended actions before it can actually execute that **behavior**. An object's **behavior**, or in some cases its potential **behavior**, is analyzed for suspicious activities.
  * Sand Boxing - a software management strategy that isolates applications from critical system resources and other programs. It provides an extra layer of security that prevents malware or harmful applications from negatively affecting your system.
* Helps stop attacks by providing real-time protection against the installation of malware and by scanning all incoming network data. 
* Need to use anti-malware products that are updated regularly to combat the latest threats and safely remove them from systems/networks. 

**Mobile Device Management**

* Software that allows admins to control, secure, and enforce policies on smartphones, tablets, and other endpoints. 
* Relies on endpoint software called an MDM agent and an MDM server that lives in a data center or cloud. 
* Features Include:
  * Device inventory and tracking
  * App distribution & enterprise app store
  * Remote wipe
  * Password enforcement
  * App whitelisting and blacklisting
  * Data encryption enforcement

**Network Access Control \(NAC\)**

* A security solution that controls access to your network. 
* Supports network visibility and access management via policy enforcement on devices and users of networks. 
* **Identify** - Allows you to identify who, what, where, when, and how an end-user or device is accessing your network. 
* **Assign** - Assign the correct corresponding role for that user/device or group of users/devices. 
* **Enforce** - Provide the correct user or device with the access it needs, no matter who, what, where, when, and how. 

**Next Generation Firewalls**

* "Deep-packet inspection firewall that moves beyond port/protocol inspection and blocking to add application-level inspection, intrusion prevention, and bringing intelligence from outside the firewall."
* The most obvious difference from traditional firewalls is the ability to filter packets based on applications. 
* Admins can create very granular "allow/deny" rules for controlling use of websites and applications in the network. 
* Are the most detrimental to network perform

**Security Awareness**

* Security awareness training helps prevent breaches. 
* Technological defenses require input from people. 
* The absence of security awareness training in one organization makes other organizations vulnerable. 
  * It's like leaving your house door unlocked with the keys for your car also waiting inside. 
* Security awareness training doesn't just keep people safe at work, but in their personal life too. 

**VULNERABILITY MANAGEMENT & SCANNING**

**What is Vulnerability Management & Scanning?**

* The process of identifying, evaluating, treating, and reporting security vulnerabilities in systems and software. 
* This process needs to be performed continuously in order to keep up with changes that are made to systems and the discover of new vulnerabilities over time. 

**Identifying Vulnerabilities**

* Scan typically consists of 4 stages: 
  * Scan network-accessible systems by pinging them or sending them TCP/UDP packets. 
  * Identify open ports and services running on scanned systems. 
  * If possible, remotely log in to systems to gather detailed system information. 
  * Correlate system information with known vulnerabilities. 
* Use a vulnerability database with a list of publicly known vulnerabilities. 
* Can sometimes disrupt the networks & systems they scan due to bandwidth issues. 
  * Should be scheduled to run off hours if this happens. 

**Evaluating Vulnerabilities**

* After vulnerabilities are identified, they need to be evaluated. 
  * Risks posed by them are dealt with appropriately and in accordance with an organization's risk management strategy. 
* Vulnerability management solutions will provide different risk ratings and scores for vulnerabilities.
  * Common Vulnerability Scoring System \(CVSS\) scores. 
* Results tend to have false positives, processes would need fine tuning to tailor. 

**Mitigating Vulnerabilities**

* Process of prioritizing how to treat the vulnerability with the original stakeholders to the business or network. 
  * Remediation: fully fixing or patching a vulnerability so it can't be exploited. 
  * Mitigation: lessening the likelihood and/or impact of a vulnerability being exploited. 
  * Acceptance: taking no action to fix or otherwise lessen the likelihood/impact of a vulnerability being exploited. 
* After remediation activities are completed, it's best to run another vulnerability scan to confirm that the vulnerability has been fully resolved. 

**Reporting Vulnerabilities**

* Performing regular and continuous vulnerability assessments is beneficial.
  * This enables organizations to understand the speed/efficiency of their vulnerability management program over time. 
* Solutions typically have different options for exporting and visualizing vulnerability scan data. 
  * Variety of customizable reports and dashboards. 
* **IT teams can easily understand which remediation techniques will help them fix the most vulnerabilities with the least amount of time and money.** 
* Help security teams monitor vulnerability trends over time in different parts of their network. 
  * Also helps support organizations' compliance and regulatory requirements. 

**PENTESTING TOOLS & TECHNIQUES**

**What is Pentesting?**

* A simulated cyber attack where professional ethical hackers break into corporate networks to find weaknesses. 
* The goal is to identify weaknesses before others do. 

![](https://www.evernote.com/shard/s342/res/58ee416e-fb87-a71f-0c67-745757a2e6b3)  
**Why is Pentesting Important?**

* Security should be a multi-layered approach. 
* A pentest attempts to break a security system. 
  * **If a system has sufficient defenses, alarms will be triggered during the test.** 
  * **If not, the system is considered compromised.** 
* Once a test is complete, the security teams need to perform a detailed triage to eliminate vulnerabilities. 
* Typically, penetration testers are external contractors hired by organizations. 
  * Many organizations also offer bounty programs. 
* Helps Identify:
  * **Security vulnerabilities before a hacker does.** 
  * **Gaps in security compliance.** 
  * **The response time of an organization's security team.** 
    * How long it takes the team to realize that there is a breach and mitigate the impact. 
  * **The potential real-world effect of a data breach or cybersecurity attack.** 
  * **Actionable remediation guidance.** 

**Types of Pentests**

* **White box** - Hacker will be provided with some information ahead of time regarding the target company's security info. 
* **Black box** - A 'blind' test, this is one where the hacker is given no background information besides the name of the target company. 
* **Covert** - A 'double blind' pentest, this is a situation where almost no one in the company is aware that the pen test is happening. 
* **External** - In an external test, the ethical hacker goes up against the company's external-facing technology, such as their website and external network servers. 
* **Internal** - Ethical hacker performs the test from the company's internal network. 

**Pentest Stages**

1. **Planning Phase** - Defining the scope and goals of a test, including the systems to be addressed and the testing methods to be used. 
2. **Discovery Phase** - The next step is to understand how the target application will respond to various intrusion attempts. 
3. **Attack Phase** - Use attacks to uncover a target's vulnerabilities. 
4. **Reporting Phase** - Results are compiled into a report to help create a plan of action to patch vulnerabilities and protect against future attacks. 

**Tools & Techniques**    The toolkit you use depends on the scope of the subject of the project.     IOT pentest is different from a network pentest, which is different from an autonomous vehicle ECU pentest...

* Network: An IoT environment runs on and is updated over a network, such as the Internet, BLE, 4G, LTE, Zigbee, LoRA, WiFi, MQTT, 802.11.15.4, etc. 
* Applications: IoT applications manage device - Web app, mobile app, and they can be web apps, mobile apps, or APIs \(SOAP, REST\). 
* Firmware: This is the device's software and operating system. 
* Encryption: Encryption protects communications and data stored on the device. 
* Hardware: This is the IoT device hardware \(such as chipset, storage, JTAG, UART ports, sensors, camera, etc\). 

    A tester has to be good at:

* Network security to determine what protocols are being used and what information may be at risk. 
* Web tests, to see if there are any weaknesses with any web based configuration interface on the device. 
* Embedded engineering, and using engineering tools to find any back door testing interfaces. 
* Testing obscure OS instances. 
* Reverse engineering and decompiling applications from the extracted firmware. 

    **IOT Pentest**:

* Hardware Analysis.
* Firmware/OS Analysis.
* Wireless Protocol Analysis.
* Mobile Applications. 
* Web Applications. 
* Cloud Services/Infrastructure. 

![](https://www.evernote.com/shard/s342/res/76d7f003-3a58-82eb-a9b5-c4db02116cf5)  
**Pentest Examples**

* **Network Penetration**
  * This type of test includes both internal and external network exploitation. 
    * Testing of a network includes identifying: 
      * Threat modeling.
      * Vulnerability scanning & analysis. 
      * Firewall bypassing. 
      * Router & proxy server testing. 
      * IPS & IDS evasion. 
      * Open port scanning. 
      * SSH security attacks.
* **Web Application Security**
  * Application security tests search for server-side application vulnerabilities. 
  * The test is designed to evaluate the potential risks associated with these vulnerabilities through web applications, web services, mobile applications, and secure code review.
  * The most commonly reviewed applications are web apps, languages, APIs, connections, frameworks, systems, and mobile apps.  
* **Client Side/Wireless Network**
  * Wireless and website tests inspect relevant devices and infrastructures for vulnerabilities that may lead to compromises and exploits to the wireless network. 
  * To prevent wireless network hacking, check the following during pentesting: 
    * web server misconfiguration including the use of default passwords.
    * malware and DDoS attacks. 
    * SQL injections. 
    * MAC address spoofing.
    * media player or content creation software testing vulnerabilities. 
    * cross-site scripting.
    * unauthorized hotspots and access points. 
    * wireless network traffic.
    * encryption protocols. 
* **Social Engineering Attacks**
  * These tests search for vulnerabilities an organization could be exposed to based on its employees directly. 
  * In this case, creative testing must be designed to mimic real-world situations. 
  * Specific topics such as: 
    * eavesdropping.
    * tailgating.
    * phishing attacks.
    * pretending to be an employee.
    * pretending to be vendors/contractors.
    * name-dropping or pretexting.
    * gifts or dumpster diving.
    * baiting.
  * Bad actors typically possess social engineering skills and can influence employees to create access to systems or sensitive customer data.
* **Physical Testing**
  * Physical penetration testing prevents hackers from gaining access to systems and servers by ensuring that facilities are impenetrable by unauthorized personnel.
  * IT and cybersecurity professionals focus primarily on system vulnerabilities and may overlook aspects of physical security that can result in exploitation. 
  * Physical penetration tests focus on attempts to gain access to facilities and hardware through RFID systems, door entry systems and keypads, employee or vendor impersonation, and evasion of motion and light sensors. 
  * Physical tests are used in combination with social engineering such as manipulation and deceit of facility employees to gain system access.
* **CNE & CAN Attacks**
  * In a Computer Network Exploitation \(CNE\), networks can be used to target other systems directly. 
  * In a Computer Network Attack \(CNA\), the goal is to destroy or corrupt information that exists on a victim's network through an Electronic Attack \(EA\). 
  * EA's can use techniques such as an electromagnetic pulse \(EMP\) designed to incapacitate a network or system. 
  * Types of CNAs can overlap with social engineering and include:
    * Data modification.
    * IP address spoofing.
    * Password-based attacks.
    * DDoS.
    * MitM.
    * Compromised key.
    * Application layer attacks.
* **Cloud Pen Testing**
  * Cloud providers have a shared or hands-off approach to cybersecurity.
    * Organizations are responsible for vulnerabilities testing or hacking prevention themselves. 
  * Typical cloud testing areas include: 
    * weak passwords.
    * network firewalls.
    * RDP and SSH remote administration. 
    * applications and encryption.
    * API, database, and storage access.
    * VMs.
    * unpatched operating systems. 
  * Public cloud penetration testing can be among the most complicated to perform. 
    * Utilize a white box method of testing by making use of as much information as possible about the target system. This includes the software it runs and the network architecture, the source code, etc.
  * On-premises subscribers and cybersec personnel can scan: applications, data, runtime, OS, virtualization, servers, storage, and networking. 

**WIRESHARK PACKET CAPTURE**

**What is Wireshark?**

* A graphical network packet analyzer tool.
* It captures packets in real time and displays them in human-readable format. 

**Why is Wireshark Important?**

* Wireshark has been dubbed the 'world's foremost network protocol analyzer.'
* Packets don't lie. 
* Identifying who or what is consuming the network resources/bandwidth and latency details are important.
* 'Trust, but verify.'
* Things you can do:
  * Analyze what happens in the transport and network layer, as you open a website.
  * Filter out TCP, HTTP, UDP, ARP protocols and analyze them individually. 
  * Determine the TCP port number, destination port number, packet number, source/destination IP, analyze handshaking. 
  * Determine your network throughput. 

**Packet Analysis**

![](https://www.evernote.com/shard/s342/res/67a240ab-59e4-b866-14db-ff7698f4e39d)

![](https://www.evernote.com/shard/s342/res/05441157-ce1f-5dae-ea9a-a2514ac314e4)

![](https://www.evernote.com/shard/s342/res/91e62a3c-c9ca-f17a-485e-952b34c144ed)

![](https://www.evernote.com/shard/s342/res/1d2b77b4-7d69-84f4-e185-0f07f00dbb84)

![](https://www.evernote.com/shard/s342/res/08aa5798-d2b9-f791-3310-66f8d5cdcae7)

![](https://www.evernote.com/shard/s342/res/afa9cc6a-7528-b7fd-0616-5f8852c9d164)

![](https://www.evernote.com/shard/s342/res/cba8610f-e8ba-8b6d-48c5-e51b12b0f1ec)

![](https://www.evernote.com/shard/s342/res/f8faf156-1a99-7210-b37e-dbef81f11deb)

![](https://www.evernote.com/shard/s342/res/72ab6675-6813-391c-045b-b592c5afdc8e)

**Detecting Attacks**

* TCP SYN Flood / DoS Attack

![](https://www.evernote.com/shard/s342/res/5b6b4b56-8e6f-9229-7fa2-b77830276ea9)

* Detecting DoS attack with Wireshark

![](https://www.evernote.com/shard/s342/res/a9099170-fd21-5cea-e07b-545c9366c80d)![](https://www.evernote.com/shard/s342/res/ebd70043-3a0f-ce55-bc11-a11b0c6d6b49)![](https://www.evernote.com/shard/s342/res/e2ec1155-d3f1-4a20-38c7-535aa03d6e10)![](https://www.evernote.com/shard/s342/res/bba06862-afb7-6a32-a04e-c42be6dc6932)  


* ARP Spoofing \(Cain & Abel\)

![](https://www.evernote.com/shard/s342/res/ed8412d1-9e80-70dc-a8b0-6f198e53018e)![](https://www.evernote.com/shard/s342/res/15eab610-fb4c-7e6a-164b-4a2d5974f504)![](https://www.evernote.com/shard/s342/res/2bfa7511-9e86-f736-b4ed-74f255d4bfc1)![](https://www.evernote.com/shard/s342/res/9f522d96-b4cf-10ee-49b7-f19af94b22ae)![](https://www.evernote.com/shard/s342/res/9f7e2462-cfe3-e46b-76dd-6b38f1359e4d)![](https://www.evernote.com/shard/s342/res/a6a4e9f0-fee2-09fd-04f4-6206bb424026)![](https://www.evernote.com/shard/s342/res/62f4547b-4ccf-40b7-7d6c-4320ba8118f1)  


* Now, with wireshark, launch a capture to see what's going on. 
* Look for the source: 

![](https://www.evernote.com/shard/s342/res/ae49a977-c8ab-8c72-305b-5444d023b2da)

* filter for 'http.cookie'
  * to see all the cookies that are passed through

![](https://www.evernote.com/shard/s342/res/2d9dc632-16e6-023c-1134-2a058a1fc32a)

* copy the value of the cookie \(right click -&gt; copy\)
* install Tampermonkey in chrome \(for injecting cookies\)
  * go to the website the user was going to, that you captured. 
  * launch Tampermonkey and paste it into the form and you get access from the validated cookie. 

**Examples**

* Wireshark is a very powerful and great for scanning and recon. 
* Understand baseline network traffic. 
* Filter for specific terms like POST data.
* Steal cookies.
* Meant for diagnostic, but used by hackers to refine techniques. 
* Sniff out data from IOT devices.
* Promiscuous mode and Monitor mode. 

