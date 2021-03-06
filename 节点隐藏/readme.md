# 在社区中隐藏节点

## How to Protect Ourselves From Overlapping Community Detection in Social Networks

### 亮点

- 对于重叠社团的节点隐藏，让一个节点脱离其他社团留在自己想在的社团
- 提到了社团中连边的重要程度。断开重要度大的连边使得节点与该社团联系更少。

### 方法

- BIH，先是找出节点n的全部邻居，然后计算邻居的社团重要性，断开重要性高的节点。同时还计算目标社团中节点的社团重要性，连接高的节点。
- 社团重要性：用节点与社团节点的连边/节点度。之后再除去最大值来归一化。

### 对比

- 评估：R(n)：n几点隐藏前后的社团数对比。A(n): R(n)与NMI的结合
- 用多个重叠社区划分方法对多个图进行划分，之后再A(n)评价, 横轴的变量是修改的边数。

### 不足/启发

- 如果我关注了很多个不同分区的头部大V，那我是不是就在多个社团中了？如果不是这样的话，取关重要度小的社团节点而保留对头部大V的关注会不会也能让我从该社区脱身而出？从而保持与社团最重要的联系但又在社团之外。