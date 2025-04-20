---
title: CH1 computer networks and the internet
date: 2025-04-20 21:43:48
---

# CH1 computer networks and the internet

## 1.1 what is internet?

Two ways to describe what is internet?

1. Describe the nuts and bolts of internet - the basic hardware and software components that make up the internet.
2. A networking infrastructure that provides services to distributed applications.

### 1.1.1 A nuts and bolts description

All of these devices not only the computing devices(laptops, servers ...) but also nontraditional devices(watches, cars, ...) are called **hosts** or **end systems.**

![截屏2025-02-25 15.09.52]( /images/截屏2025-02-25 15.09.52.png)

End systems are connected together by a network of **communication links** and **packet switches**.

When one end system has data to send to another end system,  the sending end system segments the data and adds header bytes to each segment. The resulting packages of informantion are called **packets**.

Two most prominent types in today's internet are **routers** and **link-layer switches**.

The sequence of communication links and packet switches traversed by a packet is known as a **route** or **path** through the network.

End system access the Internet through **Intenet Service Providers**(ISPs), including residential ISPs such as local cable or telephone companies, corporate ISPs, university ISPs, ISPs that provide WiFi access in airports, hotels, and other public places and celluar data ISPs, providing mobile access to out smartphones and other devices.

Each ISPs is in itself a network of packet switches and communication links.

**Transmission Control Protocol(TCP)** and **the Internet Protocol(IP)** are two of the most important protocols in the internet. The internet's principal protocols are collectively known as **TCP/IP**.

### 1.1.2 A services description

**Distributed Applications** - involve multiple end systems that exchange data with each other.

### 1.1.3 What is a protocol?

![截屏2025-02-25 15.54.02](/Users/lkw/my_website/source/_posts/CH1-computer-networks-and-the-internet/截屏2025-02-25 15.54.02.png)

A **protocol** defines the format and the order of messages exchanged between two or more communicating entities, as well as the actions taken on the transmission and/or receipt of a message or other event.

## 1.2 The network edge

Hosts are sometimes divided into two categories: **clients** and **servers**.

clients: desktops, laptops, and so on

servers: powerful machines that store and distribute Web pages, stream video and so on.

### 1.2.1 Access Networks

Access network - the network that **<u>physically connects an end system to the first router(edge router) on a path from the end system to any other distant end system.</u>**

![截屏2025-02-26 16.30.15](/Users/lkw/my_website/source/_posts/CH1-computer-networks-and-the-internet/截屏2025-02-26 16.30.15.png)

Access networks are marked with thick, shaded lines.

#### Home Access: **DSL**, Cable, **FTTH**, and 5G Fixed wireless.

![截屏2025-02-26 18.29.22](/Users/lkw/my_website/source/_posts/CH1-computer-networks-and-the-internet/截屏2025-02-26 18.29.22.png)

DSL(digital subscriber line):

The home's DSL modem takes digital data and translates it to high-frequency tones for transmission over telephone wires to the CO.

The analog signals from many such houses are translated back into digital format at the DSLAM.

- A high-speed downstream channel, in the 50 kHz to 1 MHz band

- A medium-speed upstream channel, in the 4 kHz to 50 kHz band

- An ordinary two-way telephone channel, in the 0 to 4 kHz band

FTTH(fiber to the home):

Provide an optical fiber path from the CO directly to the home.

![截屏2025-02-26 18.34.12](/Users/lkw/my_website/source/_posts/CH1-computer-networks-and-the-internet/截屏2025-02-26 18.34.12.png)

#### Access in the enterprise(and the home): Ethernet and WiFi



For the ethernet:

![截屏2025-03-01 22.15.52](/Users/lkw/my_website/source/_posts/CH1-computer-networks-and-the-internet/截屏2025-03-01 22.15.52.png)

For the WiFi:

![截屏2025-03-01 22.16.01](/Users/lkw/my_website/source/_posts/CH1-computer-networks-and-the-internet/截屏2025-03-01 22.16.01.png)

### 1.2.2 Physical Media

#### Guided Media

Twisted-pair Copper Wire, Coaxial Cable, Fiber Optics

#### Unguided Media

Terrestrial Radio Channels, Satellite Radio Channels

## 1.3 The network core

### 1.3.1 Packet Switching

To send a message from a source end system to a destination end system, the source breaks long messages into smaller chunks of data known as **packets**. Between source and destination, each packet travels through communication links and **packet switches**(for which there are two predominant types, **routers** and **link-layer switches**)

Most packet switches use **store-and-forward transmission** at the inputs to the links.

**Store-and-Forward Transmission**

The packet switch must receive the entire packet before it can begin to transmit the first bit of the packet onto the outbound link.

![截屏2025-02-26 18.58.37](/Users/lkw/my_website/source/_posts/CH1-computer-networks-and-the-internet/截屏2025-02-26 18.58.37.png)

At the case that there is no propagation delay:

If sending **one** packet from source to destination over a path consisting of $N$ links each of rate $R$.

$
d_{\text{end-to-end}} = N \frac{L}{R}
$

So how about the delay for $P$ packets sent over a series of $N$ links?

**Queuing Delays and Packet Loss**

**output buffer**(also called an **output queue**): stores packets that the router is about to send into that link.

queuing delays are variable and depend on the level of congestion in the network.

**since the amount of buffer space is finite**, <u>as an arriving packet finds that the buffer is completely full</u>, **packet loss** will occur - either the arriving packet of one of the already-queued packets will be dropped.

**Forwarding Tables and Routing Protocols**

Each router has a **forwarding table** that maps destination addresses to that router's outound links.

Routing protocols are used to automatically set the forwarding tables.

### 1.3.2 Circuit Switching

Two fundamental approaches to moving data through a network of links and switches: **circuit switching** and **packet switching**.

In circuit-switched networks, the resources needed along a path to provide for communication between the end system are **reserved** for the duration of the communication session between the end system.

![截屏2025-02-26 19.46.28](/Users/lkw/my_website/source/_posts/CH1-computer-networks-and-the-internet/截屏2025-02-26 19.46.28.png)

**The difference betwenn this two switching way:**

![AgAABS-o-gyHTMxf2ulPxJXgwh0BnPWw_副本](/Users/lkw/my_website/source/_posts/CH1-computer-networks-and-the-internet/AgAABS-o-gyHTMxf2ulPxJXgwh0BnPWw_副本.png)

**Multiplexing in Circuit-Switched Networks:**

**Frequency-Division Multiplexing(FDM), Time-Division Multipluxing(TDM)**

![截屏2025-02-26 20.04.03](/Users/lkw/my_website/source/_posts/CH1-computer-networks-and-the-internet/截屏2025-02-26 20.04.03.png)

For FDM, the frequency domain is segmented into four bands, each of bandwidth 4 KHZ.

For TDM, the time domain is segmented into frames, with four time slots in each frame; each circuit is assigned the same dedicated slot in the revolving TDM frams.

### 1.3.3 A Network of Networks

**The Real-World Three-Tier Model(structure 3)**

1. Tier-1 ISPS(Top Level - Global Backbone Providers)

    - These ISPs operate **large-scale international networks** and connect to each other through **peering agreements**.

    - They don’t pay anyone for transit (they exchange traffic freely with other Tier-1 ISPs).

    - Examples: **AT&T, Level 3 Communications, Sprint, NTT**.

2. Tier-2 ISPS(Regional ISPS)
    - These ISPs operate **national or regional networks** and connect to Tier-1 ISPs for broader Internet access.
    - They may also **peer** with other Tier-2 ISPs to reduce costs.
3. Tier-3 ISPS(Access ISPS / Local ISPS)
    - These ISPs serve **individual customers and businesses**.
    - They buy Internet transit from Tier-2 ISPs.

**Network Structure 4**

**PoP** is simply a group of one or more routers(at the same location) in the provider's network where customer ISPs can connect into the provider ISP.

Any ISP(except for tier-1 ISPs) may choose to **multi-home**, that is, to connect to two or more provider ISPs.

To reduce prices, a pair of nearby ISPs at the same level of the hierarchy can **peer**, that is, they can directly connect their networks togerther so that all the traffic between them passes over the direct connection rather than through upstream intermediaries.

A third-party company can create an **Internet Exchange Point(IXP)**, which is a meeting point where multiple ISPs can peer together, which is a meeting point where multiple ISPs can peer togerther.

Network Structure 4 is consisted of **access ISPs, regional ISPs, tier-1 ISPs, PoPs, multi-homing, peerig and IXPs**.

**Network Structure 5**

![截屏2025-02-27 19.24.03](/Users/lkw/my_website/source/_posts/CH1-computer-networks-and-the-internet/截屏2025-02-27 19.24.03.png)

This structure builds on top of Network structure 4 by adding **content-provider networks.**

## 1.4 Delay, Loss, and Throughput in Packet-Switched Networks

![截屏2025-02-28 16.34.13](/Users/lkw/my_website/source/_posts/CH1-computer-networks-and-the-internet/截屏2025-02-28 16.34.13.png)

**Processing Delay**

The time required to examine the packet's header and determine where to direct the packet is part of the **processing delay**. After thie nodal processing, **the router directs the packet to the queue** that precedes the link to router B.

**Queuing Delay**

At the queue, the packet experiences a **queuing dealy** as it waits to be transmitted onto the link.

**Transmission Delay**

Denote the length of the packet by $L$ bits, and denote the transmission rate of the link from router A to router B by $R$ bits/sec. For example, for a 10 Mbps Ethernet link, the rate is R = 10 Mbps; The transmission delay is $L/R$. This is the amount of time required to push all of the packet's bits into the llink.

**Propagation Delay**

The time required to propagate from the beginning of the link to router B is the **propagation delay**. The propagation speed depends on the physical medium of the link and is in the range of

$2 \cdot 10^8$ meters/sec to $3 \cdot 10^8$ meters/sec

The propagation delay is $d/s$, where $d$ is the distance between router A and router B and $s$ is the propagation speed of the link.

If we let $d_{proc}$, $d_{queue}$, $d_{trans}$, $d_{trans}$, and $d_{drop}$ denote the processing, queuing, transmission, and propagation delays, then the total nodal delay is give by

$d = d_{proc} + d_{queue} + d_{trans} + d_{prop}$

### 1.4.2 Queuing Delay and Packet Loss

Let $a$ denote the average rate at which packets arrive at the queue(a is in units of packets/sec). $R$ is the transmission rate; For simplicity, that all packets consist of $L$ bits.  Then the average rate at which bits arrive at the queue is $La$ bits/sec. The ratio $La/R$​, called the **traffic intensity**.

If $La/R > 1$​​, the queue will tend to increase without bound and the queuing delay will approach infinity. Therefore, one of the golden rules in traffic engineering is: **Design your system so that the traffic intensity is no greater than 1.**



![截屏2025-02-28 20.00.00](/Users/lkw/my_website/source/_posts/CH1-computer-networks-and-the-internet/截屏2025-02-28 20.00.00.png)

Typically, the arrival process to a queue is **random**; The arrivals do not follow any pattern and the packets are spaced apart by random amounts of time.

The qualitative dependence of average queuing delay on the traffic intensity is shown above.

**Packet Loss**

In reality, a queue preceding a link has **finite** capacity. Because the queue capacity is finite, packet delays do not erally approach infinity as the traffic intensity approaches $1$. Instead, a packet can arrive to find a full queue. With no place to store such a packet, a router will **drop** that packet; that is, the packet will be **lost**.

From an end-system viewpoint, a packet loss will look like a packet having been transmitted into the network core but never emerging from the network at the destination.

### 1.4.3 End-to-End Delay

Let's now consider the total delay from source to destination. Suppose there are $N - 1$​ routers between the source host and the destination host. Now suppose that the network is uncongeted(so that queuing delays are negligible).



> [!NOTE]
>
> $d_{end-end} = N(d_{proc} + d_{trans} + d_{prop})$
>
> $d_{end-end} = N(d_{proc} + d_{trans} + d_{prop})$

**Traceroute**

Traceroute is a simple program that can run in any Internet host. When the user specifies a destination hostname, the program in the source host sends multiple, special packets toward that destination. As these packets work their way toward the destination, the pass through a series of routers. When a router receives one of these special packets, it sends back to the source a short message that contains the name and the address of the router.

More specifically, suppoes there are $N - 1$ routers between the source and the destination. Then the source will send $N$ special packets into the network. For example, the $nth$ router receives the $nth$ packet marked $n$. For each router, as they receive the specific packet, they don't forward the packet toward its destination, but instead send a message back to the source.  

Traceroute actually repeats the experiment just described three times, so the source actually sends $3 * N$ packets to the destination.

### 1.4.4 Throughput in Computer Networks

The **instataneous throughput** at any instant of time is the rate(in bits/sec) at which Host B is receiving the file.

If the file consists of $F$ bits and the transfer takes $T$ seconds for Host B to receive all $F$​ bits, then the **average throughput** of the file transfer is F/T bits/sec.

$R_{s}$ denotes the rate of the link between the server and the router.

$R_{c}$ denotes the rate of the link between the router and the client.

If $R_s < R_c$, the throughput is $R_s$ bps

If $R_s > R_c$, the throughput is $R_c$​ bps

Thus, for this simple two-link network, the throughtput is min{$R_c$, $R_s$​}, that is, it's the transmission rate of the **bottleneck link**.

We can now approximate the time it takes to transfer a large file of $F$ bits from server to client as $F/min\{R_s, R_c\}$​.

![截屏2025-02-28 21.56.07](/Users/lkw/my_website/source/_posts/CH1-computer-networks-and-the-internet/截屏2025-02-28 21.56.07.png)

## 1.5 Protocol Layers and Their Service Models

### 1.5.1 Layered Architecture

To provide structure to the design of network protocols, network designers organize protocols in **Layers**.

![截屏2025-03-01 17.36.21](/Users/lkw/my_website/source/_posts/CH1-computer-networks-and-the-internet/截屏2025-03-01 17.36.21.png)

The protocols of the various layers are called the **protocol stack**.



**Application Layer**

The internet's application layer includes many protocols, such as the **HTTP** protocol(for web document request and transfer), **SMTP**(for the transfer of e-mail messages), and **FTP**(for the transfer of files between two end systems).

We'll refer to this packet of information at the application layer as a **message**.

**Transport Layer**

The Internet's transport layer transports application-layer messages between application endpoints. There are two transport protocols, **TCP** and **UDP**. TCP provides a **connection-oriented** service to its applications. <u>It includes guaranteed delivery of application-layer messages to the destination and flow control.</u>The UDP protocols provides a **connectionless** service to its applications. <u>This is a no-frills service that provides no reliability, no flow control, and no congestion control.</u> We'll refer to a transport-layer packet as a segment.

**Network Layer**

The Internet's network layer is responsible for moving network-layer packets known as **datagrams** from one host to another. The Internet transport-layer protocol(TCP or UDP) in a source host passes a transprot-layer segment and a destination address to the network layer. The network layer then provides the service of delivering the segment to the transport layer in the destination host.

The Internet's network layer includes the celebrated **IP** protocol, which <u>defines the fields in the datagram as well as how the end system and routers act on these fields.</u> The Internet's network layer also contains <u>routing protocols that determine the routes that datagrams take between sources and destinations.</u>

**Link Layer**

To move a packet from one node(host or router) to the next node in the route, the network layer relies on the services of the link layer. In particular, the network layer passes the datagram down to the link layer, which <u>delivers the datagram to the next node along the route</u>. At this next node, the link layer passes the datagram up to the network layer.

The services provided by the link layer depend on the specific link-layer protocol that is employed over the link. The network layer will receive a different service from each of the different link-layer protocols. We'll refer to the link-layer packets as **frames**.

**Physical Layer**

<u>While the job of the link layer is to move entire frames from one network element to an adjacent network element, the job of the physical layer is to move the individual bits within the frame from one node to the next.</u> The protocols in this layer are again link dependent and further depend on the actual transmission medium of the link(such as twisted-layer protocols, coaxial cable,...). In each case, a bit is moved across the link in a different way.

### 1.5.2 Encapsulation

![截屏2025-03-01 19.52.52](/Users/lkw/my_website/source/_posts/CH1-computer-networks-and-the-internet/截屏2025-03-01 19.52.52.png)

## 1.6 Networks Under Attack



**The bad guys can put malware into your host via the internet**

**malware** - that can also enter and infect our devices. Once malware infects our device it can do all kinds of devious things. Our compromised host may also be enrolled in a network of thousands of similarly compromised devices, collectively known as a **botnet**, which the bad guys control and leverage for span e-mail distribution or distributed denial-of-service atttacks against targeted hosts.

Much of the malware out there today is **self-replicating**: once it infects one host, it seeks into yet more more hosts.

**The bad guys can attack servers and network infrastructure**

Another broad class of security threats are known as **denial-of-service(DOS) attacks**. A DOS attack renders a network, host, or other piece of infrastructure unusable by legitimate users. Web servers, e-mail servers, DNS servers, and institutional networks can all be subject to DOS attacks.

Most Internet DOS attacks fall into one of three categories:

- Vulnerability attack	This involves sending a few well-crafted messages to a vulnerable application or operating system running on a targeted host. If the right sequence of packets is sent to a vulnerable application or operating system, the service can stop or, worse, the host can crash.
- Bandwidth flooding        The attacker sends a deluge of packets to the targeted host-so many packets that the target's access link becomes clogged, preventing legitimate packets from reaching the server.
- Connection flooding.       The attacker establishes a large number of half-open or fully open TCP connections at the target host. The host can become so bogged down with these bogus connections that it stops accepting legitimate connections.

Detail for bandwidth-flooding attack:

If all the traffic emantes from a single source, an upstream router may be able to detect the attack and block all traffic from that source before the traffic gets near the server. In a **distributed DOS(DDOS) attack**, illustrated in figure below.

![截屏2025-03-01 21.10.44](/Users/lkw/my_website/source/_posts/CH1-computer-networks-and-the-internet/截屏2025-03-01 21.10.44.png)

**The bad guys can sniff packets**

A passive reveiver that records a copy of every packet that flies by is called a **packet sniffer**. A bad guy who gains access to an institution's access router or access link to the Internet may be able to plant a sniffer that makes a copy of every packet going to/from the organization. Sniffed packets can then be analyzed offline for sensitive information.

**The bad guys can masquerade as someone you trust**

Imagine the unsuspecting receiver who receives such a packet, takes the (false) source address as being truthful, and then performs some command embedded in the packet's contents. The ability to inject packets into the Internet with a false source address is known as **IP spoofing**.

## Summary

1. Various pieces of hardware and software that make up the internet in particular and comupter networks.
2. The edge of the network, end systems, applications and the transport service provided to the applications running on the end systems.
3. Link-layer technologies and physical media in the access network.
4. Network core, packet switching, circuit switching and its pros and cons.
5. Structure of the global internet.
6. Delay, throughput and packet loss.
7. Protocol stack.
8. Security attacks.