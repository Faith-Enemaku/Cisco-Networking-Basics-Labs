# Lab 4 – Examine NAT on a Wireless Router

## Objective
In this lab, I examined how NAT operates on a wireless router by distinguishing between public and private IP addresses and observing how traffic is translated as it crosses the network.

## What I Did
- Connected multiple PCs to a wireless router and enabled DHCP so each device automatically received an IP address.
- Accessed the router’s status page to examine the public IP address assigned by the ISP and the private IP addresses used on the internal network.
- Added additional PCs and verified they received private IP addresses using ipconfig /all command.
- Used Simulation mode to generate HTTP traffic from an internal PC to an external web server.
- Examined packet headers to observe how NAT translated the private source IP address to the router’s public IP address as traffic crossed the network.

## Key Learnings
- Distinguished between public and private IP addresses.
- Understood how NAT allows multiple private devices to share one public IP.
- Observed NAT translation in real time using Simulation mode.
- Gained hands-on experience analyzing packet headers.

## Screenshots
- Topology and simulation mode traffic flow ![Device connections](screenshots/topology.png)
- Ipconfig /all output from PC3 ![ipconfigall](screenshots/ipconfig-output.png)
- Packet header showing NAT translation ![NAT](screenshots/NAT-header.png)

