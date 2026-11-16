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
