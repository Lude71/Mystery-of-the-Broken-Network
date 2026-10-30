# Networking Mastery Lab Series

## Lab 1: The Mystery of the Broken Network

### Project Overview

This project demonstrates practical network troubleshooting using Cisco Packet Tracer. I built a small enterprise network and investigated connectivity problems involving end devices, switching, VLANs, cabling, and router interfaces.

The objective was to identify faults systematically, repair the configurations, and verify connectivity using ICMP ping tests and Cisco IOS commands.

### Tools Used

- Cisco Packet Tracer
- Cisco 2911 Router
- Cisco 2960 Switches
- End devices and IPv4 configuration
- Cisco IOS CLI
- ICMP ping testing

### Network Topology

The lab contains two networks connected through router R1:

- **Administration:** `192.168.10.0/24`
- **Engineering:** `192.168.20.0/24`

R1 routes traffic between the two networks.

### IP Addressing Plan

| Device | IPv4 Address | Subnet Mask | Default Gateway |
|---|---|---|---|
| R1 G0/0 | 192.168.10.1 | 255.255.255.0 | Not applicable |
| R1 G0/1 | 192.168.20.1 | 255.255.255.0 | Not applicable |
| PC-A1 | 192.168.10.10 | 255.255.255.0 | 192.168.10.1 |
| PC-A2 | 192.168.10.11 | 255.255.255.0 | 192.168.10.1 |
| PC-E1 | 192.168.20.10 | 255.255.255.0 | 192.168.20.1 |
| PC-E2 | 192.168.20.11 | 255.255.255.0 | 192.168.20.1 |

### Troubleshooting Scenarios

The lab investigated ten scenarios:

1. Incorrect default gateway
2. Router interface administratively shut down
3. Incorrect PC IP address
4. Incorrect subnet mask
5. Disconnected Ethernet cable
6. Disabled switch port
7. Incorrect VLAN assignment
8. Access-port configuration investigation
9. Missing default gateway
10. Incorrect router interface IP address

For each scenario, I observed connectivity, examined the relevant configuration, applied a repair where necessary, and tested again.

### Verification and Results

The final tests from PC-E2 confirmed connectivity to:

- Engineering gateway: `192.168.20.1`
- Engineering PC: `192.168.20.10`
- Administration PC: `192.168.10.10`

The final cross-subnet test to PC-A1 received four replies out of four packets, with 0% packet loss.

The router interface addresses were restored to the correct subnets, and the final connectivity checks succeeded.

### Key Skills Practised

- IPv4 addressing and subnet masks
- Default gateway troubleshooting
- Router interface configuration
- Switch port administration
- VLAN membership verification
- Ethernet connectivity troubleshooting
- Cisco IOS command-line operation
- ICMP ping testing
- Structured fault diagnosis and verification

### Project Files

- `Packet-Tracer/` — Packet Tracer simulation
- `Screenshots/` — Evidence of topology, configurations, and tests
- `Documentation/` — Troubleshooting notes and reports

### Learning Outcome

This project strengthened my understanding of how endpoint configuration, switching, and routing work together. It also reinforced the importance of testing local connectivity separately from cross-subnet connectivity when diagnosing network faults.