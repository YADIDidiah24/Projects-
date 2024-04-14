# Socket Programming and Networking Application

## Introduction
In this README, I'll walk you through the development process of a multi-client chat application and the configuration of networking devices based on a subnetting scheme.

## Part 1 - Developing a Multi-Client Chat Application

### Objective
The main goal here was to create a multi-client chat application allowing multiple clients to connect to a server and communicate with each other, each having a unique name.

### Implementation Overview

**Server Implementation:** I implemented the server using Java, utilizing the `ServerSocket` class to listen for incoming client connections. Each client connection was handled in a separate thread to enable concurrent communication with multiple clients. The server maintained a list of connected clients along with their names.

**Client Implementation:** The client application was also developed in Java, using the `Socket` class to connect to the server. Upon connection, the client provided a unique name, which was sent to the server for identification. The client continuously listened for messages from the server and displayed them to the user. Additionally, the client allowed users to input messages to be sent to the server.

### Noteworthy Features

- **Client-Server Communication:** Both client and server could establish a connection using sockets.
- **Multi-client Support:** The server was capable of handling multiple client connections concurrently, with each client being managed in a separate thread.
- **Chat Interface:** Clients could input messages through the console, and received messages were printed to the console.
- **Username Handling:** Clients provided a username upon connecting to the server, which was displayed by the server when they connected or disconnected.

### Code Snippet

// Client.java
// Server.java
// ClientHandler.java


## Part 2 - Developing a Networking Application

### Objective
Here, the objective was to design an IPv4 Network Subnetting Scheme and configure networking devices accordingly.

### Implementation Overview

**Subnetting Scheme Design:** The first step involved creating a subnetting scheme based on the number of host computers required in each subnet and other network considerations.

**Device Configuration:** Once the subnetting scheme was designed, devices in the CISCO Packet Tracer environment were configured according to the provided scheme.

**IP addresses in the Addressing Table**

| Device          | Interface | IP Address    | Subnet Mask       | Default Gateway |
|-----------------|-----------|---------------|-------------------|-----------------|
| CustomerRouter  | G0/0      | 192.168.0.1   | 255.255.255.192   | N/A             |
| CustomerRouter  | G0/1      | 192.168.0.65  | 255.255.255.192   | N/A             |
| CustomerRouter  | S0/1/0    | 209.165.201.2 | 255.255.255.252   | N/A             |
| LAN-A Switch    | VLAN1     | 192.168.0.2   | 255.255.255.192   | 192.168.0.1     |
| LAN-B Switch    | VLAN1     | 192.168.0.66  | 255.255.255.192   | 192.168.0.65    |
| PC-A            | NIC       | 192.168.0.62  | 255.255.255.192   | 192.168.0.1     |
| PC-B            | NIC       | 192.168.0.126 | 255.255.255.192   | 192.168.0.65    |
| ISPRouter       | G0/0      | 209.165.200.225| 255.255.255.224   | N/A             |
| ISPRouter       | S0/1/0    | 209.165.201.1  | 255.255.255.252   | N/A             |
| ISPSwitch       | VLAN1     | 209.165.200.226| 255.255.255.224   | 209.165.200.225 |
| ISP Workstation | NIC       | 209.165.200.235| 255.255.255.224   | 209.165.200.225 |
| ISP Server      | NIC       | 209.165.200.240| 255.255.255.224   | 209.165.200.225 |

**Subnet Addressing Table**

| Subnet Address | Prefix | Subnet Mask     |
|----------------|--------|-----------------|
| 192.168.0.0    | /26    | 255.255.255.192 |
| 192.168.0.64   | /26    | 255.255.255.192 |
| 192.168.0.128  | /26    | 255.255.255.192 |
| 192.168.0.192  | /26    | 255.255.255.192 |

![image](https://github.com/YADIDidiah24/Projects-/assets/94169481/c38e2a5b-5dec-4c47-8ecc-3e839cfcf28e)

**Testing and Troubleshooting:** The final step was to test network connectivity using the ping command and troubleshoot any issues encountered.


![image](https://github.com/YADIDidiah24/Projects-/assets/94169481/559d2674-2ed5-404a-bf5c-8987042ebb20)

![image](https://github.com/YADIDidiah24/Projects-/assets/94169481/b7729232-d1c9-4c15-9e8e-6e560c8c31df)


### Noteworthy Features

- **Subnetting:** Subnets were created based on host requirements.
- **Device Configuration:** Routers, switches, and PCs were configured with appropriate IP addresses, subnet masks, and default gateways according to the subnetting scheme.
- **Testing:** Network connectivity was tested using the ping command to ensure proper communication between devices.

### Summary
This README provides an overview of the objectives, implementation, and configuration steps for both parts of the lab assessment. It outlines the development process and highlights key features and considerations in each part.
