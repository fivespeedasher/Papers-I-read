# Mining Stable Communities in Temporal Networks by Density-based Clustering

## 简介

1. 采用DBSCAN（Density-Based Spatial Clustering of Applications with Noise）算法思想。即，先计算全网络连边的相似度，再通过选定的eps来过滤掉连边，从而形成社团。这个算法缺点明显：严重地依赖eps的选取。优点是：不会被噪声点干扰（比如两个密度划分出的社团之间有个点，Kmeans划分有可能就把这两社团划分到一起去了。）
2. 运用到了时序网络，在时序网络中找出稳定的社团结构。
3. 加入修剪流程来优化Temporal-SCAN-Basic的算法：全网络节点->weak core->strong core->stable core
