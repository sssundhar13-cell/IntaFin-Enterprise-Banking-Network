# VLAN and IP Addressing Reference

Confirm the current saved configuration in Packet Tracer before changing any address or interface.

## India Head Office

| VLAN | Role | Subnet | Gateway |
|---:|---|---|---|
| 10 | Accounts | 10.0.10.0/24 | 10.0.10.1 |
| 20 | Customer Service | 10.0.20.0/24 | 10.0.20.1 |
| 30 | Management | 10.0.30.0/24 | 10.0.30.1 |
| 40 | IT | 10.0.40.0/24 | 10.0.40.1 |
| 50 | NOC / Administration | 10.0.50.0/24 | 10.0.50.1 |
| 60 | Server-related | 10.0.60.0/24 | 10.0.60.1 |
| 70 | CCTV Security | 10.0.70.0/24 | 10.0.70.1 |
| 80 | Physical Security / IoT | 10.0.80.0/24 | 10.0.80.1 |
| 99 | Network Management | 10.0.99.0/24 | 10.0.99.1 |
| 100 | Server Farm | 10.0.100.0/24 | 10.0.100.1 |

## India Branch 1

| VLAN | Department | Subnet |
|---:|---|---|
| 10 | Accounts | 10.1.10.0/24 |
| 20 | Customer Service | 10.1.20.0/24 |
| 30 | Manager | 10.1.30.0/24 |
| 40 | Wi-Fi | 10.1.40.0/24 |
| 50 | CCTV | 10.1.50.0/24 |
| 99 | Management | 10.1.99.0/24 |

## Madrid Office

| VLAN | Role | Subnet | Gateway |
|---:|---|---|---|
| 10 | Accounts / Finance | 10.2.10.0/24 | 10.2.10.1 |
| 20 | Manager / Administration | 10.2.20.0/24 | 10.2.20.1 |
| 30 | NOC | 10.2.30.0/24 | 10.2.30.1 |
| 40 | IT | 10.2.40.0/24 | 10.2.40.1 |
| 50 | CCTV | 10.2.50.0/24 | 10.2.50.1 |
| 99 | Management | 10.2.99.0/24 | — |
| 100 | Server Farm | 10.2.100.0/24 | 10.2.100.1 |

## WAN point-to-point links

| Link | Subnet | Documented endpoints |
|---|---|---|
| ISP to WAN aggregation | 172.16.0.0/30 | ISP_Router 172.16.0.1; WAN_AGGREGATION_MLS 172.16.0.2 |
| Backup router to WAN aggregation | 172.16.0.4/30 | WAN_AGGREGATION_MLS 172.16.0.5; Backup_Router 172.16.0.6 |
| Branch 1 to WAN aggregation | 172.16.1.0/30 | WAN_AGGREGATION_MLS 172.16.1.1; branch router 172.16.1.2 |
| Head Office primary to WAN aggregation | 172.16.2.0/30 | WAN_AGGREGATION_MLS 172.16.2.1; primary router 172.16.2.2 |
| Head Office primary to ASA0 | 172.16.3.0/30 | primary router 172.16.3.1; ASA0 172.16.3.2 |
| WAN aggregation to Madrid edge | 172.16.4.0/30 | WAN_AGGREGATION_MLS 172.16.4.1; Madrid edge 172.16.4.2 |
| Madrid edge to Madrid ASA | 172.16.20.0/30 | Madrid edge 172.16.20.1; MADRIDASA 172.16.20.2 |

A backup-router-to-ASA1 private link was not confirmed complete in the recorded implementation. Do not assume an address for that link without inspecting the current Packet Tracer file.
