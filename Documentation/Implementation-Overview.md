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
- HSRP for selected default-gateway redundancy
- Static routes between site networks
- DHCP services and helper addressing where configured

## Implementation boundary
This is a Packet Tracer simulation. The asymmetric backup private-WAN path and unverified IoT automation are recorded as limitations, not complete high availability or fully automated physical security.
