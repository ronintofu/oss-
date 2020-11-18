# Application Security

**Software Development Life-Cycle SDLC Models**

* Waterfall
  * Steps:
    * Requirements Gathering
    * Design
    * Implementation/Coding
    * Testing/Verification
    * Deployment
    * Maintenance
  * Each stage is completely self-contained and completed in order.
* Agile
  * Works in cycles, with each cycle producing specific deliverables.
  * A type of rapid prototyping through repeated processes.
  * Methods:
    * Scrum
    * Adaptive Software Development
    * Crystal
    * Feature-Driven Development
    * Dynamic Systems Development Method
    * Lean Software Development
    * XP \(Extreme Programming\)

**Secure DevOps**

* Also called DevSecOps or Rugged DevOps
* Security integrated into all of your dev ops, which includes database design, programming, and infrastructure.
* Having security practices integrated into the entire software delivery cycle.
* Address security concerns at the beginning of projects.
* Add automated security testing techniques.
* Continuous Integration - Security in every step with updates from a centralized, controlled repository.
* Security Automation - Repeatable/scripted tasks.
* Baselining - Reference points that require completion and approval of a set of predefined project requirements to prevent uncontrolled change and lesson vulnerabilities.
* Immutable systems - no changing to systems in place. They maintain a known, documented, and repeatable configuration.
* Infrastructure as Code \(IaC\) - Programmable infrastructure. Infrastructure configuration is included with application code.
  * The process of using definition and configuration files to provision and manage data centers. 
  * Automating this process through scripts can ensure that there is more control and less opportunity for error when deploying servers, as compared with manual configuration. 
  * The foundation for secure DevOps. 

**Compiled vs Runtime Code**

* Method for creating executable code.
* Compiled code uses a compiler program such as C or C++
* Runtime uses interpreters such as Java or .NET
  * Generally faster but less secure.

**Change Management / Version Control**

* These go hand-in-hand.
* Control and manage software changes - needed for quality and security.
* Version Control \(AKA Source Control\)
  * Prevents tampering or changing the source code or executables. Tracks software file changes or application code changes.
  * Uses distributed storage for code \(Git / GitHub or Subversion\)
* Benefits
  * Historical data on changes to files.
  * Branching and merging capabilities.
  * Traceability.

**Provisioning and Deprovisioning**

* Provisioning - The creation or update of a resource.
* Deprovisioning - The removal of a resource.
* Part of the SLDC
* Generally automated where software packages are made available to users through a self-service portal.

**Secure Coding Techniques**

* Authentication
  * Hard-coding credentials into code.
  * Use of cookies.
* Proper Error Handling
  * Errors should be generic / not divulge specific system or application information.
  * Comments should not be visible in the end-product.
  * Every input is validated against a range of acceptable values. 
    * If the input does not match that range of values, the input is rejected and an error message is generated. 
* Proper Input Validation
  * Scrub & validate input from outside or untrusted sources.
  * Use of default values and character limitations.
* Normalization
  * The conversion of data to its anticipated, simplest known form.
* Stored Procedures
  * Associated with database queries / precompiled SQL statements.
* Code Reuse/Dead Code
  * Reusing existing software modules.
  * Reused code should be validated for vulnerabilities.
  * Dead Code: no longer provides useful function, but not scrubbed.
* Use of Third-Party Libraries and SDKs
  * SDK - Software Dev Kit
  * Know where your code comes from - trusted source.
  * Check for CVE \(Common Vulnerabilities and Exposures\)
* Code Signing
  * Signing executable code using a certificate-based digital signature.
  * Proves the author's identity and provides code integrity.
* Data Exposure
  * Encryption of sensitive data at all times \(in transit and at rest\).
* Encryption
  * Standard encryption algorithms, hashing, and digital signatures.
  * TLS for data in transit.
* Obfuscation/Camo
  * Hiding back-end code.
  * Prevents code from being reverse-engineered.
* Memory Management
  * Optimizes performance by assigning blocks of memory to programs and processes.
  * Vulnerabilities may exploit improper memory utilization \(buffer overflow\).
* Server-Side vs Client-Side Execution and Validation
  * Client-Side Validation - Entered data is validated via a script on the user's browser before the form is sent to the server.
  * Server-Side Validation - Occurs on the back-end server housing the application code. Protects against malicious attempts by the user to bypass validation.

**Java** 

* Unsigned Java applets in Java Development Kit 1.1 use sandboxes to enforce security. 

