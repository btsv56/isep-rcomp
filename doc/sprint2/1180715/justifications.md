**IP Attribution**

Building C has been attributed with the address block 10.165.96.0/23. This block can accommodate 512 hosts. The bigger mask would be able to connect 256 hosts, which is not enough. Since this building contains 434 nodes, this mask is more than enough. The division of this block between the different subnets has followed a pattern. The VLAN's that needed more end nodes had a block attributed first. This way we are able to reduce waste, and we make sure that there is enough space to accommodate every VLAN in this block



**Local Servers and Administration Workstation Nodes**

**VLAN 119 - 10.165.96.0/24** 

For this subnet 250 nodes are required. This address block ensures that there are 256 nodes available. 

The range is 10.165.96.1/24 to 10.165.96.254/24.



**Wi-Fi network**

**VLAN 118 - 10.165.97.0/26**

There will be 60 nodes connected to this network, and as this address block can handle 64 nodes. 

The range is 10.165.97.1/26 to 10.165.97.62/26.



**First Floor**

**VLAN 117 - 10.165.97.64/26**

In this subnet there will be 44 nodes connected, so there is needed a mask that can handle 64 nodes. 

The range is 10.165.97.65/26 to 10.165.97.126/26.



**Ground Floor**

**VLAN 116 - 10.165.97.128/26**

This network has to be able to handle 40 nodes, so the same mask as the the subnet above will be used. 

The range is 10.165.97.129/26 to 10.165.97.190/26.



**VOIP**

**VLAN 120 - 10.165.97.192/26**

There will be 40 phones connected to this network so, once again, the same mask is applied. 

The range is 10.165.97.193/26 to 10.165.97.254/26

