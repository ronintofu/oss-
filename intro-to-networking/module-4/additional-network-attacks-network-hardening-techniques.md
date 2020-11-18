# Additional Network Attacks / Network Hardening Techniques

**Additional Network Attacks**

**Ransomware**

* Attacker uses a form of Malware that encrypts all files on the device holding them hostage for a ransom.
* If ransom is not paid, the files will never be decrypted.
* To avoid/prevent:
  * Backup your files.
  * Use firewalls.
  * Use anti-malware.
  * Train users to avoid phishing and other attacks.

**Phishing**

* Attacker uses electronic communication such as email to obtain information such as usernames and passwords, bank info, etc.
* Phishing emails are disguised as an official email from a trusted source and usually attempt to make you click a link.
* How to identify Phishing:
  * Misspelled words.
  * Strange URLs.
  * Asking for sensitive information.

**Deauthentication**

* Attacker deauthenticates \(logs out\) a user.
* Most common: WiFi deauthentication attack.
  * 1. Attacker sends deauthentication frame AP.
  * 2. User gets kicked off and attacker can:
    * Have user reconnect to evil twin access point.
    * Sniff the WPA 4-way handshake upon the user reconnecting.
    * Hijack the WiFi connection.
    * Mount a man-in-the-middle attack.

**Insider Threat**

* A malicious employee.
* A trusted person on the inside who takes advantage of their network access to cause harm or steal data.
* How to identify an insider threat?
  * Strange activity.
  * Downloading large amounts of data.
  * Accessing areas they shouldn't normally have access to.

**Logic Bomb**

* Malicious code that sets off a malicious function or activity when certain conditions are met.
* Called a "bomb" because it is set off or triggered by some condition or certain time.
* Examples:
  * Malware that triggers at a predefined time or date.
  * Malware that triggers when a specific condition is met in the system such as a time/date, a piece of software does something, a line of code is executed, etc.
  * Code inserted by an employee that deletes certain files if they are terminated from the company.

**Network Hardening Techniques**

**Network Access Control \(NAC\)**

* Defines authorized nodes and MAC addresses.
* Performs posture assessment on connecting clients.
* Posture assessment:
  * Checks for antivirus/anti-malware, patches, operating system type and version, etc.
  * Will not let the host connect if it does not conform to policy.
* Persistent Agent
  * Posture assessment performed on a recurring basis for each client.
* Non-persistent Agent
  * Performs a one-time posture assessment when the client initially connects.
* Quarantine Network/VLAN
  * Where the host goes if it doesn't pass the posture assessment for remediation.
  * This is a separate individual VLAN that has been separated from the rest of the network to house the failed/infected hosts.

**Anti-Malware Software**  
The most obvious way to enhance the security of any network is to protect the endpoints from Malware.

* Host-Based
  * Installed directly on the host computer itself.
  * All the devices need signatures updated constantly which is cumbersome to manage.
  * Large organizations require an anti-malware server to track, push, and manage updates.
* Cloud/Server-Based
  * Centralized anti-malware service that runs in the cloud or on a local server.
  * Inbound and outbound communication requests are examined by the service.
  * Easy to manage and sometimes requires no additional software to be installed on a host.
* Network-Based
  * Runs on firewalls or other nodes that process internet traffic such as proxy servers.
  * All traffic that passes through it is examined and uses signatures to identify malware.
  * Does not require any software on the host - the entire network is protected.

No single type of anti-malware protection is going to be the best option. The best option is to use multiple forms of anti-malware implementations to provide wider coverage.

**Switch Security**

* ARP Inspection
  * With Dynamic ARP Inspection \(DAI\) turned on, switches can intercept all ARP requests and replies and determine the validity of the IP-to-MAC binding.
  * Drops invalid and spoofed ARP packets.
  * Prevents ARP Poisoning/spoofing and some man-in-the-middle attacks.
* DHCP Snooping
  * Identifies trusted DHCP servers.
  * Acts like a DHCP firewall between the servers and hosts.
  * Filters all abnormal/invalid DHCP traffic.
* MAC Address Filtering
  * Switches can keep a list of MAC addresses to permit or deny access.
* Port Security
  * Allows only the specified MAC Address\(es\) to use the switchport.
  * Sticky MAC Addressing.
  * If an invalid MAC address is connected the switchport will shut down completely.
* VLANs
  * Allow us to segment the network into smaller parts and apply security to each VLAN separately.
  * Can restrict which VLANs can talk to each other and restrict other network access with VLAN ACLs.

![](https://www.evernote.com/shard/s342/res/82418900-36f4-008c-55af-b54408fa51ef)\*\*\*\*

**User Authentication**

* 802.1x/EAP
  * Users have zero network access until authenticated.

![](https://www.evernote.com/shard/s342/res/55cb36db-8ee9-feba-3039-92349a777165)

* PPP- PAP, CHAP, MS-CHAP
  * Username/Password authentication.
  * Used for remote server access, VPNs, etc.

![](https://www.evernote.com/shard/s342/res/d3c98d08-ff16-3722-abe3-644d5725e002)

* Kerberos
  * Centralized network authentication system.
  * Used with Windows Domain client authentication.
  * Can be used to secure any service requests.

![](https://www.evernote.com/shard/s342/res/a10fa992-dfd6-815b-680b-81c3f85fd41c)

* Single Sign On \(SSO\)
  * Allows access to multiple systems with a single set of credentials.
  * Creds from a Directory Server provide access to multiple applications.
  * Lightweight Directory Access Protocol \(LDAP\)
  * Authentication token passed to configured SSO applications.
* Multifactor Authentication
  * Single-factor = just a username/password.
  * Two-factor authentication.
  * Example: Adds a one-time password texted to your phone, like with Steam.
  * Security questions, PINs, Biometrics, physical token, mobile phone token, etc.

**Physical Security**

* Mantraps
* Network closets and locked racks.
* Video monitoring \(IP Cams/CCTV\)
* Door Access Controls
  * Keypads and Cipher Locks
  * Proximity Readers/Key Fob
  * Biometric Scans
* Security Guards

