# Security Protocols

**Security Protocols - Web**

* SSL - Secure Sockets Layer \(latest version: 3.0\) [{source}](https://en.wikipedia.org/wiki/Transport_Layer_Security)
  * Now depreciated by the IETF and should not be used.
  * Uses certificates for authentication and encryption for message integrity and confidentiality.
  * Establishes a stateful connection.
* TLS - Transport Layer Security [{source}](https://en.wikipedia.org/wiki/Transport_Layer_Security)
  * Based on SSL v3.0
  * Provides privacy \(symmetric encryption\), message integrity \(Message Authentication Code\), and authentication \(PKI digital certificates\).
  * Forward secrecy ensuring that any future disclosure of encryption keys cannot be used to decrypt any TLS communications recorded in the past.
* HTTPS
  * Uses SSL/TLS to secure web-based communications.
  * X.509 digital certificates.
  * 256-bit encryption keys.

**Domain Name Service \(DNS\) Security**

* Suite of Internet Engineering Task Force \(IETF\) specifications.
* Protects against DNS Cache Poisoning.
* DNS extensions provide DNS clients \(resolvers\) origin authentication of the DNS data, authenticated denail of existence, and data integrity.
  * Not confidentiality or availability.

**SSH - Secure Shell** [{source}](https://en.wikipedia.org/wiki/SSH_%28Secure_Shell%29)

* Replaces telnet for remote communications.
* Establishes a session between the client and host computers using an authenticated and encrypted connection.
* Uses the asymmetric \(public key\) RSA cryptography for both connection and authentication.
* Used for remote administration of Linux servers.
* Other protocols can tunnel through SSH.

**Secure Email**

* Secure / Multipurpose Internet Mail Exentioins \(S/MIME\)
  * A standard for encryption \(confidentiality\) and signing \(authentication\) of MIME \(email\) data.
  * Requires PKI and uses Certificate Authorities \(CA\).
  * Internal Email.
* POP3S and IMAPS
  * Use SSL to secure emails in transit between a POP or an IMAP server and the client.
  * External email.

**FTPS - Securing FTP**

* FTP - File Transfer Protocol
  * Passes credentials in clear text.
* FTPS - FTP extension that adds SSL/TLS
  * Mutual authentication of parties \(certificates\).
  * Data confidentiality \(encryption\) and integrity \(hashing\).
  * FTPS Implicit over port 990.
  * FTPS Explicit over port 21.
* SFTP \(Secure FTP\)
  * Uses SSH to transfer files \(SSL encapsulation\).

**SRTP**

* Secure voice and video transmissions.
* Voice and video calls are established with session initiation protocol \(SIP\) and data is transmitted with realtime transfer protocol \(RTP\).
* The Secure Real-Time Transport Protocol \(SRTP\)
  * Extension to RTP.
  * Intended to provide encryption, message authentication and integrity, and replay attack protection to the RTP data in both unicast and multicast applications.

**LDAPS**

* LDAP is a Directory Protocol
  * Contains sensitive information about organizational systems and users.
* Attackers may sniff the network to read unencrypted LDAP traffic.
* LDAPS over SSL/TLS
* Uses TCP port 636.

**SNMPv3**

* SNMP \(Simple Network Management Protocol\) used to manage networks.
* Each managed device has a software agent reporting configuration settings and alerts \(traps\) to a central SNMP Management Server.
* SNMPv1 & v2 sent all data as clear text.
* SNMPv3 encrypts data.
* Uses port 161.

**Network Address Allocation**

* Allocating IP addresses.
* DHCP \(Dynamic Host Control Protocol\) - Assigns internal IP addresses.
* Use of network subnets to segregate multiple hosts and control network traffic.

**Time Synchronization**

* NTP \(Network Time Protocol\) - UDP protocol used to synch time based on the atomic clock.
* NTP Servers - redundant and secured.

**Subscription Services**

* Software as a Service \(SaaS\)
* Cloud email: Gmail, microsoft office, etc.
* Network defenses:
  * Firewall / IDS/IPS
  * Web and app filtering.
  * AV
  * Patching

**Secure Copy Protocol \(SCP\)** [{source}](https://en.wikipedia.org/wiki/Secure_copy_protocol)

* A means of securely trasnferring files between a local host and a remote host or between two remote hosts. 
* Based on SSH. 



