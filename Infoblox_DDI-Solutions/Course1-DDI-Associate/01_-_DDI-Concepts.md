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

## Importance of DNS

DNS is critical network infraestructure

- Todays Apps are name-based, not address-based (Active Directory, VoIP, etc)
- Load Balancers and CDN (Content Delivery Network) rely on DNS
- Emails need names
- HTTPS & certs rely on DNS for names (DNS names are tied to secure websites)

## DNS Terminology & Defnitions

![image](https://github.com/user-attachments/assets/80a4d3b0-a4de-4548-a647-0c4793615c06)

| **Term**                          | **Explanation**                                                                                                                                                                                                                                          | **Real-Life Example**                                                                                                                                     |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| **DNS Lookup**                    | The process of resolving a domain name (e.g., `example.com`) into its corresponding IP address (e.g., `93.184.216.34`). Involves client requests and queries through multiple DNS servers in a hierarchical structure.                               | Typing `google.com` in your browser and receiving the page after the browser resolves the domain into an IP address like `142.250.190.78`.                |
| **DNS Server**                    | A server that stores and manages domain name data and responds to queries for translating domain names into IP addresses or other DNS records. Examples include recursive resolvers, root servers, and authoritative name servers.                  | Your ISP's DNS server resolving `example.com` when you browse the internet.                                                                               |
| **FQDN (Fully Qualified Domain Name)** | A complete domain name specifying its exact location in the DNS hierarchy, including the hostname and domain name (e.g., `xyz.example.com`). It includes all components up to the top-level domain (TLD), providing a unique identifier.             | Visiting `mail.google.com` to access Gmail; `mail` is the hostname, `google` the domain, and `.com` the TLD.                                              |
| **Stub Resolver / Client**        | Stub Resolver is a piece of software (DNS client) embedded in devices or applications (e.g., Windows OS or web browsers) that queries a recursive resolver to resolve a domain name. The "client" refers to the device that initiates the DNS request and contains the OS/Stub Resolver.                          | Your smartphone’s browser acting as the client when you search for a website.                                                                             |
| **DNS Query**                     | A request sent by a client or DNS server to resolve a domain name into an IP address or retrieve another type of DNS record. Queries can be recursive or iterative, depending on the context.                                                       | A browser sending a query for `openai.com` to find its associated IP address.                                                                             |
| **Recursive Query**               | A query type sent by the client/stub resolver to a recursive resolver, instructing it to resolve the requested name fully by contacting other DNS servers if necessary. By default, most clients make recursive queries.                          | Typing `nytimes.com` in your browser and your computer asking the ISP's recursive resolver to resolve the domain.                                         |
| **Iterative Query**               | A query type used by DNS servers to ask other DNS servers for information (Only between DNS servers). The server receiving the query responds with the best answer it has, which might be a referral to another server.                                                         | A recursive resolver querying a root DNS server for `example.org`, receiving a referral to the `.org` TLD server.                                         |
| **Recursive Resolver / Recursive Name Server** | A server that handles recursive queries from clients (center). It queries other DNS servers using iterative queries and caches results for future use to improve performance and reduce lookup times.                                                 | Google’s public DNS server (e.g., `8.8.8.8`) resolving queries for users worldwide.                                                                       |
| **Authoritative Name Server**     | The DNS server responsible for specific domains. It only responds to queries for the domains it manages based on its own database. For example, the authoritative server for `fz3r0.com` can respond only to queries about `fz3r0.com`.              | The DNS server managed by `example.com`’s hosting provider answering queries about `www.example.com`.                                                     |
| **RR (Resource Record)**          | The fundamental unit of data in DNS. Each record specifies a mapping between a domain name (label) and specific information (e.g., IP address). For example: `f0.fz3r0.com -> 123.123.123.123` (label: `f0.fz3r0.com`, type: `A`, info: `123.123.123.123`). | The `A` record of `example.com` pointing to `93.184.216.34` or the `MX` record pointing to its email server.                                               |
| **Zones**                         | A collection of resource records that share a common name suffix, representing a single domain or subdomain. Zones are managed on DNS servers, which might delegate parts of the domain to other servers for scalability and redundancy.            | A DNS server managing the `.com` zone, which includes records for `google.com`, `example.com`, and all other `.com` domains.                              |


## DNS Hierarchy

DNS (Domain Name System) hierarchy is the structured organization of DNS components that enables efficient and scalable domain name resolution across the internet. It follows a tree-like model with different levels of authority, ensuring that domain names (like www.example.com) are translated into IP addresses (like 192.0.2.1) effectively.

![image](https://github.com/user-attachments/assets/14589038-4f11-4e6a-b931-f143622fb7e4)

| **Level**                 | **Examples**                       | **Role**                                                                                     |
|---------------------------|-------------------------------------|---------------------------------------------------------------------------------------------|
| **1. Root Level**         | `.`                                | The highest level of the DNS hierarchy; directs queries to TLD servers.                     |
| **2. TLD (Top-Level Domains)**  | `.com`, `.org`, `.net`, `.edu`     | Manages domains within a specific TLD and points to authoritative name servers.             |
| **3. SLD (Second-Level Domains)** | `example` in `example.com`        | Registered by organizations or individuals; contains authoritative DNS records for subdomains. |
| **4. Subdomains**         | `www.example.com`, `mail.example.com` | Organizes services or sections under an SLD; resolved by the SLD's authoritative servers.    |
| **5. Authoritative Name Servers** | N/A                         | Holds DNS records (e.g., `A`, `AAAA`, `MX`) and provides definitive domain-to-IP mappings.   |
| **6. Recursive Resolvers** | Client systems (e.g., browsers)    | Queries the DNS hierarchy on behalf of clients to resolve domain names into IP addresses.    |

## DNS lookup

| **Step**                 | **Action**                                                                                   | **Result**                                 |
|--------------------------|----------------------------------------------------------------------------------------------|-------------------------------------------|
| **1. Client Request**    | The client queries the recursive resolver for a domain name.                                 | Sends DNS query to recursive resolver.    |
| **2. Recursive Resolver**| Checks its cache for the answer; if unavailable, queries the DNS hierarchy.                  | Contacts root server.                     |
| **3. Root Server**        | Directs the resolver to the appropriate TLD name server.                                    | Address of the TLD server.                |
| **4. TLD Server**         | Provides the resolver with the address of the domain's authoritative name server.           | Address of authoritative server.          |
| **5. Authoritative Server** | Resolves the domain name into an IP address or other requested information.               | Final IP address or record is returned.   |
| **6. Response to Client** | The recursive resolver sends the IP address back to the client.                             | Client connects to the destination.       |

## DNS Server Types:

| **Server Type**            | **Role in DNS Lookup**                                                                                                                                  | **Example**                                                                                          |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| **Hosts File (Client)**     | Local file on the client system used to resolve domain names to IP addresses before querying any DNS server.                                           | `C:\Windows\System32\drivers\etc\hosts` or `/etc/hosts` with an entry like `127.0.0.1 example.com`. |
| **Recursive Resolver**      | Receives client queries and resolves them by contacting other DNS servers if the answer is not in its cache.                                          | ISP or public resolvers (e.g., Google DNS `8.8.8.8`, Cloudflare `1.1.1.1`).                         |
| **Root Name Server**        | Directs the resolver to the appropriate TLD server responsible for the domain.                                                                        | One of the 13 root servers (e.g., `A.ROOT-SERVERS.NET`).                                            |
| **TLD Name Server**         | Provides the resolver with the authoritative name server for the queried domain based on the top-level domain.                                        | `.com`, `.org`, or `.uk` TLD servers.                                                               |
| **Authoritative Name Server**| Holds DNS records (e.g., A, AAAA, MX) and provides the final IP address or other requested information about the domain.                              | The authoritative server for `example.com`.                                                        |






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





