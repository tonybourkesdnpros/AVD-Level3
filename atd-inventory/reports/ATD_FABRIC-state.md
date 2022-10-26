
# Validate State Report

**Table of Contents:**

- [Validate State Report](validate-state-report)
  - [Test Results Summary](#test-results-summary)
  - [Failed Test Results Summary](#failed-test-results-summary)
  - [All Test Results](#all-test-results)

## Test Results Summary

### Summary Totals

| Total Tests | Total Tests Passed | Total Tests Failed |
| ----------- | ------------------ | ------------------ |
| 222 | 210 | 12 |

### Summary Totals Devices Under Tests

| DUT | Total Tests | Tests Passed | Tests Failed | Categories Failed |
| --- | ----------- | ------------ | ------------ | ----------------- |
| leaf1 |  44 | 40 | 4 | MLAG, BGP, Routing Table, Loopback0 Reachability |
| leaf2 |  44 | 39 | 5 | Interface State, MLAG, BGP, Routing Table, Loopback0 Reachability |
| leaf3 |  44 | 42 | 2 | Interface State, MLAG |
| leaf4 |  44 | 43 | 1 | MLAG |
| spine1 |  23 | 23 | 0 | - |
| spine2 |  23 | 23 | 0 | - |

### Summary Totals Per Category

| Test Category | Total Tests | Tests Passed | Tests Failed |
| ------------- | ----------- | ------------ | ------------ |
| NTP |  6 | 6 | 0 |
| Interface State |  74 | 72 | 2 |
| LLDP Topology |  24 | 24 | 0 |
| MLAG |  4 | 0 | 4 |
| IP Reachability |  16 | 16 | 0 |
| BGP |  42 | 40 | 2 |
| Routing Table |  32 | 30 | 2 |
| Loopback0 Reachability |  24 | 22 | 2 |

## Failed Test Results Summary

| Test ID | Node | Test Category | Test Description | Test | Test Result | Failure Reason |
| ------- | ---- | ------------- | ---------------- | ---- | ----------- | -------------- |
| 42 | leaf2 | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel6 - host1_To_Host_1 | FAIL | Interface shutdown: False - interface status: down - line protocol status: lowerLayerDown |
| 44 | leaf3 | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel6 - host2_To_Host_2 | FAIL | Interface shutdown: False - interface status: down - line protocol status: lowerLayerDown |
| 105 | leaf1 | MLAG | MLAG State active & Status connected | MLAG | FAIL | State: inactive - negotiation_status: connecting |
| 106 | leaf2 | MLAG | MLAG State active & Status connected | MLAG | FAIL | State: inactive - negotiation_status: connecting |
| 107 | leaf3 | MLAG | MLAG State active & Status connected | MLAG | FAIL | State: inactive - negotiation_status: connecting |
| 108 | leaf4 | MLAG | MLAG State active & Status connected | MLAG | FAIL | State: inactive - negotiation_status: connecting |
| 131 | leaf1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 10.255.251.1 | FAIL | Session state Connect |
| 134 | leaf2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 10.255.251.0 | FAIL | Session state Active |
| 176 | leaf1 | Routing Table | Remote Lo0 address | 192.168.100.4 | FAIL | Lo0 192.168.100.4 is not in the routing table |
| 181 | leaf2 | Routing Table | Remote Lo0 address | 192.168.100.3 | FAIL | Lo0 192.168.100.3 is not in the routing table |
| 200 | leaf1 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf1 - 192.168.100.3 Destination: 192.168.100.4 | FAIL | 100% packet loss |
| 205 | leaf2 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf2 - 192.168.100.4 Destination: 192.168.100.3 | FAIL | 100% packet loss |

## All Test Results

| Test ID | Node | Test Category | Test Description | Test | Test Result | Failure Reason |
| ------- | ---- | ------------- | ---------------- | ---- | ----------- | -------------- |
| 1 | leaf1 | NTP | Synchronised with NTP server | NTP | PASS | - |
| 2 | leaf2 | NTP | Synchronised with NTP server | NTP | PASS | - |
| 3 | leaf3 | NTP | Synchronised with NTP server | NTP | PASS | - |
| 4 | leaf4 | NTP | Synchronised with NTP server | NTP | PASS | - |
| 5 | spine1 | NTP | Synchronised with NTP server | NTP | PASS | - |
| 6 | spine2 | NTP | Synchronised with NTP server | NTP | PASS | - |
| 7 | leaf1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet1 - MLAG_PEER_leaf2_Ethernet1 | PASS | - |
| 8 | leaf1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet2 - MLAG_PEER_leaf2_Ethernet2 | PASS | - |
| 9 | leaf1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet3 - P2P_LINK_TO_SPINE1_Ethernet2 | PASS | - |
| 10 | leaf1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet4 - P2P_LINK_TO_SPINE2_Ethernet2 | PASS | - |
| 11 | leaf1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet6 - host1_Eth1 | PASS | - |
| 12 | leaf1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet7 - host1_Eth2 | PASS | - |
| 13 | leaf2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet1 - MLAG_PEER_leaf1_Ethernet1 | PASS | - |
| 14 | leaf2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet2 - MLAG_PEER_leaf1_Ethernet2 | PASS | - |
| 15 | leaf2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet3 - P2P_LINK_TO_SPINE1_Ethernet3 | PASS | - |
| 16 | leaf2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet4 - P2P_LINK_TO_SPINE2_Ethernet3 | PASS | - |
| 17 | leaf2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet6 - host1_Eth3 | PASS | - |
| 18 | leaf2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet7 - host1_Eth4 | PASS | - |
| 19 | leaf3 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet1 - MLAG_PEER_leaf4_Ethernet1 | PASS | - |
| 20 | leaf3 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet2 - MLAG_PEER_leaf4_Ethernet2 | PASS | - |
| 21 | leaf3 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet3 - P2P_LINK_TO_SPINE1_Ethernet4 | PASS | - |
| 22 | leaf3 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet4 - P2P_LINK_TO_SPINE2_Ethernet4 | PASS | - |
| 23 | leaf3 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet6 - host2_Eth1 | PASS | - |
| 24 | leaf3 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet7 - host2_Eth2 | PASS | - |
| 25 | leaf4 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet1 - MLAG_PEER_leaf3_Ethernet1 | PASS | - |
| 26 | leaf4 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet2 - MLAG_PEER_leaf3_Ethernet2 | PASS | - |
| 27 | leaf4 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet3 - P2P_LINK_TO_SPINE1_Ethernet5 | PASS | - |
| 28 | leaf4 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet4 - P2P_LINK_TO_SPINE2_Ethernet5 | PASS | - |
| 29 | leaf4 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet6 - host2_Eth3 | PASS | - |
| 30 | leaf4 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet7 - host2_Eth4 | PASS | - |
| 31 | spine1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet2 - P2P_LINK_TO_LEAF1_Ethernet3 | PASS | - |
| 32 | spine1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet3 - P2P_LINK_TO_LEAF2_Ethernet3 | PASS | - |
| 33 | spine1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet4 - P2P_LINK_TO_LEAF3_Ethernet3 | PASS | - |
| 34 | spine1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet5 - P2P_LINK_TO_LEAF4_Ethernet3 | PASS | - |
| 35 | spine2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet2 - P2P_LINK_TO_LEAF1_Ethernet4 | PASS | - |
| 36 | spine2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet3 - P2P_LINK_TO_LEAF2_Ethernet4 | PASS | - |
| 37 | spine2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet4 - P2P_LINK_TO_LEAF3_Ethernet4 | PASS | - |
| 38 | spine2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet5 - P2P_LINK_TO_LEAF4_Ethernet4 | PASS | - |
| 39 | leaf1 | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel1 - MLAG_PEER_leaf2_Po1 | PASS | - |
| 40 | leaf1 | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel6 - host1_To_Host_1 | PASS | - |
| 41 | leaf2 | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel1 - MLAG_PEER_leaf1_Po1 | PASS | - |
| 42 | leaf2 | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel6 - host1_To_Host_1 | FAIL | Interface shutdown: False - interface status: down - line protocol status: lowerLayerDown |
| 43 | leaf3 | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel1 - MLAG_PEER_leaf4_Po1 | PASS | - |
| 44 | leaf3 | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel6 - host2_To_Host_2 | FAIL | Interface shutdown: False - interface status: down - line protocol status: lowerLayerDown |
| 45 | leaf4 | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel1 - MLAG_PEER_leaf3_Po1 | PASS | - |
| 46 | leaf4 | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel6 - host2_To_Host_2 | PASS | - |
| 47 | leaf1 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan4093 - MLAG_PEER_L3_PEERING | PASS | - |
| 48 | leaf1 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan4094 - MLAG_PEER | PASS | - |
| 49 | leaf1 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan10 - VLAN_10 | PASS | - |
| 50 | leaf1 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan20 - VLAN_20 | PASS | - |
| 51 | leaf1 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan3009 - MLAG_PEER_L3_iBGP: vrf Tenant_A_OP_Zone | PASS | - |
| 52 | leaf2 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan4093 - MLAG_PEER_L3_PEERING | PASS | - |
| 53 | leaf2 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan4094 - MLAG_PEER | PASS | - |
| 54 | leaf2 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan10 - VLAN_10 | PASS | - |
| 55 | leaf2 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan20 - VLAN_20 | PASS | - |
| 56 | leaf2 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan3009 - MLAG_PEER_L3_iBGP: vrf Tenant_A_OP_Zone | PASS | - |
| 57 | leaf3 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan4093 - MLAG_PEER_L3_PEERING | PASS | - |
| 58 | leaf3 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan4094 - MLAG_PEER | PASS | - |
| 59 | leaf3 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan10 - VLAN_10 | PASS | - |
| 60 | leaf3 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan20 - VLAN_20 | PASS | - |
| 61 | leaf3 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan3009 - MLAG_PEER_L3_iBGP: vrf Tenant_A_OP_Zone | PASS | - |
| 62 | leaf4 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan4093 - MLAG_PEER_L3_PEERING | PASS | - |
| 63 | leaf4 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan4094 - MLAG_PEER | PASS | - |
| 64 | leaf4 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan10 - VLAN_10 | PASS | - |
| 65 | leaf4 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan20 - VLAN_20 | PASS | - |
| 66 | leaf4 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan3009 - MLAG_PEER_L3_iBGP: vrf Tenant_A_OP_Zone | PASS | - |
| 67 | leaf1 | Interface State | Vxlan Interface Status & Line Protocol == "up" | Vxlan1 | PASS | - |
| 68 | leaf2 | Interface State | Vxlan Interface Status & Line Protocol == "up" | Vxlan1 | PASS | - |
| 69 | leaf3 | Interface State | Vxlan Interface Status & Line Protocol == "up" | Vxlan1 | PASS | - |
| 70 | leaf4 | Interface State | Vxlan Interface Status & Line Protocol == "up" | Vxlan1 | PASS | - |
| 71 | leaf1 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback0 - EVPN_Overlay_Peering | PASS | - |
| 72 | leaf1 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback1 - VTEP_VXLAN_Tunnel_Source | PASS | - |
| 73 | leaf2 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback0 - EVPN_Overlay_Peering | PASS | - |
| 74 | leaf2 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback1 - VTEP_VXLAN_Tunnel_Source | PASS | - |
| 75 | leaf3 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback0 - EVPN_Overlay_Peering | PASS | - |
| 76 | leaf3 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback1 - VTEP_VXLAN_Tunnel_Source | PASS | - |
| 77 | leaf4 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback0 - EVPN_Overlay_Peering | PASS | - |
| 78 | leaf4 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback1 - VTEP_VXLAN_Tunnel_Source | PASS | - |
| 79 | spine1 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback0 - EVPN_Overlay_Peering | PASS | - |
| 80 | spine2 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback0 - EVPN_Overlay_Peering | PASS | - |
| 81 | leaf1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet1 - remote: leaf2_Ethernet1 | PASS | - |
| 82 | leaf1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet2 - remote: leaf2_Ethernet2 | PASS | - |
| 83 | leaf1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet3 - remote: spine1_Ethernet2 | PASS | - |
| 84 | leaf1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet4 - remote: spine2_Ethernet2 | PASS | - |
| 85 | leaf2 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet1 - remote: leaf1_Ethernet1 | PASS | - |
| 86 | leaf2 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet2 - remote: leaf1_Ethernet2 | PASS | - |
| 87 | leaf2 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet3 - remote: spine1_Ethernet3 | PASS | - |
| 88 | leaf2 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet4 - remote: spine2_Ethernet3 | PASS | - |
| 89 | leaf3 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet1 - remote: leaf4_Ethernet1 | PASS | - |
| 90 | leaf3 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet2 - remote: leaf4_Ethernet2 | PASS | - |
| 91 | leaf3 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet3 - remote: spine1_Ethernet4 | PASS | - |
| 92 | leaf3 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet4 - remote: spine2_Ethernet4 | PASS | - |
| 93 | leaf4 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet1 - remote: leaf3_Ethernet1 | PASS | - |
| 94 | leaf4 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet2 - remote: leaf3_Ethernet2 | PASS | - |
| 95 | leaf4 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet3 - remote: spine1_Ethernet5 | PASS | - |
| 96 | leaf4 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet4 - remote: spine2_Ethernet5 | PASS | - |
| 97 | spine1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet2 - remote: leaf1_Ethernet3 | PASS | - |
| 98 | spine1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet3 - remote: leaf2_Ethernet3 | PASS | - |
| 99 | spine1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet4 - remote: leaf3_Ethernet3 | PASS | - |
| 100 | spine1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet5 - remote: leaf4_Ethernet3 | PASS | - |
| 101 | spine2 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet2 - remote: leaf1_Ethernet4 | PASS | - |
| 102 | spine2 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet3 - remote: leaf2_Ethernet4 | PASS | - |
| 103 | spine2 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet4 - remote: leaf3_Ethernet4 | PASS | - |
| 104 | spine2 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet5 - remote: leaf4_Ethernet4 | PASS | - |
| 105 | leaf1 | MLAG | MLAG State active & Status connected | MLAG | FAIL | State: inactive - negotiation_status: connecting |
| 106 | leaf2 | MLAG | MLAG State active & Status connected | MLAG | FAIL | State: inactive - negotiation_status: connecting |
| 107 | leaf3 | MLAG | MLAG State active & Status connected | MLAG | FAIL | State: inactive - negotiation_status: connecting |
| 108 | leaf4 | MLAG | MLAG State active & Status connected | MLAG | FAIL | State: inactive - negotiation_status: connecting |
| 109 | leaf1 | IP Reachability | ip reachability test p2p links | Source: leaf1_Ethernet3 - Destination: spine1_Ethernet2 | PASS | - |
| 110 | leaf1 | IP Reachability | ip reachability test p2p links | Source: leaf1_Ethernet4 - Destination: spine2_Ethernet2 | PASS | - |
| 111 | leaf2 | IP Reachability | ip reachability test p2p links | Source: leaf2_Ethernet3 - Destination: spine1_Ethernet3 | PASS | - |
| 112 | leaf2 | IP Reachability | ip reachability test p2p links | Source: leaf2_Ethernet4 - Destination: spine2_Ethernet3 | PASS | - |
| 113 | leaf3 | IP Reachability | ip reachability test p2p links | Source: leaf3_Ethernet3 - Destination: spine1_Ethernet4 | PASS | - |
| 114 | leaf3 | IP Reachability | ip reachability test p2p links | Source: leaf3_Ethernet4 - Destination: spine2_Ethernet4 | PASS | - |
| 115 | leaf4 | IP Reachability | ip reachability test p2p links | Source: leaf4_Ethernet3 - Destination: spine1_Ethernet5 | PASS | - |
| 116 | leaf4 | IP Reachability | ip reachability test p2p links | Source: leaf4_Ethernet4 - Destination: spine2_Ethernet5 | PASS | - |
| 117 | spine1 | IP Reachability | ip reachability test p2p links | Source: spine1_Ethernet2 - Destination: leaf1_Ethernet3 | PASS | - |
| 118 | spine1 | IP Reachability | ip reachability test p2p links | Source: spine1_Ethernet3 - Destination: leaf2_Ethernet3 | PASS | - |
| 119 | spine1 | IP Reachability | ip reachability test p2p links | Source: spine1_Ethernet4 - Destination: leaf3_Ethernet3 | PASS | - |
| 120 | spine1 | IP Reachability | ip reachability test p2p links | Source: spine1_Ethernet5 - Destination: leaf4_Ethernet3 | PASS | - |
| 121 | spine2 | IP Reachability | ip reachability test p2p links | Source: spine2_Ethernet2 - Destination: leaf1_Ethernet4 | PASS | - |
| 122 | spine2 | IP Reachability | ip reachability test p2p links | Source: spine2_Ethernet3 - Destination: leaf2_Ethernet4 | PASS | - |
| 123 | spine2 | IP Reachability | ip reachability test p2p links | Source: spine2_Ethernet4 - Destination: leaf3_Ethernet4 | PASS | - |
| 124 | spine2 | IP Reachability | ip reachability test p2p links | Source: spine2_Ethernet5 - Destination: leaf4_Ethernet4 | PASS | - |
| 125 | leaf1 | BGP | ArBGP is configured and operating | ArBGP | PASS | - |
| 126 | leaf2 | BGP | ArBGP is configured and operating | ArBGP | PASS | - |
| 127 | leaf3 | BGP | ArBGP is configured and operating | ArBGP | PASS | - |
| 128 | leaf4 | BGP | ArBGP is configured and operating | ArBGP | PASS | - |
| 129 | spine1 | BGP | ArBGP is configured and operating | ArBGP | PASS | - |
| 130 | spine2 | BGP | ArBGP is configured and operating | ArBGP | PASS | - |
| 131 | leaf1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 10.255.251.1 | FAIL | Session state Connect |
| 132 | leaf1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.0 | PASS | - |
| 133 | leaf1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.2 | PASS | - |
| 134 | leaf2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 10.255.251.0 | FAIL | Session state Active |
| 135 | leaf2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.4 | PASS | - |
| 136 | leaf2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.6 | PASS | - |
| 137 | leaf3 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 10.255.251.5 | PASS | - |
| 138 | leaf3 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.8 | PASS | - |
| 139 | leaf3 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.10 | PASS | - |
| 140 | leaf4 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 10.255.251.4 | PASS | - |
| 141 | leaf4 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.12 | PASS | - |
| 142 | leaf4 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.14 | PASS | - |
| 143 | spine1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.1 | PASS | - |
| 144 | spine1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.5 | PASS | - |
| 145 | spine1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.9 | PASS | - |
| 146 | spine1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.13 | PASS | - |
| 147 | spine2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.3 | PASS | - |
| 148 | spine2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.7 | PASS | - |
| 149 | spine2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.11 | PASS | - |
| 150 | spine2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.15 | PASS | - |
| 151 | leaf1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.100.11 | PASS | - |
| 152 | leaf1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.100.12 | PASS | - |
| 153 | leaf2 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.100.11 | PASS | - |
| 154 | leaf2 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.100.12 | PASS | - |
| 155 | leaf3 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.100.11 | PASS | - |
| 156 | leaf3 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.100.12 | PASS | - |
| 157 | leaf4 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.100.11 | PASS | - |
| 158 | leaf4 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.100.12 | PASS | - |
| 159 | spine1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.100.3 | PASS | - |
| 160 | spine1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.100.4 | PASS | - |
| 161 | spine1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.100.5 | PASS | - |
| 162 | spine1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.100.6 | PASS | - |
| 163 | spine2 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.100.3 | PASS | - |
| 164 | spine2 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.100.4 | PASS | - |
| 165 | spine2 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.100.5 | PASS | - |
| 166 | spine2 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.100.6 | PASS | - |
| 167 | leaf1 | Routing Table | Remote VTEP address | 192.168.101.3 | PASS | - |
| 168 | leaf1 | Routing Table | Remote VTEP address | 192.168.101.5 | PASS | - |
| 169 | leaf2 | Routing Table | Remote VTEP address | 192.168.101.3 | PASS | - |
| 170 | leaf2 | Routing Table | Remote VTEP address | 192.168.101.5 | PASS | - |
| 171 | leaf3 | Routing Table | Remote VTEP address | 192.168.101.3 | PASS | - |
| 172 | leaf3 | Routing Table | Remote VTEP address | 192.168.101.5 | PASS | - |
| 173 | leaf4 | Routing Table | Remote VTEP address | 192.168.101.3 | PASS | - |
| 174 | leaf4 | Routing Table | Remote VTEP address | 192.168.101.5 | PASS | - |
| 175 | leaf1 | Routing Table | Remote Lo0 address | 192.168.100.3 | PASS | - |
| 176 | leaf1 | Routing Table | Remote Lo0 address | 192.168.100.4 | FAIL | Lo0 192.168.100.4 is not in the routing table |
| 177 | leaf1 | Routing Table | Remote Lo0 address | 192.168.100.5 | PASS | - |
| 178 | leaf1 | Routing Table | Remote Lo0 address | 192.168.100.6 | PASS | - |
| 179 | leaf1 | Routing Table | Remote Lo0 address | 192.168.100.11 | PASS | - |
| 180 | leaf1 | Routing Table | Remote Lo0 address | 192.168.100.12 | PASS | - |
| 181 | leaf2 | Routing Table | Remote Lo0 address | 192.168.100.3 | FAIL | Lo0 192.168.100.3 is not in the routing table |
| 182 | leaf2 | Routing Table | Remote Lo0 address | 192.168.100.4 | PASS | - |
| 183 | leaf2 | Routing Table | Remote Lo0 address | 192.168.100.5 | PASS | - |
| 184 | leaf2 | Routing Table | Remote Lo0 address | 192.168.100.6 | PASS | - |
| 185 | leaf2 | Routing Table | Remote Lo0 address | 192.168.100.11 | PASS | - |
| 186 | leaf2 | Routing Table | Remote Lo0 address | 192.168.100.12 | PASS | - |
| 187 | leaf3 | Routing Table | Remote Lo0 address | 192.168.100.3 | PASS | - |
| 188 | leaf3 | Routing Table | Remote Lo0 address | 192.168.100.4 | PASS | - |
| 189 | leaf3 | Routing Table | Remote Lo0 address | 192.168.100.5 | PASS | - |
| 190 | leaf3 | Routing Table | Remote Lo0 address | 192.168.100.6 | PASS | - |
| 191 | leaf3 | Routing Table | Remote Lo0 address | 192.168.100.11 | PASS | - |
| 192 | leaf3 | Routing Table | Remote Lo0 address | 192.168.100.12 | PASS | - |
| 193 | leaf4 | Routing Table | Remote Lo0 address | 192.168.100.3 | PASS | - |
| 194 | leaf4 | Routing Table | Remote Lo0 address | 192.168.100.4 | PASS | - |
| 195 | leaf4 | Routing Table | Remote Lo0 address | 192.168.100.5 | PASS | - |
| 196 | leaf4 | Routing Table | Remote Lo0 address | 192.168.100.6 | PASS | - |
| 197 | leaf4 | Routing Table | Remote Lo0 address | 192.168.100.11 | PASS | - |
| 198 | leaf4 | Routing Table | Remote Lo0 address | 192.168.100.12 | PASS | - |
| 199 | leaf1 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf1 - 192.168.100.3 Destination: 192.168.100.3 | PASS | - |
| 200 | leaf1 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf1 - 192.168.100.3 Destination: 192.168.100.4 | FAIL | 100% packet loss |
| 201 | leaf1 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf1 - 192.168.100.3 Destination: 192.168.100.5 | PASS | - |
| 202 | leaf1 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf1 - 192.168.100.3 Destination: 192.168.100.6 | PASS | - |
| 203 | leaf1 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf1 - 192.168.100.3 Destination: 192.168.100.11 | PASS | - |
| 204 | leaf1 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf1 - 192.168.100.3 Destination: 192.168.100.12 | PASS | - |
| 205 | leaf2 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf2 - 192.168.100.4 Destination: 192.168.100.3 | FAIL | 100% packet loss |
| 206 | leaf2 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf2 - 192.168.100.4 Destination: 192.168.100.4 | PASS | - |
| 207 | leaf2 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf2 - 192.168.100.4 Destination: 192.168.100.5 | PASS | - |
| 208 | leaf2 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf2 - 192.168.100.4 Destination: 192.168.100.6 | PASS | - |
| 209 | leaf2 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf2 - 192.168.100.4 Destination: 192.168.100.11 | PASS | - |
| 210 | leaf2 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf2 - 192.168.100.4 Destination: 192.168.100.12 | PASS | - |
| 211 | leaf3 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf3 - 192.168.100.5 Destination: 192.168.100.3 | PASS | - |
| 212 | leaf3 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf3 - 192.168.100.5 Destination: 192.168.100.4 | PASS | - |
| 213 | leaf3 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf3 - 192.168.100.5 Destination: 192.168.100.5 | PASS | - |
| 214 | leaf3 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf3 - 192.168.100.5 Destination: 192.168.100.6 | PASS | - |
| 215 | leaf3 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf3 - 192.168.100.5 Destination: 192.168.100.11 | PASS | - |
| 216 | leaf3 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf3 - 192.168.100.5 Destination: 192.168.100.12 | PASS | - |
| 217 | leaf4 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf4 - 192.168.100.6 Destination: 192.168.100.3 | PASS | - |
| 218 | leaf4 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf4 - 192.168.100.6 Destination: 192.168.100.4 | PASS | - |
| 219 | leaf4 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf4 - 192.168.100.6 Destination: 192.168.100.5 | PASS | - |
| 220 | leaf4 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf4 - 192.168.100.6 Destination: 192.168.100.6 | PASS | - |
| 221 | leaf4 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf4 - 192.168.100.6 Destination: 192.168.100.11 | PASS | - |
| 222 | leaf4 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf4 - 192.168.100.6 Destination: 192.168.100.12 | PASS | - |
