# Application Cryptography Attacks

**Application Attacks**

* Buffer Overflow:
  * When more data is written to a buffer than it can hold.
  * An anomaly where a program, while writing data to a buffer, overruns the buffer's boundary and overwrites adjacent memory locations.

![](https://www.evernote.com/shard/s342/res/ac0cd724-a61c-703c-d5d7-f184772d5747)

* Injection:
  * Occurs when untrusted data is sent to an interpreter as part of a command or query.
  * The most common fall into the following categories:
    * Escape characters not filtered correctly.
    * Type handling not properly done.
    * Conditional errors.
    * Time delays.
  * The way to defend against this attack is always to filter input.
  * Examples: SQL Injection, OS, LDAP, XML.
    * Command Injection: when an operating system command is submitted in an HTML string. 
* Cross-Site Scripting \(XSS\): Occurs whenever an application includes untrusted data in a new web page without proper validation or escaping, or updates an existing web page with user-supplied data using a browser API that can create HTML or JavaScript.
  * Example: Ron&lt;SCRIPT&gt;alert\('hello'\)&lt;/SCRIPT&gt;Woerner
* Cross-Site Request Forgery \(CSRF/XSRF\): An attack that forces an end user to execute unwanted actions on a web application. Also known as a 'session riding' or 'one-click' attack.
* Privilege Escalation: The act of exploiting a bug, design flaw, or configuration oversight in an operating system or software application to gain elevated access to resources that are normally protected from an application or user.

**Prevention & Response**

* Good coding practices - See OWASP.
* Filter and validate any user input.
* Use a Web Application Firewall \(WAF\).
* Build security into the Software Development Life Cycle \(SDLC\).
* Have an incident response plan in place.

**Zero-Day \(0-Day\) Exploits**

* An attack that exploits a previously unknown security vulnerability.
* It may take advantage of a security vulnerability on the same day that the vulnerability becomes generally known.
* Example: Stuxnet
* Prevention:
  * Defense-in-Depth.
  * Patch & Update.
  * Keep AV up-to-date.

**Impersonation / Masquerading / Replay Attacks**

* The act of pretending to be someone or something to gain unauthorized access to a system.
* Capturing network traffic via eavesdropping, then re-establishing a communications session by replaying captured traffic using spoofed authentication credentials.
* Prevention:
  * Token Authentication \(Kerberos\)
  * MFA/TFA
  * Encryption
  * Sequenced Session Identification

**Driver Manipulation**

* Driver: A program that controls a device such as printers, media, keyboards, etc. They are usually signed.
* Shimming: Creating a library, or modifying an existing one, to bypass a driver and perform a function other than the one for which the API was created.
* Refactoring: Set of techniques used to identify the flow and then modify the internal structure of code without changing the code's visible behavior.

**Cryptographic Attacks**

* Birthday: An attack on cryptographic hash that looks for hash collisions - exploiting the 1-to-1 nature of hashing functions.
* Known Plain Text/Cipher Text: An attacker attempts to derive a cryptographic key by using pairs of known plain text along with the corresponding cipher text.
* Frequency Analysis: Looking at the blocks of an encrypted message to determine if any common patterns exist.
* Password Attacks:
  * Dictionary: Systematically entering each word in a dictionary as a password.
  * Brute Force: Systematically attempting all possible combinations of letters, numbers, and symbols. Usually automated.
  * Rainbow Tables: All of the possible password hashes are computer in advance and those hash values are compared with the password database.
  * Pass the Hash: An attacker attempts to authenticate to a remote server or service by intercepting password hashes on a network.

