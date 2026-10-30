# Lab 1: Network Troubleshooting Report

## 1. Introduction

This report documents the troubleshooting activities performed in Cisco Packet Tracer during the Mystery of the Broken Network lab.

The objective was to identify common network faults, understand their impact on connectivity, apply appropriate corrective configurations, and verify network recovery.

## 2. Network Environment

- Router: Cisco 2911
- Switches: Cisco 2960
- End devices: Four PCs
- Administration network: 192.168.10.0/24
- Engineering network: 192.168.20.0/24

## 3. Troubleshooting Activities

| No. | Fault investigated | Observation and outcome |
|---|---|---|
| 1 | Incorrect default gateway | Cross-subnet connectivity failed; restoring the correct gateway resolved the issue. |
| 2 | Router interface shut down | Engineering connectivity was interrupted; enabling the interface restored communication. |
| 3 | Incorrect PC IP address | Incorrect addressing disrupted communication; restoring the correct IP resolved it. |
| 4 | Incorrect subnet mask | Investigated the effects of an incorrect mask and verified connectivity after restoring the correct mask. |
| 5 | Disconnected Ethernet cable | Physical disconnection interrupted communication; reconnecting the cable restored it. |
| 6 | Disabled switch port | The affected PC lost connectivity; enabling the correct switch port restored it. |
| 7 | Incorrect VLAN assignment | VLAN mismatch isolated the PC; restoring VLAN 1 resolved the issue. |
| 8 | Access-port configuration | Inspected access-port and trunk settings. The test did not produce a confirmed connectivity outage. |
| 9 | Missing default gateway | Local communication worked, but cross-subnet communication failed. Restoring the gateway resolved the issue. |
| 10 | Incorrect router interface IP | Engineering-local communication worked, but cross-subnet communication failed. Restoring the router interface IP resolved the issue. |

## 4. Final Verification

After repairing the faults, connectivity was tested from PC-E2.

The final tests confirmed:

- Gateway 192.168.20.1: 4 packets received, 0% loss.
- Engineering PC 192.168.20.10: 4 packets received, 0% loss.
- Administration PC 192.168.10.10: 4 packets received, 0% loss.

The router's GigabitEthernet0/0 and GigabitEthernet0/1 interfaces were also verified as operational.

## 5. Skills Demonstrated

- IPv4 addressing and subnet masks
- Default gateway configuration
- Router interface troubleshooting
- Switch port administration
- VLAN configuration and verification
- Physical connectivity troubleshooting
- Cisco IOS CLI commands
- ICMP connectivity testing
- Systematic fault diagnosis

## 6. Conclusion

This lab provided practical experience in identifying and resolving common network connectivity problems. It reinforced the importance of examining physical connections, endpoint configurations, switching settings, and router interfaces systematically.

The exercise also demonstrated that successful local communication does not necessarily mean that communication between different networks is working.
