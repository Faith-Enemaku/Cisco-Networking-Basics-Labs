# Lab 3 – Configure DHCP on a Wireless Router

## Objective
The goal of this lab was to configure a wireless router to automatically assign IP addresses to multiple devices using DHCP and to understand how changes to router IP settings affect connected clients.

## What I Did

### 1. Built the network topology
I created a simple home network by connecting three PCs to a wireless router using straight-through Ethernet cables. After the devices powered on and the link lights turned green, the network topology was ready.

### 2. Observed the default DHCP configuration
On PC0, I enabled DHCP and confirmed that the router automatically assigned an IP address.

- The default gateway was `192.168.0.1`, which is also the router’s IP address.
- I accessed the router’s web interface through a browser using the default credentials.
- From the Basic Setup page, I reviewed the default DHCP settings, including the starting IP address and available address range.

This step showed how DHCP operates by default on a home wireless router.

### 3. Changed the router’s IP address
I updated the router’s IP address from `192.168.0.1` to `192.168.5.1`.

- After saving the changes, the connection temporarily dropped, which was expected.
- I renewed the PC’s IP configuration to obtain a new address from the updated network.
- I was then able to reconnect to the router using the new IP address.

This demonstrated how changing a router’s IP impacts all connected devices.

### 4. Modified the DHCP address range
With the router operating on the new network, I adjusted the DHCP settings:

- Changed the DHCP starting IP address to `192.168.5.126`
- Increased the maximum number of DHCP users to `75`

After renewing the IP configuration, PC0 received an address within the updated DHCP range, confirming the changes were applied successfully.

### 5. Enabled DHCP on the remaining PCs
I enabled DHCP on PC1 and PC2.

- Each PC automatically received an IP address within the `192.168.5.0/24` network.
- This confirmed that the router was assigning unique IP addresses to multiple clients.

### 6. Verified network connectivity
To confirm the network was functioning correctly:

- I used `ipconfig` to verify IP address assignments
- I successfully pinged the router at `192.168.5.1`
- I successfully pinged PC1 from another PC

All tests confirmed proper DHCP configuration and network connectivity.

## Key Learnings
- Configured DHCP on a wireless router
- Observed how router IP changes affect connected clients
- Learned how DHCP assigns addresses within a defined range
- Verified connectivity using `ipconfig` and `ping`

## Screenshots
- Topology ![Device connections](screenshots/Topology.png)
- DHCP Enabled Router ![Router GUI setup](screenshots/DHCP-router.png)
- IP-Addressing in PC0 ![Wireless network configuration](screenshots/IP-address.png)
- Ping Results ![Laptop connected](screenshots/Ping-results.png)
