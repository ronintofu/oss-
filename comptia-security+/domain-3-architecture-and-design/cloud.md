# Cloud

**Cloud Computing**

* NIST SP800-145: "Cloud computing is a model for enabling ubiquitous, convenient, on-demand network access to a shared pool of configurable computing resources \(e.g. networks, servers, storage, applications, and services\) that can be rapidly provisioned and released with minimal management effort or service provider interaction."

**On-Premise vs Hosted vs Cloud**

* On-Premise - Servers at organization's location.
* Hosted - Servers outsourced to an external provider.
* Cloud - Using shared servers.

![](https://www.evernote.com/shard/s342/res/75344a9e-3513-e3f0-1600-ae0897eadeb0)**Essential Characteristics of Cloud Computing**

* On-Demand Self-Service
* Broad Network Access
* Resource Pooling
* Rapid Elasticity or Expansion
* Measured Service

**Cloud Computing Service Models**

* Software as a Service \(SaaS\)
  * "The capability provided to the consumer is the provider's applications running on a cloud infrastructure. The applications are accessible from various client devices through either a thin client interface, such as a web browser \(e.g., web-based email\), or a program interface. The consumer does not manage or control the underlying cloud infrastructure including network, servers, OS, storage, or even individual application capabilities, with the possible exception of limited user-specific application configuration settings."
* Platform as a Service \(PaaS\)
  * "The capability provided to the consumer is to deploy onto the cloud infrastructure consumer-created or acquired applications created using programming languages, libraries, services, and tools supported by the provider. The consumer does not manage or control the underlying cloud infrastructure including network, servers, OS, or storage, but has control over the deployed apps and possibly config settings for the app-hosting environment."
* Infrastructure as a Service \(IaaS\)
  * "The capability provided to the consumer is to provision processing, storage, networks, and other fundamental computing resources where the consumer is able to deploy and run arbitrary software, which can include OSs and apps. The consumer does not manage or control the underlying cloud infrastructure but has control over OSs, storage, and deployed apps; and possibly limited control of select networking components \(e.g., host firewalls\)."

**Cloud Deployment Models**

![](https://www.evernote.com/shard/s342/res/8ca80184-12c9-7d71-cec5-196ae9f6af05)

**Virtualization**

![](https://www.evernote.com/shard/s342/res/d80a4d7d-f7b3-120b-400e-a2e669fd8b52)

**Hypervisors**

* Underlying tech that creates and runs VMs.
* Presents the guest OSs with virtual operating platform and manages the execution of the guest OSs.
* Two implementation methods:
  * Type 1 - Native or Bare-Metal
  * Type 2 - Hosted

**Containers**

* Replacing or used with hypervisors.
* A lightweight, stand-alone, executable package of software that includes everything needed to run it:
  * Code
  * Runtime
  * System Tools
  * System Libraries
  * Settings

**VDI / VDE**

* Virtual Desktop Environment \(VDE\)
  * Desktop Virtualization
* Virtual Desktop Infrastructure \(VDI\)
  * The user's desktop is running inside a virtual machine that resides on a server in a datacenter.
  * A form of VDE that enables fully personalized desktops for each user.

**Cloud Storage - Network Storage**

* DAS \(direct attached storage\)
* NAS \(network area storage\)
* SANs \(storage area networks\)
* Date Security - Encryption on the storage device.

**Virtualization Security**

* VM Escape Protection - Leaving an assigned VM.
* VM Sprawl Avoidance - [{source}](https://www.vmware.com/techpapers/2012/controlling-virtual-machine-sprawl-10339.html)
  * Overusing shared resources.
  * Can be accomplished by planning and managing the growth in VM usage. 
  * The ability to quickly create virtual machines without the disciplines and controls of the physical world results in machines being provisioned unnecessarily without proper justification and approval.
    * Over-provisioned \(too much CPU, memory, or disk\), or consuming resources well after they no longer are required. 
* Cloud Access Security Broker \(CASB\) - Security policy enforcement points.
* Security as a Service - A subscription-based business model for acquiring and managing security functions \(virtual SOC\).

