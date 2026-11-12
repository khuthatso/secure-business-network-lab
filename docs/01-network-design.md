# Phase 1: Network Design

## Scenario
A small office network with separate zones for staff, servers, guests, and management.

## Why VLANs?
VLANs separate traffic on the same switch so a problem in one zone (like an infected guest device) cannot reach the others.

## VLAN and IP plan

| VLAN ID | Name | Subnet | Gateway |
|---|---|---|---|
| 10 | Staff | 192.168.10.0/24 | 192.168.10.1 |
| 20 | Servers | 192.168.20.0/24 | 192.168.20.1 |
| 30 | Guest | 192.168.30.0/24 | 192.168.30.1 |
| 99 | Management | 192.168.99.0/24 | 192.168.99.1 |

## Devices
- 1 router
- 1 switch
- 2 staff PCs
- 1 server
- 1 guest PC

## Security layers
1. Router ACLs: control traffic between internal VLANs
2. Switch: unused ports disabled and parked in an isolated VLAN
