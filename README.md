## 🚀 Lab Architecture

[//]: # (This is where you would put a diagram. If you don't have one, you can create a simple one with draw.io or even ASCII art.)
![Lab Architecture Diagram](https://github.com/MonsterDropz/Enterprise-homelab-/blob/main/461D1FF4-F7F6-4A47-B7CA-C3AF6FC92C05%20(1).png)



## ⚙️ Technologies Used

- **Virtualization:** Proxmox VE
- **Identity & Access:** Windows Server 2022, Active Directory Domain Services
- **Networking & Security:** pfSense Firewall, VLANs
- **Monitoring & Observability:** Zabbix Server & Agents
- **Clients:** Windows 10/11

## 📂 Project Phases

### Phase 1: ProxmVE Virtualization Foundation
- Installed Proxmox VE on a dedicated server.
- Configured network settings with a static IP.

### Phase 2: Active Directory Domain Services
- Deployed a Windows Server 2022 VM.
- Promoted the server to a Domain Controller for the `home.lab` forest.
- Configured DHCP scope on the DC.
- Created a Windows 10/11 client VM and joined it to the domain.

### Phase 3: Network Segmentation with pfSense
- Deployed a pfSense VM as the core network router/firewall.
- Configured LAN interface (`10.0.0.1/24`) and enabled DHCP.
- Created VLANs (e.g., VLAN 10 for servers) for network segmentation.
- Configured firewall rules to control inter-VLAN traffic.

### Phase 4: Monitoring with Zabbix
- Deployed an Ubuntu Server VM.
- Installed and configured Zabbix Server (via official apt repos).
- Installed Zabbix Agent 2 on the Windows Domain Controller.
- Configured hosts and templates in the Zabbix frontend to monitor server health.

## 🧪 Skills Demonstrated

- Server Virtualization & Management
- Microsoft Active Directory Deployment and Management (DHCP, Users, GPO)
- Network Security, Firewalling, and VLAN Segmentation
- System Monitoring and Alerting
- Linux and Windows Server Administration
- Troubleshooting and Problem-Solving

## 📁 Repository Contents

- `/docs`: Detailed notes on installation and configuration for each phase.
- `/images`: Diagram of the lab environment.

---
*This lab was built on physical hardware: [CyberpowerPC], [16GB DDRS 6000MHz RAM], [Storage].*
