# Public Key Infrastructure

**Public and Private Keys**

* Encrypt a document with the recipient's public key. Only their private key needs to be kept secret and only it can decrypt the message.
* The sender's private key is used to sign the message.

**PKI Components**  
Public Key Infrastructure

* Solves the issue with key management.
* A set of roles, policies, and procedures needed to manage public-key \(asymmetric\) encryption.
* The process of creating, managing, distributing, storing, using, and revoking keys and digital certificates.
* Public Key Infrastructure X.509 \(PKIX\) is the working group formed by the IETF to develop standards and models of PKI.

**PKI Digital Certificate**

* A digitally signed block of data used to prove the ownership of a public key issued by a Certificate Authority.
* Includes:
  * Information about the key.
  * Information about the identity of its owner \(called the subject\).
  * The digital signature of an entity that has verified the certificate's contents \(called the issuer\).
* X.509 v3 Standard defines the certificate formats and fields for public keys.

**Digital Certificate Components**

![](https://www.evernote.com/shard/s342/res/a923ee24-ac3a-dc0c-75f9-1f5248527da6)

**X.509 Certificate Types**

* The original file extension for X.509 is PFX.
  * A PFX certificate file is used by Microsoft and contains both the public and private keys. 
  * The container is fully encrypted. 
  * You should use OpenSSL to convert this into a PEM encoded file. 
  * The two most common file types for exporting the private key are PFX and P12.
  * Primary Enhancement Mail \(PEM\) certificates are primarily used for web servers and can be read in a text editor. 
  * The PEM encoded file contains the certificate encoded in encrypted Base64. 
* Root Certificates - for root authorities. These are usually self-signed by that authority and often kept offline.
* Domain Validation \(DV\) - includes only the domain name.
* Organizational Validation \(OV\)
  * Organizations are vetted against official government sources.
  * Common for public-facing websites.
* Extended Validation \(EV\)
  * Highest level of trust.
  * Requires a comprehensive validation of the business.
  * Provides additional validation for HTTPS web sites. 
  * It provides the name of the legal entity responsible for the web site. 
  * These certs require the most effort by the CA to validate and provide a higher level of trust than domain validation because they are validated using more information than the domain. 
* Wildcard Certificates - allows subdomains for a single registered domain \(\*.example.com\)
* Subject Alternate Name \(SAN\) - special X.509 that allows additional items \(IP addresses, domain names, and so on\).
* Code Signing Certificates
  * Used for code that is distributed over the internet, including programs or apps.
  * Verifies the code's origin and helps the user trust that the claimed sender is the originator.
* Machine/Computer Certificates
  * X.509
  * Assigned to a designated machine. 
  * During authentication, the machine requesting access must supply the certificate assigned to it. 
* Email Certificates - securing email \(S/MIME\).
* User Certificates - for individual use.

**Certificate Formats**

* Distinguished Encoding Rules \(DER\)
  * Stored as binary files. 
* Primary Enhanced Mail \(PEM\)
  * Primarily used for Unix/Linux servers and can be read in a text editor. 
  * A PEM encoded file extension contains the certificate encoded in encrypted Base64. 
  * Two formats: Base64-encoded or DER-encoded binary. 
* Personal Exchange Formate \(PFX\)
* Canonical Encoding Rules \(CER\)
  * Stored as ASCII files.
* P12
* P7B

![](https://www.evernote.com/shard/s342/res/47a4a3fd-f5e3-a2a5-2a3d-48db219464e3)

**PKI Components - Certificate Authority \(CA\)**

* Trusted entities.
* Internal - AKA self-signed.
* External / Third-Party \(Symantec, GoDaddy, etc.\)
* Duties:
  * Issues certificates.
  * Verifies the holder of a digital certificate.
  * Ensures that holders of certificates are who they claim to be.

**PKI Components - Registration Authority \(RA\)**

* Offloads work from the CA.
* Validate user's or endpoint's identities.
* Accepts registrations.
* Distributes keys.
* Does NOT issue certs.

**Certificate-Signing Request \(CSR\)**

* Request from applicant to CA top apply for a digital cert.
* Includes:
  * Applicant's public key.
  * Fully qualified domain name.
  * Legally incorporated name of the company.
  * Address.'

**Certificate Revocation**

* The process of invalidating a cert before its expiration date, often due to private key loss or compromise.
* Three levels:
  * Valid
  * Suspended
  * Revoked
* Certificate Revocation List \(CRL\)
  * Method for distributing certificate revocation information.
    * Must be often updated.
  * Certificate compared against CRL.
  * CRL must be updated and maintained constantly.
* Online Certificate Status Protocol \(OCSP\) - checks certificate status in real time.
* OSCP Stapling
  * Reduces load on CA.
  * Allows the web server to "staple" a time-stamped OCSP response as part of the TLS handshake with the client.
  * The web server is now responsible for handling OCSP requests instead of the CA.

**Certificate Trust Models**

* Single CA
  * Simples, no redundancy.
  * Self-signed cert.
* Hierarchical Model
  * Root CA - top of the hierarchy, may be offline.
  * Intermediate CA - subordinate CAs provide redundancy and load balancing.

**Trust Models**

* Certificate Chaining
* Web of Trust - A cross-certification model.
  * Peer-to-peer trust relationship with other CAs.
* Bridge CA - Cross-certification model using a central point of trust.

**Key Escrow**

* Trusted third party maintains keys.
* Addresses the possibility that a crypto key may be lost.
  * If key is lost, then the data is lost.
* Key Recovery Agent is an entity that has the ability to recover a key, key components, or plaintext messages as needed.

**Pinning**

* Hashes of public keys for popular web servers are included with applications such as web browsers.
* Mitigates the use of fraudulent certs.
* HTTP Public Key Pinning \(HPKP\) - uses public key pins, which are essentially hashed values of the public key communicated to the browser client from the server in the HTTP header

**Subject Alternative Name \(SAN\)** - [{source}](https://en.wikipedia.org/wiki/Subject_Alternative_Name)

* A field in the certificate definition that allows you to stipulate additional information, such as an IP address or host name, associated with the certificate. 



