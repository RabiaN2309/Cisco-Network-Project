# Cisco Network Project – VLAN Configuration with Telnet

## Project Overview
This project demonstrates the configuration of VLANs (Virtual Local Area Networks) along with Telnet remote access using Cisco Packet Tracer. VLANs are used to logically segment a network into smaller broadcast domains, improving network security, performance, and management — even when devices are connected to the same physical switch. Telnet was configured to allow **remote management** of the switch/router over the network.

##  Objective
- Create multiple VLANs on a Cisco switch
- Assign switch ports to their respective VLANs
- Configure devices (PCs) within each VLAN
- Configure Telnet (VTY lines) for remote access to network devices
- Verify VLAN connectivity, isolation between VLANs, and remote Telnet access

##  Tools Used
- Cisco Packet Tracer

## Network Topology
The network consists of:
- 1 or more Cisco Switches
- Multiple PCs/end devices
- VLANs configured to separate devices into different logical groups


##  Configuration Steps

### VLAN Interface Setup
1. Entered global configuration mode: `configure terminal`
2. Configured the VLAN 1 interface: `interface vlan 1`
3. Assigned an IP address to VLAN 1: `ip address 192.168.1.1 255.255.255.0`
4. Enabled the interface: `no shutdown`

### Telnet (VTY) Configuration
5. Entered VTY line configuration mode: `line vty 0 15` (allows up to 16 simultaneous Telnet sessions)
6. Set a Telnet password: `password telnet`
7. Enabled login using the password: `login`
8. Exited configuration mode: `exit`

### Sample CLI Commands Used

Switch1#en
Switch1#config t
Switch1(config)#int vlan 1
Switch1(config-if)#ip address 192.168.1.1 255.255.255.0
Switch1(config-if)#no shut
Switch1(config-if)#exit
Switch1(config)#line vty 0 15
Switch1(config-line)#password telnet
Switch1(config-line)#login
Switch1(config-line)#exit


##  Verification & Results
- VLAN 1 interface came up successfully (`%LINK-5-CHANGED` and `%LINEPROTO-5-UPDOWN` confirmed interface and line protocol state changed to up)
- Telnet password and login authentication configured on VTY lines 0–15
- Switch was accessible remotely via Telnet using IP `192.168.1.1` and the configured password

## Files in this Repository
- `*.pkt` — Cisco Packet Tracer project file (open with Cisco Packet Tracer software)
- Screenshots of topology and configuration output *(if added)*

## 📖 How to Open This Project
1. Download the `.pkt` file from this repository
2. Open it using **Cisco Packet Tracer** (free download from Cisco Networking Academy)
3. Explore the topology and device configurations

##  About
This project was completed as part of hands-on practice in networking fundamentals, focusing on VLAN segmentation and switch configuration.
