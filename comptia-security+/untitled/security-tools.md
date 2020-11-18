# Security Tools

**Protocol Analyzers**

* AKA Packet Sniffers.
* Gathering packet-level information on a network.
* Examples:
  * Wireshark
  * TCPDump

**Network Scanners / Mappers**

* Knowing what's on your network.
* Network enumeration.
* Examples:
  * Solarwinds
  * Nmap/ZenMap
  * Fing \(iOS & Android\)

**Vulnerability Scanner**

* Software utility that scans a range of IP addresses and tests for the presence of known vulnerabilities in software configuration and accessible services.
* Relies upon a database of known vulnerabilities.
* Examples:
  * Nessus \(Tenable\)
  * OpenVAS: Linuix
  * Nexpose Community Edition: Scan web apps, databases, and virtual environments.
  * Qualys FreeScan: Checks for hidden malware and SSL issues, among other network vulnerabilities.

**OWASP ZAP**

* ZAP - Zed Application Proxy
* Discovers security vulnerabilities in web apps.

**Exploitation Frameworks**

* Platforms used for penetration testing and risk assessments.
* Frameworks contain a set of exploits for known vulnerabilities.
* Examples:
  * Metasploit - [https://www.metasploit.com](https://www.metasploit.com)
  * Canvas
  * Core Impact
* Browser Exploitation Framework \(BeEF\) - pentesting tool for exploiting web vulnerabilities.

**Kali Linux**

* Debian-derived Linux distro designed for digital forensics and pentesting.
* Preinstalled with numerous pentesting programs.
* Can be run from HD, Live CD, or Live USB.
* Supported platform of the Metasploit Framework.

**Social Engineering Toolkit \(SET\)**

* Searchable info resource for Social Engineering.

**Wireless Scanners**

* Gather info about WiFi networks.
* Detect access points \(rogue or valid\).
* Break encryption keys.
* Examples:
  * Aerodump
  * Kismet/KisMAC
  * Netstumbler
  * Vistumber
  * inSSIDer

**Configuration Compliance**

* Microsoft Baseline Security Analyzer \(MBSA\): A software vulnerability scanner to analyze targeted Microsoft systems, to detect whether software security patches or baseline config settings are missing.
* Center for Internet Security \(CIS\)
* Nessus

**Banner Grabbing**

* A technique to ID operating systems, apps, and services on a system.
* Narrows vuln searches.
* Netcat
  * Free download for Windows & Linux
  * Read/Write TCP & UDP network connections.
  * Run from the command line.

**Password Crackers**

* Used to disclose passwords and assess password strength.
* Online password-cracking tools enable you to type in the hash and get the password returned in plain text.
* Examples:
  * Brutus
  * Cain & Able
  * John the Ripper
  * THC Hydra
  * Hashcat

**Honeypots / Honeynets**

* Use:
  * Systems or networks exposed to capture malicious activity.
  * Gather investigation evidence.
  * Study attack strategies.
* Separate from any business network.
* [http://www.honeyd.org](http://www.honeyd.org)/

**Steganography**

* Means "hidden writing" - hiding messages, often in other media, so that unintended recipietns are not even aware of any message.
* Approaches:
  * Least significant bit insertion.
  * Masking and filtering.
  * Algorithms and transofrmations.
* Common steganography tools include:
  * OpenPuff
  * Camouflage
  * StegHide
  * rSteg
  * zSteg
  * Outguess

**Data Sanitization Tools**

* Sanitization - the process of removing contents from a device or media.
* Examples:
  * DBAN
  * BCWipe
  * Cryptographic Erase \(CE\)

**Command Line Tools**

* man
* ping
* netstat
* tracert
* nslookup/dig
* arp
* ip/ifconfig
* tcpdump
* nmap
* netcat
* SysInternals Suite
  * Autoruns
  * Process Explorer

**Anti-Spoofing**

* A router function. 
* An application compares the incoming or outgoing IP address ot an ACL. 
* Other types of anti-spoofing perform similar functions on MAC address or switch ports. 

