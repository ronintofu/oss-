# Module 2 - Cryptography

**Crypto Basics**

**What is Cryptography?**

* The art of protecting information by transforming it into an unreadable format.
* Since ancient times, people have relied on cryptography to keep their secrets secure.
* Evolution:
  * Scytale Cipher - 7th Century BCE
  * Caesar Shift Cipher - 1st Century CE
  * Steganography
  * Pigpen Cipher - 1500s
  * Enigma Code - 1920s
    * Cracked by Alan Turing
  * Data Encryption - 1970s

**Why is it important?**

* Due to the large number of transactions on the internet, cryptography is key in ensuring the security of transactions.
* Cryptography makes secure web sites and safe electronic transmissions possible.
* For a web site to be secure, all of the data transmitted between the computers must be encrypted.

**Encryption/Decryption**

* Encryption - The process of converting data into a code, especially to prevent unauthorized access.
* Decyryption - Converting of encrypted data into its original form. Decoded such that only authorized users can decrypt data \(requires secret key/password\).

![](https://www.evernote.com/shard/s342/res/a11bf7a9-f02d-474c-0ccf-8fb7cfe2defa)  
**Authentication**

* Authentication is used to confirm that:
  * A Message is from the stated source \(who they say they are\).
  * The integrity has not been changed or altered.

**Integrity**

* Meant to provide assurance that data has not been modified in an unauthorized manner after it has been created, transmitted, or stored.

**Non Repudiation**

* Assurance that an entity cannot deny the validity of something.
* Makes it difficult to successfully deny who/where a message came from as well as its authenticity.

**Crypto Methods**

**Symmetric Keys**

* This type of cryptography uses a shared key between parties.

![](https://www.evernote.com/shard/s342/res/fb9bed6b-729c-c45d-0e6a-50dcc671ed70)

* Symmetric encryption is efficient and scales well, but difficult to distribute keys.
* Encryption is done in 2 ways:
  * **Stream Ciphers** - Digits/letters encrypted one at a time.
  * **Block Ciphers** - Encrypts a number of bits as a single unit.

![](https://www.evernote.com/shard/s342/res/2ee80889-a775-40ab-ce94-2b61c292a45c)  
**Asymmetric Keys**

* Uses both a public key and a private key.

![](https://www.evernote.com/shard/s342/res/4b8c20ea-7496-a8c4-a10b-7ae63b5a66dc)

* Many secure protocols we use today are based off of this.
  * SSH
  * SSL
  * TLS
* **Keypair** - A pair of keys where a private key is linked to a known public key.
* **Digital Signatures** - Essentially signatures that provide integrity using asymmetric cryptography.

![](https://www.evernote.com/shard/s342/res/a7b29f8a-cd5e-897e-698b-394d414d9162)  
**Hashing**

* A method of cryptography that converts any form of data into a unique string of text.
* A hash is designed to act as a one-way function.
* A unique piece of data will always produce the same hash.
* The most widely used hashing functions are MD5, SHA1, & SHA-256

**Associated at the Integrity level of cryptography.  
Rainbow tables work to break hashing.  -** [https://www.geeksforgeeks.org/understanding-rainbow-table-attack/](https://www.geeksforgeeks.org/understanding-rainbow-table-attack/)  
![](https://www.evernote.com/shard/s342/res/16cdc84e-da2c-2b36-3f53-015a3f8ba804)  


* Who uses hashing?
  * The average user encounters hashing daily in the context of passwords.
  * When you create an account and password, your provider likely does not save your password; it saves the hash.
  * Every time you try to log in, they compare the hash to the one they have saved. When both match, you are authorized to access the account.

![](https://www.evernote.com/shard/s342/res/a09b5cb9-fa5a-6df7-af93-89c867d38c86)

* Hashing & Cybersecurity - When an organization has been compromised, it typically means that hackers have acquired the hashes that represent the passwords.
* Hackers then run the hashes of common words & combinations to decipher some of the passwords that users have saved.
* Salting is adding random data to a password before hashing it, then storing that "salt value" with the hash.
  * This process makes it harder for hackers to crack passwords of hashed data that they have acquired.

![](https://www.evernote.com/shard/s342/res/34d222a9-47cb-1b5f-b47a-93a6755702a6)  
**Session Keys**

* Single use symmetric keys that are used for encrypting all messages in one communication session.
* Sometimes generated after an asymmetric session is started to provide further security.

**Kerckhoff's Principle**

* A cryptographic system should be secure even if everything about the system, except the key, is public knowledge.
* Kerckhoff's principle is applied in virtually all contemporary encryption algorithms \(DES, AES, etc\).

**Algorithms: RSA vs Diffie-Hellman vs PGP**  
[https://learn.nexgent.com/modules/cyber-security-specialist-module2/sections/cyber-security-specialist-module2-section3/lessons/cyber-security-specialist-module2-algos](https://learn.nexgent.com/modules/cyber-security-specialist-module2/sections/cyber-security-specialist-module2-section3/lessons/cyber-security-specialist-module2-algos)

**Algorithms**

* Cryptography, at its very core, is math.
* Math created the algorithms that are the basis for all encryption.
* Encryption is the basis for privacy and security on the internet.
* A cryptographic algorithm is a set of well-defined but complex mathematical instructions used to encrypt or decrypt data.

**Random Number Generator**

* An RNG is a device that generates a sequence of numbers that can not be reasonably predicted.
* Essential to cryptography: key generation, nonces, salts.
* No known way to produce true random numbers, especially in finite state machines.

**Diffie-Hellman**

* A way of generating a shared secret between two parties.
* Done in such a way that the secret cannot be seen by observing the communication.

![](https://www.evernote.com/shard/s342/res/75e0b1be-1867-9f02-2bfa-f603d8380ba1)![](https://www.evernote.com/shard/s342/res/f4ef3094-aca8-702d-2759-e06a6baf2d31)  
**RSA**

* Asymmetric cryptography algorithm that involves 4 steps:
  * Key Generation
  * Key Distribution
  * Encryption
  * Decryption

1. A client \(i.e browser\) sends its public key to the server and requests some data.
2. The server encrypts the data using client's public key & sends the encrypted data.
3. Client receives this data and decrypts it.

![](https://www.evernote.com/shard/s342/res/1606893e-0e63-1c0a-8070-00e02050f2a2)

* The security of RSA depends on how it is implemented and used.
* One important factor is the size of the key.
  * The larger the number of bits in a key, the more difficult it is to crack.
    * The largest key size that has been factored/cracked is 768 bits long. NIST recommends 2048bit - 2096bit keys are also used. 
* You can not derive public keys from a private key, nor vice versa \(it's mathematically impossible\).
* To make things more efficient, a file will generally be encrypted with symmetric-key algorithm, and then the symmetric key will be encrypted with RSA encryption.
  * Under this process, only an entity that has access to the RSA private key will be able to decrypt the symmetric key.

**PGP** - Pretty Good Privacy

* Data encryption program that gives cryptographic privacy and authentication for online communication.
* Used to encrypt/decrypt texts and emails \(a standard today\).

![](https://www.evernote.com/shard/s342/res/0189b505-40d3-1bf1-b608-3d75bc2e091d)

**Public Key Infrastructure**  
[https://learn.nexgent.com/modules/cyber-security-specialist-module2/sections/cyber-security-specialist-module2-section3/lessons/cyber-security-specialist-module2-pki](https://learn.nexgent.com/modules/cyber-security-specialist-module2/sections/cyber-security-specialist-module2-section3/lessons/cyber-security-specialist-module2-pki)

**What is PKI?**

* The framework of encryption that protects communications between the server and the clients.

![](https://www.evernote.com/shard/s342/res/5a20281c-2ca2-ce0d-ef00-5d61c3fb696f)  
The user's public key can only decrypt files. It cannot be used to encrypt anything. It can only decrypt items that have been encrypted with the corresponding private key.![](https://www.evernote.com/shard/s342/res/19792767-b618-6d36-743a-e19ddb8e2c18)  


* The public key is available to any user that connects to the website.
* The private key is a unique key generated when a connection is made.
* When communicating, the client uses the public key to encrypt/decrypt and the server uses the private key. This protects the user's information from theft or tampering.
* Primarily used for encrypting/signing data.
* Encrypting scrambles it in a way that makes it readable to only authorized entities.
* Signing data is a way to authenticate.

**How Does PKI Work?**

* Follows typical asymmetric protocol but expands on it with Certificate Authority & Registration Authority
* Certificate Authority \(CA\) - Provides assurance about the parties identified in a PKI Certificate.
  * [https://www.ssl.com/faqs/what-is-a-certificate-authority/](https://www.ssl.com/faqs/what-is-a-certificate-authority/)
* Registration Authority \(RA\) - A subordinate to the CA, is the one who issues out the PKI Certificate.

This provides a "Chain of Trust" and essentially gives the system a system of 'checks and balances'.![](https://www.evernote.com/shard/s342/res/85aa73a3-470f-35fe-ccd9-cfe250fdac52)  


* PKI is based on a mechanism called 'digital certificate'.
  * Think of certificates as virtual ID cards.
* X.509 is a widely accepted international format.

![](https://www.evernote.com/shard/s342/res/121f753d-9a28-dd3a-3190-eeba5f8671b5)  
A secure session is established because two machines can present one another with their respective certificates.

**Security Limitations**

* PKI provides chain of trust so that identities on a network can be verified.
* A PKI is only as strong as its weakest link.
* If one CA is compromised, the security of the entire PKI is at risk.

Certification Authority Browser Forum \(CA Browser Forum\)  
![](https://www.evernote.com/shard/s342/res/e22b267c-0870-6a46-62a2-eb565d792aab)  
  


**Attacks**

**Cryptography Attacks - What They Are**

* In cryptography, the goal of the attacker is to break the secrecy of the encryption and learn the secret message and/or the secret key.
* There are dozens of different types of attacks that have been developed against different types of cryptosystems with varying levels of effectiveness.

**Passive Attacks**

* The main goal of a passive attack is to obtain unauthorized access to the information.
* Actions such as intercepting and eavesdropping on the communication channel can be regarded as passive attack.

![](https://www.evernote.com/shard/s342/res/741848d1-3e69-d7b5-b22a-516b9493e9de)  
May go unnoticed which means the original recipient or owner of the data may still think the data is secure.  
**Active Attacks**

* Involves changing the information in some way by conducting some process on the information.
  * Modifying the info in an unauthorized manner.
  * Initiating unintended or unauthorized transmission of information.
  * Alteration of authentication data such as originator name or timestamp associated with information.
  * Unauthorized deletion of data.
  * Denial of access to information for legitimate users \(denial of service\).

![](https://www.evernote.com/shard/s342/res/1cd46290-5afd-c8b7-d1da-6d5cd14e867b)  
**Types of Attacks**

* In cryptography, the following three assumptions are made about the security environment and the attacker's capabilities:
  1. Details of encryption scheme \(public vs propriety algorithms\).
  2. Availability of plain text cipher text.
  3. Cryptographic attacks.
* Brute Force Attack:
  * Attacker tries to decrypt the message with each possible secret key and checks the result.
  * Modern ciphers protect themselves against brute force attacks by using a large secret key \(makes guess all of the possibilities impossible\).
  * The longest available key length of the AES cipher is 256 bits, which means there are 2256 possible AES keys.
    * There are an estimated 2266 atoms in the observable universe.
* Man-in-the-Middle Attack:
  * The MitM attack assumes that an attacker can insert themselves in the communication channel between the sender and receiver.
  * When the sender sends a message to the recipient, the attack intercepts it before it reaches its destination.
  * In a successful MitM attack, the attack can decrypt the intercepted message, read it, and possibly modify it, then pass it to the originally intended recipient.
* Replay Attack:
  * Attacker replays a valid session between a legitimate user and some form of server.
  * In this attack, the attacker captures every piece of traffic between the user and server during normal operation.
  * The attack then resends the first piece of traffic and waits for the server's response before sending the next piece and so on.
  * If the server does not implement protection against replay attacks, the attacker may achieve a valid session with the server masquerading as the original user.
  * To protect against replay attacks, many people who use ciphers in daily life \(like the server\) will generate a random number to be included in each session - a nonce.

![](https://www.evernote.com/shard/s342/res/679419a9-c7f9-9fa2-def2-193ee3eb7f08)

* Side Channel Attack:
  * Attacks that use unintended side effects of cryptographic operations to glean information about the plaintext and/or secret key being processed.
  * Two types: Power Analysis and Timing Attacks.
* Power Analysis Attack:
  * The amount of power used and how long the power is used for can vary based on the operations performed.
  * When a cryptographic algorithm is being run on a computer, this may reveal information about the data being processed by the algorithm.

![](https://www.evernote.com/shard/s342/res/7cca52f4-43b6-4be5-7770-62611ad7f37c)

* Timing Attack:
  * A timing attack on a cryptographic algorithm exploits the fact that the algorithm may take different amounts of time to run with different plaintexts or secret keys.

![](https://www.evernote.com/shard/s342/res/c9ab8d6d-2139-848b-5752-d5982ba84abf)  
**Practicality**

* The attacks on cryptosystems described here are highly academic, as a majority of them come from the academic community.
* The fact that any attack exists should be a cause of concern.

![](https://www.evernote.com/shard/s342/res/49ba9323-c9cc-e20c-18ef-57fec41e3c9c)

