# Disaster Recovery & Business Continuity Plans

**Disaster Recovery / Business Continuity Plans**

* Backup Concepts
* Recovery Sites
  * Hot Site
  * Warm Site
  * Cold Site
* Order of Restoration
  * Recovery Time Objective
  * Recovery Point Objective
* Geographic Considerations
* Continuity of Operations Planning

**Planning Documents**

* Business Continuity Plan \(BCP\) - ensure the restoration of organizational functions in the shortest possible time, even if services resume at a reduced level of effectiveness or availability. Similar to Continuity of Operations Plan \(CoOP\).
* Disaster Recover Plan \(DRP\) - ensure a full recovery of operational capacity following a disaster \(natural or manmade\).
* Should be determined and written prior to an incident.
* A restoration plan also should include contingency planning.

**Recovery Sites**

* Backup Sites - Locations for recovering systems and/or business operations.
  * Hot Site - Servers, networks, and telecom equipment in place and online to reestablish service. Most expensive.
  * Warm Site - Some equipment in place. May not be online. Requires admins to install and configure systems to resume ops.
  * Cold Site - Facility that isn't immediately ready to use. May need to bring your own equipment. Least expensive.

**Order of Restoration**

* Prioritized restore sequence.
* Based on Business Impact Assessment \(BIA\)
* Most critical systems restored first.
* Recovery Time Objective \(RTO\) - The maximum amount of time that a process or service is allowed to be down and the consequences still to be considered acceptable.
* Recovery Point Objective \(RPO\) - The point of last known good data prior to an outage that is used to recover systems.

**Types of Backups**

* Full - Complete backup of all data.
  * The most time and resource intensive form of backup.
* Incremental - Requires a full backup. Capture what has changed since the last incremental backup.
  * Requires each incremental backup along with the full for complete restoration.
* Differential - saves the data that has changed since the last full backup.
  * Requires the full backup and most recent differential backup.
* Copies and Snapshots - Like a full backup. Stored on the system.

**Backup Strategy**

* Grandfather-Father-Son Backup - Define three sets of backups.
  * The first set, the son, represents daily backups.
  * A second set, the father, is used to perform full backups.
  * The fine set of three, the grandfather, is used to perform full backups on the last day of each month.
  * Over time, the son becomes the father and the father the grandfather.
  * The most common strat.

**Geographic Considerations**

* Alternate Site Planning
* Locations for Recovery
* Utilities
* Proximity to a Main Site
* Personnel
* Legal Implications
* Use of Cloud Services

**Continuity of Operations Planning \(CoOP\)**

* Policies and procedures - designed to ensure that an organization can recover from a potentially destructive incident and resume operations as quickly as possible following that event.
* Ensures systems, data, and personnel availability.
* Failover - system redundancy.
* Availability of alternate processing, work sites, and facilities.
* Alternate business practices.
* Testing, training, and exercises.

