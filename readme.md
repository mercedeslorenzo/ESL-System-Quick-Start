# ESL System Quick Start

## Arquitecture

This pages shows Electronic Shelf Label (ESL) systems built on top of Telink's chipsets. The general architecture is demonstrated in the following diagram. A complete ELS system normally includes the following building blocks:

![Architecture](http://wiki.telink-semi.cn/dokuwiki/lib/exe/fetch.php?media=pasted:20181022-182247.png")

### Host/Server

Unified management of all device information Control gateway and tag nodes networking Update tag information to the specified node

### Gateway

Subnet management, caching and distributing tag information Receive status updates from tags Monitor the operating status of the network Support OTA

### ESL Node

Telink works with our design partners to provide complete solutions to end customers. In this process, Telink mainly focus on the part between the Gateway and the ESL nodes, where ESL nodes runs on Telink ultra-low-power RF SoC and the Gateway communicates with these nodes using Telink high performance RF SoC as well. The backend systems such as Gateway management systems, cloud server, cloud management systems and interfaces are provide by the ESL total solution design houses.

The development kit provided by Telink demonstrates a complete ESL node reference design and the connection between the Gateway and the ESL nodes. The kit includes:

* ESL nodes with E-paper display
* Telink ESL dongle that can demonstrate the RF connectivity on Gateway
* Burning Key
* PC tools (burning tools, ESL tools for controlling ESL nodes)

## Software Download

Download Telink Tools [Burning and Debugging Tool](http://wiki.telink-semi.cn/dokuwiki/doku.php?id=menu:tools:telink_bdt)

Download ESL Software [ESL_Software](http://wiki.telink-semi.cn/tools_and_sdk/ESL/ESL_Quick_Guide.zip)

![Software Download](http://wiki.telink-semi.cn/dokuwiki/lib/exe/fetch.php?media=pasted:20181023-101939.png")

## Quick Setup Guide

1. __Step 1__: First read 4byte flash address from 0x1c000,if it not all 0xff,means it has been joined in a PAN,please erase these to keep it Factory Settings,Then setting Node IEEE Address write some 8byte address in a special flash address from 0x1d000

![Step 1](http://wiki.telink-semi.cn/dokuwiki/lib/exe/detail.php?id=menu%3Asolution%3Aesl&media=pasted:20181023-100929.png")

2. __Step 2__: Download the bin files to the Node(mcu:8258) and Gateway(mcu:8267)

3. __Step 3__: Run ESL_Server.exe, Power on Gateway and Node,you can see the dispay of IEEE ADDR on the screen is same as the input in Step1

![Step 3](http://wiki.telink-semi.cn/dokuwiki/lib/exe/detail.php?id=menu%3Asolution%3Aesl&media=pasted:20181023-093928.png)

4. __Step 4__: Add a New Gateway ,setting Gateway information

![Step 4](http://wiki.telink-semi.cn/dokuwiki/lib/exe/detail.php?id=menu%3Asolution%3Aesl&media=pasted:20181022-192103.png)

5. __Step 5__: Add a node in the new PAN, a simple pan is be builded

![Step 5](http://wiki.telink-semi.cn/dokuwiki/lib/exe/detail.php?id=menu%3Asolution%3Aesl&media=pasted:20181022-191601.png)

6. __Step 6__: Refresh a picture to node

![Step 6](http://wiki.telink-semi.cn/dokuwiki/lib/exe/detail.php?id=menu%3Asolution%3Aesl&media=pasted:20181023-104400.png)
