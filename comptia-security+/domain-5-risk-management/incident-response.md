# Incident Response

**Incident Definition**

* NIST - 'An occurrence that actually or potentially jeopardizes the confidentiality, integrity, or availability of an information system or the information the system processes, stores, or transmits or that constitutes a violation or imminent threat of violation of security policies, security procedures, or acceptable use policies.'
* Cybrary - 'An incident is an unplanned disruption or degradation of a network or system service and needs to be resolved immediately.'

**NIST Incident Response Process**![](https://www.evernote.com/shard/s342/res/fc615ab6-3e2b-90a5-f310-427804e2dcb4)**Incident Response Plan**

* The documentation of a predetermined set of instructions or procedures to to detect, respond to, and limit consequences of a malicious cyber attacks against an organization's information system\(s\). \[NIST\]
* NIST Computer Security Incident Handling Guide \(SP 800-61\) provides guidance on exact elements to include:
  * Mission, strategies, and goals of incident response.
  * Senior management approval.
  * Approach to incident response.
  * Metrics for measuring response capabilities and effectiveness.
  * Roadmap for maturing response capability.
  * How the incident response program fits into the organization.

**Incident Response Plan \(IRP\)**

* Documented incident types/category definitions.
  * Natural
  * Mechanical
  * Accidental / Human Error
  * Malicious / Compromise C-I-A
  * Policy Violation
* Roles and responsibilities.
  * Granting clear authority for actions to be taken during an incident.
  * Who can/does perform IRP activities:
    * Incident Alerting
    * Identification / Triage
    * Decisions Making - Must be an organizational executive.
    * Equipment Collection / Confiscation
    * Forensics - Independence / Segregation of Duties
    * Repair / Recovery
    * Reporting
    * Communicating - Talking outside the organization.
* Cyber-incident response teams.
  * Computer Emergency Response Team \(CERT\)
  * Cyber Incident Response Team \(CIRT\)
  * Computer Security Incident Response Team \(CSIRT\)
  * Formalized, standing, or ad-hoc.
  * Internal or external.
  * Central, distributed, or coordinating.
  * Includes:
    * Systems, network, database admins.
    * Legal
    * HR
    * Management
* Reporting requirements/escalation.
  * Document.
  * Included in many help desk systems.
  * Collecting evidence \(physical, virtual, etc.\)
  * Reporting / Disclosing To:
    * Internal Management \(Legal, HR, CEO, CFO\)
    * Legal Authorities / Law Enforcement \(Local, FBI\)
    * Affected Organizations / Clients / Customers
    * CERT \(www.cert.org\)
    * Internet Crime Compliance Center \(IC3\) - [www.ic3.org](http://www.ic3.org)
    * Insurance \(Cyber\)
  * Also needs to report what outside agencies \(if any\) should be notified. 
  * Escalation guidelines would indicate under what circumstances you need to ask for additional assistance. 
* Testing, Exercises, and Training.
  * Be prepared.
  * Prepare each role with training.
  * Practice using real world scenarios.
  * Test systems and processes to find issues.
  * Tabletop and functional exercises.



**Incident Preparation**

* Create an "Incident Response Plan" or IRP.
* Hardware/Software/Communications
  * 'Jump Kit'
* Testing & Exercises
* Creating Checklists
  * Technical
  * Procedures
  * Contacts

**Incident Detection / Identification / Analysis**

* Alerting
  * Logs - IDS, SIEM, AV
  * Humans
* Incident triage / validation.
* Determine incident scope.
  * What and who is affected.
  * Number of systems affected.
  * Identification type:
    * system
    * data
    * personnel
    * etc
* Analysis - Impact and Recoverability Effort
* Escalation
* Documentation & Notification

**Incident Containment**

* Ensuring incident doesn't continue or spread.
* Securing the scene / limiting access / isolating systems \(quarantine\)
  * Physical
  * Network
  * Logical
* Gathering Evidence

**Eradication**

* Find and eliminate the root cause.
* Removing elements of the incident, such as malware.
* Actions:
  * AV Clean-Up
  * Patching / Updating Software
  * Re-Imaging Systems
  * Restoring from Backup

**Incident Recovery**

* The process of restoring and returning affected systems and devices back into your business environment.
* Repair
  * Restoring from backup
  * Patching
  * Hardening systems \(using known baseline\)
  * Access control \(network or systems\)
  * Authentication \(change passwords\)
* Procedural Changes
* Documentation

**Post Incident**

* Lessons Learned
* After-action meeting with all Incident Response Team members.
* Capture actions such as the cause, the cost, and recommendations for preventing future incidents.
* Discuss what you've learned from the data breach.
* Regulatory or legal requirements.
* Update IRP





