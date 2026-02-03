# Azure-Secure-Web-Infrastructure-
## Project Overview 
The purpose of this project was to demonstrate the deployment of a public-facing web server that balances accessiblity with a tight security posture. This infrastructure 
was manually hardened to reduce the attack surface. 
****************************************************************************************************************************************************************************************
Goal: Create a Globally Accessible Web Server (HTTP) While Making the Management Interface (SSH) Invisible 
## Security Measures Implemented

* **Network Hardening:** 

-Replaced default "Allow All" firewall rules with granular NSG
* **Least Privelege Access::**

-Restricted SSH on Port 22 to a single trusted IP address
* **Traffice Segmentation:**

-Configured a VNET to isolate management traffic from public network traffic
* **Live Monitoring:**

-Utilized `access.log` monitoring to track request patterns in real time
-Identify bot scanning actvity vs regular traffic

## Technologies Used
* **Cloud Provider:**
-Microsoft Azure (West US 3 Region)
* **OS:** Ubuntu 24.04 LTS (Linux)
* **Web Server:**
-Nginx
* **Networking:**
- Azure VNet
- Network Security Groups (NSG)
- Public IP (Via Terminal)


