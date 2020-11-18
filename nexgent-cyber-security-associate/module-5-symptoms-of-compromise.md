# Module 5 - Symptoms of Compromise

**Network Systems**

**What Are Indicators of Compromise?**

* Cyber attacks rarely occur with an alert or an alarm. 
* Attacks are often detected after the damage has been done. 

**Signs of a Cyberattack**

* Unusual Outbound Network Traffic 
  * Look for suspicious traffic leaving the network. It's not just about what comes into your network, it's about outbound traffic as well. 
  * Compromised systems will often call home to command-and-control servers. 
  * Outbound indicators may be much easier to monitor. 
* Irregular Privileged User Account Activity
  * Attacks rapidly escalate from compromising a single computer to taking over multiple computers/entire environments in just a few hours. 
  * They do this by reading an authentication database, stealing credentials, and reusing them. 
  * They learn which users/service accounts have elevated privileges and permissions, then go through those accounts to compromise assets within the environment. 
  * If you suddenly notice a high volume of elevated log-ons across multiple servers or high-value individual computers, ring the alarms. 
* Irregular Information Flow
  * Look for large flows of data from internal points to other internal computers or to external computers \(server to server, server to client, network to network\). 
  * Data flows might be limited but also targeted. 
  * Often aggregate stolen data to internal collection points before moving it outside. 
  * Some organizations now intercept all previously undefined and unapproved HTTPS traffic using a security inspection device.
  * Learn your baseline. 
* Focused Spear Phishing
  * Focused spear phishing email campaigns against specific company employees using document files \(C suite, project leaders, etc.\)
  * Not sent to everyone in the company. 
  * Often using information that has been learned by attackers that had previously compromised other team members. 
* Slow Connections
  * Slow and sluggish behavior is the most common sign that indicates your network is under attack. 
  * Attack is usually a well-orchestrated attack like DDoS. 
  * A company's computers may also be a part of a botnet that is being controlled by an outside entity. 
* ARP Spoofing
  * Attack in which an attacker sends falsified ARP \(Address Resolution Protocol\) messages over a LAN. 
  * Results in the linking of an attacker's MAC address with the IP address of a legitimate server on the network. 
  * Once the attacker's MAC address is connected to an authentic IP address, the attacker will begin receiving any data that is intended for that IP address.
  * ARP spoofing can enable malicious parties to intercept, modify, or even stop data in-transit \(MitM, Session Hijacking, DoS attacks\). 
  * Packet filters are useful in ARP spoofing prevention because they are capable of filtering out and blocking packets with conflicting source address information. 
* DNS Cache Poisoning
  * Attack in which corrupt data is inserted into the cache database of the DNS name server.
  * In a DNS cache poisoning attack, a malicious party sends forged responses from an impostor DNS in order to reroute a domain name to a new IP address. 
  * Once an attacker has sent a forged DNS response, the corrupt data provided by the attacker gets cached by the real DNS name server, hence "poisoning" it. 
  * IT teams should configure DNS servers to rely as little as possible on trust relationships with other DNS servers. 
  * Restrict query responses to only provide information about the requested domain. 

**Threat Indicators and Defensive Measures**

* Know your strengths and weaknesses. 
* Build Security Awareness into your company culture. 
* Make Cybersecurity assessments a continuous process. 
* Preventive controls. 
* Vendor Relations - know who has access to your data and work with them to make sure your data is secure.

**Challenges**

* The problem with cyber security is that most companies don't know what their high value assets are. 
* It is important to understand the environment you are trying to protect to actually make detection and prevention better. 
* Constant surveillance is critical, with early warning indicators and multiple layers of defense. 
* The company should already have developed and be monitoring internal measures of cyber security ratings and external metrics. 
* Senior management should require and independent cybersecurity review process on a yearly basis. 
* Corporations need to manage cybersecurity at the enterprise level and must continuously improve the ability of each element layer by layer. 

**Ask Yourself**

* Are we thinking about security the right way? 
* Do we have the right strategy? 
* Where do we stand in relation to "best practices" or industry standards?
* What are the company's risks and challenges?
* What external metrics should we be tracking? 
* Are we measuring things in the right way? 

**Host Symptoms**

**What are indicators of compromise?**

* Cyberattacks rarely occur with an alert or an alarm.
* Attacks are often detected only after the damage is done. 

**Signs of a Cyberattack**

* Unexpected Popups: 
  * If windows pop up without users clicking, then the system is most likely compromised. 
  * Might likely be part of a botnet, and the back end is click websites on your behalf. 
  * Could be a victim of "click fraud". 
* Mysterious Computer Behavior: 
  * Strange behavior of systems is always a red flag.
  * Changed passwords.
  * Unsolicited software installs.
  * Automatic mouse movements.
  * Tampered security settings.
  * Unfamiliar toolbars.
* Inability to download updates:
  * Malicious programs in the computer also prohibit users from downloading important updates. 
  * Do anything to stop actions that will make their operating system more secure. 
  * Also blocks users from downloading and installing AV updates. 
* Unfamiliar programs running in task manager:
  * One of the ways to detect a security breach is to open Task Manager and detect suspicious processes that are running in the background. 
  * These processes will often have cryptic names and the user should investigate these for confirming the breach. 
  * The programs are usually startup processes and they will be utilizing the CPU and other resources more than any other program. 
  * Many times, the CPU gets overheated even when the machine is idle due to malicious programs running in the background. 
* Botnets: 
  * A botnet is a collection of internet-connected devices that an attacker has compromised. 
  * Commonly used for DDoS attacks. 
  * Malicious actors build botnets by infecting connected devices with malware. 
  * Once an attacker has compromised a device on a specific network, all the vulnerable devices on that network are at risk of being infected. 
  * Challenges to shutting botnets down include the widespread availability and ongoing purchases of insecure devices like IoT devices. 
  * The near impossibility of simply locking infected machines out of the internet, and difficulty tracking down and prosecuting the botnet creators. 
  * When consumers go into a store to buy a security camera or other connected device, they look at features, recognizable brands, and most importantly the price. 
  * Meanwhile, as people continue to buy low-cost, insecure devices, the number of vulnerable end points just keeps going up. 
  * Install updates in a timely fashion. 

**Web Application Symptoms**

**What are web applications?**

* Web applications are programs allowing users to submit and retrieve data to/from a database over the internet. 
* The data is then presented to the user within their browser as information is generated dynamically by the web application through a web server. 

**How do web applications work?**  
![](https://www.evernote.com/shard/s342/res/76bfbb9e-e8dd-b635-c0a5-97d5a236d7fb)![](https://www.evernote.com/shard/s342/res/f72160c6-ad8c-843e-ef04-a9a1c945b976)  
**Web Application Attacks**

* Despite their advantages, web applications do raise a number of security concerns stemming from improper coding. 
* Serious weaknesses/vulnerabilities allow criminals to gain direct and public access to databases in order to churn sensitive data - aka web application attack. 
* Websites depend on databases to deliver the required information to visitors. 
* If web applications are not secure, an entire database of sensitive information is at serious risk of an attack.

 **SQL Injection**

* An injection attack that makes it possible to execute malicious SQL statements. 
* Attackers can use SQL injection vulnerabilities to bypass application security measures. 
* TO make an SQL injection attack, an attacker must first find vulnerable user inputs within the web page or web application. 
* A web page or web application that has an SQL injection vulnerability uses such user input directly in an SQL query.
* Attacker creates malicious payload and sends content, malicious SQL commands are executed in the database. 

![](https://www.evernote.com/shard/s342/res/2794a16c-873f-dc64-2ade-95ed64a64a7e)  
**Cross Site Scripting**

* Client side code injection attack.
* The attacker aims to execute malicious scripts in a web browser of the victim by including malicious code in a legitimate web page or web application. 
* Actual attack occurs when the victim visits the web page or web application that executes the malicious code. 
* The web page or web application becomes a vehicle to deliver the malicious script to the user's browser. 
* Session hijacking is a serious concern with XSS vulnerabilities. 

![](https://www.evernote.com/shard/s342/res/5ce57f8f-119b-5eed-34f7-5f1d89d7a103)**Directory Traversal**

* HTTP attack which allows attackers to access restricted directories and execute commands outside of the web server's root directory.
* Web servers provide two main levels of security mechanisms:
  * Access Control Lists \(ACLs\)
  * Root Directory
* An ACL is used in the authorization process, it's a list which the web server's administrator uses to indicate which users or groups are able to access, modify, or execute particular files on the server, as well as other access rights.
* An attacker can make use of this vulnerability to step out of the root directory and access other parts of the file system. 
* Ensure you have installed the latest version of your web server software, and ensure that all patches have been applied. 
* Filter any user input.  

![](https://www.evernote.com/shard/s342/res/d8ad0084-64c4-9601-874d-c1dc7d1405ad)**Challenges**

* Websites and related web applications must be available 24/7/365 to provide the required service. 
* Firewalls and SSL provide no protection against a web application attack. 
* Web applications often have direct access to the backend data. 
* Most web applications are custom-made and involve a lesser degree of testing than off-the-shelf software. 

