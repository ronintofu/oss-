# WiFi Security

**Wireless Access Methods**

* Open Authentication - Only need to know the network name/SSID.
  * Captive Portal - Web page that is launched first when connecting through a network.
* Shared Authentication
  * The client and the wireless access point must negotiate and share a key prior to initiating communications.
  * Pre-Shared Key \(PSK\) - Each user uses the same key to connect to the WiFi.
* Enterprise
  * A server handles distribution of cryptographic keys and/or digital certificates.
  * Extensible Authentication Protocol \(EAP\)

**WiFi Protected Setup \(WPS\)**

* Standard to simplify Wireless Access Point \(AP\) setup for home users.
* Three modes:
  * PIN Entry
  * Push-Button Configuration \(PBC\)
  * Near Field Communicaiton \(NFC\)

**Wireless Cryptographic Protocols**

* Wired Equivalent Privacy \(WEP\) - This original wireless encryption standard should not be used today.
* WiFi Protected Access \(WPA\) - WPA was developed in response to security concerns over WEP.
* WiFi Protected Access Version 2 \(WPA2\)
  * Required for WiFi certified devices.
  * Uses AES for encryption.
  * Based on the IEEE 802.11i standard.

**WiFi Protected Access 2 \(WPA2\)**

* Counter Mode with Cipher Block Chaning Message Authentication Code Protocol \(CCMP\)
  * Replaced TKIP
  * Based on AES encryption cipher.
  * CCM combines CTR for confidentiality and CBC-MAC for authentication and integrity.
* Fully implements the IEE802.11i-2004 WiFi security standards.

**Authentication Protocols**

* Extensible Authentication Protocol \(EAP\)
  * Requires an authentication server.
  * Allows authentication methods beyond username/password.
  * Provides support for public certificates.
  * Four modes:
    * PEAP - Protected EAP
    * EAP-TLS - EAP-Transport Layer Security
    * EAP-TTLS - EAP Tunneled Transport Layer Security
    * EAP-FAST - EAP Flexible Authentication via Secure Tunneling

![](https://www.evernote.com/shard/s342/res/d7b9f4d4-4288-0f88-c0ed-fd51ef52d001)

* IEEE 802.1x
  * The IEEE standard for port-based network access control.
* RADIUS Federation
  * A group of RADIUS servers that assist with network froaming. 
  * The servers will validate the login credentials of a user belonging to another RADIUS server's network. 
  * Using RADIUS to authenticate between entities.
  * As part of PEAP negotiation, client establishes a TLS session with a RADIUS server.
  * Client authenticates with RADIUS server.

