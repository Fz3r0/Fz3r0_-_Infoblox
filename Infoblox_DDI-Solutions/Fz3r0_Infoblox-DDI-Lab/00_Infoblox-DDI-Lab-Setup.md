# 🔥🧱🛡️ Infoblox DDI (DNS, DHCP, IPAM): `DDI Lab - Part 1 :: Setup Lab`

![My Video](https://user-images.githubusercontent.com/94720207/165892585-b830998d-d7c5-43b4-a3ad-f71a07b9077e.gif)

### 🐦 Twitter  : [@fz3r0_OPs](https://twitter.com/Fz3r0_OPs)
### 🐱 Github  : [Fz3r0](https://github.com/fz3r0) 

---
 
#### Keywords: `Infoblox` `DDI`

---

<br>

# 📝❓📄 `Index`

- 

# ⬇️⚙️🖥️ Download and Setup Infoblox Virtual Lab

Instructions for download and setup Infoblox for first time:

## ⬇️ Download Infoblox DDI Evaluation Copy

1. ⭕ Register and wait for an e-mail with the download instructions: 

- https://info.infoblox.com/resources-evaluations-ddi-eval

![image](https://github.com/user-attachments/assets/f0ffa4b6-b295-4078-8070-52d8472e193a)

- [**Infoblox Demo Download Link**](https://www.infoblox.com/product-evaluation-portal-ddi/?mkt_tok=MjQwLVBUSy03NTEAAAGXlXkftYyoa_RSDlJjlMJbK_cf8f_56_Ry-p8QzB386ogaH7sJ-1YvXG4xcmKl1g2oLXqErF3bpJiwAbi9-cN5PCXPtNAlIW_YCM6pyk-xiU1oYBo)

2. ⭕ Select the hypervisor you want to use and download the file: VMware for the .ova, or KVM for QEMU

![image](https://github.com/user-attachments/assets/7ad5946c-2e2f-468b-8d44-e73e03238015)

3. ⭕ .ova is ready to be installed on VMware Workstation:

![image](https://github.com/user-attachments/assets/ca231586-6a27-4b0e-a9a5-87588fcf60d5)

## ⚙️ Setup Infoblox DDI in VMware Workstation

1. ⭕ Doubleclick on the .ova file to import to VMware Workstation, then select `TE-815` (This version supports DHCP, DNS, etc... TR versions are only for reporting):

![image](https://github.com/user-attachments/assets/f966023d-890e-4ecb-bbad-7de8235e130c)

2. ⭕ Click on Import:

![image](https://github.com/user-attachments/assets/24cc54a8-4179-46db-96fd-f47475115960)

3. ⭕ Run the machine and wait for the credentials prompt (`admin` : `infoblox`)

    - **You must be patient for the machine to boot!!!**. 

![image](https://github.com/user-attachments/assets/94bb2246-e97b-404a-a7e6-7f24103ae3b0)



## 🖥️ Setup Infoblox IP manually

📋 **`NOTE`**: In my case I don't need to change the IP Address, it automatically set an IP inside my subnet, but if you want to manually set an address you can follow the next steps:

![image](https://github.com/user-attachments/assets/8eca9f75-b0e7-4d15-9161-97178d079237)

1. ⭕ Select the network and IP that you want to use, for example, I will **bridge** my VMware machine (bridge uses the same network as the physical host of the VM = My PC). That mean, I can use the same subnet as my home network/gateway/LAN. You can check it with a simple `ipconfig`

![image](https://github.com/user-attachments/assets/37aba813-a04a-4288-9562-df2ac26be208)

![image](https://github.com/user-attachments/assets/31180a8b-3443-436e-bfed-f53f2dc23c5d)

|  **Subnet**  |       192.168.1.0      |
|:------------:|:----------------------:|
|   **Mask**   |      255.255.255.0     |
|    **PC**    |      192.168.1.71      |
| **Infoblox** | **`192.168.1.200/24`** |

2. ⭕ Set the network like the next example with command: `set network`

![image](https://github.com/user-attachments/assets/2a9642ed-dbe8-48ad-ade3-4874f41f6d5a)

3. ⭕ You can check again the config using the command: `show network` and `show interface`

![image](https://github.com/user-attachments/assets/6adfaf16-ecab-4e80-8070-33e6289b0bf4)


## 🖥️ Set temporary FREE licence

📋 **`NOTE`**: The licence is free for 60 days, in this case using the model `IB-V815`

1. Execute command: `set temp_licence`

2. Select `4 - Add NIOS licence`

![image](https://github.com/user-attachments/assets/7d1f8e3e-c2db-4603-8058-638a4ac15b13)

3. Select `2 - IB-V815`


# 📚🗂️🎥 Resources

- https://launchpad.education.infoblox.com/student/catalog/list?category_ids=33680-dns-dhcp-and-ipam-ddi
- https://launchpad.education.infoblox.com/student/collection/1679502-9851?sid=f71ddc86-5c52-4c0c-9803-ef455206a209&sid_i=0
- https://www.youtube.com/watch?v=uRUMAyOT_v8&list=PLByRZeLczdFu69rmOAIq--J-RqnObceIF&index=3
- https://www.youtube.com/watch?v=pqwl3CMCjF4
- https://www.youtube.com/watch?v=aSc7w81cTJg
- https://www.youtube.com/watch?v=u4832TYEeIg
  
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





