# Secure Systems Design

**Hardware / Firmware Security**

* FDE - Full Disk Encryption
  * Bitlocker
    * Works with TPM hardware. 
    * Encrypts drive contents so that data cannot be stolen. 
    * Can encrypt both user and system files. 
    * Enabled/disabled by an admin. 
  * Veracrypt
* SED - Self-Encrypting Drive
  * Has a controller chip built in that automatically encrypts/decrypts a drive.
  * Media Encryption Key \(MEK\)
  * Key Encryption Key \(KEK\) - Supplied by the user.
* Trusted Platform Modules \(TPM\)
  * A specialized chip on an endpoint device that stores encryption keys specific to the host system for hardware authentication. Usually on the system motherboard.
* Hardware Security Modules \(HSM\)
  * A physical computing device that safeguards and manages digital keys for strong authentication and provides crypto processing.
  * These modules traditionally come in the form of a plug-in card or an external device that attaches directly to a computer or network.
* Basic Input/Output System \(BIOS\) - Boot-up configuration.
* Unified Extensible Firmware Interface \(UEFI\) - Modern boot-up configuration, replacing BIOS.
* Secure Boot and Attestation
  * A cryptographic hash of the BIOS/UEFI OS boot loader and drivers that gets compared against a stored hash. This is done to prevent rootkits and boot sector viruses.
* Root of Trust \(RoT\)
  * Highly reliable hardware, firmware, and software components that perform specific, critical functions.
  * A security process that has to begin with some unchangeable hardware identity often stored in a TPM.
* Supply Chain - Confirming the origin of hardware is secure.

**Operating System Types**

* Network
* Server
  * Windows
  * Linux
* Workstation
* Appliance \(AKA IoT\) - Limited to a specific purpose.
* Kiosk - Public Computer
* Mobile OS

**Operating System Security**

* Trusted Operating System/Baseline
* Secure Configurations
* Least Functionality / Single Purpose
* Disabling Unnecessary Ports and Services
* Disable Default Accounts & Passwords
* Application White & Blacklisting
* Patch Management Process
  * Patch - A set of changes to a computer program or its supporting data designed to update, fix, or improve it. This includes fixing security vulnerabilities and other bugs.
  * Hotfixes - Small, specific-purpose updates.
  * Service Pack - A collection of hot fixes that have been combined.
  * Updates - Provides more comprehensive improvements for features, additional security, or adds software enhancements and compatibility.
  * Upgrades - New version of the software.

**Operating System Hardening**

* Secure Configurations
* Trusted Operating Systems
* Least Functionality
* Application White & Blacklisting
* Disable Default Accounts & Passwords
  * Windows Guest Account
  * Changing Account Names
  * Routers / Switches
* Disabling Unnecessary Ports and Services
  * There are 65,535 TCP and UDP ports. These ports are divided into three ranges:
    * 0-1023 \(Well Known\)
    * 1024-49151 \(Registered\)
    * 49152-65535 \(Dynamic/Private\)
  * Common Ports:
    * 80 - HTTP
    * 443 - HTTPS
    * 21 - FTP
    * 22 - FTPS / SSH
    * 110 - POP3
    * 995 - POP3 SSL
    * 143 - IMAP
    * 992 - IMAP SSL

**Peripherals**

* Wireless Keyboards & Mice
* Displays
* WiFi-enabled MicroSD Cards
* Printers/MFDs
* External Storage Devices
* Mobile Devices/Smartphones
* Digital Cameras

**Demilitarized Zone \(DMZ\)**

* You should implement every computer on the DMZ as a _bastion_ host because any system on the DMZ can be compromised. 
* _Bastion -_ A special-purpose computer on a network specifically designed and configured to withstand attacks. 
  * The computer generally hosts a single application, such as a proxy server, and all other services are removed or limited to reduce the threat to the computer. 

