# Access Protocols

**Directories / Directory Service Protocols**

* Repositories of an organization's network resources and users.
* Most follow a hierarchical database format, based on the X.500 Standard.
* A directory service manages the entries and data in the directory and enables access control and identity management.
* Types: Microsoft Active Directory \(AD\) & LDAP

**Lightweight Directory Access Protocol \(LDAP\)**

* A standardized directory access protocol.
* Main purpose is to query the LDAP user database - pared-down X.500-based directories.
* Supported by most major vendors including Microsoft AD and OpenLDAP
* Hierarchical structure.
* An open protocol.
* Weakness of LDAP:
* Can be subject to LDAP injection attacks:
  * Similar to SQL injection attacks.
  * Occurs when user input is not properly filtered.

**LDAP Data Interchange Format \(LDIF\)**

* Enables LDAP servers toe exchange directory information. 
* Servers must be able to authenticate to the server using the correct format 
* A standard plain text data interchange format for representing LDAP directory content and update requests. 
* [{wiki}](https://en.wikipedia.org/wiki/LDAP_Data_Interchange_Format)

**LDAP Security**

* LDAP is vulnerable to snooping.
* Encrypt communications using SSL/TLS to secure LDAP transmissions.
* Certificates can validate authentication requests.
* LDAPv3 bind requests should use Simple Authentication and Security Layer \(SASL\)

**Directory Information Tree** - a hierarchical structure that can be searched for directory information. This holds LDAP entries. 

**Kerberos**

* A symmetric key authentication protocol.
* Kerberos v5 uses mutual authentication between the requesting client and the supporting server through a Key Distribution Center \(KDC\)
* Once authenticated with the KDC, user is given a Ticket Granting Ticket \(TGT\)
  * Tickets are encrypted and have a limited life span.
  * Ticket lists user's privileges.
* Each time the user wishes to access some resource on the network, the user's computer presents the KDC with the TGT; the TGT then sends that user's computer to a service ticket, granting the user access to that service.
* Works like using a driver's license to cash a check.

**Kerberos Ticket**

* Contains information linking it in the user.
* User presents ticket to network for a service.
* Difficult to copy.
* Expires after a few hours or a day.

**Kerberos Key Distribution Center**

* Comprised of Three Components: 
  * Kerberos Database
    * stores all the information about the principals and the realm they belong to, among other things.
  * _Authentication Service \(AS\)_
    * responsible for issuing a ticket-granting ticket \(TGT\) to a client when they initiate a request to the AS.
  * _Ticket-Granting Service \(TGS\)_
    *  responsible for validating TGTs and granting _service tickets_.
      * Service tickets allow an authenticated principal to use the service provided by the application server, identified by the SPN \(Service Principle Name\). 

**Kerberos Authentication Process**

* Each time the user wishes to access some resource on the network, the user's computer present the KDC with the TGT.
* The TGT then sends that user's computer a service ticket, granting the user access to that service.
* User's computer then sends the service ticket to the server the user is trying to access.
* As a final authentication check, that server then communicates the TGT to confirm and validate the service ticket.

![](../../.gitbook/assets/image%20%285%29.png)

**Remote Authentication Dial-In User Service \(RADIUS\)**

* Developed in 1992. 
* Became industry standard.
* Suitable for high volume service control applications such as dial-in access to a corporate network.
* Still in use today.
* An IETF Standard
* Implemented by most of the major OS manufacturers.
* Uses UDP transport to a centralized server providing authentication and access control for networks.
* A RADIUS client is typically a device such as a wireless AP.
  * Responsible for sending user credentials and connection parameters to the RADIUS server.

![](../../.gitbook/assets/image%20%282%29.png)

* RADIUS user profiles are stored in a central database.
  * All remote servers can share.
* Advantages of a central service:
  * Increases security due to a single administered network point.
  * Easier to track usage for billing and keeping network statistics.

**Diameter**

* Diameter was created to deal with VoIP and wireless services.
* Addresses new technologies that RADIUS was not designed to handle.
* Backwards compatible with RADIUS but not all RADIUS servers work with Diameter.

![](https://www.evernote.com/shard/s342/res/be0f7213-9d57-d3d0-056c-cf97795e7bfc)**Terminal Access Controller Access Control System Plus \(TACACS+\)**

* Handles authentication, authorization, and accounting \(AAA\) services.
* Similar to RADIUS
* TCP rather than UDP in its transport method.
* Client/server model.
* Communicates by forwarding user authentication information to a centralized server.
* TACACS+ advantages over RADIUS:
  * TCP rather than UDP as its transport method means it is more reliable.
  * Encrypts the entire packet, not just authentication.
  * Controls the authorization of router commands.

![](../../.gitbook/assets/image%20%288%29.png)

**Password Authentication Protocol \(PAP\)**

* Legacy
* User ID and password sent clear text.
* No protection for playback or trial-and-error attacks.

**Challenge Handshake Authentication Protocol \(CHAP\)**

* Provides on-demand authentication over encrypted channels.
* Server first authenticates client.
* Client generates a one-way hashing function \(MD5 algorithm\) and sends to the service.
* Client hash is compared against service's hash by the authenticator service.
* Process is repeated at random intervals to prevent replay attacks.

**MSCHAP & PEAP**

* MSCHAPv2 - Microsoft proprietary version.
  * Uses a new string each time for authentication.
  * The client and server mutually authenticate and use two encryption keys.
* Should not be used alone.
* Use MS-CHAP with Protected Extensible Authentication Protocol \(PEAP\) or L2TP/IPSec
* PEAP
  * Provides a TLS/SSL tunnel.
  * Protects the authentication traffic.
  * Uses a certificate on the authentication server.

**NT LAN Manager \(NTLM\)**

* Legacy authentication from Microsoft.
* Replaced by Kerberos.
* Similar to CHAP and MSCHAP.
* All NTLM versions use relatively weak cryptographic schemes.
* Lacks MFA support.

**Federated Services**

* Security Assertion Markup Language \(SAML\)
  * An Extensible Markup Language \(XML\) framework for creating and exchanging security information between online systems.
  * Main purpose is SSO for enterprise users over the web.
  * Three main functions:
    * The user seeking to verify its identity is the principle.
    * The entity that can verify the identity of the end user is the ID provider.
    * The entity that uses the ID provider to verify the ID of the end user is the Service Provider.
  * Defines security authorizations on web pages as opposed to web page elements in HTML. 
* Shibboleth system uses SAML. 
* OAuth
  * Framework used for internet token-based authorization.
  * Purpose is API authorization between applications.
  * Current version is 2.0
  * Allows access tokens to be issued to third-party clients \(resource consumers\) with the approval of the resource owner, such as a social media site.
  * OAuth2.0 uses the JSON and HTTP protocols.
  * Uses SSL/TLS to prevent eavesdropping.
* Simple Web Tokens and JSON Web Tokens
* OpenID Connect
  * An identity layer based on OATH 2.0 specifications.
  * Used for consumer single sign-on.
  * OpenID Connect implements authentication as an extension to the OATH 2.0 auth process.
  * Provides additional security - signing, encryption of ID data, and session management.
  * Uses an ID token structure, including the authentication of end user via JSON Web Token \(JWT\).
  * A JWT is used to prove that an authentic source created the originating data.

**Two-Phase Commit**

* A two-phase commit ensures that an entire transaction is executed to ensure data integrity. 
* If a portion of a transaction cannot complete, the entire transaction is not performed. 

**Secure European System for Applications in a Multi-vendor Environment \(SESAME\)** [{source}](https://www.cosic.esat.kuleuven.be/sesame/html/sesame_what.html)

* Sophisticated single-sign-on with added distributed access control features and cryptographic protection of interchanged data.
* To access the distributed system, a user first authenticates ta an Authentication Server to get a cryptographically protected token used to prove his or her ID.
* The user then presents the token to a Privilege Attribute Server to obtain a guaranteed set of access rights contained in a Privilege Attribute Certificate \(PAC\)[. {source}](http://cadse.cs.fiu.edu/corba/corbasec/faq/multi-page/node147.html)

