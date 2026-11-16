# Security Architecture

## Segmentation
Department, management, server, CCTV and physical-security traffic are separated into distinct VLANs and subnets at the sites where configured.

## Firewall boundaries
ASA firewalls provide routed security boundaries between site LANs and WAN/outside networks. Static routes, NAT/PAT and access-control rules are used where configured.

## Inter-site access
The documented policy permits selected employee-network communication between India and Madrid while restricting selected server and CCTV destinations. Validate the current ACL counters and reproduce both allowed and denied tests.

## Head Office backup-side evidence
The latest ASA1 screenshot shows:
- Private-WAN interface GigabitEthernet1/3 at 172.16.5.2/30
- Static routes for the India branch and Madrid networks using 172.16.5.1 as next hop
- The Head Office edge-router HSRP screenshot shows the backup router becoming Active after the primary interface is shut down

These screenshots support the recorded backup-router HSRP transition and ASA1 private-WAN route configuration. They do not alone prove complete application-level or firewall-path failover. Validate traffic through the backup path before claiming full high availability.

## CCTV and IoT
The Head Office design includes a CCTV VLAN and a separate physical-security/IoT segment. RFID readers and wireless sensors were assigned to the IoT gateway network in the recorded design. Do not claim automated door, smoke-alarm or HVAC response unless the automation is configured and demonstrated.

## Known limitations
- End-to-end application and firewall-path continuity through the backup path still requires dedicated testing.
- Madrid local NOC/IT-to-CCTV policy requires verification before claiming monitoring access.
- Packet Tracer ASA diagnostics are limited compared with real ASA software.
