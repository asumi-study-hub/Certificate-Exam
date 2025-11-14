# Module 2: Network Operation

> _Created: 14 November 2025 | Last Updated: 14 November_

## Navigation

- [Network Protocols](#network-protocols)
- [Additional Network Protocols](#additional-network-protocols)
- [Firewalls and Network Security Measures](#firewalls-and-network-security-measures)
- [Virtual Private Networks (VPNs)](#virtual-private-networks-vpns)
- [Security Zones](#security-zones)
- [Subnetting and CIDR](#subnetting-and-cidr)
- [Proxy Servers](#proxy-servers)
- [Virtual Networks and Privacy](#virtual-networks-and-privacy)
- [VPN Protocols: Wireguard and IPSec](#vpn-protocols-wireguard-and-ipsec)
- [Glossary Terms from Module 2](#glossary-terms-from-module-2)

---

## Network Protocols

**Network Protocols: The Rules of Communication**

-   Network protocols are sets of rules that ensure data is delivered correctly and structured appropriately between devices on a network.
-   They are essential for reliable communication, guiding how devices interact and exchange information.

**Key Protocols in Action**

-   **Transmission Control Protocol (TCP):** Establishes a connection and verifies devices (handshake) before data streaming, ensuring reliable communication.
-   **Address Resolution Protocol (ARP):** Determines the MAC address of the next router or device, ensuring data packets reach the correct destination.
-   **Hypertext Transfer Protocol Secure (HTTPS):** Provides a secure method for communication between client and web servers, encrypting data using SSL/TLS.
-   **Domain Name System (DNS):** Translates human-readable domain names (like website addresses) into numerical IP addresses that computers use to locate servers.

**Security Implications of Protocols**

-   Protocols like HTTPS are crucial for network security, as they encrypt data to protect sensitive information from malicious actors.
-   Understanding these protocols is vital for security analysts to identify vulnerabilities and secure networks effectively.

[Back to Navigation](#navigation)

---

## Additional Network Protocols

In previous readings and videos, you learned how network protocols organize the sending and receiving of data across a network. You also learned that protocols can be divided into three categories: communication protocols, management protocols, and security protocols.

This reading will introduce you to a few additional concepts and protocols that will come up regularly in your work as a security analyst. Some protocols are assigned port numbers by the Internet Assigned Numbers Authority (IANA). These port numbers are included in the description of each protocol, if assigned.

## Network Address Translation

The devices on your local home or office network each have a private IP address that they use to communicate directly with each other. However, in order for the devices with private IP addresses to communicate with the public internet, they need to have a single public IP address that represents all devices on the LAN to the public. For outgoing messages, the router can replace a private source IP address with its public IP address and perform the reverse operation for responses. This process is known as Network Address Translation (NAT) and it generally requires a router or firewall to be specifically configured to perform NAT. NAT is a part of layer 2 (internet layer) and layer 3 (transport layer) of the TCP/IP model.

| Private IP Addresses | Public IP Addresses |
|---------------------|---------------------|
| Assigned by the router | Assigned by ISP and IANA |
| Unique only within private network | Unique address in global internet |
| No cost to use | Costs to lease a public IP address |
| **Address ranges:** | **Assignable address ranges:** |
| 10.0.0.0-10.255.255.255 | 1.0.0.0-9.255.255.255 |
| 172.16.0.0-172.31.255.255 | 11.0.0.0-126.255.255.255 |
| 192.168.0.0-192.168.255.255 | 128.0.0.0-172.15.255.255 |
| | 172.32.0.0-192.167.255.255 |
| | 192.169.0.0-233.255.255.255 |

## Dynamic Host Configuration Protocol

Dynamic Host Configuration Protocol (DHCP) is in the management family of network protocols. DHCP is an application layer protocol used on a network to configure devices. It works with the router to assign a unique IP address to each device and provide the addresses of the appropriate DNS server and default gateway for each device. DHCP servers operate on UDP port 67 while DHCP clients operate on UDP port 68.

## Address Resolution Protocol

By now, you are familiar with IP and MAC addresses. You've learned that each device on a network has a public IP address, a private IP address, and a MAC address that identify it on the network. A device's IP address may change over time, but its MAC address is permanent because it is unique to a device's network interface card. The MAC address is used to communicate with devices within the same network, but sometimes, the MAC address is unknown. This is why the Address Resolution Protocol (ARP) is needed. ARP is mainly a network access layer protocol in the TCP/IP model used to translate the IP addresses that are found in data packets into the MAC address of the hardware device.

Each device on the network performs ARP and keeps track of matching IP and MAC addresses in an ARP cache. ARP does not have a specific port number since it is a layer 2 protocol and port numbers are associated with the layer 7 application layer.

## Telnet

Telnet is an application layer protocol that is used to connect with a remote system. Telnet sends all information in clear text. It uses command line prompts to control another device similar to secure shell (SSH), but Telnet is not as secure as SSH. Telnet can be used to connect to local or remote devices and uses TCP port 23.

## Secure Shell

Secure shell protocol (SSH) is used to create a secure connection with a remote system. This application layer protocol provides an alternative for secure authentication and encrypted communication. SSH operates over the TCP port 22 and is a replacement for less secure protocols, such as Telnet.

## Post Office Protocol

Post office protocol (POP) is an application layer (layer 4 of the TCP/IP model) protocol used to manage and retrieve email from a mail server. POP3 is the most commonly used version of POP. Many organizations have a dedicated mail server on the network that handles incoming and outgoing mail for users on the network. User devices will send requests to the remote mail server and download email messages locally. If you have ever refreshed your email application and had new emails populate in your inbox, you are experiencing POP and internet message access protocol (IMAP) in action. Unencrypted, plaintext authentication uses TCP/UDP port 110 and encrypted emails use Secure Sockets Layer/Transport Layer Security (SSL/TLS) over TCP/UDP port 995. When using POP, mail has to finish downloading on a local device before it can be read. After downloading, the mail may or may not be deleted from the mail server, so it does not guarantee that a user can sync the same email across multiple devices.

## Internet Message Access Protocol (IMAP)

IMAP is used for incoming email. It downloads the headers of emails and the message content. The content also remains on the email server, which allows users to access their email from multiple devices. IMAP uses TCP port 143 for unencrypted email and TCP port 993 over the TLS protocol. Using IMAP allows users to partially read email before it is finished downloading. Since the mail is kept on the mail server, it allows a user to sync emails across multiple devices.

## Simple Mail Transfer Protocol

Simple Mail Transfer Protocol (SMTP) is used to transmit and route email from the sender to the recipient's address. SMTP works with Message Transfer Agent (MTA) software, which searches DNS servers to resolve email addresses to IP addresses, to ensure emails reach their intended destination. SMTP uses TCP/UDP port 25 for unencrypted emails and TCP/UDP port 587 using TLS for encrypted emails. The TCP port 25 is often used by high-volume spam. SMTP helps to filter out spam by regulating how many emails a source can send at a time.

## Protocols and Port Numbers

Remember that port numbers are used by network devices to determine what should be done with the information contained in each data packet once they reach their destination. Firewalls can filter out unwanted traffic based on port numbers. For example, an organization may configure a firewall to only allow access to TCP port 995 (POP3) by IP addresses belonging to the organization.

As a security analyst, you will need to know about many of the protocols and port numbers mentioned in this course. They may be used to determine your technical knowledge in interviews, so it's a good idea to memorize them. You will also learn about new protocols on the job in a security position.

| Protocol | Port |
|----------|------|
| DHCP | UDP port 67 (servers)<br>UDP port 68 (clients) |
| ARP | none |
| Telnet | TCP port 23 |
| SSH | TCP port 22 |
| POP3 | TCP/UDP port 110 (unencrypted)<br>TCP/UDP port 995 (encrypted, SSL/TLS) |
| IMAP | TCP port 143 (unencrypted)<br>TCP port 993 (encrypted, SSL/TLS) |
| SMTP | TCP/UDP Port 25<br>SMTPS TCP/UDP port 587 (encrypted, TLS) |

## Key Takeaways

As a cybersecurity analyst, you will encounter various common protocols in your everyday work. The protocols covered in this reading include NAT, DHCP, ARP, Telnet, SSH, POP3, IMAP, and SMTP. It is equally important to understand where each protocol is structured in the TCP/IP model and which ports they occupy.

[Back to Navigation](#navigation)

---

## Firewalls and Network Security Measures

### Types of Firewalls

-   **Hardware Firewalls:** These are physical devices that inspect data packets before they enter the network, offering a basic defense.
-   **Software Firewalls:** These are programs installed on computers or servers that perform the same functions as hardware firewalls but are not physical devices.
-   **Cloud-based Firewalls (FaaS):** Offered by cloud service providers, these software firewalls are hosted in the cloud and protect an organization's onsite network and cloud assets.

### Firewall Operations

-   **Stateless Firewalls:** These firewalls operate based on predefined rules and do not track information from data packets, making them less secure.
-   **Stateful Firewalls:** These firewalls keep track of information and proactively filter out threats by analyzing network traffic for suspicious characteristics and behavior.
-   **Next-Generation Firewalls (NGFWs):** These provide advanced security beyond stateful firewalls, including deep packet inspection and intrusion protection, often connecting to cloud-based threat intelligence services.

[Back to Navigation](#navigation)

---

## Virtual Private Networks (VPNs)

**Understanding Internet Vulnerabilities**

-   When you connect to the internet, your requests go through your Internet Service Provider (ISP), which can expose your private information.
-   This exposure means your internet activity, physical location, and personal data like bank accounts could be intercepted and linked to you.

**How VPNs Provide Security**

-   A VPN changes your public IP address and hides your virtual location, keeping your data private, especially on public networks.
-   VPNs encrypt your data as it travels across the internet, ensuring confidentiality and making it unreadable to unauthorized parties.

**Encapsulation and Encrypted Tunnels**

-   VPNs use encapsulation, a process that wraps your sensitive data in other data packets that routers can read, allowing your requests to reach their destination while keeping your personal data encrypted.
-   An encrypted tunnel is established between your device and the VPN server, making your data unhackable without a cryptographic key and providing significant protection against malicious actors.

[Back to Navigation](#navigation)

---

## Security Zones

**Understanding Security Zones**

-   Security zones segment a network, acting as a barrier to internal networks, maintaining privacy, and preventing issues from spreading.
-   An example is a hotel separating public Wi-Fi from staff networks, or a university having separate subnets for faculty and students.

**Types of Security Zones**

-   **Uncontrolled Zone:** This refers to any network outside an organization's control, such as the internet.
-   **Controlled Zone:** This protects the internal network from the uncontrolled zone and includes several sub-zones.

**Layers within the Controlled Zone**

-   **Demilitarized Zone (DMZ):** This outer layer contains public-facing services like web servers, proxy servers, and DNS servers, acting as a network perimeter.
-   **Internal Network:** This contains private servers and data that require protection.
-   **Restricted Zone:** Located within the internal network, this zone protects highly confidential information accessible only to employees with specific privileges.

**Security Measures with Firewalls**

-   Ideally, the DMZ is situated between two firewalls: one filtering external traffic and another filtering traffic entering the internal network.
-   This multi-layered defense prevents attacks from spreading between zones, and security analysts regulate access control policies on these firewalls.

[Back to Navigation](#navigation)

---

## Subnetting and CIDR

Earlier in this course, you learned about network segmentation, a security technique that divides networks into sections. A private network can be segmented to protect portions of the network from the internet, which is an unsecured global network.

For example, you learned about the uncontrolled zone, the controlled zone, the demilitarized zone, and the restricted zone. Feel free to review the video about [security zones](https://www.coursera.org/learn/networks-and-network-security/lecture/GccYm/security-zones) for a refresher on how network segmentation can be used to add a layer of security to your organization's network operations. Creating security zones is one example of a networking strategy called subnetting.

### Overview of Subnetting

**Subnetting** is the subdivision of a network into logical groups called subnets. It works like a network inside a network. Subnetting divides up a network address range into smaller subnets within the network. These smaller subnets form based on the IP addresses and network mask of the devices on the network. Subnetting creates a network of devices to function as their own network. This makes the network more efficient and can also be used to create security zones. If devices on the same subnet communicate with each other, the switch changes the transmissions to stay on the same subnet, improving speed and efficiency of the communications.

### Classless Inter-Domain Routing Notation for Subnetting

Classless Inter-Domain Routing (CIDR) is a method of assigning subnet masks to IP addresses to create a subnet. Classless addressing replaces classful addressing. Classful addressing was used in the 1980s as a system of grouping IP addresses into classes (Class A to Class E). Each class included a limited number of IP addresses, which were depleted as the number of devices connecting to the internet outgrew the classful range in the 1990s. Classless CIDR addressing expanded the number of available IPv4 addresses.

CIDR allows cybersecurity professionals to segment classful networks into smaller chunks. CIDR IP addresses are formatted like IPv4 addresses, but they include a slash ("/'") followed by a number at the end of the address, This extra number is called the IP network prefix. For example, a regular IPv4 address uses the 198.51.100.0 format, whereas a CIDR IP address would include the IP network prefix at the end of the address, 198.51.100.0/24. This CIDR address encompasses all IP addresses between 198.51.100.0 and 198.51.100.255. The system of CIDR addressing reduces the number of entries in routing tables and provides more available IP addresses within networks. You can try converting CIDR to IPv4 addresses and vice versa through an online conversion tool, like [IPAddressGuide](https://www.ipaddressguide.com/cidr), for practice and to better understand this concept.

**Note:** You may learn more about CIDR during your career, but it won't be covered in any additional depth in this certificate program. For now, you only need a basic understanding of this concept.

### Security Benefits of Subnetting

Subnetting allows network professionals and analysts to create a network within their own network without requesting another network IP address from their internet service provider. This process uses network bandwidth more efficiently and improves network performance. Subnetting is one component of creating isolated subnetworks through physical isolation, routing configuration, and firewalls.

### Key Takeaways

Subnetting is a common security strategy used by organizations. Subnetting allows organizations to create smaller networks within their private network. This improves the efficiency of the network and can be used to create security zones.

[Back to Navigation](#navigation)

---

## Proxy Servers

### Proxy Server Fundamentals

-   A proxy server acts as an intermediary between the internet and an internal network, forwarding client requests to other servers.
-   It has a public IP address, distinct from the private network, which helps hide the internal network's IP from malicious actors.

### Security and Efficiency Benefits

-   Proxy servers determine if connection requests are safe, adding a layer of security by scrutinizing incoming traffic.
-   They use temporary memory to store frequently requested data, reducing the need to fetch information from internal servers repeatedly and thus enhancing security by limiting internal server contact.

### Types of Proxy Servers

-   **Forward Proxy Server:** Regulates and restricts internet access for internal users, hiding their IP addresses and approving outgoing requests.
-   **Reverse Proxy Server:** Manages internet access to internal servers, accepting and approving external traffic before forwarding it to protect confidential data.
-   **Email Proxy Server:** Filters spam and verifies sender addresses to prevent phishing attacks, as demonstrated by an example of filtering 95% of messages as spam at a large ISP.

[Back to Navigation](#navigation)

---

## Virtual Networks and Privacy

This section of the course covered a lot of information about network operations. You reviewed the fundamentals of network architecture and communication and can now use this knowledge as you learn how to secure networks. Securing a private network requires maintaining the confidentiality of your data and restricting access to authorized users.

In this reading, you will review several network security topics previously covered in the course, including virtual private networks (VPNs), proxy servers, firewalls, and security zones. You'll continue to learn more about these concepts and how they relate to each other as you continue through the course.

### **Common Network Protocols**

Network protocols are used to direct traffic to the correct device and service depending on the kind of communication being performed by the devices on the network. Protocols are the rules used by all network devices that provide a mutually agreed upon foundation for how to transfer data across a network.

There are three main categories of network protocols: communication protocols, management protocols, and security protocols.

1.  Communication protocols are used to establish connections between servers. Examples include TCP, UDP, and Simple Mail Transfer Protocol (SMTP), which provides a framework for email communication.
2.  Management protocols are used to troubleshoot network issues. One example is the Internet Control Message Protocol (ICMP).
3.  Security protocols provide encryption for data in transit. Examples include IPSec and SSL/TLS.

Some other commonly used protocols are:

-   HyperText Transfer Protocol (HTTP). HTTP is an application layer communication protocol. This allows the browser and the web server to communicate with one another.
-   Domain Name System (DNS). DNS is an application layer protocol that translates, or maps, host names to IP addresses.
-   Address Resolution Protocol (ARP). ARP is a network layer communication protocol that maps IP addresses to physical machines or a MAC address recognized on the local area network.

### **Wi-Fi**

This section of the course also introduced various wireless security protocols, including WEP, WPA, WPA2, and WPA3. WPA3 encrypts traffic with the Advanced Encryption Standard (AES) cipher as it travels from your device to the wireless access point. WPA2 and WPA3 offer two modes: personal and enterprise. Personal mode is best suited for home networks while enterprise mode is generally utilized for business networks and applications.

### **Network Security Tools and Practices**

#### **Firewalls**

Previously, you learned that firewalls are network virtual appliances (NVAs) or hardware devices that inspect and can filter network traffic before it's permitted to enter the private network. Traditional firewalls are configured with rules that tell it what types of data packets are allowed based on the port number and IP address of the data packet.

There are two main categories of firewalls.

-   **Stateless:** A class of firewall that operates based on predefined rules and does not keep track of information from data packets
-   **Stateful:** A class of firewall that keeps track of information passing through it and proactively filters out threats. Unlike stateless firewalls, which require rules to be configured in two directions, a stateful firewall only requires a rule in one direction. This is because it uses a "state table" to track connections, so it can match return traffic to an existing session

Next generation firewalls (NGFWs) are the most technologically advanced firewall protection. They exceed the security offered by stateful firewalls because they include deep packet inspection (a kind of packet sniffing that examines data packets and takes actions if threats exist) and intrusion prevention features that detect security threats and notify firewall administrators. NGFWs can inspect traffic at the application layer of the TCP/IP model and are typically application aware. Unlike traditional firewalls that block traffic based on IP address and ports, NGFWs rules can be configured to block or allow traffic based on the application. Some NGFWs have additional features like Malware Sandboxing, Network Anti-Virus, and URL and DNS Filtering.

#### **Proxy Servers**

A proxy server is another way to add security to your private network. Proxy servers utilize network address translation (NAT) to serve as a barrier between clients on the network and external threats. Forward proxies handle queries from internal clients when they access resources external to the network. Reverse proxies function opposite of forward proxies; they handle requests from external systems to services on the internal network. Some proxy servers can also be configured with rules, like a firewall. For example, you can create filters to block websites identified as containing malware.

#### **Virtual Private Networks (VPN)**

A VPN is a service that encrypts data in transit and disguises your IP address. VPNs use a process called encapsulation. Encapsulation wraps your unencrypted data in an encrypted data packet, which allows your data to be sent across the public network while remaining anonymous. Enterprises and other organizations use VPNs to help protect communications from users' devices to corporate resources. Some of these resources include servers or virtual machines that host business applications. Individuals also use VPNs to increase personal privacy. VPNs protect user privacy by concealing personal information, including IP addresses, from external servers. A reputable VPN also minimizes its own access to user internet activity by using strong encryption and other security measures. Organizations are increasingly using a combination of VPN and SD-WAN capabilities to secure their networks. A software-defined wide area network (SD-WAN) is a virtual WAN service that allows organizations to securely connect users to applications across multiple locations and over large geographical distances.

#### **Key Takeaways**

There are three main categories of network protocols: communication, management, and security protocols. In this reading, you learned the fundamentals of firewalls, proxy servers, and VPNs. More organizations are implementing a cloud-based approach to network security by incorporating a combination of VPN and SD-WAN capabilities as a service.

[Back to Navigation](#navigation)

---

## VPN Protocols: Wireguard and IPSec

A VPN, or virtual private network, is a network security service that changes your public IP address and hides your virtual location so that you can keep your data private when you're using a public network like the internet. VPNs provide a server that acts as a gateway between a computer and the internet. This server creates a path similar to a virtual tunnel that hides the computer's IP address and encrypts the data in transit to the internet. The main purpose of a VPN is to create a secure connection between a computer and a network. Additionally, a VPN allows trusted connections to be established on non-trusted networks. VPN protocols determine how the secure network tunnel is formed. Different VPN providers provide different VPN protocols.

This reading will cover the differences between remote access and site-to-site VPNs, and two VPN protocols: WireGuard VPN and IPSec VPN. A VPN protocol is similar to a network protocol: It's a set of rules or instructions that will determine how data moves between endpoints. An endpoint is any device connected on a network. Some examples of endpoints include computers, mobile devices, and servers.

### Remote Access and Site-to-Site VPNs

Individual users use remote access VPNs to establish a connection between a personal device and a VPN server. Remote access VPNs encrypt data sent or received through a personal device. The connection between the user and the remote access VPN is established through the internet.

Enterprises use site-to-site VPNs largely to extend their network to other networks and locations. This is particularly useful for organizations that have many offices across the globe. IPSec is commonly used in site-to-site VPNs to create an encrypted tunnel between the primary network and the remote network. One disadvantage of site-to-site VPNs is how complex they can be to configure and manage compared to remote VPNs.

### WireGuard VPN vs. IPSec VPN

WireGuard and IPSec are two different VPN protocols used to encrypt traffic over a secure network tunnel. The majority of VPN providers offer a variety of options for VPN protocols, such as WireGuard or IPSec. Ultimately, choosing between IPSec and WireGuard depends on many factors, including connection speeds, compatibility with existing network infrastructure, and business or individual needs.

#### WireGuard VPN

WireGuard is a high-speed VPN protocol, with advanced encryption, to protect users when they are accessing the internet. It's designed to be simple to set up and maintain. WireGuard can be used for both site-to-site connection and client-server connections. WireGuard is relatively newer than IPSec, and is used by many people due to the fact that its download speed is enhanced by using fewer lines of code. WireGuard is also open source, which makes it easier for users to deploy and debug. This protocol is useful for processes that require faster download speeds, such as streaming video content or downloading large files.

#### IPSec VPN

IPSec is another VPN protocol that may be used to set up VPNs. Most VPN providers use IPSec to encrypt and authenticate data packets in order to establish secure, encrypted connections. Since IPSec is one of the earlier VPN protocols, many operating systems support IPSec from VPN providers.

Although IPSec and WireGuard are both VPN protocols, IPSec is older and more complex than WireGuard. Some clients may prefer IPSec due to its longer history of use, extensive security testing, and widespread adoption. However, others may prefer WireGuard because of its potential for better performance and simpler configuration.

### Key Takeaways

A VPN protocol is similar to a network protocol: It's a set of rules or instructions that will determine how data moves between endpoints. There are two types of VPNs: remote access and site-to-site. Remote access VPNs establish a connection between a personal device and a VPN server and encrypt or decrypt data exchanged with a personal device. Enterprises use site-to-site VPNs largely to extend their network to different locations and networks. IPSec can be used to create site-to-site connections and WireGuard can be used for both site-to-site and remote access connections.

[Back to Navigation](#navigation)

---

## Glossary Terms from Module 2

### Terms and Definitions from Course 3, Module 2

**Address Resolution Protocol (ARP):** A network protocol used to determine the MAC address of the next router or device on the path

**Cloud-based firewalls:** Software firewalls that are hosted by the cloud service provider

**Controlled zone:** A subnet that protects the internal network from the uncontrolled zone

**Domain Name System (DNS):** A networking protocol that translates internet domain names into IP addresses

**Encapsulation:** A process performed by a VPN service that protects your data by wrapping sensitive data in other data packets

**Firewall:** A network security device that monitors traffic to or from your network

**Forward proxy server:** A server that regulates and restricts a person's access to the internet

**Hypertext Transfer Protocol (HTTP):** An application layer protocol that provides a method of communication between clients and website servers

**Hypertext Transfer Protocol Secure (HTTPS):** A network protocol that provides a secure method of communication between clients and servers

**IEEE 802.11 (Wi-Fi):** A set of standards that define communication for wireless LANs

**Network protocols:** A set of rules used by two or more devices on a network to describe the order of delivery of data and the structure of data

**Network segmentation:** A security technique that divides the network into segments

**Port filtering:** A firewall function that blocks or allows certain port numbers to limit unwanted communication

**Proxy server:** A server that fulfills the requests of its clients by forwarding them to other servers

**Reverse proxy server:** A server that regulates and restricts the internet's access to an internal server

**Secure File Transfer Protocol (SFTP):** A secure protocol used to transfer files from one device to another over a network

**Secure shell (SSH):** A security protocol used to create a shell with a remote system

**Security zone:** A segment of a company's network that protects the internal network from the internet

**Simple Network Management Protocol (SNMP):** A network protocol used for monitoring and managing devices on a network

**Stateful:** A class of firewall that keeps track of information passing through it and proactively filters out threats

**Stateless:** A class of firewall that operates based on predefined rules and does not keep track of information from data packets

**Subnetting:** The subdivision of a network into logical groups called subnets

**Transmission Control Protocol (TCP):** An internet communication protocol that allows two devices to form a connection and stream data

**Uncontrolled zone:** The portion of the network outside the organization

**Virtual private network (VPN):** A network security service that changes your public IP address and masks your virtual location so that you can keep your data private when you are using a public network like the internet

**Wi-Fi Protected Access (WPA):** A wireless security protocol for devices to connect to the internet

[Back to Navigation](#navigation)
