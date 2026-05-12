# TCP vs UDP Traffic Behavior Analysis for Internet Applications Using Wireshark and Cisco Packet Tracer on Windows

### Team Members
| Register No | Name |
|--------------|------|
| 23BEC1047 | S. Aishwarya |
| 23BEC1051 | S. Harini |

---

## Description
Comparative analysis of TCP and UDP traffic using Wireshark and Cisco Packet Tracer. The project simulates a network to observe DNS, HTTP communication, TCP three-way handshake, and UDP packet flow to understand transport layer protocol behavior in real internet applications.

## Tools Used
- Wireshark
- Cisco Packet Tracer
- Windows OS

## Project Presentation
All screenshots, packet analysis, and demonstration of the network setup are included in the presentation file.

File: [CCN CHAMP PROJECT_recent.pdf](CCN%20CHAMP%20PROJECT_recent.pdf)

## Network Simulation
The Cisco Packet Tracer topology used for this project is included.

File: [Proj.pkt](Proj.pkt)

---

## Packet Capture
Wireshark capture files used for analyzing TCP and UDP behavior.

File: [CCN_PROJECT1.pcapng](CCN_PROJECT1.pcapng)

---

# Table of Contents
1. Abstract  
2. Introduction  
3. Algorithm  
4. Implementation  
5. Results  
6. Inference  
7. Application Oriented Learning  
8. Conclusion  
9. References  

---

# Abstract
This project presents a comparative analysis of Transmission Control Protocol (TCP) and User Datagram Protocol (UDP) in handling network traffic for common Internet applications. The study is conducted using Wireshark for real-time packet capture and Cisco Packet Tracer for network simulation on the Windows platform.

The objective is to understand the differences between these two transport layer protocols based on key performance parameters such as reliability, delay, packet loss, and throughput.

Network traffic is generated using applications such as web browsing, file transfers, and video streaming. Wireshark captures and filters packets, enabling clear observation of protocol behavior in real time. Cisco Packet Tracer is used to visualize packet flow across the network.

TCP is studied as a connection-oriented protocol that provides reliable communication through mechanisms such as three-way handshake, sequence numbers, acknowledgements, and retransmissions. UDP, on the other hand, is a connectionless protocol that sends data without error checking or retransmissions.

The observations show that TCP is suitable for applications where reliability is essential, while UDP is better suited for real-time applications where speed and low latency are more important than perfect delivery.

The combination of real-time packet capture and network simulation provides a clear understanding of protocol behavior in practical networking environments.

---

# Introduction
Communication over computer networks is essential for modern digital applications including web browsing, file transfer, video streaming, and cloud services.

At the transport layer of the networking stack, two key protocols manage communication between devices:

- Transmission Control Protocol (TCP)
- User Datagram Protocol (UDP)

TCP is a connection-oriented protocol that ensures reliable data delivery through mechanisms such as acknowledgements, retransmissions, and ordered packet delivery.

UDP is a connectionless protocol that transmits packets without establishing a connection, making it faster but less reliable.

Because of these characteristics:

- TCP is commonly used in applications where accuracy and reliability are critical.
- UDP is used in applications where speed and low latency are prioritized.

This project studies the behavior of TCP and UDP using two tools:

- **Wireshark** for real-time packet capture and analysis
- **Cisco Packet Tracer** for network simulation

By generating traffic through activities such as web browsing and DNS queries, the behavior of both protocols is analyzed using performance parameters including delay, throughput, reliability, and packet loss.

---

# Algorithm

This project focuses on **network traffic analysis** rather than traditional programming.

### Step 1: Generate Network Traffic
Traffic is generated using applications such as:
- Web browsing
- File downloads
- Video streaming

These actions produce packets transmitted using TCP or UDP.

### Step 2: Capture Packets
Wireshark captures packets from the selected network interface. Each packet contains details such as:

- Source IP
- Destination IP
- Protocol type
- Port numbers
- TCP flags

### Step 3: Apply Filters
Specific protocols are isolated using filters.

Examples:
tcp
udp
tcp.flags.syn == 1


### Step 4: Analyze Packet Behavior

**TCP Analysis**
- Three-way handshake (SYN, SYN-ACK, ACK)
- Sequence numbers
- Acknowledgements
- Retransmissions

**UDP Analysis**
- Continuous packet transmission
- No acknowledgements
- No retransmissions

### Step 5: Study Performance Graphs
Wireshark graphs such as:

- Time sequence graphs
- Throughput graphs

are used to evaluate delay, speed, and packet flow.

### Step 6: Network Simulation
Cisco Packet Tracer simulates the network topology to visualize packet movement between devices.

---

# Implementation (Real Time)

The project was implemented using **Cisco Packet Tracer** and **Wireshark** on a Windows system.

### Network Topology

The simulated network consists of:

- Two PCs
- One switch
- One router
- One server

The server is configured with:

- HTTPS service
- DNS service

DNS entry configured:
example.com → 192.168.2.10


Client systems use the DNS server to resolve the domain name.

### Communication Flow

1. DNS request is sent using **UDP**
2. DNS server resolves the domain name
3. Web browser connects to server using **TCP**
4. HTTP data transfer occurs

---

# Network Configuration

| Device | Network Address | IPv4 Address | Gateway |
|------|------|------|------|
| PC0 | 192.168.1.0/24 | 192.168.1.2 | 192.168.1.1 |
| PC1 | 192.168.1.0/24 | 192.168.1.3 | 192.168.1.1 |
| Server0 | 192.168.2.0/24 | 192.168.2.10 | 192.168.2.1 |
| Router G0/0 | 192.168.1.0/24 | 192.168.1.1 | — |
| Router G0/1 | 192.168.2.0/24 | 192.168.2.1 | — |

Cisco Packet Tracer simulation mode is used to observe packet flow.

Wireshark captures real-time packets and displays details such as:

- Source IP
- Destination IP
- Port numbers
- Sequence numbers
- Checksums

Testing was performed using:

- `ping` to verify connectivity
- DNS resolution
- Webpage access through IP and domain name

---

# Results

The captured packets and simulations demonstrate:

- TCP traffic during web browsing
- DNS queries using UDP
- TCP three-way handshake
- Packet retransmissions
- Sequence number tracking
- Throughput analysis
- Round-trip time measurements

Wireshark graphs confirm the presence of network traffic and allow detailed protocol analysis.

---

# Inference

The simulated network successfully demonstrated TCP and UDP behavior.

Observations include:

- DNS queries used **UDP**
- Webpage communication used **TCP**
- TCP ensured reliable communication through handshake and acknowledgements
- UDP allowed faster communication with minimal overhead

These results confirm that:

- **UDP is suitable for fast services like DNS**
- **TCP is ideal for reliable services like web browsing**

---

# Application Oriented Learning

This project demonstrates real-world networking concepts such as:

- IP addressing
- Routing between networks
- DNS domain resolution
- TCP reliable communication
- UDP fast data transmission

Tools like Wireshark and Cisco Packet Tracer help visualize and analyze real network behavior in a controlled environment.

If implemented physically, the network would require hardware such as:

- Routers
- Switches
- Servers
- Client systems

Since the project uses simulation software, no hardware cost was required.

---

# Conclusion

This project analyzed TCP and UDP behavior in real-time network communication.

A simulated network was created using Cisco Packet Tracer, while packet-level traffic was analyzed using Wireshark.

The experiment demonstrated:

- UDP usage in DNS communication
- TCP usage in web browsing
- Reliable data transfer through TCP handshakes
- Faster but less reliable UDP communication

Some challenges encountered included configuration errors in IP addressing and connectivity issues. These were resolved by verifying network settings and analyzing packet exchanges.

Future improvements could include:

- Analysis of additional protocols
- Measurement of packet loss and latency
- Testing in larger network environments

---

# References

1. Wireshark Documentation  
   https://www.wireshark.org/docs/

2. Cisco Packet Tracer – Cisco Networking Academy Learning Resources  
   Cisco Systems Inc.

3. Postel, J. (1981). Transmission Control Protocol (TCP)  
   RFC 793, Internet Engineering Task Force (IETF)

4. Postel, J. (1980). User Datagram Protocol (UDP)  
   RFC 768, Internet Engineering Task Force (IETF)

5. Mockapetris, P. (1987). Domain Names – Concepts and Facilities  
   RFC 1034 and RFC 1035, Internet Engineering Task Force (IETF)

---

# License

This project is licensed under the MIT License.

You are free to use, modify, and distribute this project for educational or research purposes, provided that proper credit is given to the original authors.

See the LICENSE file for full license details.
