# Frames & MAC

**MAC, Hubs, and Switches**

**What is a MAC Address?**

* A MAC address is assigned to every single NIC \(hard-coded\).
  * A physical address that is physically assigned.
* Media Access Control.
  * 12 hexadecimal digits.
  * Each digit is 4 binary bits.
  * 48 bits in total length.
  * AKA "Hardware" or "Physical" Address.
    * Sometimes referred to as "burned in" address.
  * The first half of the MAC address \(first 6 hexadecimal digits, or the first 24 bits\) refers to the OEM \(Original Equipment Manufacturer\).
    * Each OEM has their own unique identifier in the first six digits.
    * https://macvendors.com/
  * The second half of the MAC address is a unique identifier to that NIC.
* Checking MAC address:
  * Windows: "Ipconfing /all"
  * Mac: "ifconfig"
  * Linux: "ifconfig"
* Ethernet Frame
  * 1500 Bytes of data \(the payload\).
  * Get attached the Source & Destination MAC address for routing purposes.
    * Gets put on the header of the frame, or the front.
  * CRC \(Cyclic Redundancy Check\)
    * Gets put on the footer of the frame, or the end.
    * Checks to make sure all the bits are included.

![](https://www.evernote.com/shard/s342/res/b8e02a9a-32ef-c66d-9ec1-03eaead48fe4)

**Hubs & Switches**

* Hubs
  * A repeater.
    * Can only send data 100m on a Cat5e cable, so a repeater allows you to send it further.
  * All hosts receive all traffic, that is every single thing connected to a hub receives every piece of data that goes through it.
    * Every host that receives a frame from a hub has to process it, even if it's not the intended destination.
  * Outdated tech.
* Switches
  * Keeps a table of every MAC address connected.
  * Knows what ports hosts are connected to.
  * Uses something called a MAC address table for addressing and sending to the proper connected device.
  * Only sends to the proper recipient.

**Broadcast Domains**

**Unicast**

* A single destination addressed to a particular device on the network.

![](https://www.evernote.com/shard/s342/res/25d2c42d-4e87-ee52-74a7-f8cbb45b77be)

* One sender and one receiver.
* Most common transmission method.

  
**Multicast**

* One or more senders and multiple receivers.

![](https://www.evernote.com/shard/s342/res/5c3d3d73-eeac-9e8f-12d8-1081d32c5ef7)

* Delivers the same transmission to an entire group.
* Delivers via dedicated addresses or address ranges.
* The most complex transmission method to manage.

  
**Broadcast**

* MAC Broadcast Address
  * FF-FF-FF-FF-FF-FF \(HEX\) or 48 1s \(Binary\)
* Every device must receive the traffic.

![](https://www.evernote.com/shard/s342/res/df66b78e-c373-d3ce-97cb-f81e8f95102c)

* * In this scenario, the broadcast is an ARP request
    * 192.168.10.45 will send back a unicast with its MAC address and the MAC address table will be updated.

Broadcast Storm

* Is created from a loop in a broadcast, where duplicated frames are being sent out endlessly.

![](https://www.evernote.com/shard/s342/res/b9753efb-6c94-baaa-9a53-825cf81c86af)

* * In this diagram, say A sends out an ARP request looking for B.
    * Sends from A to first switch, then to second and third switch.
    * Then sends to the hub, then B.
    * B responds, into the hub.
    * Hub sends out to switches, which start the loop because the hub is flooding the network.
    * **WILL CAUSE A CRASH**
      * If a switch were in the place of the hub, this would never happen.
* If all routers forwards broadcast messages, the entire internet could potentially crash.

**Broadcast Domain**

* A logical group.
* Broadcast traffic cannot leave broadcast domains.
* Routers are the border police of broadcast domains.
  * Separate broadcast domains.

![](https://www.evernote.com/shard/s342/res/fa9909c5-c214-062f-747a-e7949de77531)

* A network is its own broadcast domain.
* Switches can also separate BC domains with VLANs, or virtual LANS.

