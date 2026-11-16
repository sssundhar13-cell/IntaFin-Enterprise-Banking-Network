# Testing and Validation

Use these checks against the current saved simulation. Record the source device, destination, command, result and screenshot.

## Baseline checks

| Layer | Device / command | Validation |
|---|---|---|
| Interface | Router / MLS: show ip interface brief | Required interfaces up/up |
| VLAN | MLS: show vlan brief | Required VLANs present |
| Trunk | Switch / MLS: show interfaces trunk | Required VLANs allowed |
| Routing | Router / MLS: show ip route | Connected and static routes present |
| HSRP | MLS0 and MLS1: show standby brief | Correct active/standby state |
| ACL | MLS / ASA: show access-lists or show access-list | Intended entries and counters |

## Recorded scenarios
- Employee VLAN communication between India and Madrid was tested in the documented scenarios.
- Selected remote server and CCTV destinations were intentionally blocked in documented tests.
- Head Office HSRP state and failover behavior were checked for the relevant multilayer-switch pair.
- Branch camera access from the designated Head Office NOC endpoint was tested against the branch camera ACL.

## Retest before submission
1. Confirm intended interfaces are up.
2. Verify each site's VLAN and gateway configuration.
3. Verify WAN next hops and static routes.
4. Check HSRP state on both members of each configured pair.
5. Run one expected-allow and one expected-deny test per security boundary.
6. Capture fresh screenshots and record observed results.

A command example is not proof that a test passed. Record only results actually observed.


## Additional evidence received (November 2026)

The following screenshots were supplied for the project evidence set. The image files are prepared for upload; the repository evidence register records their upload state.

- HSRP Active/Standby: primary router priority 110 is shown Active and backup router priority 100 is shown Standby, using virtual IP 200.0.0.1.
- HSRP Failover: the primary router GigabitEthernet0/0/0 is administratively shut down; the backup router output shows it taking the Active state.
- ASA1 private-WAN: ASA1 interface GigabitEthernet1/3 is shown as 172.16.5.2/30, with static routes pointing to 172.16.5.1.
- The remaining screenshots cover the full topology, India Head Office, Branch Office, Madrid Office, VLAN/ACL output, CCTV/IoT and an India–Madrid endpoint test.

These images are evidence of the displayed test state. Re-run the tests against the final saved Packet Tracer file before making broader high-availability claims.
