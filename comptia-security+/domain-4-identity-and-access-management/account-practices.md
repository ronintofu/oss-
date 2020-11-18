# Account Practices

**General Concepts**

* On-boarding/off-boarding.
* Standard naming convention for user IDs.
* Least privilege.
* Time-of-day restrictions.
* Location-based policies.

**Account Types**

* _User Accounts_ - issued to users for authentication.
* _Guest Accounts_
  * Should be disabled by default with minimal privileges and time limits.
  * Issued on a temporary basis and usually have an expiration date.
* _Shared and Generic Accounts_
  * No repudiation.
  * Examples: conference rooms, kiosk computer.
  * Restrict as much as possible.
* Change the names of default system accounts.

**Account Types**

* Service Accounts
  * Used by systems/apps
  * Restrict human use.
  * Restrict access rights/authorization.
  * Set a complex password.
* Privileged Accounts / Admin Accounts
  * Each user should have a separate admin account.
  * Types: Windows Admin & Linux Root.
  * Run as a general user and only increase privileges as needed.
    * Windows UAC \(User Access Account\)
    * Linux Sudo
  * Restrict authorization & increase logging.

**Account Restrictions**

* Time of Day Restrictions
  * Limits the time of day a user may log onto a system.
  * Time blocks for permitted access are chosen.
  * Can be set on individual systems.
* Account Expiration
  * Orphaned accounts: accounts that remain active after an employee has left the organization.
  * Dormant accounts: not accessed for a lengthy period of time.
  * Both can be security risks.
  * Account expiration can be a set date or number of days of inactivity.
* Recommendations for dealing with orphaned or dormant accounts:
  * Establish a formal process.
  * Terminate access immediately.
  * Monitor logs.
* Orphaned accounts remain a problem in today's organizations.
* Password expiration sets a time when the user must create a new password.

**Account Policy Enforcement**

* Credential Management
* Group Policy
* Password Policies / Complexity
* Expiration
* Recovery
* Disablement / Locking

**Password Policies**

* _Password History_
  * Allows you to configure how many new passwords must be created before an old one can be reused. 
  * This setting enhances security by allowing the administrators to ensure that old passwords are not being reused continually. 
  * Reused passwords are sometimes referred to as rotating passwords. 
* _Password Age_
  * Allows you to configure the minimum or maximum number of days that must pass before a user is required to change the password. 
  * It is a good security practice to enforce a password age of 30 to 60 days. 
  * Some companies force users to change their passwords monthly or quarterly. 
  * This interval should be determined based on how critical the information is and on how frequently passwords are used.
* _Password Length_
  * Allows you to configure the minimum number of characters that must be used in a password. 
  * At minimum, this policy should be configured to 7 or 8 characters. 
* _Password Lockout_
  * Allows you to configure the number of invalid logon attempts that can occur before an account is locked. 
  * Also allows you to configure the number of days that the account remains in this state. 
  * You may want to configure the account lockout policy so that an admin must be contacted to enable the account again. 
* _Password Complexity_
  * Allows you to configure which characters should make up a password to reduce the possibility of dictionary or brute force attacks. 
  * A typically password complexity policy forces a user to incorporate:
    * Numbers
    * Letters
      * Upper & Lower Case
    * Special Characters

**Password Weaknesses**

* Weakness of passwords is linked to human memory.
  * Humans can only memorize a limited number of items.
  * Long, complex passwords are most effective but also the most difficult to memorize.
* Users must remember passwords for many different accounts.
* Security policies mandate passwords must expire.
  * Users must repeatedly memorize passwords.
* Users often take shortcuts.
  * Using weak passwords.
  * Reuse the same password for multiple accounts.
    * Easier for an attacker who compromises one account to access others.

**Password Defenses**

* Creating strong passwords.
* Most passwords consist of:
  * Root
  * Attachment
* Attack Program Method
  * Tests password against 1000 common passwords.
  * Combines common pws with common suffixes.
  * Uses 5000 common dictionary words, 10000 names, 100000 comprehensive dictionary words.
  * Makes common substitutions for letters in the dictionary words.
* General observations to create a strong pw:
  * Do not use dict or phonetic words, birthdays, fam or pet names, or other personal info.
  * Do not use short passwords.
* Managing passwords:
  * Prevent an attacker from obtaining the encrypted pw file.
  * 

