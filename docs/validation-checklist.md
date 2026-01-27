# Validation Checklist

## VLAN / Trunking
- show vlan brief
- show interfaces trunk

## STP
- show spanning-tree vlan 10
- show spanning-tree vlan 20
Confirm DIST1 is root primary and DIST2 is secondary.

## HSRP
- show standby brief
Confirm correct active/standby per VLAN.

## Inter-VLAN Routing
- Ping HR ↔ Engineering (allowed by baseline)
- Ping Finance → Engineering (should fail due to ACL)

## Guest Policy
- From Guest host: ping internal 10.10.20.x (should fail)
- From Guest host: reach internet (should succeed with NAT)

## NAT (EDGE1)
- show ip nat translations
- show ip nat statistics
