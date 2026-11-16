# Network Design

This section documents the logical architecture, site roles and design principles of the IntaFin banking network simulation.

## Sites
- India Head Office
- India Sub-Branch 1
- India Sub-Branch 2 (verify implementation in the current saved simulation)
- Madrid Office, Spain

## Architecture
- WAN aggregation through a multilayer switch
- Site edge routers and ASA firewalls
- Multilayer switches for inter-VLAN routing
- Access switches for endpoint connectivity
- VLAN-based department and security segmentation
- HSRP for selected gateway redundancy
- Static routing between site networks
- DHCP services and helper addressing where configured

See VLAN-and-IP-Addressing-Plan.md for the documented subnet reference.
