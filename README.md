# Azure-Secure-Web-Infrastructure

## Project Overview
The purpose of this project was to demonstrate the deployment of a public-facing web server that balances accessibility with a tight security posture. This infrastructure was manually hardened to reduce the attack surface.

**Goal:** Create a Globally Accessible Web Server (HTTP) While Making the Management Interface (SSH) Invisible.

## Security Measures Implemented

* **Network Hardening:** Replaced default "Allow All" firewall rules with granular NSG.
* **Least Privilege Access:** Restricted SSH on Port 22 to a single trusted IP address.
* **Traffic Segmentation:** Configured a VNet to isolate management traffic from public network traffic.
* **Live Monitoring:** Utilized `access.log` monitoring to track request patterns in real time and identify bot scanning activity vs regular traffic.

## Technologies Used
* **Cloud Provider:** Microsoft Azure (West US 3 Region)
* **OS:** Ubuntu 24.04 LTS (Linux)
* **Web Server:** Nginx
* **Networking:**
  * Azure VNet
  * Network Security Groups (NSG)
  * Public IP (Via Terminal)

## Project Verification

### 1. Network Architecture
**Visualizing the Hub-and-Spoke Topology:**
This diagram confirms the successful deployment of the Virtual Network (VNet) in the West US 3 region, connecting the Virtual Machine to the network interface.
![Network Topology Diagram](SS2-Topology.png)

### 2. Security Configuration (NSG)
**Implementing "Least Privilege" Access:**
The firewall rules below demonstrate traffic segmentation.
* **Rule 310 (Web):** Allows public HTTP traffic (Port 80) from `Any` source.
* **Rule 110 (SSH):** Restricts administrative SSH traffic (Port 22) strictly to my personal IP address (`99.26...`), blocking all other attempts.
![Firewall Rules](SS1-Firewall.png)

### 3. Live Deployment
**Public Web Server Access:**
Successful HTTP response from the Nginx server, verifying that the application is running and accessible via the public IP.
![Live Web Page](SS3-Webpage.png))


