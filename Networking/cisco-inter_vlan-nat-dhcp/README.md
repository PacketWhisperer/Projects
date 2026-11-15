# Cisco VLAN, Inter-VLAN Routing, DHCP, NAT/PAT & ACL Lab

## Project Overview

This project demonstrates the configuration of a small enterprise network using Cisco devices in Cisco Packet Tracer.

The network is segmented into multiple VLANs, with inter-VLAN communication handled by Router-on-a-Stick. A centralized DHCP server provides IP addressing to all VLANs using DHCP Relay.

The network also includes static routing, NAT/PAT for external connectivity, and Extended ACLs to control traffic between network segments.

## Network Topology
/topology.png

The topology consists of:
- R1 – Main router
- R2 – ISP simulation router
- SW1 – Layer 2 switch
- Three VLANs (USERS, SALES, IT)
- Centralized DHCP Server
- External HTTP Server

## Technologies and Features

- VLAN configuration and segmentation
- IEEE 802.1Q trunking
- Router-on-a-Stick
- Inter-VLAN Routing
- DHCP Server and DHCP Relay
- Static Routing
- NAT/PAT (Port Address Translation)
- Extended Access Control Lists (ACL)
- Network connectivity testing and troubleshooting

## IP Addressing

| VLAN / Network | Network Address | Default Gateway |

| VLAN 10 – USERS | 192.168.10.0/24 | 192.168.10.1 |
| VLAN 20 – SALES | 192.168.20.0/24 | 192.168.20.1 |
| VLAN 30 – IT | 192.168.30.0/24 | 192.168.30.1 |
| R1 – R2 Link | 203.0.113.0/30 | - |
| External Network | 198.51.100.0/24 | 198.51.100.1 |

### DHCP Configuration

A centralized DHCP server (192.168.10.10) provides IP addresses to all three VLANs.

| DHCP Pool | Address Range | Default Gateway |

| USERS | 192.168.10.100–199 | 192.168.10.1 |
| SALES | 192.168.20.100–199 | 192.168.20.1 |
| IT | 192.168.30.100–199 | 192.168.30.1 |

DHCP Relay is configured on VLAN 20 and VLAN 30 subinterfaces to forward DHCP requests to the centralized server.

## Security and Traffic Control

An Extended ACL named `BLOCK_IT` is configured on R1.

The ACL restricts traffic initiated from VLAN 10 and VLAN 20 towards VLAN 30, while allowing other traffic and explicitly permitting ICMP Echo Replies required for connectivity initiated from VLAN 30.

## NAT/PAT

NAT Overload (PAT) is configured on R1 to allow devices from all internal VLANs to access the external network using a single WAN interface IP address.

## Routing

Static routing is used between the internal network and the simulated ISP network.

## Testing and Verification

The following functionality was tested:
- DHCP address assignment in all VLANs
- Inter-VLAN connectivity
- DHCP Relay operation
- Connectivity to the external HTTP server
- NAT/PAT translations
- ACL traffic filtering between VLANs

All implemented features were successfully tested in Cisco Packet Tracer.

## Repository Structure

- `topology.png` – Network diagram and Packet Tracer project
- `\configs` – Device configuration files
- `\tests` – test results
