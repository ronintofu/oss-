# Distribution/Core Layer/VLAN

**Flat network**

* Network were first implemented in a "flat manner where all PCs, servers, and ---- are connected to each other using Layer 2 switches.

  
**Hierarchical Design**

* Involves dividing the network into discrete layers.
* Each layer or tier in the hierarchy provides specific functions that define its role within the overall network.
* Local traffic remains local.
* Only traffic that is destined for other networks is moved to a higher layer.
* Advantages:
  * Modularity.
  * Eases Growth and Scalability.
  * Predictability.
* Typical Hierarchy:
  * Access Layer
    * Grant the workgroup/user access to network apps and functions.
  * Distribution:
    * Provides policy-based connectivity.
    * Aggregates the access layer switches wiring closets and provides policy based connectivity.
  * Core:
    * Provides fast transport between distribution switches within the enterprise campus.
    * High-speed backbone, which is designed to switch packets as fast as possible.

  
**Access Layer**

* Layer 2 Switching.
* High Availability.
* Port Security.
* QoS.
* Address Resolution Protocol \(ARP\) Inspection.
* Spanning Tree.
* Power over Ethernet \(PoE\).

  
**Distribution Layer**

* The distribution layer is the aggregation point for access switches.
* Policy-based security in the form of access control lists \(ACLs\) and filtering.
* Routing services.
* Route redistribution.
* Route summarization.
* FHRP Redundancy and load balancing.
* QoS features.

  
**Core Layer**

* Core Layer is also referred to as the network backbone.
* Core layer is designed to switch packets as fast as possible.
* The core layer provides.
  * Avoid CPU-intensive packet manipulation caused by security, QoS, or other processes.
  * Providing high-speed switching \(I.E., fast transport\)
  * Providing reliability and fault tolerance.
  * Scaling by using faster, and not more, equipment.

  
**Network Size**Network categorization based on the number of devices

* Small
  * Up to 200 devices.
* Medium
  * 200-1000 devices.
* Large
  * 1000+ devices.

  
**Two-Tier Collapsed Core Design**

* The three-tier hierarchical design maximizes performance, network availability, and the ability to scale the network design.
* Therefore, a two-tier hierarchical design where the core and distribution layers are collapsed into one layer is often more practical.
* A collapsed core is when the distribution layer and core layer functions are implemented by a single device.
* The primary motivation for the collapsed core design is reducing network cost, while maintaining most of the benefits of the three-tier hierarchical model.

![](https://www.evernote.com/shard/s342/res/da6c3944-d008-79db-5d04-b10dea61bff0)

**VLAN**

**VLAN Overview**

* Virtual Local Area Network \(VLAN\)
  * Logical LAN or Logical Subnet.
  * It defines a broadcast domain.

  
**VLAN Benefits**

* Reduce CPU overhead.
* Reduce unnecessary broadcast traffic.
* Reduce security risks.
* Offer flexible designs.
* Reduce STP workload.

  
**VLAN Range**

* Standard VLAN Range
  * 1-1005
* Legacy VLAN Range
  * 1002-1005
* Extended VLAN Range
  * 1006-4094
* Native/Default Range
  * 1

Sh VLAN Br will show every VLAN  in config global.

**VLAN Best Practices**

* VLAN Numbering
* Naming
* Placement
* Trunking Requirement
* Test & Verification

  
**Trunk**  
![](https://www.evernote.com/shard/s342/res/0596aded-7dc8-f76c-8142-6663025ac827)  
  
- A trunk link carries traffic for multiple VLANs

![](https://www.evernote.com/shard/s342/res/96e3a8d4-b242-78e9-2de0-11a716cf75aa)  
**DTP Concept**

* Dynamic Trunking Protocol is a Cisco proprietary point-to-point protocol.
* DTP is used to negotiate a trunk between two Cisco devices.
* DTP may utilize either IEEE 802.1Q or Cisco ISL trunking protocol.
* Ethernet trunk interfaces support several different modes:
  * Access \(OFF\)
    * Switch\(config-if\)\#switchport mode access
  * Trunk \(ON\)
    * Switch\(config-if\)\#switchport mode trunk
  * Dynamic Desirable
    * Switch\(config-if\)\#switchport mode dynamic desirable
  * Dynamic Auto
    * Switch\(config-if\)\#switchport mode dynamic auto
  * Nonegotiate
    * Switch\(config-if\)\#switchport nonegotiate

**DTP Modes Combination Scenarios**

* A trunk will not come up in case of encapsulation mismatch.

![](https://www.evernote.com/shard/s342/res/18b7e777-2aa5-c2e1-a3b9-c8eb30a67998)  
  
some people fear birthdays - segment packet frame bit  
**DTP Verification**

* Show interfaces interface-id switchport.
* Show interfaces trunk.
* Show dtp.

**VTP Concept**

* VLAN Trunking Protocol \(VTP\) is a Cisco-proprietary L2 messaging protocol.
* VTP runs over trunk links and synchronizes the VLAN databases of all switches in the VTP domain.
* VTP reduces the administrative burden of manually creating VLANs on all switches in VLAN domain.
* 3 Types of VTP Adverts:
  * Summary Advert
    * Carries info like domain name, VTP version, config revision \#, time stamp, MD5 encryption hash code.
  * Subset Advert
    * Contains the specific changes that have been performed like adding deleting or change of name in a VLAN.
  * Advertisement Requests
    * A VTP client can request any VLAN info it lacks through advertisement requests.

  
**VTP Modes**

* Server
  * The default VTP role
  * Servers can create, delete, and rename VLANs.
* Client
  * Cannot make VLAN changes.
  * Synchronize their databases with other switches in the domain.
* Transparent
  * It can create, delete, and rename VLANs.
  * It does not synchronize its database with any other switches.

  
**VTP Versions**

* Version 1
  * Default on Cisco IOS switches.
* Version 2
  * Token Ring Support
* Version 3
  * Extended VLAN range \(1-4094\)
  * Per-port VTP.
  * Extended authentication support.

  
**VTP Password**

* Password must match on all switches in the VTP domain.

  
**VTP Configuration**  
![](https://www.evernote.com/shard/s342/res/722d17d2-0655-042b-392e-04bcf565c4da)  
**VTP Verification**

* show vtp status
* show vlan brief
* show interfaces interface-id switchport
* show interfaces interface-id trunk

  
**VTP Best Practices**

* Adding a new switch to a VTP Domain
  * 1. With the switch disconnected from the network, set it as a VTP transparent and delete the vlan.dat file from its flash memory.
  * 2. Reboot the switch.
  * 3. Configure the correct VTP settings such as domain, pass, mode, and version.
  * 4. Connect the switch to the network and verify that it receives the correct info.

  
**Network Address Translation**

* A Short-term solution to the problem for the depletion of IP addresses.
  * Long term solution to IPv6
  * CIDR
  * NAT

  
**Types of NAT**

* Static NAT - mapping an unregistered IP address to a registered IP address on a one-to-one basis.
* Dynamic NAT - Maps an unregistered IP address to a registered IP address from a group of registered IP addresses.
* Overloading - A form of dynamic NAT that maps multiple unregistered IP addresses to a single registered IP address by using different ports. This is known also as a PAT \(Port Address Translation\).

![](https://www.evernote.com/shard/s342/res/94a5faa6-07f2-c257-fdab-a4abe6633861)

