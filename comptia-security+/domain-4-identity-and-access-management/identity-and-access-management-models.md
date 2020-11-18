# Identity & Access Management Models

**Access Control Models**

* _MAC - Mandatory Access Control_
  * Assigning labels to resources and accounts \(objects\).
  * Users and system accounts \(subjects\) are assigned a classification level.
  * Examples: SECRET, CONFIDENTIAL, PROPRIETARY, and PUBLIC
  * Subjects access rights must be above the objects classification.
  * Access is non-discretionary.
  * Used in Government & Military.
  * Rigid and most secure.
  * To determine if a file may be opened:
    * Compare the object and subject labels.
    * Subject must have equal or greater level than object to be granted access.
  * Two major implementations of MAC:
    * Lattice Model
      * Subjects and objects are assigned a 'rung' on the lattice.
      * Multiple lattices can be placed beside each other.
    * Bell-LaPadula Model
      * Similar to the Lattice model.
      * Subjects may not create a new object or perform specific functions on lower level objects.
  * Examples of MAC implementation:
    * Windows 7/Vista has 4 levels.
    * Specific actions by a subject with lower classification require admin approval.
* _DAC - Discretionary Access Control_
  * Access rights at the discretion of the system or info owner / security principal.
  * Owner assigns security access / has flexibility in accessing info or systems.
  * Allows dynamic sharing.
  * Increased risk of unauthorized disclosure or access.
  * Least restrictive model.
  * Every object has an owner.
    * Owners have total control over their objects.
    * Owners can give permissions to other subjects over their objects.
  * DAC weaknesses:
    * Relies on decisions by end users to set proper sec levels
      * Incorrect permissions may be granted.
    * Subject's permissions will be 'inherited' by any program the subject executes.
    * Trojans are a particular problem with DAC.
* _ABAC - Attribute Based Access Control_
  * Defined in NIST 800-162, Attribute Based Control Definition and Considerations
  * Attributes are characteristics that define specific aspects of the subject, object, environment conditions and/or requested actions that are predefined and preassigned by an authority.
  * Considers all of the various attributes associated with the subject and object in making the access control decision.
  * A dynamic access control method.
  * Based on the Extensible Access Control Markup Language \(XACML\)
* _RBAC - Role-Based Access Control_
  * Access control based on established roles or job functions in an organization.
  * Group-based permissions.
  * Reduces effect of permissions creep.
  * Users or subjects are assigned roles under RBAC. 
* _RBAC - Rule-Based Access Control_
  * Uses the settings in preconfigured security policies to make all access decisions.
  * Rule-based access control includes controls such as the time of day, the day of the week, specific terminal access, and GPS coordinates of the requester.
  * Implemented with Access Control Lists \(ACLs\)

![](../../.gitbook/assets/image%20%2814%29.png)

**Best Practices for Access Control**

* Establishing best practices for limiting access.
  * Can help secure systems and data.
* Examples of best practices:
  * Separation of duties.
    * Fraud can result from single user being trusted with complete control of a process.
    * Requiring two or more people responsible for functions related to handling money.
  * Job rotation.
    * System is not vulnerable to actions of a single person.
    * Employees can rotate within their department or across departments.
    * Limits amount of time individuals are in a position to manipulate security configurations.
    * Helps expose potential avenues for fraud.
      * Individuals have different perspectives and may uncover vulnerabilities.
    * Reduces employee burnout.
  * Least privilege.
    * Limiting access to information based on what is needed to perform a job function.
    * Helps reduce attack surface by eliminating unnecessary privileges.
    * Should apply to users and processes on the system.
    * Processes should run at minimum security level needed to correctly function.
    * Temptation to assign higher levels of privilege is great.

![](../../.gitbook/assets/image%20%2816%29.png)

* Implicit deny.
  * If a condition is not explicitly met, access request is rejected.
  * Ex: network router rejects access to all except conditions matching the rule restrictions.
* Mandatory vacations.
  * Limits fraud, because the perpetrator must be present daily to hide the fraudulent actions.
  * Audit of employee's activities usually scheduled during vacation for sensitive positions.

**Access Control Lists \(cont. from** [**{Network Components}**](../untitled/network-components.md)**\)**

* Set of permissions attached to an object.
* Specifies which subjects may access the object and what operations they can perform.
* When subject requests to perform an operation:
  * System checks ACL for an approved entry.
* ACLs usually viewed in relation to operating system files.
* Each entry in the ACL table is called _Access Control Entry \(ACE\)._
* ACE structure \(Windows\)
  * Security identifier for the user or group account or session.
  * Access mask that specifies access rights controlled by ACE.
  * Flag that indicates type of ACE.
  * Set of flags that determine whether objects can inherit permissions.

**Group Policies** 

* Microsoft Windows Feature
  * Provides centralized management and configuration of computers and remote users using Active Directory \(AD\).
  * Usually used in enterprise environments.
  * Settings stored in Group Policy Objects \(GPOs\)
* Local Group Policy
  * Fewer options to configure than a Group Policy.
  * Used to configure settings for systems not part of AD.

**Biometrics**

* Fingerprint Scanner
* Retinal Scanner
* Iris Scanner
* Voice Recognition
* Facial Recognition
* Signature
* Gait \(how fast and how they walk\)
* Signature Dynamics
  * The biometric method that analyzes both the physical motions performed when a signature is signed and the specific features of a person's signature. 
  * It usually captures the speed of the signing, the pressure of th epen, and the way the pen is held. 

**Tokens**

* Physical device used for access.
* Software or hardware based.
* One-Time Passwords \(OTP\)
  * HOTP - HMAC OTP: Uses a hash.
  * TOPT - Time-Based OTP: Limited Time Availability
* Examples: Wireless Keycard, Key Fob, or Any Physical Device
* Contains a digital certificate and/or static password token.

**Physical Access Controls**

* Proximity Cards
  * Hold little info.
  * Determines access by matching the card ID \# to access database info.
* Smart Cards
  * Provides an authenticating crypto key to its reader.
  * May include other info on a programmable chip such as biometrics or certs.
* Both use embedded microchips.

**Certificate-Based Authentication**

* PIV/CAC/Smart Card
* Personal Identity Verification Cards
  * Contactless smart card used by US Federal Workers
* Common Access Card \(CAC\)
  * A credit card sized "smart" card used by US DoD workers.
  * Inserted into a smart card reader authenticated with a PIN.
* IEEE 802.1x
  * Certificate based network authentication.
  * Allows only authorized devices to connect to the network.
  * Allows a company to reduce the exposure of sensitive systems to unmanaged devices on internal networks. 
  * Can be used on wired networks to segment traffic intended for the WAP. 

**File System Security**  
AKA "Flat Files"

* Leverage access controls, encryption, and RAID.
* Microsoft NTFS allows file-level access control where FAT allows only share-level access.
* Consider using encryption for sensitive directories/media.

**Database Security**

* Store organizations most sensitive / critical data.
* Leverage network security & access controls within the Database Management System \(DBMS\)
* Transparent Data Encryption \(TDE\) for data.
* Crypto key management.
* _Data Control Language \(DCL\)_ - implements security through access control and granular restrictions. 

**Database View** 

* Database security feature that provides granular access controls. 
* Used to limit user and group access to certain information based on the user privileges and the need to know.
* Views can be used to restrict information based on group membership, user rights, and security labels.
* Views implement least privilege and need-to-know and provide content-dependent access restrictions.
* Views do not provide referential integrity, which is provided by constraints or rules.
* An example of content-dependent access control in which the access control is based on the sensitivity of information and the user privileges granted. 
  * This leads to higher overhead in terms of processing because the data as granularly controlled by the content and the privileges of users. 
* Can limit user access to portions of data instead of the entire database. 

