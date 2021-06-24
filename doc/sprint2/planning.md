RCOMP 2019-2020 Project - Sprint 2 planning
===========================================
### Sprint master: 1180712 ###

# 1. Sprint's backlog #

| Task | Task Description |  	
|---	|---	|
| T.2.1	|  Development of a layer two and layer three Packet Tracer simulation for building A, and also encompassing the campus backbone.|
| T.2.2 |  Development of a layer two and layer three Packet Tracer simulation for building B, and also encompassing the campus backbone. Integration of every members Packet Tracer simulations into a single simulation.		|
| T.2.3	|  Development of a layer two and layer three Packet Tracer simulation for building C, and also encompassing the campus backbone.	|
| T.2.4 |  Development of a layer two and layer three Packet Tracer simulation for building D, and also encompassing the campus backbone.	|

# 2. Technical decisions and coordination #
Packet tracer version: 7.3.0.0838  
For the switch representing the main, intermediate and horizontal cross-connects the name of it should reflect that and identify the building and the floor.   
Example:  

  - Horizontal cross-connect NF, where N is the identifier of the building and F is the floor.  
  - Intermediate cross-connect N, where N is the identifier of the building.  
  - Main cross-connect  

For the switches representing the consolidation points the name should be in the following format:  
  - Consolidation point BFN, where B is the building, F is the floor and N is the order of the consolidation point in that floor.

For the remaining devices the name should clearly identify what type of device it represents and of course be numbered according to the building, floor and order.
Example:
  - Access point BFN, where B is the building, F is the floor and N is the order of the access point in that floor.  

  The vlan names should be in the following formats, where N identifies the building:  

  - outlets_ground_floor_N  

  - outlets_first_floor_N  

  - access_points_N  

  - servers_N  

  - IP-phones_N  

  - campus_backbone  

VLANID: 100-140  
VTP domain name: vtdbg1  
IPv4 address space to be used: 10.165.96.0/20  
ISP router IPv4 node address: 17.10.10.85/30

IPv4 network addresses attribution:
---------
| Group element | IPv4 address block | VLAN/Type of outlets | IPv4 network address | IPv4 end node free addresses |
|---- |----- |-----|-----|-----|
| Bruno Ribeiro - Building A: 194 nodes | 10.165.102.0/23 | 111 - End user outlets on the ground floor (40 nodes) |10.165.102.128/26 | 10.165.102.129/26- 10.165.102.190/26 |
| | | 112 - End user outlets on floor one (40 nodes) | 10.165.102.192/26 | 10.165.102.193/26 -10.165.102.254/26 |
| | | 113 - Wi-Fi network (24 nodes) | 10.165.103.0/27 | 10.165.103.1/27-10.165.103.30/27 |
| | | 114 - Local servers and administration workstations (70 nodes) | 10.165.102.0/25 | 10.165.102.1/25- 10.165.102.126/25 |
| | | 115 - VoIP (IP-phones) (20 nodes) | 10.165.103.32/27 | 10.165.103.33/27- 10.165.103.62/27 |
| Bruno Veiga - Building B:277 nodes | 10.165.100.0/23 | 100 - End user outlets on the ground floor(60 nodes) | 10.165.101.0/26 | 10.165.101.1/26-10.165.101.62/26 |
| | | 101 - End user outlets on floor one (70 nodes) | 10.165.100.128/25 | 10.165.100.129/25- 10.165.100.254/25 |
| | | 102 - Wi-Fi network (100 nodes) | 10.165.100.0/25 | 10.165.100.1/25 - 10.165.100.126/25                       |
| | | 103 - Local servers and administration workstations (12 nodes) | 10.165.101.128/28 | 10.165.101.129/28- 10.165.101.142/28 |
| | | 104 - VoIP (IP-phones) (35 nodes) | 10.165.101.64/26 | 10.165.101.65/26- 10.165.101.126/26 |
| Pedro Brandão - Building C: 434 nodes | 10.165.96.0/23 | 116 - End user outlets on the ground floor (40 nodes) | 10.165.97.128/26 | 10.165.97.129/26-                        10.165.97.190/26 |
| |  | 117 - End user outlets on floor one (44 nodes) | 10.165.97.64/26 | 10.165.97.65/26-                        10.165.97.126/26 |
| | | 118 - Wi-Fi network (60 nodes) | 10.165.97.0/26 | 10.165.97.1/26-                        10.165.97.62/26 |
| | | 119 - Local servers and administration workstations (250 nodes) | 10.165.96.0/24       | 10.165.96.1/24 -                       10.165.96.254/24 |
| | | 120 - VoIP (IP-phones) (40 nodes) | 10.165.97.192/26 | 10.165.97.193/26-                        10.165.97.254/26 |
| João Leal - Building D: 425 nodes | 10.165.98.0/23 | 106 - End user outlets on the ground floor (40 nodes) | 10.165.99.0/26 | 10.165.99.1/26- 10.165.99.62/26 |
| | | 107 - End user outlets on floor one (50 nodes) | 10.165.99.64/26 | 10.165.99.65/26- 10.165.99.126/26 |
| | | 108 - Wi-Fi network (60 nodes) | 10.165.99.128/26 | 10.165.99.129/26 - 10.165.99.190/26 |
| | | 109 - Local servers and administration workstations (250 nodes) | 10.165.98.0/24 | 10.165.98.1/24 - 10.165.98.254/24 |
| | | 110 - VoIP (IP-phones) (25 nodes) | 10.165.99.192/27 | 10.165.99.193/27- 10.165.99.222/27 |

| Type of outlets     | VLAN | IPv4 network address | Attribution                         |
| ------------------- | ---- | -------------------- | ----------------------------------- |
| Backbone: 120 nodes | 105  | 10.165.104.0/25      | Building A: 10.165.104.1/25         |
|                     |      |                      | Building B: 10.165.104.2/25         |
|                     |      |                      | Building C: 10.165.104.3/25         |
|                     |      |                      | Building D: 10.165.104.4/25         |
|                     |      |                      | Main cross-connect: 10.165.104.5/25 |

# 3. Subtasks assignment #

#### Example: ####
  * 1180573 - Development of a layer two and layer three Packet Tracer simulation for building A, and also encompassing the campus backbone  
  * 1180712 - Development of a layer two and layer three Packet Tracer simulation for building B,  and also encompassing the campus backbone. Integration of every members Packet Tracer simulations into a single simulation.
  * 1180715 - Development of a layer two and layer three Packet Tracer simulation for building C, and also encompassing the campus backbone  
  * 1180723 - Development of a layer two and layer three Packet Tracer simulation for building D, and also encompassing the campus backbone  

