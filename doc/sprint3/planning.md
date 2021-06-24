RCOMP 2019-2020 Project - Sprint 3 planning
===========================================
### Sprint master: 1180723 ###

# 1. Sprint's backlog #

| Task | Task Description |  	
|---	|---	|
| T.3.1	|  Update  the campus.pkt layer  three  Packet  Tracer  simulation  from  the previous sprint, to include the described features in this sprint for building A.	|
| T.3.2 |  Update  the campus.pkt layer  three  Packet  Tracer  simulation  from  the previous sprint, to include the described features inthis sprint for building B.	|
| T.3.3	|  Update  the campus.pkt layer  three  Packet  Tracer  simulation  from  the previous sprint, to include the described features inthis sprint for building C.  |
| T.3.4 |  Update  the campus.pkt layer  three  Packet  Tracer  simulation  from  the previous sprint, to include the described features inthis sprint for building D. Final integration of each member’s Packet Tracer simulation into  a single simulation. |

# 2. Technical decisions and coordination #
Packet tracer version: 7.3.0.0838  

OSPF area IDs, VoIP phone numbers and prefix digits schema
-----
| Group element/Building | OSPF Area ID | VoIP schema|
|---- |----- |-----|
|Bruno Ribeiro / Building A| 1 | 1... (1000 - 1999) |
|Bruno Veiga / Building B| 2 | 2... (2000 - 2999) |
|Pedro Brandão / Building C| 3 | 3... (3000 - 3999) |
|João Leal / Building D| 4 | 4... (4000 - 4999) |
|Backbone| 0 | N/A |

DNS domains and IPv4 node addresses of the DNS name server
----
|DNS domains|IPv4 address|
|----|----|
|rcomp-19-20-db-g1 (highest level)| 10.165.102.2 |
|building-B| 10.165.101.130 |
|building-C| 10.165.96.2 |
|building-D| 10.165.98.3 |

The name of the domain’s DNS name server is to be ns within that domain.

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

# 3. Subtasks assignment #

  * 1180573 - T.3.1
  * 1180712 - T.3.2
  * 1180715 - T.3.3
  * 1180723 - T.3.4

