---
title: "Unlocking the World of Computer Networks: Explore, Understand, and Connect!🌐"
datePublished: Wed May 24 2023 16:00:28 GMT+0000 (Coordinated Universal Time)
cuid: cli1w64wv000b09jm62syd06f
slug: unlocking-the-world-of-computer-networks-explore-understand-and-connect
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1684943938137/43e8a174-7728-44c9-97f8-2f64313d761d.jpeg
tags: computer-networking, networking-for-beginners, wemakedevs

---

### Where did it all begin?

Tim Berners developed the www. World wide web is basically a project that stores the documents that are accessible across the world through the Internet.

Let me show you the world's first website😶‍🌫️

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678001718786/7d33129a-0c65-4665-b2fb-444955d8c70b.png align="center")

"[Link to the world's first website](http://info.cern.ch/hypertext/WWW/TheProject.html)" This website has a collection of resources about the Internet, Servers, Web model, etc.

### Client-Server architecture

Suppose you want to access www.google.com from your browser(Client), by entering the domain name and clicking enter, The request is sent to the Google server, and it sends back the response to your browser.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678012782544/ccf755c1-666b-42a0-a3c6-16e9b63f775f.png align="center")

These are the things happening when you inspect the web page, in a network domain. Large Data is transferred over the internet in the form of packets or small chunks of data.

Data transfer through IP (Internet Protocol) address involves sending these packets of data from one device to another using their IP addresses. An IP address is a unique identifier assigned to every device that is connected to a network, whether it is a local network or the internet.

## Command to know your IP Address:

```bash
 curl ifconfig.me -s
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682838839590/88374f73-25cf-4142-b4d1-edffc2fd86c0.png align="center")

### How does your machine get an IP Address?

![What Is an IP Address?](https://portforward.com/what-is-ip/ip-address-small.webp align="left")

You buy a Modem/Router from the Internet Service Provider(ISP) to access the Internet, which contains a global IP Address. All the devices connected to this router will have the same IP address. And the router will assign each device a local IP address. It is done based on DHCP(Dynamic Host Configuration Protocol). When any of these devices makes a request to any server on the internet, that site for example let's say google.com can see the Global IP address.

The response sent by google.com comes to the router and is then sent to the device that actually requested through NAT(Network Access Translator). And in that particular device there might be many applications accessing the internet, so to which application the response should be transferred is decided upon port numbers.

There are **2<sup>16 </sup>** ports available in total, and ports from 0 to 1023 are reserved. These are the ports which are typically associated with specific protocols or services, they are not limited to those uses. Applications and services can use any available port, including reserved ports, as long as they do not conflict with other applications or services on the same device.

Some of the most commonly used reserved ports include:

* Port 80: This is the port used by HTTP (Hypertext Transfer Protocol) for web traffic.
    
* Port 443: This is the port used by HTTPS (HTTP Secure) for secure web traffic.
    
* Port 22: This is the port used by SSH (Secure Shell) for secure remote access.
    

Ports from 1024 to 49151 are called registered ports that are assigned by the Internet Assigned Numbers Authority (IANA) to certain services or applications.

* Port 3306: This is the port used by MySQL
    
* Port 27017: This is the port used by MongoDB
    

The port range from 49152 to 65535 is known as the dynamic or private port range which is available for your own use to run your applications.

## What are Network Protocols

![System design basics (Part 2) - Network protocols](https://media.licdn.com/dms/image/C5612AQF2WlGS--s_Vw/article-cover_image-shrink_720_1280/0/1629873089173?e=2147483647&v=beta&t=vfZiO21HLz-pxTjBY3UhL9Pb1OUlz30TVzyMFkUeP0k align="center")

### What are the essential requirements to Communicate?

1. A common language for both ends to understand
    
2. A way to address to whom you want to communicate
    
3. A connection for the content to reach the recipient.
    

Think of any example you are a part of in your daily routine such as sending an E-mail, phone calls, or even video calls. All these require the before stated points.

### And the rules for these steps to take place in a defined order are called "Protocols".

Some of the most commonly used protocols are:

* TCP (Transmission Control Protocol): A protocol that provides reliable, ordered, and error-checked delivery of data packets over a network.
    
* IP (Internet Protocol): A protocol responsible for addressing and routing data packets across networks, enabling communication between devices.
    
* FTP (File Transfer Protocol): A protocol used for transferring files between a client and a server over a network.
    
* HTTP (Hypertext Transfer Protocol): A protocol used for transmitting web pages and other data on the World Wide Web.
    
* HTTPS (Hypertext Transfer Protocol Secure): A secure version of HTTP that encrypts data transmission to ensure secure communication.
    
* SMTP (Simple Mail Transfer Protocol): A protocol used for sending email messages between servers.
    
* IMAP (Internet Message Access Protocol): A protocol used by email clients to retrieve emails from a mail server.
    
* POP (Post Office Protocol): A protocol used for downloading email messages from a mail server to a client device.
    
* DNS (Domain Name System): A protocol that translates domain names (like [**www.example.com**](http://www.example.com)) into IP addresses, enabling easy access to websites and services on the internet.
    

## Network Devices

Network devices are hardware components that are used to connect devices and enable communication between them.

Some of the most common network devices include:

* Routers: These are devices that are used to connect multiple networks together and route data between them based on IP addresses.
    
    ![What Is a Router and How Does It Work?](https://www.lifewire.com/thmb/l-s2qLLInBVfIl6AokC7Zi7Jqqk=/1500x0/filters:no_upscale():max_bytes(150000):strip_icc()/71qNsDlUZL._SL1500_-db9624bf30494933b4d2279b89ea19ef.jpg align="left")
    
* Switches: These are devices that are used to connect devices within a network and facilitate communication between them.
    

![What Is a Network Switch?](https://pimages.toolbox.com/wp-content/uploads/2022/07/26120446/Ciscos-Industry-Standard-Network-Switch.png align="center")

* Hubs: These are devices that are used to connect multiple devices within a network and broadcast data to all devices connected to the hub.
    

![Network Hub at best price in New Delhi by Online Solution | ID: 11098507333](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQSIgjMPJKEhXl755Xrb0SgnkvWeqcd2HkFkHzqWnNOlQ&usqp=CAU&ec=48665698 align="center")

* Repeaters: These are devices that are used to amplify and regenerate network signals over long distances.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682962806869/56a623dd-0bf9-46f0-a33c-c51cbd857560.png align="center")
    
* Gateways: These are devices that are used to connect different types of networks together, such as a local area network (LAN) and a wide area network (WAN).
    
    ![8 Port GSM Gateway Device at Rs 45000 | GSM Gateway Devices in Prayagraj |  ID: 20437292748](https://5.imimg.com/data5/MV/HT/MY-74225086/8-port-gsm-gateway-device-500x500.jpg align="center")
    

## Geographic scope and scale of the network.

1. **LAN (Local Area Network)** is a type of network that connects devices within a small geographic area, such as a home, office, or school. Devices on a LAN can communicate with each other directly, without the need for an internet connection. Examples of devices that can be connected to a LAN include computers, printers, and routers.
    
2. **WAN (Wide Area Network)** is a type of network that connects devices across a large geographic area, such as across cities, countries, or even continents. WANs typically use the internet or other telecommunications networks to connect devices.
    

SONET (Synchronous Optical Network) and Frame Relay are two technologies commonly used in Wide Area Networks (WANs) to transport data over long distances.

SONET is a fiber optic communication system that provides high-speed data transmission rates of up to 10 Gbps. It uses synchronous transmission technology and is particularly suited for long-haul transmission over large distances.

Frame Relay is a WAN protocol that operates at the data link layer of the OSI model. I*t* uses virtual circuits to establish logical connections between devices, allowing data to be transmitted efficiently over shared resources.

Examples of devices that can be connected to a WAN include servers, routers, and modems.

1. **MAN (Metropolitan Area Network)** is a type of network that connects devices within a larger geographic area than a LAN, but smaller than a WAN. A MAN typically covers a geographic area the size of a city or town. MANs are typically used by businesses, universities, or other organizations that need to connect multiple locations within a city or town. Examples of devices that can be connected to a MAN include switches, routers, and hubs.
    

**In summary, LANs connect devices within a small geographic area, WANs connect devices across large geographic areas, and MANs connect devices within a larger geographic area than a LAN but smaller than a WAN.**

## Network Topology

![Network Topologies – Anyone-Anytime-Anywhere](https://tara.layak.in/images/stories/bus.gif align="center")

Network topology refers to the physical or logical layout of a network, let's see a few types of them:

Bus Topology: There is a Backbone network and computers are connected to it. If the link gets broken, the entire network is spoiled. Only one device can send data at a time because of this single network channel.

![Bus Topology – Ej Laturnas](https://ejlaturnas.files.wordpress.com/2019/11/87ac7-bus_network_topology_ani.gif align="center")

Ring Topology: Computers are connected in a ring-like structure. The connection between each device in this network enables ease of communication. The limitations are unwanted calls being received by the devices that are in between the 2 devices that want to communicate, and if the link breaks the network is lost.

![Token Ring and Token Bus Working Animation - Inst Tools](https://instrumentationtools.com/wp-content/uploads/2016/07/instrumentationtools.com_token-ring-communication..gif align="center")

Star Topology: There is one central device that is connected to all the devices in the network. Make sure that the central device is stable and running all the time or else the network is collapsed.

![Flaws in the 3 common Networking Topologies | by Ned Poplaski (CISSP) |  Medium](https://miro.medium.com/v2/resize:fit:1264/1*ncy9CziCe31kAU0doORPIA.gif align="center")

Tree Topology: Also called Hybrid Topology which is a combination of two or more topologies. For example, the below picture shows the combination of Ring and Start Topologies. This approach is basically customized to meet specific requirements and fault tolerance.

![What is Hybrid Topology? Definition and Explanation - javatpoint](https://static.javatpoint.com/computer/images/what-is-hybrid-topology.jpg align="center")

Mesh Topology: Every single device is connected to every single device in the network. Reduces data transfer time, but is expensive at the same time due to the use of more cable, and adding a new device into the network is also complicated and therefore less scalable.

![Compare and Contrast Network Topologies (Star, Mesh, Bus, Hybrid etc)](https://www.networkstraining.com/wp-content/uploads/2018/10/mesh-topology.jpg align="center")

## Network Models

### 1\. OSI (Open Systems Interconnection) Model

The OSI model is a seven-layer model that breaks down the communication process into seven distinct layers, with each layer responsible for a specific set of functions.

![Computer Network Models](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS0_vDwbN8iBTYanrZgeKrWUi-LfvgZJ0Zvu0JojVtGSjcSVNYxZCFD9xgSgB06Js04RJFNA-pZcZM&usqp=CAU&ec=48665698 align="center")

1. Application Layer: Provides services to end-users, such as email or web browsing.
    
2. Presentation Layer: Formats and presents data to the application layer.
    
3. Session Layer: Establishes, manages, and terminates sessions between devices.
    
4. Transport Layer: Provides reliable data transfer between endpoints.
    
5. Network Layer: Routes packets to their destination across multiple networks.
    
6. Data Link Layer: Transmits frames of data between devices on the same network.
    
7. Physical Layer: Transmits raw data bits over a communication channel.
    

### 2\. TCP/IP Model

![TCP/IP Model: What are Layers & Protocol? TCP/IP Stack](https://www.guru99.com/images/1/093019_0615_TCPIPModelW1.png align="center")

1. Application Layer: Provides services to end-users, such as email or web browsing.
    
2. Transport Layer: Provides reliable data transfer between endpoints.
    
3. Internet Layer: Routes packets to their destination across multiple networks.
    
4. Network Access Layer: Transmits data between devices on the same network.
    

There are some similarities and differences between these two models

Similarities:

1. Layered Approach: Both models use a layered approach to break down the complex process of network communication into smaller, more manageable components.
    
2. Common Functionality: Both models address similar functionality in terms of data transmission, addressing, routing, and error handling.
    
3. Compatibility: The TCP/IP model is often considered a practical implementation of the concepts defined in the OSI model. The TCP/IP model's network layer corresponds to the OSI model's network layer, and the TCP/IP model's transport layer corresponds to the OSI model's transport layer.
    

Differences:

1. Layer Structure: The OSI model has seven layers, while the TCP/IP model has four layers. The OSI model provides a more detailed and comprehensive breakdown of network functions, whereas the TCP/IP model combines some of the layers for simplicity.
    
2. Development: The OSI model was developed by the International Organization for Standardization (ISO) in the 1980s, whereas the TCP/IP model was developed by the Department of Defense (DoD) in the 1970s.
    
3. Flexibility: The OSI model is more flexible and allows for interoperability between different vendors' systems. The TCP/IP model is more commonly used in practice, especially on the Internet, and is considered more practical and efficient for real-world network implementations.
    

## Network Security

![Network Security Solutions | VMware](https://www.vmware.com/content/dam/digitalmarketing/vmware/en/images/gallery/illustrations/illu-sec-lock-protection-whtbg.png align="left")

Let's understand network security concepts such as Firewalls, IDS (Intrusion Detection Systems), IPS (Intrusion Prevention Systems), VPNs (Virtual Private Networks), and SSL (Secure Socket Layer).

1. Firewalls: Firewalls act as a protective barrier between a network and the outside world. They monitor and control incoming and outgoing network traffic, allowing authorized communication and blocking potentially harmful or unauthorized traffic.
    
2. IDS (Intrusion Detection Systems): IDSs are security tools that monitor network traffic for suspicious activity or patterns that may indicate a potential intrusion or attack. They generate alerts to notify administrators of any detected threats.
    
3. IPS (Intrusion Prevention Systems): IPSs are similar to IDSs but go a step further by actively blocking or preventing detected malicious activities. They can automatically take action to stop or mitigate attacks, such as blocking specific IP addresses or network traffic.
    
4. VPNs (Virtual Private Networks): VPNs create secure, encrypted connections over public networks like the Internet. They allow remote users to securely access a private network, such as a corporate network, by creating a virtual tunnel that encrypts data transmission.
    
5. SSL (Secure Socket Layer): SSL, now known as TLS (Transport Layer Security), is a security protocol that encrypts data transmission between a web browser and a web server. It ensures that data sent between the two endpoints is encrypted and protected from unauthorized access.
    

## Network Troubleshooting

![How to Troubleshoot Network Issues: Unleash Your Inner IT Hero - Obkio](https://obkio.com/static/gen/img/og/1200px-how-to-troubleshoot-network-issues.jpg align="left")

Network troubleshooting is the process of identifying and resolving problems that occur in a computer network. It involves resolving issues, finding their root causes, and implementing solutions to restore proper network functionality.

Some of the most common occurring issues are:

1. Network Congestion: Network congestion happens when there is too much traffic on a network, leading to slowdowns or performance issues. It can occur due to heavy data usage, insufficient bandwidth, or network bottlenecks. To troubleshoot congestion, you can identify the source of high traffic, optimize network resources, or upgrade network infrastructure if needed.
    
2. Packet Loss: Packet loss occurs when data packets sent over a network fail to reach their destination. It can be caused by network errors, faulty hardware, or network congestion. To troubleshoot packet loss, you can perform network tests, check for faulty cables or equipment, adjust network settings, or prioritize critical traffic.
    
3. Latency Issues: Latency refers to the delay experienced when transmitting data across a network. It can be caused by long physical distances, network congestion, or processing delays. Troubleshooting latency involves measuring and analyzing network delays, optimizing network settings, and minimizing unnecessary network hops.
    

### Checksum:

A checksum is like a digital fingerprint that helps detect errors in data. It's a calculated value based on the data, and it's sent along with the data. When the data is received, the recipient calculates a new checksum and compares it with the received checksum to see if the data arrived without errors.

### Three-Way Handshake:

The three-way handshake is a process that two devices use to start a connection. First, one device sends a message to the other saying "let's connect." Then, the other device responds with a message saying "I got your message, let's connect." Finally, the first device confirms the connection by sending another message. This handshake ensures both devices are ready to communicate before they start sending data.

### Control Plane:

The control plane is like the brain of a network. It handles the management and coordination of network devices. It includes protocols and mechanisms that help devices exchange information, make decisions, and configure the network. The control plane is responsible for tasks like routing, network discovery, and network policy enforcement.

### MiddleBoxes:

Middleboxes are network devices that sit in the middle of data transmission paths. They perform various functions to manage and secure network traffic. Examples of middleboxes include firewalls, load balancers, and intrusion detection systems (IDS). These devices help control and direct network traffic, ensure security, and optimize network performance. They play a crucial role in filtering, inspecting, and modifying network traffic as it flows through the network.

### Timers:

Timers are like alarms used by networking protocols to keep track of time. They help protocols perform specific actions or trigger events after a certain duration or when a condition is met. For example, timers can be used to resend data if it's not acknowledged within a set time or to control the timing of certain protocol operations. They ensure that network protocols function correctly and efficiently.

### Cookies:

Cookies are small text files stored on a user's device by websites they visit. They help websites remember user preferences and store information, such as login credentials or items added to a shopping cart. Cookies enhance the user experience by allowing websites to personalize content and provide targeted advertisements based on browsing behavior. They are harmless text files and can be managed or cleared by the user.

### Error Status Codes:

Error status codes are numbers returned by web servers to indicate the status of a requested web page or resource. The codes are grouped into categories, such as 2xx for successful responses, 4xx for client errors, and 5xx for server errors. Common examples include 404 (Not Found), indicating that the requested page does not exist, and 500 (Internal Server Error), indicating an issue with the server. These codes help diagnose and troubleshoot issues when browsing the internet.

### Some essential commands to know:

1. Ping is a command that is used to test the connectivity between two devices. It sends ICMP echo requests to the target device and waits for ICMP echo replies. If the target device replies, it means that the connection is working.
    
    ```bash
    ping google.com
    ```
    
2. Traceroute is a command that is used to find the path taken by the packets to reach the target device. It sends ICMP echo requests to the target device and waits for ICMP time-exceeded messages. If the target device replies, it means that the connection is working.
    
    ```bash
    traceroute google.com
    ```
    
3. Nslookup is a command that is used to find the IP address of a domain name. It sends a DNS query to the DNS server and waits for a response.
    
    ```bash
    nslookup google.com
    ```
    
4. Netstat is a command that is used to display the network connections and routing tables. It can be used to find the open ports on a device.
    
    ```bash
    netstat -tulpn
    ```
    
5. Hostname is a command that is used to display the name of the current host.
    
    ```bash
    hostname
    ```
    

In this blog, we have explored various essential concepts in computer networking, ranging from network models and protocols to network security and troubleshooting. By gaining knowledge in these networking topics, you now have a solid foundation to understand how networks function, how data is transmitted, and how to address potential issues. As technology continues to evolve, networking will remain a crucial aspect of our interconnected world.

![Thank You GIF by Camtyox on DeviantArt](https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/3f6c4afc-7680-42d7-9859-ce7d521c2f37/dcei9fh-e06b7871-ec40-4b6f-a30e-7ba56b0ca82d.gif?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcLzNmNmM0YWZjLTc2ODAtNDJkNy05ODU5LWNlN2Q1MjFjMmYzN1wvZGNlaTlmaC1lMDZiNzg3MS1lYzQwLTRiNmYtYTMwZS03YmE1NmIwY2E4MmQuZ2lmIn1dXSwiYXVkIjpbInVybjpzZXJ2aWNlOmZpbGUuZG93bmxvYWQiXX0.m0pGw0Y-8PZLUP-MIIbkKwSBfXX6F0onvlpA3qbruVs align="left")

Thank you for reading this blog till the end! I hope you found it informative and helpful in gaining a better understanding of computer networks, if yes then please leave a like on this. I appreciate your support and interest in my content. If you have any specific topics or questions you would like me to cover, please let me know.