# Configuration and CLI Reference

These are verification command examples for the Packet Tracer devices. Run them on the named device and check model support before use.

## Multilayer switches
Targets: MLS0, MLS1, WAN_AGGREGATION_MLS, MADRID_MLS

    enable
    show ip interface brief
    show vlan brief
    show interfaces trunk
    show ip route
    show access-lists
    show standby brief

## Routers
Targets: INDIA_HEAD_OFFICE_PRIMARY_ROUTER, Backup_Router, IND_Sub_Branch_1_Router, MADRID_EDGE_ROUTER

    enable
    show ip interface brief
    show ip route
    show arp
    show running-config
    show standby brief

## ASA firewalls
Targets: ASA0, IND_Sub_Branch_1_ASA, MADRIDASA

    enable
    show interface ip brief
    show route
    show access-list
    show running-config

## Safety notes

- These are primarily verification commands, not a complete replacement configuration.
- Confirm the device, interface and current running configuration before making changes.
- Back up the known-good configuration before editing.
- Some ASA diagnostics available on physical appliances are not implemented in Packet Tracer.
