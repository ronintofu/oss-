# Operating Systems



**HOST COMMAND LINE TOOLS**

**Accessing the Command Line**

* Windows: Command Prompt \(or PowerShell\)
  * Pre-Windows 9: Run -&gt; type "cmd" -&gt; Enter
  * Windows 8 or later: Win-Key -&gt; type "cmd" -&gt; Enter
  * Any version of Windows: search box -&gt; "cmd" -&gt; Enter
  * Any version of Windows: Win-Key + R -&gt; "cmd" -&gt; Enter
* **Mac**: Navigate to Applications -&gt; Utilities -&gt; Terminal
* **Linux**: CTRL + ALT + T \(doesn't work for me on some distros, but Super + T does\)

**IPCONFIG/IFCONFIG**

* Displays the IP address info of a host.
* Can also be used to obtain the MAC address of a host.
* Windows:
  * ipconfig or ipconfig /all \(/all to find the MAC address\).
  * ipconfig /release and ipconfig /renew \(makes it get new IP address via DHCP\).
  * Can be also used to flush and register DNS in Windows:
    * ipconfig /flushdns
    * ipconfig /registerdns
* Mac/Linux:
  * ifconfig or ifconfig -a \(-a to find the MAC address\).

**Ping**

* The protocol responsible for ping is ICMP \(Internet Control Messaging Protocol\)
* Tests layer 3 connectivity to any node.
  * Ex: "ping 8.8.8.8"
* Ping is the most widely use command line tool in networking.
* The first step in troubleshooting connectivity is to try a ping.
* Can specify IPv6 pings as well with the -6 flag or "ping6" command.
  * Windows: ping / ping -t or ping -6
  * Mac/Linux: ping or ping6

**ARP**

* Displays the ARP cache info from the Address Resolution Protocol.
* Used to identify IP address to MAC address mappings.
* Used to identify if a host knows how to reach another host.
* All Operating Systems:
  * arp -a \(displays arp cache\)
  * arp - s \(input a static arp entry\)
  * arp -d \(deletes an arp entry\)

**Trace Route**

* Traces out the hop by hop route in an IP endpoint.
* Shows the latency to each hop.
* Can specify IPv6 traces as well.
* Windows:
  * tracrt or tracert -6
* Mac/Linux:
  * traceroute or traceroute6

**Pathping**

* Similar to Trace Route but includes the local hop and excludes the latency on the initial trace.
* Performs a statistics computation on each hop to track the amount of lost vs sent packets and latency at each hop.
* "pathping" on all OSes.

  
**nslookup**

* Performs a Name Server Lookup
* Uses DNS to look up a specified hostname and find the IP address.
* Can also be used to perform a reverse lookup.
  * Looks up specified IP address and displays the hostname.
* "nslookup" on every OS.

**netstat**

* Displays the active Layer 4 \(TCP/UDP\) sessions on a host.
* Every OS:
  * netstat -a \(displays all sessions and listening ports\)
  * netstat -b \(displays the application associated with each session\)
  * netstat -n \(displays everything in numerical form\)

**nbtstat**

* Windows ONLY
* Displays the NetBIOS over TCP/IP statitstics.
* nbtstat -a \(displays the NetBIOS name table and MAC address of the specified computer name\)
* nbtstat - c \(displays the NetBIOS name cache and name to IP mappings\)
* nbtstat - R \(purged the name cache and reloads all preloaded name entries in the LMHOSTS file\)
* nbtstat -RR \(re-registers all names with WINS without rebooting\)

