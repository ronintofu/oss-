# Network Security Continued

**WLAN Security**

**Encryption Standards**

* WEP \(Wired Equivalent Policy
  * Uses 4 different keys with RC4 encryption.
  * Overall WEP algorithm has inherent security flaws.
* WPA \(Wi-Fi Protected Access\)
  * TKIP \(Temporal Key Integrity Protocol\)
  * Pre-Shared Key \(PSK\)
  * WPA Enterprise Authentication \(external server authorization\)
  * Still seen as inherently unsecured.
* WPA2
  * The strongest wireless encryption standard for a long time.
  * AE Encryption \(Advanced Encryption Standard\)
  * Key size up to 256 bits.
  * Power of processing/software have caught up and made WPA2 more hackable.
* WPA3
  * All WPA3-enabled devices use the latest security methods available.
  * Disallows outdated legacy protocols
  * Requires the use of Protected Management Frames \(PMF\)
  * WPA3 - Personal
    * Uses Simultaneous Authentication of Equals \(SAE\) to prevent brute force attacks.
      * [https://ieeexplore.ieee.org/document/4622764](https://ieeexplore.ieee.org/document/4622764)
  * WPA3 - Enterprise
    * Uses 802.1X Authentication
      * [https://www.securew2.com/solutions/802-1x/\#:~:text=Configure%20802.1x%20on%20Linux&text=The%20manual%20configuration%20is%20relatively,the%20information%20of%20your%20network.](https://www.securew2.com/solutions/802-1x/#:~:text=Configure%20802.1x%20on%20Linux&text=The%20manual%20configuration%20is%20relatively,the%20information%20of%20your%20network.)
  * Open Networks
    * Uses no authentication.
    * Uses Opportunistic Wireless Encryption
      * [https://tools.ietf.org/html/rfc8110](https://tools.ietf.org/html/rfc8110)
  * IoT Onboarding
    * Uses Device Provisioning Protocol \(DPP\) to quickly onboard devices.
      * [https://www.wi-fi.org/download.php?file=/sites/default/files/private/Device\_Provisioning\_Protocol\_Specification\_v1.1\_1.pdf](https://www.wi-fi.org/download.php?file=/sites/default/files/private/Device_Provisioning_Protocol_Specification_v1.1_1.pdf)

  
**Basic WLAN Threats**

* War Driving & War Chalking
  * Driving around to identify wireless networks that can be accessed.
  * Uses standardized symbols to convey the WiFi details in public view.

![](https://www.evernote.com/shard/s342/res/26f000ac-eea5-51c6-c26b-cb698dddda2a)

* WEP/WPA/WPS Attacks
  * Software utilities for cracking.
    * WEP key crack.
    * WPA PSK crack.
    * WPS \(Wireless Protected Setup\)
      * PIN can be easily brute-forced.
* Rogue AP
  * Evil Twin
    * Setting up a secondary access point, set exactly the same as the SSID as the original AP with the same subnet to convince users to connect to the Evil Twin instead of the original.

  
**Security Measures**

* Disable SSID Broadcast
  * Very basic, prevents SSID from showing but does not prevent the network from being found \(nothing can\).
* MAC Filtering \(White/Black Listing\)
  * Create a list of permitted or denied MAC addresses.
  * Only approved MAC Addresses get access \(requires updating\).
  * Good when there are only specific devices that need access.
* Client Isolation
  * Public wireless SSIDs are normally single broadcast domain.
  * Any connected host can see and hear other connected hosts.
  * Modern APs can create an isolated network that is only between the AP and the client itself which provides security for any connected host.
* Network Authentication
  * By using external authentication servers we can require usernames and passwords to access the wireless network in addition to the regular PSK \(802.1X with EAP, RADIUS, LDAP, etc\)
* DTLS Encryption
  * Datagram Transport Layer Security
  * Provides secure connection between the AP and WLC.
  * Encrypts all management traffic between the AP and WLC.
  * Enabled by default.
  * Data encryption is disabled by default.
  * Data Encryption requires DTLS License installed on WLC.

**ACCESS CONTROL LISTS**

**What's an ACL?**

* ACLs are used with routers, switches, and firewalls.
* With ACLS we can:
  * Add layer 3 and layer 4 security.
  * Protect our network from outside attackers.
  * Control the traffic that passes through our network.
  * Identify those who are allowed in and out.
* The ACL includes those who are permitted and those who are denied.

  
**Rules for ACLs**

* Two step process:
  * 1. Create the Access List
    * Include permissions and denies.
  * 2. Apply the Access List
    * To an interface on the router.
    * Can apply inbound or outbound individually.
* Need at least one permit statement in the list.
  * Otherwise all traffic is denied \(implicit deny\).
* All ACLs are processed from top to bottom.
  * More precise ACL statements go at the top of the list.
  * The last line of the list will always be an implicit deny.
* 1 ACL can be applied per protocol, per interface, per direction.
  * We can apply 1 access list per protocol \(IP or TCP or UDP for example\), per interface \(such as G0/0\), per direction \(as in inbound or outbound\).
  * Thus you can deploy multiple ACLs.
  * Cannot apply an inbound/outbound list multiple times, just one in and one out.

  
**Standard ACL**

* Standard IP ACL Rules
  * Numbered range 1-99.
  * Filtering based on the source only \(where the traffic is coming from\). 
  * Apply the list closest to the destination.
    * This is on the outbound side of the external facing router.
    * Not doing so can unintentionally cut off the source.
* Cisco IOS Commands
  * Create the access list.
    * From Global Configuration Mode \(config\)\#
    * "access-list &lt;1-99&gt; &lt;permit\|deny&gt; &lt;ip address&gt; &lt;wildcard mask&gt;
      * example: access-list 1 deny 192.168.100.0 0.0.0.255
    * The wildcard mask is always the inverse of the subnet mask, so instead of 255.255.255.0 we have 0.0.0.255 here.
      * [https://www.cbtnuggets.com/blog/technology/networking/networking-basics-what-are-wildcard-masks-and-how-do-they-work](https://www.cbtnuggets.com/blog/technology/networking/networking-basics-what-are-wildcard-masks-and-how-do-they-work)
    * Can add as many to a list as necessary.
  * Apply the access list.
    * Apply to an interface:
      * "ip access-group &lt;acl \#&gt; &lt;direction \(in or out\)&gt;"
    * Apply to a Virtual Terminal / Virtual Teletype \(VTY\) line:
      * use a secure shell to connect to router over the line.
      * routers have 5 VTY lines by default \(VTY 0-4\).
      * "access-class &lt;acl \#&gt; &lt;direction \(in or out\)&gt;"

  
**Extended ACL**[https://www.dummies.com/programming/networking/cisco/extended-access-control-lists-acls/\#:~:text=Extended%20Access%20Control%20Lists%20\(ACLs\)%20allow%20you%20to%20permit%20or,you%20to%20be%20very%20specific.](https://www.dummies.com/programming/networking/cisco/extended-access-control-lists-acls/#:~:text=Extended%20Access%20Control%20Lists%20%28ACLs%29%20allow%20you%20to%20permit%20or,you%20to%20be%20very%20specific.)

* Extended IP ACL Rules
  * Numbered range 100-199.
  * Filtering based on the protocol, source, destination, & port.
  * Apply the ACL closest to the source.
    * Not as important as with the Standard ACL because you won't cut off a host from something.
* Cisco IOS Commands
  * 1. Create the access list.
    * From Global Configuration Mode \(config\)\#
    * "access-list &lt;100-199&gt; &lt;permit\|deny&gt; &lt; protocol&gt; &lt;source IP&gt; &lt;wildcard mask&gt; &lt;destination IP&gt; &lt;wildcard mask&gt; eq &lt;port&gt;"
    * Example: Access-list 100 deny tcp 192.168.50 0.0.0.0 0.0.0.0 255.255.255.255 eq 80
      * 0.0.0.0 255.255.255.255 = "any"
      * Any time it is the host, you can type "host" instead of the IP.
  * 2. Apply the access-list
    * "ip access-group &lt;acl \#&gt; &lt;direction \(in or out\)&gt;"
    * "access-class &lt;acl \#&gt; &lt;direction \(in or out\)&gt;
* Show Commands:
  * "show access-list"
  * "show running-config \| include access-list"

