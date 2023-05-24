# Netpractice

## Get started

With these resources you can get through it in every level but it not easy anyway

---

### Learn Basic Network 

Useful links:
[Classless Inter-Domain Routing]: https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing
[Subnet mask sheet]: https://dnsmadeeasy.com/support/subnet
[CIDR]: https://cidr.xyz/
[Broadcast Address]: https://en.wikipedia.org/wiki/Broadcast_address# 42-net-practice

## Overview
1. There are 10 levels available for training.
2. Complete the empty fields and click on button `Check again` to verify whether your configuration is correct or not.
3. Once the exercise is successful, click on button `Get my config` to download your configuration.
4. When you have successfully completed a level, click on button `Next level`.

## Networking Basics
### What is IP?
IP is a connectionless protocol that operates at the network layer of the OSI model. IP enables communication between hosts by carrying data within packets. Each host is assigned an IP address which is used to ensure that traffic is sent to the correct destination, synonymous in many ways to a postal address that we place on a letter.
An IP address (in the case of v4) is built upon 32-bits, expressed in four numbers known as octets. Each octet is 8 bits i.e one byte.
- `Network` - the network the IP address belongs to. For example the street name.
- `Host` - the host identifier of the device for the network. For example the house number.
![](https://www.packetcoders.io/content/images/2019/05/image2-1.png)
### What is Subnet Mask?
A subnet mask is a 32-bit number created by setting host bits to all 0s and setting network bits to all 1s. In this way, the subnet mask separates the IP address into the network and host addresses.
The “255” address is always assigned to a broadcast address, and the “0” address is always assigned to a network address. Neither can be assigned to hosts, as they are reserved for these special purposes.
![](https://www.packetcoders.io/content/images/2019/05/image1-4.png)

### What are the types of an IP address?

There are two important types of an IP address, which are:

    Static IP address: which stay permanent and it doesn’t change, and it’s used mostly for important equipement, such as (businesses, servers…)
    Dynamic IP address: which changes occasionally, and it’s used for consumer equipement, such as (laptop, smartphone, tablet…)


### What is the purpose of the IP addresses?

    The purpose of the IP address is to handle the connection between devices that send and recieve data all across the network.
    The IP address uniquely identifies every device on the internet, without one there’s no other way to contact them.
    IP addresses allow computing devices to communicate with destinations like websites and streaming services, and they let websites know who is connecting.

### What is the difference between the IPv4 and the IPv6?

    IPv4: deployed in the 1981, works with a 32-bits address, and has over 4.3 billion addresses (which is a small amount of addresses compared to IPv6), so IP addresses must be reused and masked, and it uses Numeric Dot-Decimal Notation (ex: 192.108.42.64), and you have to configure it manually.
    Ipv6: deployed in the 1998, works with a 128-bits address, and has over 340 undecillion addresses (which is 340 trillion, trillion, trillion, trillion [36 zeros]), so every device can have it's unique IP address, and it uses Alphanumeric Hexadecimal Notation (ex: 2002:0de6:0001:0042:0100:8c2e:0370:7234), and it supports auto-configuration.


### What is TCP/IP?

TCP/IP stands for Transmission Control Protocol/Internet Protocol, which is a set of rules that guide and allow computers to communicate on a network such as the internet.

### What is the difference between TCP and IP?

    TCP and IP are two separate computer network protocols.
    IP is the part that obtains the address which the data is sent to, while TCP is the part that is responsible for data delivery once that IP address has been found.


### How does TCP/IP exactly work?

TCP/IP job is to divide the different communication tasks into layers, each layer has a different function. Data goes through four individual layers before it is recieved on the other end, TCP/IP then goes through these layers in reverse to reassemble the data and represent it to the reciepent.

The four layers of the TCP/IP model are:

    Datalink Layer: also called the physical layer, is what handles the physical parts of sending and recieving data using the Ethernet, or WiFi, etc…
    Internet Layer: also called the network layer, and it controls the movement of the packets around the internet.
    Transport Layer: is what provides a reliable data connection between two devices, it divides the data into packets, knows the packets that are recieved from the other device, and it makes sure that the other device knows the packets it recieves.
    Application Layer: is the group of the applications that requires a network communication, which is what the user typically interacts with, such as emails, and messaging, because the lower layer handles the details of communication, and there’s no need for the applications to concern themselves with it.


### What is a switch?

A switch is a device that connects devices within the same network, usually a LAN network (which is a Local Area Network), and forwards data packets to and from those devices, unlike a router, a switch only sends the data to the devices it is intended for (which may be another switch, a router, or a user's computer).


### What is a router?

A router is a device that connects two or more packet-switched networks or subnetworks, it serves two primary functions, managing the traffic between these networks by forwarding data packets to their intended IP addresses, and allowing multiple devices to use the same internet connection.
How does a router work?

A router’s job is to direct and guide the packets that are sent so they get to their destination (which is their IP address) as efficiently as possible, and in order to send the packets effictively, a router uses an internal routing table (which is a list of paths to various network destination), a router read a packet header to determine where it is heading to, then it consults with the routing table to decide which path is the most efficient so the packet reaches its destination.
What is the difference between a Modem and a Router?

A router forms networks, and manages the flow of data within and between those networks, while a modem connects those networks to the internet. In another way, a router only connects the devices with each other to make a LAN between them all, but with no access to the internet, on the other hand, a modem can connect to one device only, but provides access to the internet.

And in order to make a LAN that connects to the internet, you should combine both a modem and a router together, so that the router connects all the devices while a modem give them access to the internet.
What is a loopback address?

A loopback address is an address that is built into the IP domain system in order to allow for a device to send and receive its own data packets. And it is a distinct reserved IP address range that starts from 127.0.0.0 and ends at 127.255.255.255, and its used for various kind of analysis, usually for testing purposes and debugging.

### What is a subnet?

A subnet or a subnetwork is a network inside a network. Subnets make networks more efficient.

Subnetting is the process of stealing bits from the HOST part of IP address in order to divide the large network into smaller ones called subnets. After subnetting, we end up with NETWORK SUBNET HOST fields, and we always reserve an IP address to identify the subnet and another one to identify the broadcast subnet address, and through subnetting, network traffic can travel a shorter distance without passing through unnecessary routes to reach its destination.

### How to calculate a subnet mask from IP address step by step?

We will work with the IP address 10.20.4.13/29
Step 1: Find Subnet Number:

Subtract prefix number from /32
32 - 29 = 3

Calculate Subnet Mask:
8 bits - 3 bits = 5 bits (Network bits turned on)

You might be asking why 8 bits, 8 bits are required for each octet.

|-------|-------|-------|-------|-------|-------|-------|-------|
| 128   | 64    | 32    | 16    | 8     | 4     | 2     | 1     |
|-------|-------|-------|-------|-------|-------|-------|-------|
| 1     | 1     | 1     | 1     | 1     | 0     | 0     | 0     |
|-------|-------|-------|-------|-------|-------|-------|-------|
| 128 + | 64 +  | 32 +  | 16 +  | 8     | =     248             |
|-------|-------|-------|-------|-------|-------|-------|-------|

Subnet Mask = 255.255.255.248

Step 2: Find Subnet Size:

Raise 2 to the power of deducation (8 - 3 = 5) -> Let's called it n.

2 ** n    = Subnet Size.
2 ** 3    = Subnet Sizes for each subnet.
2 * 2 * 2 = 8

NOTE: 8 is the block size for the subnet, so for example:
the increments will now be 0 8 16 24 32 and so on (we add 8 each time)

Step 3: Find Broadcast Address:

Subnet size - 1
(2 ** n) - 1  = Broadcast Address
(2 ** 3) - 1  = (8 - 1) = 7

Step 4: Locate IP Address Subnet:

Identify subnet block for IP address:
-> Where in each increment is the address 10.20.4.13/29 located (0 8 16 32 40)?

13 falls between 8 and 16 and therefore the address is in the valid host range of the subnet 10.20.4.8/29

Step 5: Calculate The Valid Hosts:

Subnet size - 2
(2 ** n) - 2 = Valid Host Range
(2 ** 3) - 2 = (8 - 2) = 6

And from these steps, we can know 4 important things:

Subnet Address    -> 10.20.4.8/29
Min Host Address  -> 10.20.4.9/29
Max Host Address  -> 10.20.4.14/29
Broadcast Address -> 10.20.4.15/29


### Tools
[IP Calculator](https://jodies.de/ipcalc) - ipcalc takes an IP address and netmask and calculates the resulting broadcast, network, Cisco wildcard mask, and host range.

### References
- [techtarget.com](https://www.techtarget.com/searchnetworking/tip/IP-addressing-and-subnetting-Calculate-a-subnet-mask-using-the-hosts-formula) - How to calculate a subnet mask from hosts and subnets
- [softwaretestinghelp.com](https://www.softwaretestinghelp.com/subnet-mask-and-network-classes/) - Guide to Subnet Mask (Subnetting) & IP Subnet Calculator
- [avinetworks.com](https://avinetworks.com/glossary/subnet-mask/) - Glossary Subnet mask
- [packetcoders.io](https://www.packetcoders.io/a-beginners-guide-to-subnetting/) - A Beginners Guide to Subnetting




