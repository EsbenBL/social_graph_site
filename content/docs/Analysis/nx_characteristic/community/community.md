---
Title : "Communities"
---

# Community Detection

We have used [Louvain Partition](\docs\methodology\Modularity\modularity) to make communities. In the plot below, we have plotted the community size for each of the 22 detected communities. Note that this is based on the GCC;


## Community Size
As expected from the initial examination of the plotted network, most of the nodes are partitioned onto 5-8 very large communities, followed by a series of remarkably smaller communities.
The plot below shows the distribution of community size, where each community is named after the 3 most connected nodes in the given community.
<img src="/community_size.png" alt="Community Network" style="width:800px;"/>


## Community Network
The following network shows how the communities are distributed and clustered in the network;

<img src="/community_network.png" alt="Community Network" style="width:800px;"/>

## Discipline Network

We can compare the network partition from the Louvain algorithm to the partition based on the conventional 5 social science disciplines;

<img src="/gcc_network.png" alt="Field Network" style="width:800px;"/>

