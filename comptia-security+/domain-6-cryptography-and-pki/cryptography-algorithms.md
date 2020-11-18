# Cryptography Algorithms

**Obfuscation**

* The act of making something difficult to understand.
* Substitution Cipher - Substitutes one symbol for another.
  * Example: ROT13 \(rotate 13 places\)

![](https://www.evernote.com/shard/s342/res/53a7643c-5951-efd9-8cee-a7e508cf8d3f)

* **XOR \(eXclusive OR\)** -  a logical operation that outputs true only when inputs differ \(one is true, the other is false\).

![The Exclusive-OR function in terms of OR and AND.](https://www.allaboutcircuits.com/uploads/articles/XOR-gate-circuit-calculation.jpg)

![](../../.gitbook/assets/image%20%281%29.png)

**Symmetric Algorithms**

* _Data Encryption Standard \(DES\)_
  * Adopted by NIST in 1977.
  * Block cipher using 64-bit blocks \(56-bit key + 8 bits of parity\).
  * Short key length subject to brute-force attacks.
* _3DES \(Triple DES\)_
  * DES algorithm computed three times.
  * Using a 'key bundle' three different DES keys, each of 56 bits = total bit strength of 168 bits \(known as 3TDEA\).
  * Also options to reuse keys.
  * Uses 48 rounds of computation.
    * Offers high resistance to differential cryptana

![](../../.gitbook/assets/image%20%283%29.png)

* _Advanced Encryption Standard \(AES\)_
  * Original name 'Rijndael"
  * Free for any use public or private, commercial or non-commercial.
  * Adopted by NIST in 2001.
  * Block cipher with 128 block size.
  * Three key lengths: 128, 192, and 256.
  * It uses multiple encryption rounds to reach these key lengths:
    * 10 rounds for 128-bit
    * 12 rounds for 192-bit
    * 14 rounds for 256-bit
* _RC4 / RC5 / RC6 - Rivest Cipher_
  * RC4 - Stream Cipher
  * RC5/6 - Block Ciphers
  * Works with key sizes between 40 and 2048 bits.
* _Blowfish / Twofish_
  * A symmetric block cipher that can use variable-length keys from 32 bits to 447 bits.
  * Twofish uses 128-bit blocks.
* _International Data Encryption Algorithm \(IDEA\)_
  * 128-bit key
  * Similar to DES, but more secure due to having a longer key.
  * Used in PGP.
* _One-Time Pad \(OTP\)_
  * Most secure crypto implementation.
  * Use of a key as long as the plain-text message.
  * Only used once, then destroyed.
* _Skipjack_
  * NSA developed block cipher used in clipper chip.
  * Uses an 80-bit key to encrypt 64-bit blocks of data.
* _GOST_
  * A Soviet and Russian government standard symmetric key block cipher.
  * Block size of 64 bits. 
  * Developed to counter Data Encryption Standard \(DES\). 
* _Psuedo Random Number Generator \(PRNG\)_
  * A type of algorithm that generates a number that is "random enough" for cryptographic purposes. 
  * Used in AES, DES, and Blowfish.

**Cipher Modes**

* _Counter Mode \(CTR\)_
  * Turns a block cipher into a stream cipher.
  * Used to generate a keystream.
  * Each block combines a nonce or IV with a sequentially assigned number to produce a unique counter block that is then encrypted.
* _Cipher-Block Chaining \(CBC\)_
  * Uses an IV with the first block.
  * Thereafter, each block of plain text is obfuscated with the cipher text from the previous block before it is encrypted.
  * Introduces more diffusion & reduces effects of plain-text attacks.

**Asymmetric Encryption**

* Uses two keys.
  * One for encryption.
  * One for decryption.
* Keys are mathematically related.
* Public / Private key encryption.
* Only the private key needs to be kept secret.
* Only the private key can decrypt the message.

**Asymmetric Algorithms**

* Extra computational overhead.
* Used primarily for:
  * Secure exchange of shared keys for symmetric encryption.
  * Digital signatures.
* Solves the issue of key exchange with symmetric encryption.
* _Rivest, Shamir, and Adleman \(RSA\)_
  * Used for key exchange and digital signatures.
  * Key can be any length.
  * Algorithm works by multiplying two large prime numbers.
  * Derives two different numbers: one public key and one private key.
* _Diffie-Hellman Key Exchange \(D-H\)_
  * Two parties, without prior arrangement, can agree on a secret key that is known only to them.
  * Only used to generate a shared key \(not encryption\).
  * Key can be safely & secretly shared on a public network.
* _Diffie-Hellman Ephemeral \(DHE\)_
  * Uses a different key for every conversation.
  * Supports perfect forward secrecy.
* _Elliptical Curve Cryptography \(ECC\)_
  * Technique using elliptical curves to calculate simple but difficult-to-break encryption keys.
  * Uses smaller key sizes to obtain the same level of security \(160-bit ECC = 1024-bit RSA\).
  * Requires fewer resources than RSA. 
* _Elliptical Curve Diffie-Hellman Ephemeral \(ECDHE\)_
  * Variant of DHE using ECC for perfect forward secrecy.
* _El Gamal_
  * An extension to the Diffie-Hellman using an ephemeral key.
* _Pretty Good Privacy \(PGP\) and GNU Privacy Guard \(GPG\)_
  * Developed by Phillip R. Zimmerman in 1991.
  * Used to encrypt and sign email messages.
  * Establishes a web of trust between the users. 
    * A web of trust implies that the users generate and distribute their public keys. 
    * These keys are signed by users for each other, establishing a community of users who trust each other for communication. 
    * Every user has a collection of signed public keys stored in a file known as a web ring. 
  * PGP provides the following functionalities: 
    * Confidentiality through the International Data Encryption Algorithm \(IDEA\).
    * Integrity through the Message Digest 5 \(MD5\) hashing algorithm. 
    * Authentication through public key certificates. 
    * Non-repudiation through encrypted signed messages. 
* _Knapsack_ [{source}](https://en.wikipedia.org/wiki/Merkle%E2%80%93Hellman_knapsack_cryptosystem)
  * AKA Merkle-Hellman Knapsack Crypotosystem
    * One of the earliest public key cryptosystems. 

**Hashing**

* 'Digital fingerprint'
* Work by taking a string of any length and producing a fixed-length string for output.
* Changing the original changes the hash value.
* Originator takes a hash of  the file and provides hash to receiver.
* Receiver takes hash of file and compares with original to ensure file integrity.

**Hashing Algorithms**

* _Secure Hash Algorithm \(SHA, SHA-1, SHA-2, SHA-3\)_
  * Developed by the US NSA
  * SHA-1 can generate a 160-bit hash from any variable-length string of data.
  * SHA-2 = SHA-22, SHA-256, SHA-348, and SHA-512 \(based on their digest lengths\)
  * SHA-3, published in 2012, not widely used yet.
* _Message Digest Algorithm \(MD2, MD4, MD5\)_
  * The most widely known hashing function.
  * Produces a 16-byte hash value, usually expressed as a 32 digit hexadecimal number.
  * Considered compromised. Rainbow tables have been published which allow people to reverse MD5 hashes made without good salts.
* _Message Authentication Code \(MAC\)_
  * Authentication of messages using a secret key.
  * Used in electronic fund transfers to protect against fraud.
* _Hash-Based Message Authentication Code \(HMAC\)_
  * HMAC combines a cryptographic hash function and a secret crypto key.
  * HMAC does not encrypt the message, only the key.
* _Keyed Hashing for Message Authentication Code \(KHMAC\)_
  * Used to digitally sign packets that are transmitted on Internet Protocol Security \(IPSec\) connections. 
* _RACE Integrity Primitives Evaluation Message Digest \(RIPEMD\)_
  * Design based on MD4.
  * 160-bit version of the algorithm \(RIPEMD-160\) performs comparably to SHA-1.
* _HAVAL_
  * Processes 1024-bit block sizes of information. 
  * Creates message digests of variable sizes rather than a fixed output value. 
  * Produces hashes in lengths of 128, 160, 192, 224, and 256. 

**Rainbow Tables and Salts**

* _Rainbow Table_
  * A pre-computed table for reversing cryptographic hash functions.
  * All of the possible hashes are computed in advance.
* _Salt_
  * Random data that is used as an additional input to hash

**Key Stretching**

* Processes used to take a weak key and make it stronger, usually by making it longer.
* _Bcrypt_
  * Based on the blowfish algorithm.
  * Provides an adaptive hash function based on a key factor.
* _Password-Based Key Derivation Function 2 \(PBKDF2\)_
  * Algorithm applies a pseudo-random function to the password combined with a salt of at least 64 bits, and then repeats the process at least 1000 times.





