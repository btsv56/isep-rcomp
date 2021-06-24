RCOMP 2019-2020 Project - Sprint 2 - Member 1180573 folder
===========================================
#### IPv4 network addresses establishment ####

For building A was given this block address: **10.165.102.0/23**  

This reason behind this is that although the total number of nodes is less than 256, if we add all the blocks needed to serve each network in the building, this value exceeds 256, requiring a smaller mask, that's of 23 (512 nodes). Calculations:

- End user outlets on the ground floor : 40 nodes

- End user outlets on floor one : 40 nodes

- Wi-Fi network : 24 nodes

-  Local servers and administration workstations : 70 nodes

- VoIP : 20 nodes

  
  $$
  Total: 40 + 40 + 24 + 70 + 20 = 194
  $$
  

As we can see the total number of nodes need doesn't surpass the 24 bit mask, but we are ignoring the fact that inside this block there are 4 well defined networks, that is, for each network there will be losses. To prevent this we have to calculate first how much nodes we will use for each smaller network to choose the appropriate mask for the whole building network.

So for the **Ground Floor Network** we need **40 nodes** and the least available mask to fulfill this is the mask of /26, witch has **64 nodes**.

For the **First Floor Network** is the same, it is needed **40 nodes** and the least available mask to fulfill this is the mask of /26, witch has **64 nodes**.

For the **Wi-Fi Network** we need ***24* nodes**, and the least available mask to fulfill this is the mask of /27, witch has **32 nodes**.

For the **DMZ Network** we need **70 nodes**, and the least available mask to fulfill this is the mask of /25, witch has **128 nodes**.

And for the **VoIP Network** we need **20 nodes**,  and the least available mask to fulfill this is the mask of /27, witch has **32 nodes**.

Now if we add this all we get:
$$
64 + 64 + 32 + 128 + 32 = 320
$$
If we gonna need 320 nodes for all the networks inside the building, the building will need an IP address block size of 512, with the prefix-length of /23.



#### Static routing tables creation

For the static routing table we simplified it the most using the least *IP* addresses for each router.

So each cross-connect has a router and the one who is obligated to know each of the router is the **Main Cross-Connect**. For this reason we believe that the obligation to redirect packages to each building is the responsibility of **Main Cross-Connect**. Hence the way we built the routing tables was as follows:

- For each router in each building there is only the **default-route**, this is because if the packet has an address destination outside the building it automatically sends it to the **Main Cross-Connect** so that it decides what to do.
- In the case of **Main Cross-Connect**, there is already a larger list, containing the networks of **each** building and the default-route that is connected to the *ISP*, sending any unknown packet to the Internet.



