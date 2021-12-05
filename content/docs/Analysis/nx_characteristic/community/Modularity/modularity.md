---
title: "Louvain Modularity"
---

# Louvain Modularity

We optimize modularity based on the Louvian Partition Algorithm, which is:

{{< katex display >}}
\Delta M=\left[\frac{\sum_{in}+2k_{i,in}}{2W} - \left(\frac{\sum_{tot}+k_{i}}{2W}\right)^2 \right] - \left[\frac{\sum_{in}}{2W} - \left(\frac{\sum_{tot}}{2W}\right)^2 - \left(\frac{k_{i}}{2W}\right)^2 \right]
{{< /katex >}}

Is used to make [these networks](/docs/Analysis/nx_characteristic/community/community/)


{{< readfile file="/static/tables/community_tf.html" >}}
