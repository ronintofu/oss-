# Virtualization

**Virtualization**

Use a single physical machine's hardware to run multiple virtual machines within it.

* Key Points
  * Use system's hardware.
  * Allocate CPU/RAM/Storage to VMs
  * Cannot exceed the CPU/RAM/Storage that is available on the physical hardware.
* Benefits
  * Better use of hardware resources.
  * Power saving/reduced footprint.
  * Recovery \(VMs can be saves as files\).
  * Flexibility \(VMs can be moved\).
  * Researching operating systems & other software \(sandbox\).

  
**Type 1 Hypervisor**Type 1 \(Bare Metal\) Hypervisors

* VMWare vSphere/ESXi
* Microsoft Hyper-V
* Citrix XenServer

![](https://www.evernote.com/shard/s342/res/305742fc-be78-8534-1cd9-5e4a789d1241)

Installed directly on a bare metal server \(directly onto a completely bare server with no software/OS\).  
Can connect to the \(VM\) server via a web client or other interface.

* Configurations to the VM server are done directly in the web client.

  
**Type 2 Hypervisor** - Installed on a Host OS

* VMware Workstation/Fusion
* Oracle VirtualBox
* Parallels \(Mac\)

![](https://www.evernote.com/shard/s342/res/a2f1e5dd-f8f0-072f-bf30-984780d08669)  
**Virtualized Networking \(Type 1\)**

* Physical NICs are connected to the vSwitches, which are connected \(virtually\) to the vNIC in the VMs\)
* A vRouter can provide networking between the VMs in the server.
* A vFirewall can provide firewall services between VMs and between the server and external network.

![](https://www.evernote.com/shard/s342/res/e897f8e8-ef13-82a1-e7f1-42fb24d06e0b)\*\*\*\*

**USE CASES**

**Physical to Virtual Migration, AKA: P to V**

\*\*\*\*![](https://www.evernote.com/shard/s342/res/ce401860-0b8b-561f-23d9-35e6b9ccd5b5)\*\*\*\*

**VDI - Virtual Desktop Infrastructure**

* Virtualization of desktops/operating systems that run in a data center.
* Endpoints such as thin clients access their virtual machine via the network.

![](https://www.evernote.com/shard/s342/res/02f4a46e-809b-9254-1394-63353ce9d574)

* Easier to manage than individual hosts.
* More security.
* Easier to backup.
* Cost savings.

A regular computer can still get into this network, it would be called a "thick client" in this case.

  
**Data Center & Cloud**

\*\*\*\*![](https://www.evernote.com/shard/s342/res/c470b5da-fc4e-2996-c178-53966a8de6b0)

* Data centers benefit from virtualization because of the ability to run more services and software in a smaller footprint.
* Public cloud computing is all about accessing services and resources from a remote data center and only paying for what you use.
* Virtualization and high speed networking truly enable the era of cloud computing.
  * Apps like food delivery and ordering
  * Uber, Lyft, etc.
  * Etc.

  
**RECAP**  


* Virtualization uses a physical computer's hardware to run multiple virtual machines within it.
* Type 1 Hypervisor is called a Bare Metal Hypervisor.
* Type 2 Hypervisor is called a Hosted Hypervisor.
* Understand the benefits of virtualization.
* Know the types of virtual network devices.
* VDI is all about virtualization the end user desktops.
  * Virtual Desktop Infrastructure.

**Cloud Computing**

**IaaS** - Infrastructure as a Service

* A complete hosted infrastructure in the cloud which provides access to networking features, computing hardware for desktops and servers, storage space, and internet access all as a service \(pay for what you use\). You configure the servers and the network and the IaaS provider takes care of the data center and all the hardware that everything runs on.

Examples:

* Amazon Web Services \(S3, EC2, VPC\)
* Microsoft Azure
* Google Compute Engine
* Rackspace Open Cloud

![](https://www.evernote.com/shard/s342/res/b6812a74-27e2-ba8c-b798-4178757c12c3)

* All services are configured via the internet.
* A VPN can be established to directly connect the cloud hosted network to the main company network.

  
**SaaS** - Software as a Service

* Hosted software solutions and services that are normally licensed on a subscription basis. Some SaaS \(such as basic GMail\) are free and money is made instead by serving ads through the software instead of charging a sub fee.

Examples:

* Google Apps \(Docs, GMail, Drive, etc\)
* Microsoft Office 365
* DropBox
* Salesforce

![](https://www.evernote.com/shard/s342/res/abef41ec-a3af-1a07-a177-e64551395cd9)  
**PaaS** - Platform as a Service

* Everything needed for setting up a web application in the cloud is provided as a hosted service. This allows software companies and software developers to build applications without having to worry about anything else. The servers, storage, OS, and databases are all maintained by the provider.

Examples:

* Amazon AWS \(RDS, EFS, EC2 Container Service\)
* Heroku
* Cloud Foundry
* AppEngine

![](https://www.evernote.com/shard/s342/res/ebcf689f-a57c-2dd1-1dbd-544c7445bd0d)

* SaaS can be built on a PaaS which can be built on an IaaS.

  
**CLOUD DEPLOYMENT MODELS**  


* Public Cloud
  * Everything needed to run the network and applications is fully deployed in the cloud.
* Private Cloud.
  * An "on-premise" cloud meaning the entire network, virtualization tech, servers, and applications are deployed on-premise, inside a company's datacenter.
* Hybrid Cloud
  * Some companies prefer to have their own private cloud and also make use of the public cloud. In order to be a true Hybrid Cloud the public and private clouds need to be connected to each other \(through a VPN\). With connectivity between the clouds, the resources can be shared between them.
* Community Cloud
  * The entire infrastructure is shared between multiple organizations. It could be hosted publicly, privately, or as a Hybrid, and the costs are shared amongst the community. The organizations that are part of the community usually have similar privacy, security, performance, and compliance requirements.

