# NAT / Internet Edge

## NAT
- PAT (overload) for inside VLANs to EDGE1 outside interface.
- Inside interface(s): links to DIST1 and DIST2
- Outside interface: ISP-facing

## Routing
- DIST1 + DIST2 use default routes to EDGE1.
- EDGE1 uses a default route to ISP and static routes back to campus VLANs.
