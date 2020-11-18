# Real World IP Routing

**Intro to IP & Routing**

* Routers can send traffic between locally connected networks by default.
* Routers always reference their routing table to route traffic.

![](https://www.evernote.com/shard/s342/res/e05ee84a-28b4-cf52-9269-33875e696190)

* Cisco IOS: "show IP route"
  * Lists all known routes.
  * Directly connected routes.
  * Dynamically learned routes.
  * Static routes.
  * Gateway of last resort, AKA default route.
    * IP Route 0.0.0.0 \| 0.0.0.0 \(destination\)

![](https://www.evernote.com/shard/s342/res/edbd0b4e-961b-4848-57a1-9fba72f719ff)![](https://www.evernote.com/shard/s342/res/3898cfb3-9f07-df3c-b554-6712246eef46)  
![](https://www.evernote.com/shard/s342/res/1ea89b74-eb69-f299-7c40-48410022dc65)IGP - Interior Gateway ProtocolEGP - Exterior Gateway ProtocolBGP - Bording Gateway Protocol  
  
**Static Routing**

* Manually configured routes.
  * Cisco IOS:
    * \#configure terminal
    * \(config\)\#ip route 192.168.100.0 255.255.255.0 10.10.10.1
* Static routing alone is sufficient in small networks.
* Static routes override dynamically learned routes by default.
* Static routing alone is not fault tolerant.

  
![](https://www.evernote.com/shard/s342/res/dc471286-1141-d957-606b-49cc6e0dcfc7)![](https://www.evernote.com/shard/s342/res/1cbc5482-0c6d-30e8-e5ac-2367fb7ad703)  


* Advantages
  * Easy to implement in a small network
  * No ads are sent, unlike with dynamic routing protocols
  * Less bandwidth than dynamic.
  * No routing algorithm or update mechanisms are used
  * No CPU cycles are used to calculate/communicate
  * Very predictable as the start/destination are always the same
  * Preferred over dynamically learned routes
* Dis
  * If link fails, static cannot reroute
  * Configuration and maintenance is time-consuming
  * Config is error-prone especially in large networks
  * Admin intervention is required to maintain changing route info.
  * Does not scale well, maintenance becomes cumbersome.
  * Requires complete knowledge of entire network for proper implementation.

**Dynamic Routing**

* Routing Protocols
  * Allow routers to dynamically learn and share routes with one another
  * Autonomous system
  * Adds fault tolerance
  * RIP, IGRP, EIGRP, OSPF, BGP, IS-IS
* Interior Gateway Protocols
  * Share routes in a single Autonomous System
  * RIP, IGRP, EIGRP, OSPF
* Exterior Gateway Protocols
  * Share routes between autonomous systems
  * BGP IS-IS, EGP

![](https://www.evernote.com/shard/s342/res/cbee7ca4-41a2-268f-0477-f01c78a9b9d2)  
**Distance-Vector or Link-State**Routing protocols fall into one of these two categories, which describe how the routers learn and share routing information.

* Link-State
  * Finds the path with the lowest costs between nodes \(shortest path\).
  * Every node builds a graph of the network showing which nodes are connected to other nodes.
  * Using the Dijkstra algorithm each node independently calculates the best logical path to every destination.
  * Examples of link-state routing protocols are: Open Shortest Path First \(OSPF\) and Intermediate System to Intermediate System \(IS-IS\).
* Distance-Vector
  * Based on calculating the distance and direction \(vector\) to networks.
  * Examples of pure distance-vector routing protocols are Router Information Protocol \(RIP\), Interior Gateway Routing Protocol \(IGRP\), and Enhanced Interior Gateway Routing Protocol \(EIGRP\).
  * Border Gateway Protocol \(BGP\) is also based on distance-vector, but is not exclusively DV and is also classified as a path vector protocol.
  * Popular algorithms: Bellman-Ford, DUAL \(Cisco proprietary\).

  
**EIGRP** - Enhanced Interior Gateway Routing Protocol![](https://www.evernote.com/shard/s342/res/e4024841-8689-2b12-7e39-74fe6493ac4a)  


* Interior Gateway \(within an AS - autonomous system\).
* Hybrid or Advanced Distance-Vector.
* Diffusing Update Algorithm \(DUAL\).
* Cisco proprietary \(until 2013\).
* Default Metrics: Bandwidth and Delay.
* Simple to configure and loop free.
* Rapid Convergence.
* Supports unequal cost path load balancing.
* Topology Table.
* Neighbor Table.

  
**OSPF** - Open Shortest Path First![](https://www.evernote.com/shard/s342/res/957b91c0-687b-b9fb-e647-c076f5a22450)

* Interior Gateway \(within an AS\)
* Link-state, Dijkstra
* Metric: Path Cost
* Uses Hierarchical "Areas"
* Area 0 is the"backbone are" \(usually ISP\)
* Backbone Router \(BR\)
* Area Border Router \(ABR\)
* Autonomous System BR \(ASBR\)
* Message Types \(Advertisements\):
  * Hello
  * Link State Request \(LSR\)
  * Link State Update \(LSU\)
  * Link State Acknowledgement \(LSA\)

