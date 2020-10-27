---
layout: post
title: Understanding Networks
published: true
---
## Network Models

There are 2 main network models. The Open Systems Interconnection (OSI) 7-layer model and the Transmission Control Protocol/Internet Protocol (TCP/IP) model. These models help us to understand better how networks function and they are compared in the following table.

![OSI vs TCP_IP model.png]({{site.baseurl}}/_posts/OSI vs TCP_IP model.png)

## Network Packet

Data first comes from an application into the network card. The network card then creates
the frame and sends it out into the network. Data is sent in discrete chunks of ones and zeros called packets or frames. A single frame can be up to 1500 bytes long which is about 12,000 ones and zeroes (8 bits to a byte). As a frame enters the receiving network card, the data is segmented and sent to the appropriate application. The frame is then destroyed within the network card itself.

A frame can be segmented and represented as follow:

![Packet.png]({{site.baseurl}}/_posts/Packet.png)


### Media Access Control

_**MAC (Media Access Control)**_ address is the physical address of a device, it is a unique identifier for a _**NIC (Network Interface Card)**_ and is broken up into 6 pairs. The first 3 pairs are the OEM number or identifiers. The last 3 pairs are burned into each device at the factory and each card gets a unique ID.

Frames have a destination and source MAC address. NICs use MAC addresses to decide whether or not to process a frame. _**CRC (Cyclic redundancy check)**_ is used as a way to check that the data is good. If the packet is corrupted it will be resent. 

- **Broadcast** happens when the MAC address on the frame is recognized by all the NICs in the network.

- **Unicast** happens when the MAC address on the frame has a specific destination. 

Anytime you have a group of computers that can hear each other’s broadcast, they are in a broadcast domain. Anytime you plug into a hub, all the computers on that hub are going to be a member of a single broadcast domain. The MAC address for a broadcast is all F’s and it looks like this FF-FF-FF-FF-FF-FF.
    
### IP Packet

MAC addresses don’t identify in anyway that computers are all part of a single local area network. This is when IP address comes into play. Unlike MAC addresses, IP addresses are not fixed with a network card. An IP packet consist of the destination IP, source IP and the data itself. An IP packet sit within frames and they never change, frames consist of the destination MAC address, the source MAC address and the CRC.

When a computer looks at the destination IP and realize that it is not part of the network, it  puts a frame around the IP packet that have the destination MAC address of the router which is also known as the default gateway.

The default gateway is the connection to your router itself. When the packet reaches the router, it looks up the routing table and changes the frame before sending out the packet to the destination.

### Network Protocols

Port numbers range from 0 to 65,535 but the first 1024 are reserved.
We have two protocols, _**TCP (Transmission Control Protocol)**_ and _**UDP (User Datagram Protocol)**_ , TCP is connection-oriented and UDP is connectionless and does not verify receipt of data. TCP has two parts to it, one is a sequencing number which allows you to reassemble data and the second part is the acknowledgement which tells the other computer that all the data has been received.![]({{site.baseurl}}/)
