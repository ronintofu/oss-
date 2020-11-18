# Inter-VLAN Routing / Etherchannel / DHCP Snooping / Troubleshooting Serial Links

**Inter-VLAN Routing**

![](https://www.evernote.com/shard/s342/res/11e5475f-52dc-a155-744b-f897071429ef)

* Each VLAN is a unique broadcast domain.
* Computers on separate VLANs are, by default, not able to communicate.
* Each VLAN is a unique IP subnetwork.
* A L2 switch forwards frames inside each VLAN but not between different VLANs.
* A L3 device can transport traffic between VLANs.

  
**Router on a Stick \(ROAS\)**

* Inter-VLAN routing can be performed by an external router that connects to each of the VLANs on a switch.
* ROAS configuration is useful when no L3 switch exist in an environment.
* ROAS configuration particularly used at smaller remote sites.
* The Router's interface is divided into sub-interfaces, which acts as a default gateway to their respective VLANs.

![](https://www.evernote.com/shard/s342/res/dff0893a-afbb-96b8-bdc6-1be1fd3893e6)**Switched Virtual Interface**

* SVI is a logical interface configured on a layer 3 Switch thus eliminating the need for a physical router.
* An SVI can be created for each VLAN.
* No switchport sub-command on a physical interface will make the interface routed instead of switched.

  
**ROAS Configuration**

\*\*\*\*![](https://www.evernote.com/shard/s342/res/f395e13a-d566-0cab-6a0c-57d0cb72255d)\*\*\*\*

**SVI Configuration**

\*\*\*\*![](https://www.evernote.com/shard/s342/res/11cb0e02-6804-d2c8-ad93-b204e5b40560)  
**Verification**

* Show ip route
* Show ip interface brief
* Show interface vlan id
* Show ip int brief \| ex unassigned
* Show vlan brief

**Etherchannel**

  
![](https://www.evernote.com/shard/s342/res/ccc1c5d6-022e-a34a-5e68-2f03e9e334dd)\*\*\*\*

**Concept**  
Etherchanneling is combining trunks.

* Etherchannel is a tech that lets you bundle multiple physical links into a single logical link.
* Benefits:
  * Allows creation of a high bandwidth logical link.
  * Up to 8 links can be combined into one logical link.
  * Can be configured as L2 or L3.
  * Load balances among the physical links involved.

  
**Requirements**

* Ports in port-channel should have:
  * Same speed.
  * Same duplex.
    * The amount of traffic you are allowed.
  * Same allowed VLANs.
  * Same access or trunking mode.
  * Same Native VLAN.
  * Same STP.

  
**Methods**  
There are two ways of configuring an Etherchannel

* Static
  * Mode: ON
* Dynamic:
  * Mode PAgP \(Cisco proprietary aggregating protocol\)
  * Mode: LACP \(IEEE standardized aggregation protocol, 802.3ad\)

  
**Modes**

* ON
  * Dynamic negotiation off.
* Auto
  * Passively listen for PAgP method.
* Desirable
  * Actively negotiate PAgP.
* Active
  * Actively negotiate  LACP.
* Passive
  * Passively listen for LACP.

  
![](https://www.evernote.com/shard/s342/res/cdee1a2b-35f3-fc02-190e-0cbf38079810)\*\*\*\*

**Configuration**

* Select the interfaces to bundle in port-channel.

![](https://www.evernote.com/shard/s342/res/d54c0710-7938-1655-404e-52218a2faf0c)

* Trunk port configuration can be defined on the interface port-channel as well.

  
**Verification**

\*\*\*\*![](https://www.evernote.com/shard/s342/res/f33b11db-d7d7-b00e-3121-980d70835c73)  


**DHCP Snooping**

* We need DHCP snooping to prevent a man-in-the-middle attack on the network.
* The potential exists for an attacker to pretend \(spoof\) to the DHCP server and respond to DHCPDISCOVER messages before teh real server has time to respond.
* DHCP snooping allows switches on the network to trust the port a DHCP server is connected.
* All ports are untrusted by default. When the client machine sends a DHCPDISCOVER message with DHCP snooping enabled, the switch will only send the DHCP

  
**Configuration**

\*\*\*\*![](https://www.evernote.com/shard/s342/res/ca5e1622-d777-0b6a-ce1b-8bee06fb9171)\*\*\*\*

**Troubleshooting Serial Links**

\*\*\*\*![](https://www.evernote.com/shard/s342/res/b706dc85-73ee-d727-0acd-6fe335d3b4a3)  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  


