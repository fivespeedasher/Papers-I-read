# Mining Stable Communities in Temporal Networks by Density-based Clustering

## 公式与定义

1. 时序快照下两节点间的结构相似度：
2. 两节点间eps-稳定相似度：即全部时间里上个式子的值大于eps的个数。
3. (tau-eps)-连边：指的是上式个数超过tau的连边
4. 上式连边组成的邻居称为(tau-eps)-邻居
5. 结构可达：两个节点可以经过一系列的(tau-eps)-连边到达
6. (miu,tau,eps)-稳定核：1.(tau-eps)-邻居数大于等于miu。2.至少有tau个快照有同样的miu个重复出现的eps连边
7. (miu,tau,eps)-稳定社团：稳定核的基础上找出结构可达的其他节点构成网络，网路中的连通片就是社团了。

## 所提算法

1. TSCAN-B：1. 先遍历所有的节点，对它所有连边进行计算相似度，然后判断该节点是否是稳定核。2.在由所有的稳定核找结构可达节点再找出社团。缺点：第一步中每条边的稳定相似度都被大量地反复计算。  
2. TSCAN-A：1. 找出每个点的(tau-eps)-稳定邻居，若此邻居数大于miu，则把该节点加入weak core中。2. weak core中统计节点在所有时间上超过miu个稳定邻居的快照数，如果快照数不小于tau则列入strong core。3. 在strong core中统计节点在所有时间上至少有miu个同样的稳定邻居的快照数，若快照数不小于tau则称为stable core。4.找社团。  
3. TSCAN-S：把TSCAN中的strong core当成stable core来寻找社团。 

## 评价方法

1. 指标：平均的separability, density, cohesiveness and clustering coefficient
2. 对单一网络的各方法的相应时间段内各种评估指标、对各个网络的各种方法的各指标求均值。![fig8&9](fig8%269.png)
