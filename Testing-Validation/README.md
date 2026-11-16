# Testing and Validation

Use this folder to record validation against the current saved Packet Tracer file.

## Baseline verification

| Layer | Device / command | Expected check |
|---|---|---|
| Interface | Router / MLS: `show ip interface brief` | Required links up/up |
| VLAN | MLS: `show vlan brief` | Required VLANs present |
| Trunk | Switch / MLS: `show interfaces trunk` | Required VLANs allowed |
| Routing | Router / MLS: `show ip route` | Connected and static routes present |
| HSRP | Router / MLS: `show standby brief` | Correct active / standby state |
| ACL | MLS: `show access-lists`; ASA: `show access-list` | Intended rules and hit counters |

## Screenshot-supported results

- India Head Office and Madrid layouts are documented in the screenshot gallery.
- Head Office edge-router HSRP evidence shows the primary at priority 110 and Active, the backup at priority 100 and Standby, with virtual IP `200.0.0.1`.
- A failover screenshot shows the backup becoming Active after the primary router interface is shut down.
- ASA1 route output shows its private-WAN address `172.16.5.2` and routes via `172.16.5.1`.
- VLAN / ACL output and CCTV / IoT segment addressing are documented in their screenshots.
- A PC command-prompt screenshot records the India / Madrid employee endpoint addressing and a successful repeat ping to `10.2.10.21` after the initial ARP warm-up.

## Important limitations

- The captured HSRP failover verifies the router HSRP transition. It does not by itself prove every ASA, WAN and application path remains available end-to-end during all failures.
- IoT gateway and RFID / sensor addressing are documented; automated door, smoke-alarm or HVAC actions must not be claimed unless separately configured and tested.
- Some ASA diagnostic commands are not implemented in Packet Tracer.

See [the screenshot evidence register](../Screenshots/Evidence-Register.md) for the source evidence.
