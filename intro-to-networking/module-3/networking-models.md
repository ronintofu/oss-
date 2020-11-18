# Networking Models

**THE OSI MODEL - Intro to OSI and the 7 Layers**

Open Systems Interconnection \(OSI\)

![](https://www.evernote.com/shard/s342/res/42a7d11e-3caf-51f2-ff73-87ee2894d422)

* Created by International Standards Organization \(ISO\).
  * Published in 1984 as ISO 7498.
* A 7-layer visual model.
* Characterizes and standardizes the communication functions.
* A way to reference and understand the relationship between network communication protocols, hardware, software, standards, and concepts.
* Each layer serves the layer above it. \(TOP DOWN\)
* **7. Application**
  * Application services end user processes such as file transfers, email, remote terminal access, domain name resolution, web transfer, network management, etc. Protocols such as FTP & Telnet.
* **6. Presentation**
  * Provides translation to/from the application layer. Performs data encryption, decryption, compression, and decompression. Associated with file formats such as JPEG, MPEG, etc.
* **5. Session**
  * Coordinates, establishes, manages, and tears down sessions between applications on either side of the connection. Maintains separate sessions for the different application data streams.
* **4. Transport**
  * Segments and reassembles data from upper layers and unites them into the same data stream. Provides flow control for data-loss prevention as well as reliable and unreliable transport methods.
* **3. Network**
  * Provides logical network addressing and path determination/routing services. Responsible for packet delivery, fragmentation, and sequencing. This is the layer where Internet Protocol resides.
* **2. Data Link**
  * Includes the Logical Link Control \(LLC\) sub-layer which provides error detection and control. Delivers frames using unique hardware addressing via the Media Access Control \(MAC\) sub-layer.
* **1. Physical**
  * Turns raw bits into electric signaling and defines physical network media such as copper cabling, fiber optics, and wireless transmission standards. Concerned with bit rates and transmission modes.

**Passing Through the Layers**

Protocol Data Unit \(PDU\) - Describes the data as it moves through each layer.![](https://www.evernote.com/shard/s342/res/8fdfa7e2-fe70-efb6-42d5-191991c61747)  


**Devices and Protocols in OSI**

Examples of protocols and standards at each layer.

![](https://www.evernote.com/shard/s342/res/ffa8c012-d802-37a3-93fa-2f2866e9b5d6)  


**Remembering the Layers**

![](https://www.evernote.com/shard/s342/res/44bb7dba-f5a4-bed4-83b7-20665bf4d5e1)

