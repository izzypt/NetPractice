# NetPractice

![image](https://github.com/izzypt/NetPractice/assets/73948790/86afd98e-a091-4fdb-ab79-7e4343dc3c56)

A System Administration related exercise, to discover networking and configure small-scale networks.


# Networking basics

A network is a collection of interconnected devices (such as computers, servers, routers, switches, and other hardware) that can communicate with each other and share resources. 


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

# The OSI Model

![image](https://github.com/izzypt/NetPractice/assets/73948790/a8209bd5-003b-4a3f-aa07-cd6ace630a27)


- The OSI (Open Systems Interconnection) model is a conceptual framework that helps us understand how a network functions and operates at different levels.

- It provides a structured and systematic approach to comprehend the complex processes involved in network communication.

- By dividing the networking tasks into seven distinct layers, the OSI model makes it easier to grasp the different functionalities and interactions that occur when data is transmitted between devices on a network. 

- It was developed by the International Organization for Standardization (ISO) to facilitate interoperability between different vendors' networking hardware and software. 

- The criteria that separate the layers are the specific functions and responsibilities that they handle in the networking process:

    - Application Layer (Layer 7):
        - The Application layer is the topmost layer and is responsible for providing network services directly to end-users or applications.
        - It deals with user interfaces, file transfers, email services, web browsing, and other high-level application protocols.
        - Examples of protocols at this layer include ***HTTP*** (for web browsing), ***SMTP*** (for email), and ***FTP*** (for file transfer).
    
    - Presentation Layer (Layer 6):
        - The Presentation layer is responsible for ***data translation***, ***encryption***, and ***compression*** to ensure that data sent by one application can be properly interpreted by another.
        - It takes care of data formatting, ***character encoding***, and ***encryption/decryption*** processes.
        - Commonly used encryption and compression protocols like ***SSL/TLS*** and ***JPEG*** operate at this layer.
    
    - Session Layer (Layer 5):
        - The Session layer establishes, maintains, and terminates communication sessions between devices on a network.
        - It manages session synchronization, checkpointing, and recovery processes.
        - This layer helps in maintaining and resuming communication if a connection is interrupted.
    
    - Transport Layer (Layer 4):
        - Responsible for ensuring reliable end-to-end communication between devices.
        - Its primary functions include segmenting data received from the Application layer above into smaller units (segments) and providing reliable delivery (in the case of TCP) or connectionless communication (in the case of UDP.
        - The Transport layer receives data from the Application layer and segments it into smaller units (segments in TCP or datagrams in UDP) for efficient transmission across the network.
      
            - TCP (Transmission Control Protocol) is a reliable, connection-oriented protocol. It establishes a connection between the sender and receiver before data transmission and ensures that all data segments are acknowledged and retransmitted if needed, guaranteeing that data arrives intact and in the correct order.

            - UDP (User Datagram Protocol): UDP is a connectionless, unreliable protocol. It does not establish a connection before sending data and does not provide error-checking or retransmission. While it offers faster communication compared to TCP, it does not guarantee delivery.
    
    - Network Layer (Layer 3):
        - The Network layer deals with routing data packets between different networks and is responsible for logical addressing and path determination.
        -  Data is encapsulated into packets, also known as datagrams.
        -  The Network layer adds a header to the data received from the Transport layer, which includes the source and destination IP addresses, as well as other relevant information for routing the packet to its destination.
        -  Once the packet is created, the Network layer is responsible for routing it through different networks to reach the intended destination.
        -  Routers operate at this layer and use IP (Internet Protocol) addresses to direct data to the correct destination.
        - The most common protocol at this layer is the IPv4 or IPv6 (IP Protocol).

    - Data Link Layer (Layer 2):
        - The Data Link layer is responsible for data framing, error detection, and media access control.
        - It ***organizes raw bits into frames*** and ***ensures reliable data transmission within the local network segment***.
        - Ethernet, Wi-Fi, and PPP are common data link layer protocols.
    
    - Physical Layer (Layer 1):
        - The Physical layer deals with the physical transmission of data over the network medium.
        - It defines the hardware specifications, such as cables, switches, and network interface cards (NICs), and how bits are transmitted over the medium.

- The purpose of the OSI model is to provide a common reference model that allows different networking technologies and protocols to interoperate.
- By dividing the networking process into distinct layers, the model simplifies network design, troubleshooting, and development.
- It also enables vendors to develop networking hardware and software independently, as long as they adhere to the standards and interfaces defined by each layer.
- This modularity and layering make it easier to understand the complex networking processes and facilitates the development of new technologies without disrupting the existing ones.

# TCP/IP (Transmission Control Protocol/Internet Protocol) 

Is the foundational set of protocols used for communication on the internet and most modern computer networks. 

Understanding TCP/IP addressing is essential for configuring a small-scale network. 

Here are some fundamentals:

1. ***IP Addressing***:

    - IP addressing is at the core of TCP/IP and is used to uniquely identify devices on a network.
    - IP addresses are organized in IP classes
    - An IP address is
       - a 32-bit (IPv4) , which looks like this: ```192.168.1.1```
       - or a 128-bit (IPv6) numeric label, which looks like: looks like: ```2001:0db8:85a3:0000:0000:8a2e:0370:7334```
    - IPv4 addresses are more common, but IPv6 addresses are becoming increasingly important due to the exhaustion of IPv4 addresses.
    ![image](https://github.com/izzypt/NetPractice/assets/73948790/e78e31f6-114f-44ea-b3f3-9c00f418dc37)

2. ***IP Classes***:

   ![image](https://github.com/izzypt/NetPractice/assets/73948790/5870a28c-72ad-46a1-86ee-06be9e6847d7)

    - IPv4 addresses are divided into classes, which determine the size of the network and the number of hosts it can accommodate.
    - There are five classes: A, B, C, D, and E.
    
        - Class A:
          - Begins with a binary "0" in the first bit and has 8 bits for the network portion
          - allowing for a large number of hosts but a limited number of networks.
        - Class B:
          - Begins with binary "10" in the first two bits and has 16 bits for the network portion
          - providing a balance between the number of networks and hosts.
        - Class C:
          - Begins with binary "110" in the first three bits and has 24 bits for the network portion
          - allowing for many networks with a limited number of hosts.
        - Class D:
          - Begins with binary "1110" in the first four bits
          - and is reserved for multicast addresses (used for one-to-many communication).
        - Class E:
          - Begins with binary "1111" in the first four bits
          - and is reserved for experimental purposes.

    ![image](https://github.com/izzypt/NetPractice/assets/73948790/628b4da1-1146-4802-ad33-93156aae0ec6)


4. ***Subnetting***:

   Beginners guide to subnetting: https://www.packetcoders.io/a-beginners-guide-to-subnetting/
   
    - A subnet, or subnetwork, is a network inside a network.
    - Subnetting allows network administrators to divide a large network into smaller, more manageable subnetworks (subnets).
    - It involves borrowing bits from the host portion of an IP address to create subnets.
    - Through subnetting, network traffic can travel a shorter distance without passing through unnecessary routers to reach its destination.
    - Subnetting make networks more efficient, it helps optimize network performance, security, and address allocation.

        ![image](https://github.com/izzypt/NetPractice/assets/73948790/8cd74454-d03c-4701-b8d1-f4d2f734e916)

6. ***Subnet Mask***:
    
    - A subnet mask is like an IP address, but for only internal usage within a network.
    - A subnet mask is a 32-bit value (similar in format to an IP address) that accompanies an IP address to identify the network and host portions.
    - It contains a series of binary "1s" followed by binary "0s."
    - The "1s" in the mask correspond to the network bits, and the "0s" correspond to the host bits.

    For example, a subnet mask of 255.255.255.0 (or /24 in CIDR notation) indicates that the first 24 bits represent the network portion, and the remaining 8 bits represent the host portion.

7. ***CIDR Notation***:

   - CIDR (Classless Inter-Domain Routing) notation is a compact way to represent IP addresses and subnet masks.
   - It consists of the IP address followed by a slash and the number of bits used for the network portion. For example, 192.168.1.0/24 represents an IPv4 network with a subnet mask of 255.255.255.0.

8. ***DHCP (Dynamic Host Configuration Protocol)***:

   - DHCP is a protocol used to automatically assign IP addresses to devices on a network.
   - Instead of manually configuring each device's IP address, DHCP servers dynamically allocate and manage IP addresses for devices as they join the network.

By understanding these fundamentals, you can start configuring a small-scale network and handle IP address assignment, subnetting, and related aspects effectively. Remember that practice and hands-on experience will solidify your understanding of TCP/IP addressing.

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

- What is a subnet: https://www.cloudflare.com/learning/network-layer/what-is-a-subnet/
- How to calculate a subnet: https://community.spiceworks.com/networking/articles/2491-how-to-calculate-a-subnet-mask
- IP, subnet and cidr: https://www.digitalocean.com/community/tutorials/understanding-ip-addresses-subnets-and-cidr-notation-for-networking

> A subnet mask is like an IP address, but for only internal usage within a network. Routers use subnet masks to route data packets to the right place. 


- A subnet mask is used to divide an IP address into two parts:
  -  the ***network part***
  -  and the ***host part***. 
- It is a 32-bit value (for IPv4) that serves as a filter to determine which portion of the IP address represents the network and which part identifies the specific device within that network.

> Suppose Bob answers Alice's letter, but he sends his reply to Alice's place of employment rather than her home. Alice's office is quite large with many different departments. To ensure employees receive their correspondence quickly, the administrative team at Alice's workplace sorts mail by department rather than by individual employee. After receiving Bob's letter, they look up Alice's department and see she works in Customer Support. They send the letter to the Customer Support department instead of to Alice, and the customer support department gives it to Alice.

> In this analogy, "Alice" is like an IP address and "Customer Support" is like a subnet mask. By matching Alice to her department, Bob's letter was quickly sorted into the right group of potential recipients. Without this step, office administrators would have to spend time laboriously looking for the exact location of Alice's desk, which could be anywhere in the building.


This process yields the network address, which is used by routers to determine how to forward data to the appropriate destination.

- For example, let's take the IPv4 address 192.168.1.1 with a subnet mask of 255.255.255.0. 
  - The logical AND operation between these two values will result in the network address 192.168.1.0. 
  - The "0" in the host part of the address indicates that this portion can be used to represent multiple devices (in this case, 256 host addresses, ranging from 192.168.1.1 to 192.168.1.254).

The subnet mask helps define the size of the network and its range of valid IP addresses. Smaller subnet masks (e.g., 255.255.255.0) allow for more hosts within the same network, while larger subnet masks (e.g., 255.255.0.0) create smaller networks with fewer available host addresses.


# MAC and MAC Adresses

- MAC address stands for Media Access Control address. 
- It is a unique identifier assigned to a network interface card (NIC) or network adapter of a network device, such as a computer, laptop, smartphone, router, or switch.
- The MAC address is a hardware-based address, burned into the NIC during manufacturing, and it is used to uniquely identify a device on a local network segment.

![image](https://github.com/izzypt/NetPractice/assets/73948790/47eaa5c7-dc7a-44c0-a520-9d67431b1c48)


Key characteristics of MAC addresses:

1. Uniqueness: Each MAC address is globally unique, meaning no two devices on the planet should have the same MAC address. This uniqueness is crucial for proper functioning of network communication.

2. Format: A MAC address is typically represented as a string of six pairs of hexadecimal digits, separated by colons or hyphens. For example, a MAC address could look like "00:1A:2B:3C:4D:5E."

3. Locality: MAC addresses are used at the Data Link Layer (Layer 2) of the OSI model and are relevant within the local network segment or LAN. Routers operate at the Network Layer (Layer 3) and use IP addresses to direct traffic between different networks.

The purpose and usage of MAC addresses in networking:

1. Address Resolution: MAC addresses play a critical role in local network communication. When devices communicate within a LAN, they use MAC addresses to send data directly to the intended recipient. When a device wants to communicate with another device on the same network, it uses the destination device's MAC address to encapsulate the data into frames and transmit it over the local network.

2. Data Link Layer Operation: The Data Link Layer uses MAC addresses for frame addressing and media access control. Each frame transmitted over a local network includes both the source and destination MAC addresses in its header. Switches and bridges within the local network use MAC addresses to determine how to forward frames to their intended destination.

3. MAC Table in Switches: Switches maintain a MAC table that associates MAC addresses with the corresponding physical ports to which devices are connected. When a switch receives a frame with a destination MAC address, it looks up the MAC table to determine which port to forward the frame to, optimizing local network traffic flow.

4. Wireless Networking: In Wi-Fi (wireless) networks, MAC addresses are used for device identification and authentication. Devices associate with Wi-Fi access points using their MAC addresses, and network administrators can implement MAC address filtering to control access to the network.

It's important to note that MAC addresses are specific to the local network and are not used for routing data between different networks (which is the role of IP addresses at the Network Layer). For internet communication, devices rely on IP addresses to route data packets across different networks until they reach their destination.
