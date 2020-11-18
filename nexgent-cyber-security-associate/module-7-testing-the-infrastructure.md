# Module 7 - Testing the Infrastructure

**ATTACKS**

**THREAT DETECTION:** [https://learn.nexgent.com/modules/cyber-security-specialist-module7/sections/cyber-security-specialist-module7-section2/lessons/cyber-security-specialist-module7-threatdetection](https://learn.nexgent.com/modules/cyber-security-specialist-module7/sections/cyber-security-specialist-module7-section2/lessons/cyber-security-specialist-module7-threatdetection) 

**What is threat detection?**

* **The process in which you find threats on your network, systems, or applications.** 
* The idea is to detect threats before they are exploited as attacks. 

    Hackers are after:

* User Credentials
* PII \(Personally Identifiable Information\)
* Intellectual Property
* Ransom
* Revenge

**Analyzing Threat Analytics**

* Organizations are able to gauge a baseline for normal user behavior. 
  * What kind of data they access.
  * What times they log in. 
  * Where they are located.
* Attacker behavior has no real "baseline". 

![](https://www.evernote.com/shard/s342/res/c2937d51-c5e8-ff0b-aea9-c17926f6b980)  
**Setting Traps**

* Some targets are just too tempting for an attacker to pass up. 
* Security teams know this, so they set traps in hopes that an attacker will take the bait - deception technology.
  * Intruder trap could include a honeypot target that may seem to house network services.
  * When an attacker goes after this bait, it triggers an alert so the security team know there is suspicious activity in the network that should be investigated. 
* Instead of waiting for a threat to appear in the organization's network, a threat hunt enables security analysts to actively go out into their own network, endpoints, and security technology to look for threats or attackers that may be lurking as-yet undetected. 
* This is an advanced technique generally performed by veteran security and threat analysts. 
* Ideally, a well-developed security threat detection program should include all tactics we have discussed.
  * Monitor the security of the organization's employees, data, and critical assets. 

**Threat Hunting**

* Requires technical and human element. 
  * Security analysts that can see trends/patterns and reports them.
  * Combination of tools act as a net across an organization's network. 
* Security Event Threat Detection
* Network Threat Detection
* Endpoint Threat Detection
* In the end, a combination of all these defensive methods should be employed for best coverage.

**Threat Detection Technology**    Typically composed of 5 key security tools: 

1. Endpoint Detection & Response
2. Network Traffic Analysis
3. Malware Sandboxes
4. Cyber Threat Intelligence
5. Central Analytics & Management

**Threat Response**

* Ideally, security teams deal with threats before they are weaponized into attacks. 
  * Examples of response range from quarantining malware, phishing awareness training, and patching known vulnerabilities with system updates. 
* Once a threat turns into an incident, a different type of response is required. 
  * An incident response plan helps IT staff identify, respond to and recover from cybersecurity incidents. The objective of an incident response plan is to prevent damages like service outage, data loss or theft, and illicit access to organizational systems. 
  * Understanding threats allows your organizations to respond appropriately to them.
* Leveraging advanced frameworks like MITRE ATT&CK \([https://attack.mitre.org/](https://attack.mitre.org/)\) improves the sophistication of security teams. 
* With behavioral analytics and threat hunting tools, a SOC analyst can proactively apply security solutions. 
* When threats turn into incidents, automation and an organized incident response team can help speed recovery. 

**SOCIAL ENGINEERING:** [https://learn.nexgent.com/modules/cyber-security-specialist-module7/sections/cyber-security-specialist-module7-section2/lessons/cyber-security-specialist-module7-socialengineering](https://learn.nexgent.com/modules/cyber-security-specialist-module7/sections/cyber-security-specialist-module7-section2/lessons/cyber-security-specialist-module7-socialengineering)

**What is Social Engineering?    The art of manipulating people so they give up confidential information.** 

* Easier to exploit your natural inclination to trust than it is to discover ways to hack your software. 

**What Does an Attack Look Like?**

* Text from a friend.
  * Take advantage of your trust/curiosity.
  * Contain a malicious link or download. 
* Email from a trusted source. 
  * Compelling story with pretext. 
* Baiting.
* Response to a question you never had.
* Creating distrust.

**Techniques**

* Social engineering has proven to be a very successful way for a criminal to "get inside" your organization. 
* Once a social engineer has a trusted employee's password, he can simply log in and snoop around for sensitive data. 
* With an access card or code, in order to physically get inside a facility, the criminal can access data, steal assets, or even harm people. 
* They work just as well over e-mail, the phone, or social media. 
* **What all the attacks have in common is that they use human nature to their advantage, preying on our greed, fear, curiosity, and even our desire to help others.** 

**Examples**

* Preparation/Reconnaissance is key for all these attacks. 
  * On the phone.
  * In the office. 
  * Online.
* Offer an incentive.
* "Fake it till you make it."
* Act like you own the place. 

**Prevention**

* Security awareness training is the number one way to prevent social engineering. 
  * Employees should be aware that social engineering exists and be familiar with the most commonly used tactics. 
* Fortunately, social engineering awareness lens itself to storytelling. 
  * Stories are much easier to understand and much more interesting than explanations of technical flaws.
  * Quizzes and attention-grabbing or humorous posters are also effective reminders about not assuming everyone is who they say they are.
* But it isn't just the average employee who needs to be aware of social engineering. 
  * Senior leadership and executives are primary enterprise targets. 
* Keep retraining security awareness.
* Case studies on the latest techniques with examples. 
* Review processes. 
* Emergency procedures. 
* Review and refine incident management. 

**Toolkit**

* Social Engineering Framework
  * Covers "best practices" from hacker's perspective.
  * Psychological Principles
  * Attack Vectors
  * Influencing Others
* Social Engineering Toolkit
  * Automates pen testing with social engineering \(spear phishing attacks, fake legitimate-looking websites, USB drive attacks, etc\). 

**ATTACKING WEBSITES:** [https://learn.nexgent.com/modules/cyber-security-specialist-module7/sections/cyber-security-specialist-module7-section2/lessons/cyber-security-specialist-module7-attackingwebsites](https://learn.nexgent.com/modules/cyber-security-specialist-module7/sections/cyber-security-specialist-module7-section2/lessons/cyber-security-specialist-module7-attackingwebsites)

**OWASP Top 10**![](https://www.evernote.com/shard/s342/res/e9ff2950-f9e6-40bf-5703-c5dbc18f7856)  
**High Profile Attacks**

* Adobe
  * Adobe announced in October 2013 the massive hacking of its IT infrastructure. Personal information of 2.9 million accounts was stolen \(logins, passwords, names, credit card info\).
  * Another file discovered on the internet later brought the number of accounts affected by the attack to 150 million \(only 38 million active accounts\). 
  * To access this information, the hackers took advantage of a security breach at the publisher, specifically related to security practices around passwords. 
  * The stolen passwords had been encrypted instead of being chopped as recommended. 
* Sony
  * April 2011, PlayStation Network was attacked. 
  * The multiplayer gaming service, online gaming purchasing, and live content distribution contained personal data of 77 million users, which was leaked. 
  * Banking info of tens of thousands of players was compromised. 
  * This cyber attack could have been largely avoided. 
  * Hackers used a well-known network vulnerability that Sony chose to ignore. 
    * Data was unencrypted and could easily be hijacked thanks to a very simple SQL injection. 
* South Korea
  * January 2014, data from 100 million credit cards had been stolen over the course of several years. 
  * In addition, 20 million bank accounts had also been hacked. 
  * 2 million South Koreans had their credit cards blocked or replaced. 
  * Behind the theft an employee of the Korea Credit Bureau \(KCB\), a solvency company. 
    * He stole personal information from customers of credit card companies when he worked for them as a consultant by simply copying the data to an external hard drive. 
    * He then resold the data to credit traders and telemarketing companies. 
* Target
  * Data from 110 million customers was hijacked between Nov 27 and Dec 15 including data of 40 million customers and personal data.
  * The American secret services had detected abnormal bank movements and warned Target. 
  * It had installed malware in cash registers to read info from the credit card terminals. This technique is known as RAM scraping.
  * Once the data had been hijacked, the attackers resold it on the black market. 
  * Target was ultimately required to pay over 18 million dollars as settlement. 
* Alteryx
  * A marketing analytics firm left an unsecured database online that publicly exposed sensitive info for about 123 million U.S. households. 
  * The data included 248 fields of info for each household ranging from addresses and income to ethnicity and personal interests. 
  * Details included contact info, mortgage ownership, financial histories, and whether a household contained a dog or cat enthusiast, etc. 
  * All of this was exposed on a publicly accessible AWS S3 storage cache. 
* Equifax
  * Detected July 2017, contained personal data of 143 million American, Canadian, and British customers as well as 200k credit card numbers. 
  * Complaints against the company as well as suspicions of insider trading were levied since the vulnerability of Apache Struts used by the hackers was well known and several execs of the company sold stock just days before news of the breach was announced. 
* AdultFriendFinder
  * In 2015, the dating site was attacked for the first time. 
  * The info of 4 million accounts was made public on a forum only accessible on Tor. 
  * The next year, a new attack much more violent than the first one hit for more than 400 million accounts. 
  * The stolen info was less sensitive in total but 20 years of personal data was stolen. 
  * Attackers used a LFI \(Local File Inclusion\) breach, a technique that consists of introducing a local or remote file into an online resource. 
  * In addition, some former users had the unpleasant surprise to learn their personal information had not been deleted despite their account cancellations. 
  * This hacking record largely dethroned the Ashley Madison site cyberattack. 
    * August 2015, the Ashley Madison extramarital dating site was hacked and personal data of more than 30 million users across more than 40 countries was harvested. 
* Marriott
  * Info from up to 500 million guests, including banking data. 
  * The hack started in 2014, lasted until 2018 when it was noticed. 
  * Internal security tool found someone trying to access its database in 2018. 
  * Marriott faces a $123m fine by UK authorities. 

![](https://www.evernote.com/shard/s342/res/cebfb4f0-c57e-6e5e-aa73-43a1e6d9f2f6)  
![](https://www.evernote.com/shard/s342/res/87067699-a9f3-4284-b390-d2abfb6f57fb)  
  
**Examples \(for assessing vulnerabilities of websites\)**

* The first move is always to enumerate and find as much info as you can about your target. 

![](https://www.evernote.com/shard/s342/res/75996a3b-9f2c-21fc-e378-d85fedc10e28)

* Doing a UDP port scan and scanning more than the top 1000 ports would be considered if the above scan's info was not enough. 
* The only port we are allowed to interact with \(without credentials\) is port 80/443.
* Launch gobuster to enumerate for any interesting files on the webserver while digging for information manually. 

![](https://www.evernote.com/shard/s342/res/4ca4bb65-4ee9-2473-dbbc-719d2ec36732)

* Seeing that the website looks custom built, I am inclined to test for an Unrestricted File Upload vulnerability. 

![](https://www.evernote.com/shard/s342/res/521135f9-913b-fee8-73e1-d89b60745d10)  
![](https://www.evernote.com/shard/s342/res/2c1c140c-2aed-67f4-b0d9-be4f81e109f5)  
![](https://www.evernote.com/shard/s342/res/e103e4a1-18db-2840-f432-2fc298ecb6f5)  


* Seeing that the webserver runs perl scripts, we grab a perl reverse shell, set the IP/Port and we are rewarded with a low-privileged shell. 
* Server is hosting 40+ different websites....

![](https://www.evernote.com/shard/s342/res/4df9c3df-fb81-7bf6-1eae-0e09b1804ef3)

* Surprisingly, read access to all the hosted websites was available. 
* Could read all the sites' backend codes.
* Notably, inside the cgi-admin/pages directory, all the perl scripts were connecting to a MySQL database as root. 
* The credentials for the database were there in cleartext. 

    What can an attacker do?

* Dump the contents of all the databases, resulting in the data of all 35 companies to be leaked in the public domain. 
* Drop all the databases, effectively deleting the data of the 35 companies. 
* Leave a backdoor for persistent access as apache with a cronjob, in case they want a return trip. 

    What to do next?

* Next look at SMB ports, there should be some folder somewhere that is being shared in the system among systems. 
* What kind of Linux is the server running? What version? What vulnerabilities does this version of Linux have?

    What can attacker do with root?

* Read/modify ALL files on the entire server. 
* Leave a persistent backdoor \(as done with apache\).
* Install and potentially spread malware into the server's intranet. 
* Install ransomware. 
* Use the server as a crypto miner
* Use it as a proxy.
* Use it as a C2C server.
* Use it as part of a botnet.
* rm -rf \(delete EVERYTHING\). 

**ATTACKING MOBILE APPLICATIONS:** [https://learn.nexgent.com/modules/cyber-security-specialist-module7/sections/cyber-security-specialist-module7-section2/lessons/cyber-security-specialist-module7-attackingmobile](https://learn.nexgent.com/modules/cyber-security-specialist-module7/sections/cyber-security-specialist-module7-section2/lessons/cyber-security-specialist-module7-attackingmobile)

**Mobile Attacks**     Mobile apps were downloaded over 205 billion times in just 2018 alone.     ~60% of digital consumption is done via smartphones and tablets now. **Mobile Apps 101**

* Most of the applications have a client-server architecture. 
  * The client runs the operating system, which is most frequently Android or iOS. 
* This client is downloaded to the device from the app distribution platforms, where developers publish their wares.
* As perceived from the user's POV, the client installed on the smartphone is the mobile applcation. 
  * This is what the user interacts with to make purchases, pay bills, read emails, etc. 

![](https://www.evernote.com/shard/s342/res/97386f64-1054-fcba-57f4-698e71c4dfe0)

* There's another component: the server, which is hosted by the developer. 
  * Often this role is performed by the same software that is responsible for generating and processing content on the site. 
  * In other words, most often the server-side component is a web application that interacts with the client over and API. 
  * It's where the info is stored and processed. 
  * Responsible for syncing user data between devices. 

**Client-Side Vulnerabilities**

* 60% of the vulnerabilities are on the client side. 
* IPC \(Insecure Interprocess Communications\) tend to be the leading common entry point for attackers. 

![](https://www.evernote.com/shard/s342/res/9d127386-2208-10f6-2c97-48a876c06b72)  
![](https://www.evernote.com/shard/s342/res/05a7a0a8-904d-a2b7-2b3d-263cc9649228)**Server-Side Vulnerabilities**

* The server component of a mobile application is basically a web application. 
* Server-side components contain vulnerabilities both in application code and in the app protection mechanisms. 

![](https://www.evernote.com/shard/s342/res/750e36f4-8f54-6f65-6cad-7581624aef6d)**Mobile Threats**

* Application-based threats - when people download apps that look legit but actually skim data from their device. 
  * Examples are spyware and malware that steal personal and business information without people realizing what's going on. 
* Web-based threats - subtle and tend to go unnoticed. 
  * These happen when people visit affected sites that seem fine on the front-end but,  in reality, automatically download malicious content onto devices. 
* Network-based threats - especially bad because cyber-criminals can steal unencrypted data while people use public WiFi networks. 
* Physical threats - occur when someone loses their mobile device or has it stolen. 
  * Hackers have direct access to the hardware where private data is stored or where they have access to data, this threat is especially dangerous to enterprises.

**Mobile Threats**

* Malicious apps
* Spyware
* Public WiFi
* Lack of End-to-End Encryption
* Inactive Apps
* IoT Mobile Security Threats
* Botnets
* Lost/Stolen Devices

![](https://www.evernote.com/shard/s342/res/e0a9a137-7c2c-f5a3-a44f-5c14514e1331)

**IMPLICATIONS**

**RISK & VULNERABILITY IMPACT:** [https://learn.nexgent.com/modules/cyber-security-specialist-module7/sections/cyber-security-specialist-module7-section3/lessons/cyber-security-specialist-module7-risk](https://learn.nexgent.com/modules/cyber-security-specialist-module7/sections/cyber-security-specialist-module7-section3/lessons/cyber-security-specialist-module7-risk)

**What is Risk?**    Cybersecurity is all about understanding, managing, controlling, and mitigating risk to your organization's critical assets.                             **Risk = Threat x Vulnerability x Asset**    Risk is a concept of quantifying the likelihood of financial loss for the organization.**Identify and Prioritize**

* Assets include servers, client contact information, sensitive partner documents, trade secrets, etc.
* Work with business users and management to create a list of all valuable assets. 
* Because most organizations have a limited budget for risk assessment, you will likely have to limit the scope of the project to mission-critical assets. 
* Accordingly, you need to define a standard for determining the importance of each asset. 
  * Common criteria include the asset's monetary value, legal standing, and important to the organization. 
* Once the standard has been approved by management and formally incorporated into the risk assessment policy, use it to classify each asset you identified ans critical, major, or minor. 

**Identifying Threats**

* A threat is anything that could exploit a vulnerability to breach security and cause harm to your organization. 
  * Natural disaster.
  * System failure.
  * Accidental human interference. 
  * Malicious entities. 

**Identifying Vulnerabilities**

* A vulnerability is a weakness that a threat can exploit to breach security and harm your organization. 
* Vulnerabilities can be identified through: 
  * vulnerability analysis
  * audit reports
  * NIST vulnerability database
  * vendor data
  * commercial computer incident response teams
  * system software security analysis
* You can reduce your software-based vulnerabilities with proper patch management.
  * Remember physical vulnerabilities also.

**Analyze Controls**

* Analyze the controls that will minimize or eliminate the probability that a threat will exploit a vulnerability in the system.
* Nontechnical controls include security policies, administrative actions, and physical/environmental mechanisms.
* Both technical and nontechnical controls can further be classified as preventive or detective controls. 
  * Preventive controls attempt to anticipate and stop attacks. 
    * Encryption/authentication devices are an example. 
  * Detective controls are used to discover attacks or events through such means as audit trails and intrusion detection systems. 

**Determine Incident Likelihood**

* Assess the probability that a vulnerability might actually be exploited. 
* Take into account: 
  * Type of vulnerability.
  * Capability and motivation of the threat source. 
  * Existence and effectiveness of your controls. 
* Rather than a numerical score, many organizations use the categories such as: high, medium, and low to assess the likelihood of an attack or other adverse event. 

**Assess Threat Impact**

* Impact analysis should include the following factors: 
  * The mission of the system including the processes implemented by the system. 
  * The criticality of the system, determined by its value and the value of the data to the organization. 
  * The sensitivity of the system and its data. 
* An attack or adverse event can result in compromise or loss of information, system confidentiality, integrity, and availability. 
  * As with the likelihood of determination, the impact on the system can be qualitatively assessed as high, medium, or low. 
* The following additional items should be included in the impact analysis:
  * The estimated frequency of the threat's exploitation of a vulnerability on an annual basis. 
  * The approximate cost of each of these occurrences. 

**Prioritize Risks**

* For each threat/vulnerability pair, determine the level of risk to the IT system, based on the following: 
  * The likelihood that the threat will exploit the vulnerability. 
  * The impact of the threat successfully exploiting the vulnerability. 
  * The adequacy of the existing or planned information system security controls for eliminating or reducing the risk. 
* A useful tool for estimating risk in this manner is the risk-level matrix. 
  * High likelihood that the threat will occur is given a value of 1.0 or 100
  * Medium = 0.5 or 50.
  * Low = 0.1 or 10.
* Risk is calculated by multiplying the threat likelihood value by the impact value and risks are categorized as high, medium, or low based on the result. 

![](https://www.evernote.com/shard/s342/res/338176de-daf1-0316-470c-b516ed1fee1d)**Recommend Controls**

* Using the risk level as a basis, determine the actions that senior management and other responsible individuals must take to mitigate the risk. 
* Here are some general guidelines for each level or risk: 
  * High - a plan for corrective measures should be developed ASAP. 
  * Medium - a plan for corrective measures should be developed within a reasonable period of time. 
  * Low - the team must decide whether to accept the risk or implement corrective actions. 
* As you consider controls to mitigate each risk, be sure to consider: 
  * Organizational policies.
  * Cost-benefit analysis.
  * Operational impact.
  * Feasibility.
  * Applicable regulations.
  * The overall effectiveness of the recommended controls.
  * Safety and reliability. 

**Document**

* The final step in the risk assessment process is to develop a risk assessment report to support management in making appropriate decisions on budget, policies, and procedures. 
* For each threat, the report should describe: 
  * Corresponding vulnerabilities. 
  * Assets at risk.
  * Impact to your IT infrastructure. 
  * Likelihood of occurrence and the control recommendations. 

![](https://www.evernote.com/shard/s342/res/3ff65129-7a99-d3de-deb5-15e5a4b3bf19)

**PRIVACY ISSUES**: [https://learn.nexgent.com/modules/cyber-security-specialist-module7/sections/cyber-security-specialist-module7-section3/lessons/cyber-security-specialist-module7-privacy](https://learn.nexgent.com/modules/cyber-security-specialist-module7/sections/cyber-security-specialist-module7-section3/lessons/cyber-security-specialist-module7-privacy)

**What is Internet Privacy?**    Refers to the personal privacy that you're entitled to when you display, store, or provide information regarding yourself on the internet.     This can include both personally identifying information \(PII\) as well as non-personally identifying information, such as your behavior on a website. **Data Security vs Data Privacy**

* Both data security and privacy are strongly interconnected to each other but not the same. 
* Understanding the differences between the two will help you understand who each of them works and how they compliment one another. 
  * Data privacy is all about authorized access, concerning who has it and who defines it. 
  * Security, on the other hand, is about securing data against unauthorized access. In other words, data security is about the technical implementation of what data privacy dictates. 
* Industries that are subject to compliance standards have to adhere to privacy laws and other legal implications. 

**Privacy Threats**

* Tracking
* Surveillance
* Theft

**Privacy Risks**

* Using the same credentials for multiple accounts. 
* Staying logged into websites. 
* Using services without reading ToC.
* Opening suspicious attachments. 

**Best Practices**

* Secure your web browser. 
* Use a VPN.
* Keep software patched and updated. 
* Install an AV program. 
* Activate firewall. 
* Delete cookies at browser exit. 
* Adjust website settings \(Google, Facebook, etc\). 

**Privacy Moving Forward**

* Each time you browse the internet, your privacy is under constant threat. 
  * Criminals, governments, and corporations all want the data. 
* The desire for privacy on the internet is only going to increase with time. 
* More internet users are realizing the importance of protecting their privacy and personal data. 
  * This is evident from the fact that over the last few years, there has been significant growth in the use of VPNs and other anonymizing technologies. 
* Privacy on the internet is your basic right. 

