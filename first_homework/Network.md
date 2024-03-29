# A technical report about  computer network

- ### Definition

  A **computer network** is a digital telecommunications network which allows nodes to share resources. In computer networks, computing devices with each other using connections  between nodes. These data links are established over  such as wires or optic cables, or such as Wi-Fi.

- ### Network packet

  A **network packet** is a formatted unit of data carried by a packet-switched network. A packet consists of control information and user data, which is also known as the payload. Control information provides data for delivering the payload, for example: source and destination network addresses, error detection codes, and sequencing information. Typically, control information is found in packet headers and trailers.

  In packet switching, the bandwidth of the communication medium is shared between multiple communication sessions, in contrast to circuit switching, in which circuits are preallocated for the duration of one session and data is typically transmitted as a continuous bit stream.

  There is no denying that packet switching, which we are using today, is far better than the circuit switching because of better fault handling. Suppose we lost or broke a package on the road, we can use error detecting codes to find the broken package, and resend the package. In my humble opinion, it is much harder for bit stream to achieve this effect.

  In the seven-layer OSI model of computer networking, *packet* strictly refers to a protocol data unit at layer 3, the network layer. The correct term for a data unit at layer 2, the data link layer, is a *frame*, and at Layer 4, the transport layer, the correct term is *segment* or *datagram*. For TCP/IP communication over Ethernet, a TCP segment is carried in one or more IP packets , which are each carried in one or more Ethernet frames.

- ### OSI model

  - #### Definition

    The **Open Systems Interconnection model** (**OSI model**) is a conceptual model that characterizes and standardizes the communication functions of a telecommunication or computing system without regard to its underlying internal structure and technology. Its goal is the interoperability of diverse communication systems with standard communication protocols. The model partitions a communication system into abstraction layers. The original version of the model had seven layers.

  - #### Chart

    [![Capture.png](https://i.postimg.cc/HsT9L72Q/Capture.png)](https://postimg.cc/Z0Dd7nXR)

  - #### Layer 1: Physical Layer

    This layer may be implemented by a PHY chip.

    The physical layer consists of the electronic circuit transmission technologies of a network. It is a fundamental layer underlying the higher level functions in a network, and can be implemented through a great number of different hardware technologies with widely varying characteristics.

    The physical layer defines the means of transmitting raw bits rather than logical data packets over a physical data link connecting network nodes. The bitstream may be grouped into code words or symbols and converted to a physical signal that is transmitted over a transmission medium. The physical layer provides an electrical, mechanical, and procedural interface to the transmission medium. The shapes and properties of the electrical connectors, the frequencies to broadcast on, the line code to use and similar low-level parameters, are specified here.

  - #### Layer 2: Data Link Layer

    The **data layer**, or **layer 2**, is the second layer of the seven-layer OSI model of computer networking. This layer is the protocol layer that transfers data between adjacent network nodes in a wide area network (WAN) or between nodes on the same local area network (LAN) segment.

    The data link layer has two sublayers: *logical link control* (LLC) and *media access control* (MAC).

    A MAC address is intended as a unique serial number. MAC addresses are typically assigned to network interface hardware at the time of manufacture. The most significant part of the address identifies the manufacturer, who assigns the remainder of the address, thus provide a potentially unique address. This makes it possible for frames to be delivered on a network link that interconnects hosts by some combination of repeaters, hubs, bridges and switches, but not by network layer routers. Thus, for example, when an IP packet reaches its destination (sub)network, the destination IP address (a layer 3 or network layer concept) is resolved with the Address Resolution Protocol for IPv4, or by Neighbor Discovery Protocol (IPv6) into the MAC address (a layer 2 concept) of the destination host.

    

  - #### Layer 3: Network Layer

    The network layer provides the functional and procedural means of transferring variable length data sequences (called packets) from one node to another connected in "different networks". A network is a medium to which many nodes can be connected, on which every node has an *address* and which permits nodes connected to it to transfer messages to other nodes connected to it by merely providing the content of a message and the address of the destination node and letting the network find the way to deliver the message to the destination node, possibly routing it through intermediate nodes. If the message is too large to be transmitted from one node to another on the data link layer between those nodes, the network may implement message delivery by splitting the message into several fragments at one node, sending the fragments independently, and reassembling the fragments at another node. It may, but does not need to, report delivery errors.

  - #### Layer 4: Transport Layer

    In computer networking, the **transport layer** is a conceptual division of methods in the layered architecture of protocols in the network stack in the Internet protocol suite and the OSI model. The protocols of this layer provide host-to-host communication services for applications. It provides services such as connection-oriented communication, reliability, flow control, and multiplexing.

    The best-known transport protocol of TCP/IP is the Transmission Control Protocol(TCP), and lent its name to the title of the entire suite. It is used for connection-oriented transmissions, whereas the connectionless User Datagram Protocol (UDP) is used for simpler messaging transmissions. TCP is the more complex protocol, due to its stateful design incorporating reliable transmission and data stream services.

  - #### Layer 5: Session Layer

    In the seven-layer OSI model of computer networking, the **session layer** is **layer 5**.

    The session layer provides the mechanism for opening, closing and managing a session between end-user application processes, i.e., a semi-permanent dialogue. Communication sessions consist of requests and responses that occur between applications. Session-layer services are commonly used in application environments that make use of remote procedure calls (RPCs).

    Other examples of session layer implementations include Zone Information Protocol(ZIP) – the AppleTalk protocol that coordinates the name binding process, and Session Control Protocol (SCP) – the DECnet Phase IV session-layer protocol.

  - #### Layer 6: Presentation Layer

    The presentation layer is responsible for the formatting and delivery of information to the application layer for further processing or display. It relieves the application layer of concern regarding syntactical differences in data representation within the end-user systems. An example of a presentation service would be the conversion of an EBCDIC-coded text computer file to an ASCII-coded file.

    Serialization of complex data structures into flat byte-strings (using mechanisms such as TLV or XML can be thought of as the key functionality of the presentation layer.

    Encryption is typically done at this level too, although it can be done on the application , session, transport, or network layers, each having its own advantages and disadvantages. Decryption is also handled at the presentation layer. For example, when logging on to bank account sites the presentation layer will decrypt the data as it is received. Another example is representing structure, which is normally standardized at this level, often by using XML. As well as simple pieces of data, like strings, more complicated things are standardized in this layer. Two common examples are 'objects' in object-oriented programming, and the exact way that streaming video is transmitted.

  - #### Layer 7: Application Layer

    In the OSI model, the definition of the application layer is narrower in scope. The OSI model defines the application layer as the user interface responsible for displaying received information to the user. In contrast, the Internet Protocol Suite does not concern itself with such detail. OSI also explicitly distinguishes additional functionality below the application layer, but above the transport layer at two additional levels: the session layer, and the presentation layer. OSI specifies a strict modular separation of functionality at these layers and provides protocol implementations for each layer.

- ### **Transmission Control Protocol** (**TCP**)

  - ####   Definition

    The **Transmission Control Protocol** (**TCP**) is one of the main protocols of the Internet protocol suite. It originated in the initial network implementation in which it complemented the Internet Protocol (IP). Therefore, the entire suite is commonly referred to as *TCP/IP*. TCP provides reliable, ordered, and error-checked delivery of a stream of octets (bytes) between applications running on hosts communicating via an IP network. Major internet applications such as the World Wide Web, email, remote administration, and file transfer rely on TCP. Applications that do not require reliable data stream service may use the User Datagram Protocol (UDP), which provides a connectionless datagram service that emphasizes reduced latency over reliability.

  - ####  Structure

    Processes transmit data by calling on the TCP and passing buffers of data as arguments. The TCP packages the data from these buffers into segments and calls on the internet module [e.g. IP] to transmit each segment to the destination TCP.

    A TCP segment consists of a segment *header* and a *data* section. The segment header contains 10 mandatory fields, and an optional extension field (*Options*, pink background in table). The data section follows the header and is the payload data carried for the application. 

    [![Capture.png](https://i.postimg.cc/qMpHB8yL/Capture.png)](https://postimg.cc/JtY2PHTD)
    
    [![1280px-Tcp-state-diagram-fixed-new-svg.png](https://i.postimg.cc/dQHz2DfR/1280px-Tcp-state-diagram-fixed-new-svg.png)](https://postimg.cc/QV74sNhV)
    
    [![1024px-TCP-CLOSE-svg.png](https://i.postimg.cc/7hXN1C9F/1024px-TCP-CLOSE-svg.png)](https://postimg.cc/wRyJgjS2)
    
    To establish a connection, TCP uses a three-way handshake. Before a client attempts to connect with a server, the server must first bind to and listen at a port to open it up for connections: this is called a passive open. Once the passive open is established, a client may initiate an active open. To establish a connection, the three-way (or 3-step) handshake occurs:
    
    1. **SYN**: The active open is performed by the client sending a SYN to the server. The client sets the segment's sequence number to a random value A.
    2. **SYN-ACK**: In response, the server replies with a SYN-ACK. The acknowledgment number is set to one more than the received sequence number i.e. A+1, and the sequence number that the server chooses for the packet is another random number, B.
    3. **ACK**: Finally, the client sends an ACK back to the server. The sequence number is set to the received acknowledgement value i.e. A+1, and the acknowledgement number is set to one more than the received sequence number i.e. B+1.
    
    At this point, both the client and server have received an acknowledgment of the connection. The steps 1, 2 establish the connection parameter (sequence number) for one direction and it is acknowledged. The steps 2, 3 establish the connection parameter (sequence number) for the other direction and it is acknowledged. With these, a full-duplex communication is established.
    
    The connection termination phase uses a four-way handshake, with each side of the connection terminating independently. When an endpoint wishes to stop its half of the connection, it transmits a FIN packet, which the other end acknowledges with an ACK. Therefore, a typical tear-down requires a pair of FIN and ACK segments from each TCP endpoint. After the side that sent the first FIN has responded with the final ACK, it waits for a timeout before finally closing the connection, during which time the local port is unavailable for new connections; this prevents confusion due to delayed packets being delivered during subsequent connections.
    
  - #### Resource usage
  
    Most implementations allocate an entry in a table that maps a session to a running operating system process. Because TCP packets do not include a session identifier, both endpoints identify the session using the client's address and port. Whenever a packet is received, the TCP implementation must perform a lookup on this table to find the destination process. Each entry in the table is known as a Transmission Control Block or TCB. It contains information about the endpoints (IP and port), status of the connection, running data about the packets that are being exchanged and buffers for sending and receiving data.
  
    The number of sessions in the server side is limited only by memory and can grow as new connections arrive, but the client must allocate a random port before sending the first SYN to the server. This port remains allocated during the whole conversation, and effectively limits the number of outgoing connections from each of the client's IP addresses. If an application fails to properly close unrequired connections, a client can run out of resources and become unable to establish new TCP connections, even from other applications.
  
    Comment: This approach (table entry) allows communication between processes on different machines and prevent them from affecting each other. But one thing we should remember is that port is also a kind of resource, which needs to be closed if it is not in use.
  
  - #### Reliable transmission
  
    TCP uses a *sequence number* to identify each byte of data. The sequence number identifies the order of the bytes sent from each computer so that the data can be reconstructed in order, regardless of any packet reordering, or packet loss that may occur during transmission. The sequence number of the first byte is chosen by the transmitter for the first packet, which is flagged SYN. This number can be arbitrary, and should, in fact, be unpredictable to defend against TCP sequence prediction attacks.
  
    Acknowledgements (ACKs) are sent with a sequence number by the receiver of data to tell the sender that data has been received to the specified byte. ACKs do not imply that the data has been delivered to the application. They merely signify that it is now the receiver's responsibility to deliver the data.
  
    Reliability is achieved by the sender detecting lost data and retransmitting it. TCP uses two primary techniques to identify loss. Retransmission timeout (abbreviated as RTO) and duplicate cumulative acknowledgements (DupAcks).
  
    Comment: It is very important for packages to have an identifier for ordering because they may be transmitted out of order. This is also important when a package is lost on the way. When it comes to security, the first number should be arbitrary.
  
  - #### Dupack-based retransmission
  
    If a single packet (say packet 100) in a stream is lost, then the receiver cannot acknowledge packets above 100 because it uses cumulative ACKs. Hence the receiver acknowledges packet 99 again on the receipt of another data packet. This duplicate acknowledgement is used as a signal for packet loss. That is, if the sender receives three duplicate acknowledgements, it retransmits the last unacknowledged packet. A threshold of three is used because the network may reorder packets causing duplicate acknowledgements. This threshold has been demonstrated to avoid spurious retransmissions due to reordering.
  
    Comment: This approach is suitable for most of the situation. But if we want to retransmit all the lost packages in the end rather than at once, maybe we should find another way.
  
  - #### Timeout-based retransmission
  
    Whenever a packet is sent, the sender sets a timer that is a conservative estimate of when that packet will be acked. If the sender does not receive an ACK by then, it transmits that packet again. The timer is reset every time the sender receives an acknowledgement. This means that the retransmit timer fires only when the sender has received *no* acknowledgement for a long time.  Further, in case a retransmit timer has fired and still no acknowledgement is received, the next timer is set to twice the previous value (up to a certain threshold). Among other things, this helps defend against a man-in-the-middle denial of service attack that tries to fool the sender into making so many retransmissions that the receiver is overwhelmed.
  
    Comment: This approach is important in making the retransmissions in an rational scale and attack-proof.
  
  - #### Error detection
  
    Sequence numbers allow receivers to discard duplicate packets and properly sequence reordered packets. Acknowledgments allow senders to determine when to retransmit lost packets.
  
    To assure correctness a checksum field is included
  
  - #### Flow control
  
    TCP uses a sliding window flow control protocol. In each TCP segment, the receiver specifies in the *receive window* field the amount of additionally received data (in bytes) that it is willing to buffer for the connection. The sending host can send only up to that amount of data before it must wait for an acknowledgement and window update from the receiving host.
  
    Comment: This is quite interesting that your download speed is growing from zero to the highest pitch due to the sliding window flow control.
  
  - #### Congestion control
  
    Acknowledgments for data sent, or lack of acknowledgments, are used by senders to infer network conditions between the TCP sender and receiver. Coupled with timers, TCP senders and receivers can alter the behavior of the flow of data. This is more generally referred to as congestion control and/or network congestion avoidance.
  
    In TCP, the **congestion window** is one of the factors that determines the number of bytes that can be outstanding at any time. The congestion window is maintained by the sender. Note that this is not to be confused with the sliding window size which is maintained by the receiver. The congestion window is a means of stopping a link between the sender and the receiver from becoming overloaded with too much traffic. It is calculated by estimating how much congestion there is on the link.
  
    The flow of data over a TCP connection is also controlled by the use of the *receive window* advertised by the receiver. By comparing its own congestion window with the *receive window*, a sender can determine how much data it may send at any given time.
  
  - #### Vulnerabilities
  
    - ##### Denial of service
  
      By using a spoofed IP address and repeatedly sending purposely assembled SYN packets, followed by many ACK packets, attackers can cause the server to consume large amounts of resources keeping track of the bogus connections. 
  
    - ##### Connection hijacking
  
      An attacker who is able to eavesdrop a TCP session and redirect packets can hijack a TCP connection. To do so, the attacker learns the sequence number from the ongoing communication and forges a false segment that looks like the next segment in the stream. Such a simple hijack can result in one packet being erroneously accepted at one end. 
  
    - ##### TCP veto
  
      An attacker who can eavesdrop and predict the size of the next packet to be sent can cause the receiver to accept a malicious payload without disrupting the existing connection. The attacker injects a malicious packet with the sequence number and a payload size of the next expected packet.
  
- ### User Datagram Protocol (UDP)

  - #### Definition
  
    With UDP, computer applications can send messages, in this case referred to as *datagrams*, to other hosts on an Internet Protocol (IP) network. Prior communications are not required in order to set up communication channels or data paths.
  
  - #### Structure
  
    [![Capture.png](https://i.postimg.cc/Y9cpJMKy/Capture.png)](https://postimg.cc/WDnLZR4M)
  
  - #### Reliability and congestion control
  
    Lacking reliability, UDP applications must be willing to accept some packet loss, reordering, errors or duplication. 
  
    Most often, UDP applications do not employ reliability mechanisms and may even be hindered by them
  
    Comment ：It is  quite clear that UDP is suitable for Streaming media, in that kind of situation, the latency and the speed is the major concern, package loss does not bring fatal fault.
  
- ### Comparison of UDP and TCP

  The major difference between UDP and TCP is that UDP is stateless, not ordered and unreliable. But at the same time, it is lightweight and can be sent to multiple device at once.

- ### Wired technologies

  - #### Coaxial cable

    Coaxial cable conducts electrical signal using an inner conductor (usually a solid copper, stranded copper or copper plated steel wire) surrounded by an insulating layer and all enclosed by a shield, typically one to four layers of woven metallic braid and metallic tape. The cable is protected by an outer insulating jacket. Short coaxial cables are commonly used to connect home video equipment

    [![RG-6-coaxial-cable.png](https://i.postimg.cc/D07Q2V37/RG-6-coaxial-cable.png)](https://postimg.cc/mz61w5rn)

    Long distance coaxial cable was used in the 20th century to connect radio networks, television networks, and Long Distance telephone networks though this has largely been superseded by later methods

  - #### Twisted pair

    It typically consists of 4 pairs of copper cabling that can be utilized for both voice and data transmission. The use of two wires twisted together helps to reduce crosstalk and electromagnetic induction.

    A twisted pair can be used as a balanced line, which as part of a balanced circuit can greatly reduce the effect of noise currents induced on the line by coupling of electric or magnetic fields. 

    [![FTP-cable3.jpg](https://i.postimg.cc/tJ3zGhSn/FTP-cable3.jpg)](https://postimg.cc/1VzFpNZy)

    Comment: The advantage is that it can minimize the noise on the line, and it is a cheap solution for this problem.

  - #### Optical fiber

    An **optical fiber** is a flexible, transparent fiber made by drawing glass silica or plastic to a diameter slightly thicker than that of a human hair Optical fibers are used most often as a means to transmit light between the two ends of the fiber and find wide usage in fiber-optic communications, where they permit transmission over longer distances and at higher bandwidths (data rates) than electrical cables.

    [![Fibreoptic.jpg](https://i.postimg.cc/3JRfsqjg/Fibreoptic.jpg)](https://postimg.cc/jCphNZF5)

    The per-channel light signals propagating in the fiber have been modulated at rates as high as 111 gigabits per second (Gbit/s) by NTT,although 10 or 40 Gbit/s is typical in deployed systems. In June 2013, researchers demonstrated transmission of 400 Gbit/s over a single channel using 4-mode orbital angular momentum multiplexing

    Each fiber can carry many independent channels, each using a different wavelength of light wavelength-division multiplexing (WDM)). The net data rate (data rate without overhead bytes) per fiber is the per-channel data rate reduced by the FEC overhead, multiplied by the number of channels (usually up to 80 in commercial dense WDM systems as of 2008). As of 2011 the record for bandwidth on a single core was 101 Tbit/s (370 channels at 273 Gbit/s each).The record for a multi-core fiber as of January 2013 was 1.05 Pbit/s.In 2009, Bell Labs broke the 100 (Pbit/s)·km barrier (15.5 Tbit/s over a single 7000 km fiber)

    Comment: Optical fibers have higher bandwidth, no electromagnetic noise, and low loss rate in long distance. 

- ### Wireless technologies

  - #### Microwave

    **Microwaves** are a form of electromagnetic radiation with wavelengths ranging from about one meter to one millimeter; with frequencies between 300 MHz (1 m) and 300 GHz (1 mm),  so terrestrial microwave communication links are limited by the visual horizon to about 40 miles (64 km). [![Capture.png](https://i.postimg.cc/D0vqpxJm/Capture.png)](https://postimg.cc/Fd6d7gxQ)

    Microwaves are used in spacecraft communication, and much of the world's data, TV, and telephone communications are transmitted long distances by microwaves between ground stations and communications satellites. Microwaves are also employed in microwave ovens and in radar technology.

    [![Capture.png](https://i.postimg.cc/X73C81Sb/Capture.png)](https://postimg.cc/3WSNrBxS)
  
    Comment: Most of the wireless communication we knew today belongs to Microwave, including WiFi, Bluetooth. Microwave is suitable for short-distance communication, and they can convey larger amount of information( compare to radio)
  
  - #### Communications satellite
  
    A **communications satellite** is an artificial satellite that relays and amplifies radio telecommunications signals via a transponder; it creates a communication channel between a source transmitter and a receiver at different locations on Earth. 
    
    The first and historically most important application for communication satellites was in intercontinental long distance telephony. 
    
    After the 1990s, satellite communication technology has been used as a means to connect to the Internet via broadband data connections. This can be very useful for users who are located in remote areas, and cannot access a broadband connection, or require high availability of services.
    
  
- ### Network interface controller

  - #### Definition

    A **network interface controller** (**NIC**, also known as a **network interface card**, **network adapter**, **LAN adapter** or **physical network interface**,[[1\]](https://en.wikipedia.org/wiki/Network_interface_controller#cite_note-1) and by similar terms) is a [computer hardware](https://en.wikipedia.org/wiki/Computer_hardware) component that connects a [computer](https://en.wikipedia.org/wiki/Computer) to a computer network.

    [![1280px-Network-card.jpg](https://i.postimg.cc/L6qW3YZc/1280px-Network-card.jpg)](https://postimg.cc/SJhVyKdd)

    Network controllers were originally implemented as expansion cards that plugged into a computer bus. The low cost and ubiquity of the Ethernet standard means that most new computers have a network interface controller built into the motherboard. 

    
  
  - #### Implementation
  
    Network controllers were originally implemented as expansion cards that plugged into a computer bus. The low cost and ubiquity of the Ethernet standard means that most new computers have a network interface controller built into the motherboard. 
  
     A separate network card is typically no longer required unless additional independent network connections are needed or some non-Ethernet type of network is used. A general trend in computer hardware is towards integrating the various components of systems on a chip, and this is also applied to network interface cards.
  
  - #### Performance and advanced functionality
  
    The NIC may distribute incoming traffic between the receive queues using a [hash function. Each receive queue is assigned to a separate interrupt; by routing each of those interrupts to different CPUs or CPU cores, processing of the interrupt requests triggered by the network traffic received by a single NIC can be distributed improving performance
  
    With multi-queue NICs, additional performance improvements can be achieved by distributing outgoing traffic among different transmit queues. By assigning different transmit queues to different CPUs or CPU cores, internal operating system contentions can be avoided. 
  
    An Ethernet network controller typically has an 8P8C socket where the network cable is connected. Older NICs also supplied BNC, or AUI connections. Ethernet network controllers typically support 10 Mbit/s Ethernet, 100 Mbit/s Ethernet, and 1000 Mbit/s Ethernet varieties. Such controllers are designated as *10/100/1000*, meaning that they can support data rates of 10, 100 or 1000 Mbit/s. 10 Gigabit Ethernet NICs are also available, and, as of November 2014, are beginning to be available on computer motherboards.
  
    Comment: Nowadays, the performance of  Network interface controller is far beyond the speed limit of the outer Internet.
  
- ### Ethernet hub

  An **Ethernet hub**, **active hub**, **network hub**, **repeater hub**, **multiport repeater**, or simply **hub** is a network hardware device for connecting multiple Ethernet devices together and making them act as a single network segment.

  [![HP-Ether-Twist-Hub8.jpg](https://i.postimg.cc/8zGXLydY/HP-Ether-Twist-Hub8.jpg)](https://postimg.cc/D8CcTPMQ)

  Hubs are now largely obsolete, having been replaced by network switches except in very old installations or specialized applications. 

  A hub works at the physical layer (layer 1) of the OSI model.

  As a *multiport repeater* it works by repeating bits (symbols) received from one of its ports to all other ports. A hub cannot further examine or manage any of the traffic that comes through it: any packet entering any port is rebroadcast on all other ports.
  
  Comment: The reason why hub is replaced with switches is that it does not have any control or management over the connection, which is not sophisticated.
  
- ### Network switch

  A **network switch** (also called **switching hub**, **bridging hub**, officially **MAC bridge**) is networking hardware that connects devices on a computer network by using packet switching to receive, and forward data to the destination device.

  [![Internals-of-a-Cisco-small-business-SG300-28-28-port-Gigabit-Eth.jpg](https://i.postimg.cc/02zPLyLv/Internals-of-a-Cisco-small-business-SG300-28-28-port-Gigabit-Eth.jpg)](https://postimg.cc/hfRkmcDZ)

  A switch is more intelligent than an Ethernet hub, which simply retransmits packets out of every port of the hub except the port on which the packet was received, unable to distinguish different recipients, and achieving an overall lower network efficiency.

  An Ethernet switch operates at the data link layer (layer 2) of the OSI model to create a separate collision domain for each switch port. Each device connected to a switch port can transfer data to any of the other ports at any time and the transmissions will not interfere.

  A layer 2 switch operating as a network bridge may interconnect devices in a home or office. The bridge learns the MAC address of each connected device. Bridges also buffer an incoming packet and adapt the transmission speed to that of the outgoing port.
  
  A layer-3 switch can perform some or all of the functions normally performed by a router. Most network switches, however, are limited to supporting a single type of physical network, typically Ethernet, whereas a router may support different kinds of physical networks on different ports.
  
  A *layer-4 switch* is vendor-dependent, it almost always starts with a capability for network address translation, and may add some type of load distribution based on TCP sessions or advanced QoS capabilities.
  
  A Layer-7 switch may distribute the load based on uniform resource locators (URLs), or by using some installation-specific technique to recognize application-level transactions. A layer-7 switch may include a web cache and participate in a content delivery network (CDN).
  
- ### Router

  A **router** is a networking device that forwards data packets between computer networks. Routers perform the traffic directing functions on the Internet. 

  A router is connected to two or more data lines from different IP networks. When a data packet comes in on one of the lines, the router reads the network address information in the packet header to determine the ultimate destination. Then, using information in its routing table or routing policy, it directs the packet to the next network on its journey.

  [![1280px-Adsl-connections.jpg](https://i.postimg.cc/jjx76fFK/1280px-Adsl-connections.jpg)](https://postimg.cc/PC7JTCHF)

  The most familiar type of IP routers are home and small office routers that simply forward IP packets between the home computers and the Internet. 

   A router is considered a layer-3 device because its primary forwarding decision is based on the information in the layer-3 IP packet, specifically the destination IP address.
  
- ### Modem

  A **modem** (portmanteau of modulator-demodulator) is a hardware device that converts data into a format suitable for a transmission medium so that it can be transmitted from computer to computer (historically over telephone wires).

  [![Tele-Guide-terminal.jpg](https://i.postimg.cc/WzVzjFJt/Tele-Guide-terminal.jpg)](https://postimg.cc/qhm4x7wd)

  Comment： The biggest advantage is that it can use electric wire that is not designed to convey network, which can be implemented in a wide range.

- ### Firewall

  In computing, a **firewall** is a network security system that monitors and controls incoming and outgoing network traffic based on predetermined security rules.

  Firewalls are generally categorized as network-based or host-based. Network-based firewalls are positioned on the gateway computers of LANs, WANs and intranets .The host-based firewall may be a daemon or service as a part of the operating system or an agent application such as endpoint security or protection. 

  [![Firewall.png](https://i.postimg.cc/FR5CrNF7/Firewall.png)](https://postimg.cc/cKhBTqnS)

  Network layer firewalls, also called packet filters, operate at a relatively low level of the TCP/IP protocol stack, not allowing packets to pass through the firewall unless they match the established rule set. 

  Application-layer firewalls work on the application level of the TCP/IP stack (i.e., all browser traffic, or all telnet or FTP traffic), and may intercept all packets traveling to or from an application.

  A proxy server (running either on dedicated hardware or as software on a general-purpose machine) may act as a firewall by responding to input packets (connection requests, for example) in the manner of an application, while blocking other packets. 

  Comment: Firewall has much more function than we imagine, like proxying or address translation, or blocking packages from certain address. The most important thing is that firewall has been combined with router and switch, and become more like a software than a hardware.

- ### Routing

  In packet switched networks, routing directs packet forwarding (the transit of logically addressed network packets from their source toward their ultimate destination) through intermediate nodes.

  There are usually multiple routes that can be taken, and to choose between them, different elements can be considered to decide which routes get installed into the routing table, such as (sorted by priority):

  1. *Prefix-Length*: where longer subnet masks are preferred (independent if it is within a routing protocol or over different routing protocol)
2. *Metric*: where a lower metric/cost is preferred (only valid within one and the same routing protocol)
  3. *Administrative distance*: where a lower distance is preferred (only valid between different routing protocols)
  
- ### Network performance

  - #### Grade of service

    In circuit switched networks, network performance is synonymous with the grade of service. 

    In a Loss System, the Grade of Service is described as that proportion of calls that are lost due to congestion in the busy hour.
  
  - #### Quality of service
  
     In an  Asynchronous Transfer Mode(ATM) network, performance can be measured by line rate, quality of service (QoS), data throughput, connect time, stability, technology, modulation technique and modem enhancements.
  
     Quality of service is the ability to provide different priority to different applications, users, or data flows, or to guarantee a certain level of performance to a data flow. 
  
    For example, a required bit rate, delay, delay variation, packet loss or bit error rates may be guaranteed. 
  
  - #### Network congestion
  
    **Network congestion** in data networking is the reduced quality of service that occurs when a network node or link is carrying more data than it can handle. Among the ways to classify congestion control algorithms are:
  
    - By type and amount of feedback received from the network: Loss; delay; single-bit or multi-bit explicit signals
    - By incremental deployability: Only sender needs modification; sender and receiver need modification; only router needs modification; sender, receiver and routers need modification.
    - By performance aspect: high bandwidth-delay product networks; lossy links; fairness; advantage to short flows; variable-rate links
    - By fairness criterion: Max-min fairness; proportionally fair; controlled delay
  
    Comment: It is quite interesting that congestion can happen anywhere. Imagine that too many request came to the service, then the service must abandon some request or deal with some requests first. For example, the service can abandon the early request because the sender may no longer waiting.
  
  - #### Network congestion
  
    In computer networking: **resilience** is the ability to provide and maintain an acceptable level of service in the face of faults and challenges to normal operation.
  
    Comment: Imagine that a service is overwhelmed by a single request or a fault, than it should melt down to deal with other requests.
  
  - 
  
- ### Data center network architectures

  - #### Three-tier DCN

    The legacy three-tier DCN architecture follows a multi-rooted tree based network topology composed of three layers of network switches, namely access, aggregate, and core layers.

    However, three-tier architecture is unable to handle the growing demand of cloud computing.The higher layers of the three-tier DCN are highly oversubscribed. Moreover, scalability is another major issue in three-tier DCN.
  
  - #### Fat tree DCN
  
    The architecture is composed of *k* pods, where each pod contains, (k/2)2 servers, k/2 access layer switches, and k/2 aggregate layer switches in the topology. The core layers contain (k/2)2 core switches where each of the core switches is connected to one aggregate layer switch in each of the pods.
  
    [![Capture.png](https://i.postimg.cc/2SHbpNNv/Capture.png)](https://postimg.cc/dhytdX1t)
  
  - #### DCell
  
     A cell0 is the basic unit and building block of DCell topology arranged in multiple levels, where a higher level cell contains multiple lower layer cells. The cell0 is building block of DCell topology, which contains *n* servers and one commodity network switch. The network switch is only used to connect the server within a cell0. A cell1 contain *k=n+1* cell0 cells, and similarly a cell2 contains k * n + 1 dcell1. 
  
    Comment: A rational structure should use less overhead cell to manger more basic cells, at the same time, this structure should handle fault quickly with load balancing.
  
  - 
  
    
  
    
  
  
