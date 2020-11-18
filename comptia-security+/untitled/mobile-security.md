# Mobile Security

**Mobile Devices**

What is a mobile device?  
Any easily transportable computing system.

* Laptops
* Tablets
* Hybrids
* Smartphones
* Watches
* IoT

**Connection Methods**

* Cellular Communications
  * Components
    * The cellular layout \(towers\).
    * The base station \(connects to the tower\).
    * The mobile switching office \(centerpiece of the operation\).
    * The public switched telephone network \(PSTN\).
  * Voice Technologies
    * Long-Term Evolution \(LTE\)
    * Code Division Multiple Access \(CDMA\)
    * Global Systems Mobile \(GSM\)

![](https://www.evernote.com/shard/s342/res/ea9fb374-a769-712e-3902-04d11537dbd9)

* WiFi
* Bluetooth
  * Personal Area Network \(PAN\) - short-range wireless connectivity.
  * Uses a spread spectrum, frequency hopping, full-duplex signal.
  * Pairing devices forms a piconet.
  * Bluesnarfing/Bluejacking attacks.
  * If needed, set to non-discoverable.
* NFC - Near Filed Communications
  * Standards for contactless communication between devices.
  * Chips generate electromagnetic fields.
  * Modes of operation:
    * Peer-to-peer mode: two mobile devices exchange data.
    * Read/write mode: an active device receives data from a passive device.
    * Card emulation: the device is used as a contactless credit card.
* SATCOM - Satellite Communications
* ANT - Proprietary multicast wireless.
* Infrared - Using light in the infrared spectrum.
* USB / Firewire

**Mobile Device Management \(MDM\)**

* The administration of mobile devices in an organization.
* Software used to inventory, monitor, manage, and secure employees' mobile devices, deployed across multiple mobile service providers and across multiple mobile operating systems.
* Device enrollment, provisioning, and inventory.
* Configuration management / updating.
* Managing applications.
* Enforcing policies.

**MDM Capabilities**

* Mobile Application Management \(MAM\)
  * Restricting applications.
  * Digitally signing applications.
  * Distribution from a centralized, controlled source.
  * Managed through whitelisting or blacklisting.
* Mobile Content Management \(MCM\)
  * Controlling access to data and file storage.
* Push Notification Services
  * Brief message or alert.
  * Operating system push notification service \(OSPNS\)
  * Allows auto-updating base OS and client apps.

**MDM Concepts**

* Separate personal and business content.
* Storage Segmentation
  * Segregate business and personal storage.
* Containerization
  * Separate sensitive corporate info from the user's personal use of the device.
  * Ability to isolate apps & control app functions.
* Remote Wipe / Sanitation
  * Sending a command from the centralized management server to remotely clear data.
  * Used when device is lost, stolen, or the employee terminates.
* Geolocation
  * Uses the devices' GPS
  * Some apps \(Maps, Foursquare, etc\)
* Geofencing
  * Defining a geographic perimeter.
  * Example: texting in the front seat of a car.
* Full Device Encryption
  * System and application level options.
  * Use TPM when available \(laptops\).
* Screen locks or 'lockout'
  * Screen configured to automatically lock after a set amount of time.
* Passwords and Pins
  * Based on corporate policy.
* Biometrics
* Context-Aware Authentication
  * Additional criteria used for authentication or device usage.
  * Examples:
    * Location
    * Time
    * Activity

**Deployment Models**

* BYOD - Bring Your Own Device
  * Employees use own personal device.
  * Highest risk.
  * Adherence with company policies can be a challenge.
* CYOD - Choose Your Own Device
  * Employees choose from a list of approved devices.
* COPE - Company-Owned Provided Equipment
  * Company has complete control over the device.
* VDI - Virtual Desktop Infrastructure

**Enforcement & Monitoring**

* Third-Party App Stores
  * Restrict based on policy.
  * Whitelist applications.
* Rooting \(Android\) / Jailbreaking \(Apple\)
  * User takes full control of the device \(root\).
  * Should be forbidden for corporate devices.
* Sideloading
  * Transfer data between two devices - side-channel.
* USB On-the-Go \(OTG\)
  * Standard that enables mobile device communication using a USB cable.
* Custom Firmware
  * Valid use: forensics acquisition.
  * Invalid: bypass policy.
* Carrier Unlocking
  * Modifying device to use different cell carrier without having to purchase a new device.
  * Now legal in the U.S. 
* Firmware OTA Updates
  * Automatically update device when attached to corporate WiFi or computers.
  * Users may have no control of updates.

**Garmin ANT {source}**

* A proprietary \(but open access\) multi-cast wireless sensor network tech designed and marketed by ANT Wireless \(a division of Garmin Canada\).
* Primarily used for sports and fitness sensors.



