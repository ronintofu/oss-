# Security Technologies

**Host Technologies - Firewalls**

* Firewalls
  * Windows: type 'wf.msc' at cmd.
  * Linux Uncomplicated Firewall: 'ufw' or 'iptables'.
* Firewall Configuration
  * End users shouldn't be allowed to disable the firewall.
  * Monitor both incoming and outgoing network traffic.
* Output depends on the FW applications and OS:
  * Windows Event Viewer
  * Linux logging: /var/log

**Host Technologies - HIDS/HIPS**

* Sensors on each host relay to a centralized management console.
  * Compiles data to identify distributed trends.
* May be included with Host Firewall or AV solution.
* Consult Documentation.
* Issues:
  * False positives - legit traffic labelled as an attack.
  * False negatives - attacks labelled as legit traffic.
  * Matching traffic identified as an attack with the actual network traffic.
* NIST SP 800-94 - Guide to Intrusion Detection and Prevention Systems \(IDPS\)

**Antivirus & Anti-Malware**

* Windows Defender
* End-user pop-up warning.
* Centralized management console warning.
* Quarantine vs Removal.
* Issues:
  * AV not updated or has outdated signatures.
  * False positives.
  * May be ignored or not seen.
  * Incorrect decision.
  * Malware may still be present.
*  Solutions:
  * Auto-update \(need network connectivity\).
  * Detach system from the network.
  * Use multiple AV products.
  * Manual removal - hunting malware with SysInternals
  * Reimage the system.

**File Integrity Checker**

* Computers a cryptographic hash for all selected files and creates a database of the hashes.
* Hashes are periodically recalculated and compared to the hashes in the database, to check for modification.
* Output to a centralized server.
* For alerts, determined what changed and why.
* Example: Tripwire

**Application Whitelisting**

* Organization approves software apps. All others are not allowed.
* Example: Windows AppLocker
* Based on conditions:
  * Publisher, for digitally signed files.
  * Path, which identifies an application by its location.
  * File hash, which uses a system-computed cryptographic hash.

**Data Loss Prevention \(DLP\)**

* Prevent sensitive info from physically or logically leaving corporate systems.
* Designed to detect and prevent unauthorized use and transmission of confidential info.
* Should include corporate data stored in the cloud.
* Network: Content-filtering \(proxy\).
* System: Application white-listing.
* Hardware: USB blocking.

**Removable Media Control**

* Detects or prevents the use of removable media.
* Local or network.
* Set by corporate policy.
* Exception handling.
* Use only corporate owned / secured devices.
* Scan removable media on each use.
* Encryption.

**Patch Management**

* Automate updates when possible.
* Patching process:
  * Vendor notification.
  * Testing.
  * Staged deployment.
  * Reporting.
* Alerting on failed patches.
* Patching all apps / systems.

**Patch Management Services**

* Microsoft System Center Configuration Manager \(SCCM\) formerly Systems Management Server \(SMS\)
* Linux RPM \(Red Hat Package Manager\)

**Data Execution Prevention \(DEP\)**

* Hardware or Software.
* Prevents malware from executing in memory space that is reserved for operating system processes.
* Both Advanced Micro Devices \(AMD\) and Intel platforms have DEP hardware capabilities.
* Available on Windows 10.

