# Implementation Overview

## Objective
Design and simulate a multi-site banking network that separates business departments, routes traffic between sites, applies firewall and access-control policies, and includes CCTV and IoT physical-security segments.

## Sites
- India Head Office
- India Sub-Branch 1
- India Sub-Branch 2 (verify implementation in the saved simulation)
- Madrid Office, Spain

## Architecture building blocks
- Routed WAN aggregation using a multilayer switch
- Site edge routers and ASA firewalls
- Multilayer switches for inter-VLAN routing
- Access switches for endpoint connectivity
- VLAN-based department and security segmentation
- HSRP for selected default-gateway and edge-router redundancy
- Static routes between site networks
- DHCP services and helper addressing where configured

## Recent evidence update
- Head Office router screenshot evidence shows the primary ISR4331 at HSRP priority 110 / Active and the backup ISR4331 at priority 100 / Standby, using virtual IP 200.0.0.1.
- The failover screenshot records the backup router becoming Active after the primary router interface is shut down.
- ASA1 screenshot evidence shows GigabitEthernet1/3 configured as private-WAN at 172.16.5.2/30, with routes via 172.16.5.1.

## Implementation boundary
This is a Packet Tracer simulation. The captured HSRP transition and ASA1 private-WAN route configuration are evidence of those specific states. They do not prove every application flow or every firewall path remains available during every failure. Run end-to-end traffic tests through the backup path before claiming full site-level high availability.

IoT endpoints and RFID readers are addressed in the physical-security design. Do not claim automated door, smoke-alarm or HVAC response unless the automation is configured and demonstrated.
