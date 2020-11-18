# Forensics

**Strategic Intelligence / Counterintelligence**

* Gathering of info / data regarding an incident.
  * Intelligence gathering deals with collecting information to be used during prosecution as well as locating information that may be used by the opposition against you.
* Nature of the threat actor, source, or vector.
* Pull from multiple data sources \(internal and external\).
* Use of active logging.

**Order of Volatility**

* The order for collecting evidence.
* Volatile data is easily or quickly lost.
  * Resident computer memory.
  * Caches/temp storage.
  * Physical Media \(USB\)
* Capture data that will be lost first.
* Accomplished during incident identification.

**Chain of Custody**

* Provides a clear record of the path evidence takes from acquisition to disposal.
* Any items taken must be secured to preserve its integrity.
* Documentation / Tracking Form
* Evidence must be:
  * Admissible
  * Authentic
  * Complete
  * Reliable
  * Believable

**Legal Hold**

* Preservation on all forms of relevant information when litigation is reasonably anticipated.
* A request to not destroy what might be relevant to a legal matter.

**Data Acquisition**

* Capture System Image
  * A system image is a snapshot of what exists.
  * Capturing an image of the operating system in its exploited state.
    * Legal
    * Helpful in revisiting the issue after the fact to learn more about it.
  * Performed in several ways:
    * Disk to disk - physical media, original to copy.
    * Disk to an image file - physical to logical \(VM\).
    * Image file to a disk - logical to physical.
  * Use of write-blockers on original media.
  * Tools:
    * Encase
    * Forensics
    * Toolkit
    * Native Linux 'dd'
  * Copying Disks
    * A bit-level copy of the disk proves helpful in forensic investigation.
      * Making a copy at the sector level to cover every part of the area that can store user data, such as slack and free space.
* Network Traffic & Logs
  * Capture logs from static network systems.
    * Virtual machines
    * Firewalls, IDS, VPN, Routers, Switches
    * Servers
    * Access
    * Security Incident & Event Management \(SIEM\) / Centralized Logging Systems
  * Active Network Scanning \(on live systems\).
    * Wireshark
* Record Time Offset
  * Coordinating time to accurately track events.
  * NTP - Network Time Protocol: Synchs Time
  * Time Zone Differences
* System Hashes
  * Hash - Unique 'fingerprint' of system files or data.
  * Tracks integrity or any changes - the hash value will change if the file changes.
  * The National Software Reference Library \(NSRL\) is to collect 'known, traceable software applications' through their hash values and store them in a Reference Data Set \(RDS\).
    * [https://www.nsrl.nist.gov](https://www.nsrl.nist.gove)
* Screenshots
  * Images on a computer screen.
  * Tools: Alt+PrtScn buttons, Windows Snipping Tool or Snag-It
  * Used as evidence.
* Interview Witnesses
  * Liust of people contacted or asked about the incident.
  * Who you interviewed, including their names, contact info \(email, phone, address\), and what they saw \(when, where, and how\)
  * Should be conducted with legal and/or HR.

**Documentation / Track Hours**

* Document everything.
* Written narrative.
* When and what was done.
* Evidence.
* Images.
* Pictures / Video
* Calculating the number of man-hours and other related expenses.

