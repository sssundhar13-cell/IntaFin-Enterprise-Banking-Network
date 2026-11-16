# Security Architecture

## Segmentation
Department, management, server, CCTV and physical-security traffic are separated into distinct VLANs and subnets at the sites where configured.

## Firewall boundaries
ASA firewalls provide routed security boundaries between site LANs and WAN/outside networks. Static routes, NAT/PAT and access-control rules are used where configured.

## Inter-site access
The documented policy permits selected employee-network communication between India and Madrid while restricting selected server and CCTV destinations. Validate the current ACL counters and reproduce both allowed and denied tests.

## CCTV and IoT
The Head Office design includes a CCTV VLAN and a separate physical-security/IoT segment. RFID readers and wireless sensors were assigned to the IoT gateway network in the recorded design. Do not claim automated door, smoke-alarm or HVAC response unless the automation is configured and demonstrated.

## Known limitations
- The Head Office backup-router/firewall private-WAN design was asymmetric in the recorded configuration.
- Madrid local NOC/IT-to-CCTV policy requires verification before claiming monitoring access.
- Packet Tracer ASA diagnostics are limited compared with real ASA software.
