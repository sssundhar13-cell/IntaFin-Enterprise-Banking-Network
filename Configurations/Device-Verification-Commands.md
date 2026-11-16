# Device Verification Commands

These command groups are for checking the currently saved configuration. They are not a blanket configuration script. Start in privileged EXEC mode unless noted otherwise.

## India Head Office — multilayer switch pair

**Targets:** `MLS0`, `MLS1`

```cisco
enable
show ip interface brief
show vlan brief
show interfaces trunk
show ip route
show standby brief
show access-lists
```

Use both switches to compare SVI state and HSRP Active / Standby roles.

## India Head Office — edge routers

**Targets:** `INDIA_HEAD_OFFICE_PRIMARY_ROUTER`, `INDIA_HEAD_OFFICE_BACKUP_ROUTER`

```cisco
enable
show ip interface brief
show ip route
show standby brief
show arp
show running-config
```

The screenshot evidence records HSRP group 1 on `GigabitEthernet0/0/0`, virtual IP `200.0.0.1`, primary priority 110 and backup priority 100.

## WAN aggregation

**Target:** `WAN_AGGREGATION_MLS`

```cisco
enable
show ip interface brief
show ip route
show cdp neighbors
show interfaces status
```

Check routed /30 links and the expected next-hop routes. Verify each next hop is reachable before changing static routes.

## India Branch 1

**Targets:** `IND_Sub_Branch_1_Router`, `IND_Sub_Branch_1_ASA`, `IND_Sub_Branch_1_MLS`, `IND_Sub_Branch_1_Switch`

Multilayer switch / access switch checks:

```cisco
enable
show ip interface brief
show vlan brief
show interfaces trunk
show ip route
show access-lists
```

Router checks:

```cisco
enable
show ip interface brief
show ip route
show arp
```

ASA checks:

```cisco
enable
show interface ip brief
show route
show access-list
```

## Madrid Office

**Targets:** `MADRID_EDGE_ROUTER`, `MADRIDASA`, `MADRID_MLS`

Multilayer switch:

```cisco
enable
show ip interface brief
show vlan brief
show ip route
show access-lists
```

Edge router:

```cisco
enable
show ip interface brief
show ip route
show arp
```

ASA:

```cisco
enable
show interface ip brief
show route
show access-list
```

## Head Office ASA firewalls

**Targets:** `ASA0`, `ASA1`

```cisco
enable
show interface ip brief
show route
show access-list
show running-config
```

ASA command support in Packet Tracer is narrower than real ASA software. If a diagnostic command is rejected by the simulator, do not assume the device configuration is faulty; use supported interface, route and ACL output.

## NOC access switch

**Target:** `Noc_Dept_Switch4`

```cisco
enable
show vlan brief
show interfaces trunk
show spanning-tree
show mac address-table
```

## Endpoint checks

From a Packet Tracer PC command prompt:

```text
ipconfig
ping <destination-ip>
```

Use the documented source and destination addresses for each test. A successful ping proves only that specific path at that time.
