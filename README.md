# Enterprise Network Lab

## Topology
Server0 → R0 → R1 → SW0/SW1 → PC0/PC1/PC2/PC3

## What I built
- Static routing between R0 and R1
- OSPF dynamic routing
- NAT/PAT — PCs share one public IP
- ACL — blocked IT from reaching Sales

## IP Plan
Server0:  8.8.8.8/24
R0 G0/0:  8.8.8.1/24  (WAN)
R0 G0/1:  10.0.0.1/30
R1 G0/0:  10.0.0.2/30
R1 G0/1:  192.168.10.1/24
PC0:      192.168.10.2/24
PC1:      192.168.10.3/24
PC2:      192.168.20.2/24
PC3:      192.168.20.3/24

## Test Results
PC0 → gateway    ✓ 0% loss
PC0 → internet   ✓ 0% loss
PC2 → PC0        ✗ blocked by ACL
NAT translations ✓ working

## Tools used
Cisco Packet Tracer
