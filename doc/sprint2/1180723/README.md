# IPv4 network addresses establishment #

For the IPv4 network addresses establishment, we first distributed each element an address block for their building, making sure that the block had more than enough space for the required end nodes in each building. Then, for each building network, addresses were given to every type of end nodes existing in the building (e.g. ground floor end nodes, first floor end nodes, Wi-fi, Servers and VoIP), starting with the types of nodes in greater quantity. During this process, the team always made sure that the addresses didn't overlap with others and didn't have a lot of waste considering the number of nodes necessary per network. 

It was attributed to building D the address block 10.165.98.0/23, which has adequate space for the required 425 nodes.

The VLAN 109 deals with Local servers and administration workstations. Since it needs more end nodes than any other VLAN (250), it has the first parcel of the address block: 10.165.98.0/24 (10.165.98.1/24 - 10.165.98.254/24). This network address can hold up to 253 nodes.

VLAN 106 is related to end user outlets on the ground floor, and its network address is 10.165.99.0/26 (10.165.99.1/26 - 10.165.99.62/26). This network can accommodate 62 nodes, which is adequate for the required 40 nodes.

VLAN 107 refers to end user outlets on the first floor of the building. Its network address is 10.165.99.64/26 (10.165.99.65/26- 10.165.99.126/26). There are enough addresses to host 62 nodes, surpassing the required number of 50 nodes.

VLAN 108 handles the Wi-Fi network, with the network address 10.165.99.128/26 (10.165.99.129/26 - 10.165.99.190/26), having just enough address space (62 nodes) to meet the requirement (60 nodes). 

VLAN 110 is in charge of the VoIP addresses, whose network is 10.165.99.192/27 (10.165.99.193/27 - 10.165.99.222/27). There are 30 nodes fit for the target of 25 nodes.

# Static routing tables creation #

For the static routing tables, it works as follows: Every router connected to an intermediate cross-connect has only one route - the default route - which will send every package with a destination not belonging to the building's network to the main cross-connect. Then, the main cross-connect will analyse the package received and will have the routes to all the buildings and, of course, to the ISP. This means that the main cross-connect will have 5 routing entries, one for the ISP and other 4 for each building's router. Knowing that, we have established address blocks to each building, removing the need to write all the networks existing in the building, since, for each one of them, the address block attributed to every member is enough to make sure every package goes to the right building.