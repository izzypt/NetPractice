# NetPractice
A System Administration related exercise, to discover networking and configure small-scale networks.

# Networking basics

A network is a collection of interconnected devices (such as computers, servers, routers, switches, and other hardware) that can communicate with each other and share resources. 

The purpose of a network is to facilitate the exchange of data and information between these devices efficiently and securely.

### Primary types of networks:

1. ***Local Area Network (LAN):***

    - A Local Area Network (LAN) is a network that covers a relatively small geographic area, typically confined to a single building or a group of adjacent buildings.
    - LANs are commonly used in homes, offices, schools, and small businesses to connect computers and devices within a limited area.
    - The data transfer rates in LANs are usually very high, and they are characterized by low latency, making them ideal for resource sharing and real-time applications.

3. ***Wide Area Network (WAN):***

    - A Wide Area Network (WAN) is a network that spans a large geographical area, often connecting LANs or other networks across cities, states, or even countries.
    - WANs use various technologies like leased lines, fiber-optic cables, satellites, and the internet to enable communication between distant locations.
    - WANs are typically slower than LANs and may have higher latency due to the longer distances involved.

### Fundamental Components of a Network:

1. ***Nodes (Devices):***

    - Nodes are the fundamental components of a network and can be any device capable of connecting to the network.
    - Common nodes include computers, laptops, servers, printers, switches, routers, and even smartphones.
    - Each node on the network has a unique identifier (like an IP address) that allows it to be addressed and identified by other devices.
    ![image](https://github.com/izzypt/NetPractice/assets/73948790/0674269b-f852-4544-b363-10586b958630)

2. ***Communication Channels:***

    - Communication channels are the pathways through which data is transmitted between nodes on the network.
    - These channels can be physical, such as copper or fiber-optic cables, or wireless, such as Wi-Fi or radio waves.
    - The choice of communication channel depends on factors like distance, bandwidth requirements, cost, and environmental considerations.


3. ***Switches:***

    - Switches are networking devices that operate at the data link layer (Layer 2) of the OSI model.
    - They are used in LANs to connect multiple devices together and efficiently manage the data flow within the network.
    - Switches use MAC (Media Access Control) addresses to forward data to the correct destination node.


4. ***Routers:***

    - Routers are networking devices that operate at the network layer (Layer 3) of the OSI model.
    - They are used in both LANs and WANs to connect different networks together and make decisions about how to forward data packets between them.
    - Routers use IP addresses to determine the best path for data to reach its destination.

5. ***Protocols:***

    - Protocols are a set of rules and conventions that define how data is transmitted, received, and processed on a network.
    - They ensure that devices can understand each other and communicate effectively.
    - Common networking protocols include TCP/IP (Transmission Control Protocol/Internet Protocol), UDP (User Datagram Protocol), HTTP (Hypertext Transfer Protocol), and many others.

7. ***Network Interface Cards (NICs):***

    - Network Interface Cards (NICs) are hardware components that enable devices to connect to a network.
    - They are responsible for converting data from the device into packets suitable for transmission over the network and vice versa.
    - NICs can be integrated into the motherboard of computers or added as separate expansion cards.

These fundamental components work together to form a network infrastructure that enables communication and resource sharing among devices, whether within a local environment or across vast distances in a wide area network.

# IP Address vs Subnet Mask

- An ***IP address*** and a ***subnet mask*** are two fundamental components used to define and identify devices on a network. 
- An IP address uniquely identifies a device on a network, while a subnet mask determines how the IP address is divided into network and host portions.
- Together, they help in routing data effectively within and between networks.

### IP Address:

An IP address is a unique numerical label assigned to each device (such as a computer, printer, router, or smartphone) connected to a network that uses the Internet Protocol for communication. 

The primary purpose of an IP address is to identify and locate devices within a network or across the internet.

IP addresses can be of two types: IPv4 (Internet Protocol version 4) and IPv6 (Internet Protocol version 6).

- IPv4: This is the older and most widely used version of IP addresses. It is represented as four sets of decimal numbers, separated by periods (dots). Each set can have a value from 0 to 255. For example, an IPv4 address looks like: 192.168.1.1

- IPv6: This is the newer version of IP addresses, designed to overcome the limitations of IPv4 and provide a virtually unlimited address space. IPv6 addresses are represented as eight groups of four hexadecimal digits, separated by colons. For example, an IPv6 address looks like: 2001:0db8:85a3:0000:0000:8a2e:0370:7334

Regardless of the version, the IP address allows devices to send and receive data over a network. It is analogous to the postal address of a building, helping data packets find their destination on the network.

### Subnet Mask:

- A subnet mask is used to divide an IP address into two parts: the ***network part*** and the ***host part***. 
- It is a 32-bit value (for IPv4) that serves as a filter to determine which portion of the IP address represents the network and which part identifies the specific device within that network.

The subnet mask is applied to the IP address using a logical AND operation. This process yields the network address, which is used by routers to determine how to forward data to the appropriate destination.

For example, let's take the IPv4 address 192.168.1.1 with a subnet mask of 255.255.255.0. The logical AND operation between these two values will result in the network address 192.168.1.0. The "0" in the host part of the address indicates that this portion can be used to represent multiple devices (in this case, 256 host addresses, ranging from 192.168.1.1 to 192.168.1.254).

The subnet mask helps define the size of the network and its range of valid IP addresses. Smaller subnet masks (e.g., 255.255.255.0) allow for more hosts within the same network, while larger subnet masks (e.g., 255.255.0.0) create smaller networks with fewer available host addresses.
