---
title: "Louvain Modularity"
---

# Louvain Modularity

The Louvain algorithm partitions the network by finding the partition that optimizes modularity, defined as (Barabási eq. 9.12): {{< katex >}}M = \sum_{c=1}^{n_c}\left[\frac{L_c}{L}-\left(\frac{k_c}{2L}\right)^2\right]{{< /katex >}}, where {{< katex >}}n_c{{< /katex >}} is the number of communities/partitions, {{< katex >}}L{{< /katex >}} is the total number of links in the network, {{< katex >}}L_c{{< /katex >}} is the total number of links within community {{< katex >}}C_c{{< /katex >}}, and {{< katex >}}k_c{{< /katex >}} is the total degree of the nodes in this community (including links to nodes outside community {{< katex >}}C_c{{< /katex >}}). The Louvain algorithm works in 2 steps:
- **1) Modularity optimization**: Each node in the network is assigned to its own community. Sequentially, each node, {{< katex >}}i{{< /katex >}}, is moved to the neighboring community, {{< katex >}}j{{< /katex >}}, that leads to the maximum change in modularity, {{< katex >}}\Delta M{{< /katex >}}. This is done repeadtly and sequentially until {{< katex >}}\Delta M = 0{{< /katex >}}, i.e. there is no change in modularity by moving any node to another community.  The change in modularity, when moving node {{< katex >}}i{{< /katex >}} from one community to another, is calculated as (Barabási eq 9.58);
     {{< katex display >}}    
     $$\Delta M=\left[\frac{\sum_{in}+2k_{i,in}}{2W} - \left(\frac{\sum_{tot}+k_{i}}{2W}\right)^2 \right] - \left[\frac{\sum_{in}}{2W} - \left(\frac{\sum_{tot}}{2W}\right)^2 - \left(\frac{k_{i}}{2W}\right)^2 \right] $$
     {{< /katex >}}
    where {{< katex >}}\sum_{in}{{< /katex >}} is the sum of all the weights of links inside the community, {{< katex >}}C_j{{< /katex >}}, that {{< katex >}}i{{< /katex >}} is moved into (={{< katex >}}L_{C_{j}}{{< /katex >}} in an undirected network); {{< katex >}}\sum_{tot}{{< /katex >}} is the sum of all the weights of the links to nodes in {{< katex >}}C_j{{< /katex >}}; {{< katex >}}k_i{{< /katex >}} is the weighted degree of {{< katex >}}i{{< /katex >}}; {{< katex >}}k_{i,in}{{< /katex >}} is the sum of the weights of the links between {{< katex >}}i{{< /katex >}} and other nodes in {{< katex >}}C_j{{< /katex >}}; and {{< katex >}}W{{< /katex >}} is the sum of the weights of all links in the network. If {{< katex >}}\Delta M < 0{{< /katex >}}, {{< katex >}}i{{< /katex >}} stays in its current community. 
- **2) Community Aggregation**: A weighted network is created as an aggregate of the communities from the previous step: The nodes in the weighted network are the communities from step 1, the edge weights are the sum of edges between communities, and edges within a community becomes 2 self-loops.

When the network of step 2 has been created, step 1 and 2 can be repeated on the new network until there is no increase in modularity. Collectively, the 2 steps are called a pass (Barabási Chap. 9). The 2 steps in the Louvain Algorithm are depicted below, where they are repeated for 2 passes (Barabási Image 9.37):   
<center>
<img src="/louvain.jpg" alt="drawing" style="width:750px;"/>
</center>

[Back to the community networks](/docs/Analysis/nx_characteristic/community/community/)
