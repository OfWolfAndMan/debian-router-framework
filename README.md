# debian-router-framework

## Summary
As of now, there are many available network routers out there. However, turnaround time, 
along with rising costs has made it difficult for some companies to keep pace. Lead times post-pandemic
have been, at times, upwards of 6 months, which is unacceptable for many trying to run a business
and/or get a reasonable turnaround time for an RMA.

Additionally, bugs among prominent vendors is a common thing. Licensing structures have become complicated
and expensive for some. Some of the prominent vendors include:

- Cisco
- Juniper
- Arista


FRR (Free Range Routing) has been a topic of interest as of recently, as its feature set in providing a viable
routing protocol suite that can be run on most common versions of Linux, without requiring special hardware
(Albeit there's certain hardware that lacks features for a full feature set).

Platforms known for there usage of FRR include:

- VyOS
- Netgate's TNSR

Both VyOS and Netgate provide there own command line, while using the FRR feature set under the hood.

Additionally, TNSR (And to some degree, other vendors as of recent) have began using something known
as VPP (Vector Packet Processing). VPP is a capability that's been emerging over recent years, which
is capable of something the antiquated Scalar Packet Processing model (Which older routers use) is not.

Scalar packet processing is only capable of processing a single packet at a time. So if it needs to get
NATed, marked for QoS purposes, encapsulated to traverse an IPSec tunnel, etc, each packet is processed
individually. In the VPP model, packets are processed in groups rather than individually. Additionally,
VPP supports utilizing multiple CPU cores for such things.

The intention of this repository is to build a Linux router from scratch. Features you'd expect on a router 
like:

- OSPF/BGP
- Netflow exports
- Flow filtering (ACLs, route maps, etc)
- L2 High Availability (VRRP)


## Technology Stack
Please note all components in yellow are not implemented in the current 
iteration, but are being considered for future usage.

![Alt Text](Technology-Stack.jpeg?raw=True)
