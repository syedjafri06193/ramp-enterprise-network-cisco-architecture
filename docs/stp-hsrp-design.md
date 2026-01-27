# STP + HSRP Design

## STP (Rapid-PVST)
- DIST1: root primary for VLANs 10,20,30,40,99
- DIST2: root secondary for VLANs 10,20,30,40,99
- PortFast + BPDU Guard enabled on edge access ports

## HSRP (Gateway Redundancy)
HSRP VIPs:
- VLAN 10: 10.10.10.1
- VLAN 20: 10.10.20.1
- VLAN 30: 10.10.30.1
- VLAN 40: 10.10.40.1
- VLAN 99: 10.10.99.1

Load distribution:
- DIST1 active: VLAN 10,30,99
- DIST2 active: VLAN 20,40

Tracking:
- Each distribution switch tracks its edge uplink and reduces priority if the uplink fails.
