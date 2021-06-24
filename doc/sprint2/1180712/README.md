# IPv4 network addresses establishment #

For the IPv4 network addresses establishment, we first attributed each element an address block for their building, making sure that the block had more than enough space for the required end nodes in each building. Then, for each building network, addresses were given to every type of end nodes existing in the building( e.g. ground floor end nodes, first floor end nodes, Wi-fi, Servers and VoIP), starting with the types of nodes in greater quantity. During this process, there was always care to make sure that the addresses didn't overlap others and didn't have a lot of waste considering the number of nodes necessary per network. 

For example, for building B, it was attributed the address block 10.165.100.0/23 which has more than enough space for the 277 nodes that exist there. Having the address block defined, the next step is to to start attributing network addresses to each of the VLAN, starting with the VLAN with most end nodes. 

In this building VLAN 102, related to Wi-fi network is the one with most end nodes (100 nodes), which means it will have the first possible IPv4 within the block of the building, 10.165.100.0/25. This network, has potential for a maximum of 126 nodes which is more than enough to handle the VLAN. 

The next VLAN to be attributed was 101 VLAN, related to end user outlets in first floor( 70 nodes). For this VLAN, the network 10.165.100.128/25 was chosen, since it has enough space(126 nodes) and it is the first one available within the address block that doesn't overlap others existing (Wi-fi network goes from 10.165.100.0 to 10.165.100.127). 

The next one to be attributed was the VLAN 100, related to ground floor outlets (60 nodes) and the process followed was the same as explained above. This means that having in consideration that network  10.165.100.128/25 goes from 10.165.100.128 to 10.165.100.255, the IPv4 for this VLAN is 10.165.101.0/26 which has a potential for 62 nodes, which is enough. 

For the VoIP VLAN (35 nodes), network 10.165.101.64/26 was given since once again has enough space to handle it (potential for 62 end nodes)  and it is the first one available after 10.165.101.0/26(10.165.101.0/26 - 10.165.101.63).

Finally, for VLAN 103, related to local server (12 nodes), the network 10.165.101.128/28 was chosen because it can have 14 nodes inside it and was first one available after 10.165.101.64/26(10.165.101.64 - 10.165.101.127).

# Static routing tables creation #

For the static routing tables, it works as follows: Every router connected to an intermediate cross-connect has only one route, the default route that will send every package that does not belong to the building to the main cross-connect. Then. the main cross-connect will analyse the package received and will have the routes to all the buildings and, of course, to the ISP. This means that the main cross-connect will have 5 routes, one for the ISP and other 4 for each building. Knowing that we have established address blocks to each building, there is no need to write all the networks existing in the building, for each one of them the address block attributed to every member is enough to make sure every package goes to the right building.

 