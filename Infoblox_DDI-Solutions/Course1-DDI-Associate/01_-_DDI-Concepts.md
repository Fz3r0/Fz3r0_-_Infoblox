# 🔥🧱🛡️ Infoblox DDI (DNS, DHCP, IPAM): `DDI Associate : Course`

![My Video](https://user-images.githubusercontent.com/94720207/165892585-b830998d-d7c5-43b4-a3ad-f71a07b9077e.gif)

### 🐦 Twitter  : [@fz3r0_OPs](https://twitter.com/Fz3r0_OPs)
### 🐱 Github  : [Fz3r0](https://github.com/fz3r0) 

---
 
#### Keywords: `Infoblox` 

---

<br>

# 📝❓📄 `Index`

- 

# DDI (DNS, DHCP, IPAM)

## What is DDI?

**DDI = `DHCP` + `DNS` + `IPAM`**

- `DNS`: Provides Name to Address translation
- `DHCP`: Assigns IP Address automatically
- `IPAM`: Tracks Address and Network usage

## The Need for Addresses

**"I need you to assign some IP addresses to these devices"**

- `Manual`: Manually set by the admin
- `Automatic`: Automatically set using a protocol (like DHCP)

**"Networks must provide translation services... What's the IP Address of google.com??"**

- `DNS`: Automatically translate a user friendly string like `google.com` to `192.178.52.206`

## Importance of DDI

- Without DNS the network will partially function, but many apps will not work and you will have a lot of errors like URLs not loading.
- Without DHCP the users must add static IPs manually, and many users doesn't know how to do that, and can lead to some errors like IP duplicates. If DHCP server goes down, users will experience lose of IP Address after some time.
- IPAM os not critical for users, but is very useful for Network Administrators. Without IPAM users can connect and use the network, however it becomes harder for Admins to track who is using the network. IPAM helps Admins to monitor, log & control addressing of the network. 

# DNS (Domain Name System)

- DNS = RFC 1034 , RFC 1035 (IETF)
- Default Ports = UDP 53 , TCP 53
- UDP = Small Packets
- TCP = Large Packets
- Windows local HOST file = C:\windows\system32\drivers\etc\hosts
- Linux local HOST file = /etc/hosts

---

The Domain Name System (DNS) is a hierarchical and distributed name service that provides a naming system for computers, services, and other resources on the Internet or other Internet Protocol (IP) networks. It associates various information with domain names (identification strings) assigned to each of the associated entities. Most prominently, it translates readily memorized domain names to the numerical IP addresses needed for locating and identifying computer services and devices with the underlying network protocols. The Domain Name System has been an essential component of the functionality of the Internet since 1985.

Initially, the process of assigning addresses was manual. Computers and their associated hostnames and addresses were added to the HOSTS.TXT file by contacting the SRI Network Information Center (NIC) via telephone during business hours. As the network grew, Feinler introduced the WHOIS directory on a NIC server, allowing retrieval of information about resources and contacts.

![image](https://github.com/user-attachments/assets/4c5cf1b0-ce57-4a9c-ba3c-050b4c4893e9)

The DNS was created in 1983 and became one of the original Internet Standards in 1986 (After the creation of the Internet Engineering Task Force IETF). In 1984, UC Berkeley students developed the first Unix name server implementation known as BIND (Berkeley Internet Name Domain). Over the years, various developers and organizations, including the Internet Systems Consortium (ISC), contributed to the maintenance and development of BIND. In November 1987, RFC 1034 and RFC 1035 replaced the original DNS specifications from 1983. They describe the whole protocol functionality and include data types that it can carry.

## DNS Hierarchy

DNS (Domain Name System) hierarchy is the structured organization of DNS components that enables efficient and scalable domain name resolution across the internet. It follows a tree-like model with different levels of authority, ensuring that domain names (like www.example.com) are translated into IP addresses (like 192.0.2.1) effectively.

![image](https://github.com/user-attachments/assets/14589038-4f11-4e6a-b931-f143622fb7e4)

| **Level**                 | **Examples**                       | **Role**                                                                                     |
|---------------------------|-------------------------------------|---------------------------------------------------------------------------------------------|
| **1. Root Level**         | `.`                                | The highest level of the DNS hierarchy; directs queries to TLD servers.                     |
| **2. Top-Level Domains**  | `.com`, `.org`, `.net`, `.edu`     | Manages domains within a specific TLD and points to authoritative name servers.             |
| **3. Second-Level Domains** | `example` in `example.com`        | Registered by organizations or individuals; contains authoritative DNS records for subdomains. |
| **4. Subdomains**         | `www.example.com`, `mail.example.com` | Organizes services or sections under an SLD; resolved by the SLD's authoritative servers.    |
| **5. Authoritative Name Servers** | N/A                         | Holds DNS records (e.g., `A`, `AAAA`, `MX`) and provides definitive domain-to-IP mappings.   |
| **6. Recursive Resolvers** | Client systems (e.g., browsers)    | Queries the DNS hierarchy on behalf of clients to resolve domain names into IP addresses.    |

## Importance of DNS

DNS is critical network infraestructure

- Todays Apps are name-based, not address-based (Active Directory, VoIP, etc)
- Load Balancers and CDN (Content Delivery Network) rely on DNS
- Emails need names
- HTTPS & certs rely on DNS for names (DNS names are tied to secure websites)

## DNS lookup diagram

![image](https://github.com/user-attachments/assets/96625c3a-a715-4af7-a14b-f70e74167376)

![image](https://github.com/user-attachments/assets/b222436f-a219-40a2-908e-3d990cbff8d9)



# 📚🗂️🎥 Resources

- https://launchpad.education.infoblox.com/student/catalog/list?category_ids=33680-dns-dhcp-and-ipam-ddi
- https://launchpad.education.infoblox.com/student/collection/1679502-9851?sid=f71ddc86-5c52-4c0c-9803-ef455206a209&sid_i=0
- https://launchpad.education.infoblox.com/student/collection/1679502/path/2377315/activity/2360973
- https://en.wikipedia.org/wiki/Domain_Name_System
- https://www.cloudns.net/blog/dns-history-creation-first/
- http://www.webdevelopertuts.com/what-is-DNS-and-DNS-hierarchy
  
---

<span align="center"> <p align="center"> ![giphy](https://user-images.githubusercontent.com/94720207/166587250-292d9a9f-e590-4c25-a678-d457e2268e85.gif) </p> </span> 



&nbsp;

<span align="center"> <p align="center"> _I hope this information was useful for someone_ </p> </span> 
<span align="center"> <p align="center"> _and please, don't forget to enjoy your days..._ </p> </span> 
<span align="center"> <p align="center"> _...It is getting dark... so dark..._ </p> </span> 

&nbsp;

<span align="center"> <p align="center"> _In the mist of the night you could see me come, where shadows move and Demons lie..._ </p> </span> 
<span align="center"> <p align="center"> _I am [Fz3r0 💀](https://github.com/Fz3r0/) and the Sun no longer rises..._ </p> </span> 

---






---

> ![hecho en mexico 5](https://user-images.githubusercontent.com/94720207/166068790-fa1f243d-2db9-4810-a6e4-eb3c4ad23700.png)
>
> _- Hecho en México - by [Fz3r0 💀](https://github.com/Fz3r0/)_  
>
> _"In the mist of the night you could see me come, where shadows move and Demons lie..."_ 





