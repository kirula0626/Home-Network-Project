# Home-Network-Project
My interest lies in network security and networking, and I undertook this project to address some challenges I faced in my daily life. As a basic home internet user in the past, I relied on an ISP-provided router, which had limited functionality and belonged to the ISP. This led me to the idea of using the ISP router as an uplink while building my own customizable router with enhanced security features and advanced networking capabilities.

During my research, I explored <a href="https://openwrt.org/">OpenWrt</a>, <a href="https://www.pfsense.org/">pfSense</a>, and <a href="https://raspap.com/">RaspAP</a>. After using all three for a couple of months and engaging with their communities, I realized that OpenWrt was the best choice for my project.

As an intern at <a href="https://www.n-able.biz/">N-able Pvt Ltd</a> Sri Lanka, focusing on networking, and a CCNA candidate, I have intermediate networking knowledge. Additionally, my cybersecurity degree has provided me with a solid understanding of network security. For this project, I used a Raspberry Pi 4 running OpenWrt, initially configuring it as a travel router before transforming it into my home router and firewall.

To enhance my setup, I incorporated a Layer 2 managed switch to connect my PCs using VLANs. I configured OpenWrt in a router-on-a-stick setup, managing inter-VLAN routing and firewall functionalities. My network includes various end devices such as a NAS server, a Proxmox server, my personal laptop, and mobile devices connected via Wi-Fi.

The following screenshots demonstrate how the system is set up and functioning.
<br><br>
## Layer 2 Managed Network Switch
### Port Description 
- **Port 1 : Connects to OpenWRT router** 
- **Port 2,3,4,5,6,9 : Connects to End Devices inside the network**
- **Port 7 : Switch Management Port**
- **Port 8 : UpLink (ISP Internet)**
<br>

![image](https://github.com/user-attachments/assets/6c07d57a-c336-43f3-a4e8-bde614f2bf45)
<br><br><br>
**Vlan Configurartion**
<br>
![image](https://github.com/user-attachments/assets/4f706f6f-9b85-4163-a84e-419ec97715f7)
<br><br>
**PID Configurartion**
<br>
![image](https://github.com/user-attachments/assets/07251040-e1c6-4f7e-8a24-1ec89c126805)

## Openwrt
### User Interface
- <a href="https://openwrt.org/">OpenWrt</a> is a highly customizable Linux-based operating system primarily designed for embedded devices, such as routers. It is an open-source firmware that replaces the default firmware provided by device manufacturers, offering enhanced control, flexibility, and advanced features.

  - Key Features of OpenWrt:
    1. Customizability:

        - Allows full control over router configurations.
        - Users can add or remove packages to tailor the firmware to their needs.
    2. Advanced Networking Capabilities:

        - Supports features like VLANs, advanced QoS (Quality of Service), and dynamic DNS.
        - Provides robust firewall management and NAT (Network Address Translation) settings.
    3. Extensive Package Support:

        - Includes a package manager (opkg) to install software like VPN servers/clients, file sharing services, or monitoring tools.
    4. Performance:

        - Often improves the performance of older hardware by optimizing resource usage.
        - Enhances Wi-Fi performance and signal stability.
    5. Security:

        - Regular updates and community patches to fix vulnerabilities.
        - Strong support for encrypted VPNs, firewalls, and secure protocols.
    6. Open Source:

        - Developed by a global community of contributors, ensuring transparency and reliability.
    7. Common Use Cases:
        - Home Networks: Improve performance and add features unavailable on stock firmware.
        - Small Business Networks: Set up secure VPNs, bandwidth control, and advanced routing.
        - Specialized Applications: Deploy in IoT projects, create mesh networks, or use as a NAS server.

- This os is runing on Raspberry Pi 4 model B
- 4GB RAM and 32GB ROM
- Version : OpenWrt 23.05.5 r24106-10cc5fcd00
- Architecture : ARMv8 Processor rev 3
- Target Platform : bcm27xx/bcm2711
<br>

  - **User interface with Argon Theme**
  
![image](https://github.com/user-attachments/assets/6bd97ecb-aebc-4e0c-aaca-e97cf121d608)
  
  - **Device list with MAC address and it's DHCP IP with lease time**

![image](https://github.com/user-attachments/assets/51ce38cc-560c-44dc-b839-d05c8101098b)
  
  - **Wifi adapter and Information**
     - The inbult adapter is used for get internet from ISP via Wi-Fi if needed. This senario it is turned off
     - USb Wi-Fi adapter (Atheros Ar9271) is use to Broatcast Personal SSID and Guest SSID
         - Shows Signal strength
         - Can manualy Disconnect connected client(User)
         - Device MAC and BSSID

![image](https://github.com/user-attachments/assets/11f4db37-52ae-48dc-93a5-eb41360a5ed1) 
![image](https://github.com/user-attachments/assets/0dcda386-6f9b-41b9-adaf-4da05e608655)

  - **Interfaces and Information**
    - guestwifi
      - pkaya
    - lan
      - Hutta
    - tailscale
      - Fuck
    - wwan
      - Paka

![image](https://github.com/user-attachments/assets/4e01056a-a958-47ca-9559-a23e570e5c01) # Interfaces

![image](https://github.com/user-attachments/assets/de803872-a541-4cb2-9ff3-902c91025c8f) # Firewall Zone
![image](https://github.com/user-attachments/assets/278049af-9c30-4881-b3e4-c2f2601e31a4) # Trafic rules
![image](https://github.com/user-attachments/assets/36ec9443-8672-447c-a5cb-9cb6f7c69b1b) # Firewall port forwards
![image](https://github.com/user-attachments/assets/79ed862f-ec9b-4184-99ea-355678571615) # Routing

![image](https://github.com/user-attachments/assets/e52cc23c-059f-4e57-9f33-2831f53f5307) # Bandwith monitor

![image](https://github.com/user-attachments/assets/81d82ed1-bdf8-46f4-9dfe-a98458767460) # Guest Page






https://github.com/user-attachments/assets/22c07a88-5bde-45d0-8fc4-aced37b586d6




https://github.com/user-attachments/assets/fd2a4d1d-3bc0-450b-b91d-5d278d65466d



https://github.com/user-attachments/assets/fd81d605-90e3-4f2d-b874-4597145f6653





## Adblock Home
![image](https://github.com/user-attachments/assets/71b3f747-6f7f-48ff-b03b-9c41788fbdfc)

## NAS server
![image](https://github.com/user-attachments/assets/8a1fab87-f45d-434f-a627-f8a53b9970bd)
![image](https://github.com/user-attachments/assets/80622c9e-3e43-4a9d-a7cd-d57b8ba335ea)
![image](https://github.com/user-attachments/assets/3c941d68-7007-4bab-b725-0da592696816)
![image](https://github.com/user-attachments/assets/eff6aacc-e47f-4b65-969c-5f8f23b5ed52)
![image](https://github.com/user-attachments/assets/01b48d9f-ea02-43a0-866b-6f38c6c2ed4c)

## Proxmox server
![image](https://github.com/user-attachments/assets/82cc9c68-60c8-4c78-9b6f-4d7116dfd283)
![image](https://github.com/user-attachments/assets/b1442d08-b676-4824-9d44-fbc245897369)
![image](https://github.com/user-attachments/assets/c5997da1-7f78-490a-80f1-4e6a2590ef69)
![image](https://github.com/user-attachments/assets/0851bf2f-69bb-47e6-a682-b10848480a95)
![image](https://github.com/user-attachments/assets/3a67b750-a9bd-4943-9c62-36b172e67c05)




https://github.com/user-attachments/assets/6ddc3399-c045-4c2e-8bdd-81dcdb8468ac



















