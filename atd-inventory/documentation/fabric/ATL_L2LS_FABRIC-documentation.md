# ATL_L2LS_FABRIC

# Table of Contents

- [Fabric Switches and Management IP](#fabric-switches-and-management-ip)
  - [Fabric Switches with inband Management IP](#fabric-switches-with-inband-management-ip)
- [Fabric Topology](#fabric-topology)
- [Fabric IP Allocation](#fabric-ip-allocation)
  - [Fabric Point-To-Point Links](#fabric-point-to-point-links)
  - [Point-To-Point Links Node Allocation](#point-to-point-links-node-allocation)
  - [Loopback Interfaces (BGP EVPN Peering)](#loopback-interfaces-bgp-evpn-peering)
  - [Loopback0 Interfaces Node Allocation](#loopback0-interfaces-node-allocation)
  - [VTEP Loopback VXLAN Tunnel Source Interfaces (VTEPs Only)](#vtep-loopback-vxlan-tunnel-source-interfaces-vteps-only)
  - [VTEP Loopback Node allocation](#vtep-loopback-node-allocation)

# Fabric Switches and Management IP

| POD | Type | Node | Management IP | Platform | Provisioned in CloudVision |
| --- | ---- | ---- | ------------- | -------- | -------------------------- |
| ATL_L2LS_FABRIC | leaf | leaf1 | 192.168.0.21/24 | vEOS-LAB | Provisioned |
| ATL_L2LS_FABRIC | leaf | leaf2 | 192.168.0.22/24 | vEOS-LAB | Provisioned |
| ATL_L2LS_FABRIC | leaf | leaf3 | 192.168.0.23/24 | vEOS-LAB | Provisioned |
| ATL_L2LS_FABRIC | leaf | leaf4 | 192.168.0.24/24 | vEOS-LAB | Provisioned |
| ATL_L2LS_FABRIC | spine | spine1 | 192.168.0.11/24 | vEOS-LAB | Provisioned |
| ATL_L2LS_FABRIC | spine | spine2 | 192.168.0.12/24 | vEOS-LAB | Provisioned |

> Provision status is based on Ansible inventory declaration and do not represent real status from CloudVision.

## Fabric Switches with inband Management IP
| POD | Type | Node | Management IP | Inband Interface |
| --- | ---- | ---- | ------------- | ---------------- |

# Fabric Topology

| Type | Node | Node Interface | Peer Type | Peer Node | Peer Interface |
| ---- | ---- | -------------- | --------- | ----------| -------------- |
| leaf | leaf1 | Ethernet1 | mlag_peer | leaf2 | Ethernet1 |
| leaf | leaf1 | Ethernet2 | mlag_peer | leaf2 | Ethernet2 |
| leaf | leaf1 | Ethernet3 | spine | spine1 | Ethernet2 |
| leaf | leaf1 | Ethernet4 | spine | spine2 | Ethernet2 |
| leaf | leaf2 | Ethernet3 | spine | spine1 | Ethernet3 |
| leaf | leaf2 | Ethernet4 | spine | spine2 | Ethernet3 |
| leaf | leaf3 | Ethernet1 | mlag_peer | leaf4 | Ethernet1 |
| leaf | leaf3 | Ethernet2 | mlag_peer | leaf4 | Ethernet2 |
| leaf | leaf3 | Ethernet3 | spine | spine1 | Ethernet4 |
| leaf | leaf3 | Ethernet4 | spine | spine2 | Ethernet4 |
| leaf | leaf4 | Ethernet3 | spine | spine1 | Ethernet5 |
| leaf | leaf4 | Ethernet4 | spine | spine2 | Ethernet5 |
| spine | spine1 | Ethernet1 | mlag_peer | spine2 | Ethernet1 |

# Fabric IP Allocation

## Fabric Point-To-Point Links

| Uplink IPv4 Pool | Available Addresses | Assigned addresses | Assigned Address % |
| ---------------- | ------------------- | ------------------ | ------------------ |

## Point-To-Point Links Node Allocation

| Node | Node Interface | Node IP Address | Peer Node | Peer Interface | Peer IP Address |
| ---- | -------------- | --------------- | --------- | -------------- | --------------- |

## Loopback Interfaces (BGP EVPN Peering)

| Loopback Pool | Available Addresses | Assigned addresses | Assigned Address % |
| ------------- | ------------------- | ------------------ | ------------------ |

## Loopback0 Interfaces Node Allocation

| POD | Node | Loopback0 |
| --- | ---- | --------- |

## VTEP Loopback VXLAN Tunnel Source Interfaces (VTEPs Only)

| VTEP Loopback Pool | Available Addresses | Assigned addresses | Assigned Address % |
| --------------------- | ------------------- | ------------------ | ------------------ |

## VTEP Loopback Node allocation

| POD | Node | Loopback1 |
| --- | ---- | --------- |
