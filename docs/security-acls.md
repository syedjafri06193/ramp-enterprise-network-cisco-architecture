# Security ACLs

## Guest (VLAN 40) — Internet Only
Inbound on VLAN 40 SVI:
- Deny access to RFC1918 internal ranges (10/8, 172.16/12, 192.168/16)
- Permit all else (internet)

## Finance (VLAN 20) — Restricted East/West
Inbound on VLAN 20 SVI:
- Deny Finance → Engineering subnet (VLAN 30)
- Permit other traffic (internet + allowed internal)

## HR (VLAN 10) — Baseline
Inbound on VLAN 10 SVI:
- Permit HR → any (baseline; can be tightened to only approved services)
