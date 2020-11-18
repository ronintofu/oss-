# Cryptography Concepts

**Encoding vs Encrypting**

* Encrypting data is the method by which plaintext or any other type of data is converted from a readable for to an encoded version that can only be decoded by another entity if they have access to a decryption key.
* Encoding data is the process of transforming data from one form into another form using a known algorithm so that it can be reversed easily.
  * no key is required
  * Used to change human text into machine text \(e.g. ascii\)

**Cryptography Definitions**

* _Cryptography_ - the process of converting ordinary plain text into unintelligible text and vice-versa. It is a method of storing and transmitting data in a particular form so that only those for whom it is intended can read and process it.
  * Confusion
    * A technique where the relationship between the components of the message - the plain text, the key used, and the cipher text - is difficult to see.
  * Diffusion
    * A cryptographic technique whereby a change of a single input results in a change of multiple output bits.
* _Algorithm_ - a process or set of rules to be followed in calculations or other problem-solving operations.
* _Keys_ - secret value used with an algorithm to encrypt and decrypt messages.
* _Kerckhoff's Principle_ - "Only secrecy of the key provides security."

**Symmetric Encryption**

* Same key for both encryption & decryption.
* Secret key or private key.
* Advantages:
  * Easier to implement.
  * Faster.
* Disadvantage:
  * Key distribution.

**Symmetric Encryption Ciphers**

* _Block_ - Chunks of data / Fixed length group of bits.
  * Requires padding if not enough data for a block.
  * Block size.
  * More complex, not as fast.
  * May require an initialization vector.
* _Stream_ - Bits encrypted one at a time.
  * Faster / higher performance.
  * Susceptible to malicious insertions.

**Key Strength**

* Length and complexity of the key.
* Longer is more secure.
* Key entropy or randomness - generated through pseudo-random numbers.
* _Initialization Vector \(IV\)_ - a fixed-size input of a random or pseudo-random value. Ensures that each message encrypts differently.
* _Nonce_ - a random or pseudo-random number that is used only once and associated with a time stamp to increase key strength. A nonce can be used as an IV.

**Key Exchange**

* Process and method for sharing encryption keys.
* Especially when the sender or receiver are distant.
* In-band: key shared in the communications channel as the message.
* Out-of-band: using another transmission media agreed upon in advance.
* Forward Secrecy: if one key is compromised, subsequent keys will not also be compromised.

**Session & Ephemeral Keys**

* Session Keys are randomly generated to perform both encryption and decryption during the communication of a session between two parties.
* Valid only during that one communication session and are deleted.
* Ephemeral Keys - also only used for one session. Common to ephemeral key agreement protocols.

**Asymmetric Encryption**

* Uses two keys - one to encrypt and the other to decrypt.
* Keys are mathematically related.
* Public/Private key encryption.
* Only the private key needs to be kept secret and only it can decrypt the message.

**Digital Signatures / Nonrepudiation**

* Also uses Public/Private key pairs.
* Message is 'signed' using the sender's private key.
* Anyone can verify signature by using the senders public key.
* Used for repudiation \(proof of origin\).
* Used for message integrity \(proof message hasn't been altered\).
* Doesn't protect message confidentiality.

**PKI -** Public Key Infrastructure

* A set of roles, policies, and procedures needed to manage public-key \(asymmetric\) encryption.
* The process of creating, managing, distributing, storing, using, and revoking keys and digital certs.

**Hashing**

* 'Digital fingerprint'
* Work by taking a string of any length and producing a fixed-length string for output.
* Hashing Rules:
  * Speed remains the same no matter the data size.
  * Impossible to regenerate the original message from it's hash value.
  * Avoid hash collisions - each message has its own hash.
  * Changing the original changes the hash value.

**Hashing Issues**

* Precomputing hash values of common words \(rainbow tables\).
  * Solved with a salt.
* Salting uses a prefix consisting of a random string of characters to passwords before they are hashed.
* Collision Attacks try to find two input strings of a hash function that have the same output.

**Elliptical Curve & Quantum Cryptography**

* _Elliptical Curve Cryptography \(ECC\)_
  * An asymmetric public-key cryptosystem based on complex mathematical structures.
  * Uses smaller key sizes.
  * Very fast.
* _Quantum Cryptography_
  * Relies on physics rather than mathematics.
  * Based on the quantum state of photons.
  * More secure.

**Use of Proven Crypto Algorithms**

* National Institute of Standards and Technology \(NIST\) maintains publications and guidance for the use of approved cryptographic and hashing algorithms.
* Crypto best practices:
  * Use well-known and approved cryptographic algorithms.
  * Adhere to required minimum key guidance for the chosen algorithm.
  * Use approved cryptographic modes.
  * Use strong random number generators.

**Obfuscation & Steganography**

* _Obfuscation_
  * The act of making something difficult to understand.
  * Should rely on something not known or widely discovered.
  * Does not provide strong security.
* _Steganography_
  * Means 'hidden writing'.
  * Hiding messages, often in other media, so that unintended recipients are not even aware of any message.

**Crypto Use Cases**

* State of Data
  * Rest, transit, and use.
* Confidentiality
* Integrity
* Availability
* Non-repudiation

**Digital Signature Algorithm** **\(DSA\)**

* The digital signature standard for the US government. 
* Published by NIST and the NSA. 
* A pair of numbers is created and used as a digital signature. 
* These are generated using specific algorithms.
* These allow the receiver to authenticate the origin of the message. 
* Only the person transmitting data can make the signature, but anyone can authenticate the signature at the other end.
* [{Read More}](https://www.educba.com/digital-signature-algorithm/)

**Low Power Devices** 

* Should use cryptographic techniques that require less time to encrypt and decrypt data. 
* As the time to encrypt/decrypt increases, the power requirements increase as well. 
* Devices such as wireless devices, handheld computers, smart cards, and cell phones have less processing power, storage, power, memory, and bandwidth than other systems and won't benefit from algorithms with shorter key lengths. 

**Low Latency Devices** - ****Latency refers to the delay between the time the plain text is input and the cipher text is generated.

**Crypto Service Providers**

* Crypto service providers should be able to answer questions regarding which algorithm\(s\) they use to generate keys and how they store keys. 
* Crypto service providers are parties that provide cryptographic services. 
* Ex: Active Directory Certificate Services from Microsoft. 

**Simple Key management protocol for Internet Protocols \(SKIP\)** [{source}](https://www.garykessler.net/library/crypto.html)

* A key management and distribution protocol used for secure IP communication such as IPSec.
* Uses hybrid encryption to convey session keys.
  * These keys encrypt data in IP packets. 
* Uses a key exchange algorithm, such as Diffie-Hellman to generate a key-encrypting key that will be used between two parties. 
* A session key is used with a symmetric algorithm to encrypt data.
* NOT a key storage protocol. 
* A key distribution and management protocol similar to IKE. 
* Works on a session-by-session basis, although it does not require prior communication for the establishment of sessions. 
* Employs encryption standards such as DES and 3DES to provide secure communication.
* Does not deploy IKE.
* Key exchange can occur in or out of band.
  * In-band occurs over the same transmission media that is used by data and voice transmissions. 
  * Out-of-band occurs outside the data and voice transmission media.
  * In is less secure than out.

