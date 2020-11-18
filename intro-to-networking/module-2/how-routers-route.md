# How Routers Route

**More on Protocols**

  
**BGP -** Border Gateway Protocol![](https://www.evernote.com/shard/s342/res/9592d037-03be-98e7-03c3-3ccc70dee90f)

* Exterior Gateway \(outside AS\)
  * eBGP
* Interior Gateway \(within AS\)
  * iBGP
* BGP v4 - routing protocol of the internet.
* Path-Vector / Distance- Vector
* Manually configured neighbor relationships.
* Neighbors are called "BGP peers".
  * terminal would reflect neighbors as BGP peers.

**Administrative Distance**

![](https://www.evernote.com/shard/s342/res/8194f63f-a502-e29c-4d4f-eb46f1b6eedf)

* \(AD\) is a number used to rank directly connected routes, static routes, and dynamic routes from most desirable \(0\) to least desirable \(255\).
* If multiple routes exist to a specific destination, then the route with the lowest AD will be chosen.
* AD can be manually changed on a router.

