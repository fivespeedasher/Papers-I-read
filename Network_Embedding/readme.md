# Network Embedding

## Network_Embedding_Based_on_Biased_Random_Walk_for_Community_Detection_in_Attributed_Networks

### 先导知识

1. GCN: 其实就是一条公式，它可以经过与k(层数)次迭代, 更新出每个节点都特征来。这像一个编码的过程，把繁杂的信息压缩成有限维度的特征。
2. GAE: 用许多同类型的网络GCN迭代得到的特征Z,作用在其他图上,根据形形色色的节点的特征的匹配以实现解码的效果。应用面是链路预测、社团划分、重要节点识别等。
3. Embedding-bese社团划分两种形式：1.学习embedding向量后再社团划分。2.合一进行（考虑社团的embedding向量）

    - embedding：就是把一个信息拆成多个特征的线性组合，比如RGB三特征表示图片。

### 社团划分的创新

1. 基于拓扑-权重度值来改善随机游走（具体？）
2. 增加attribute-node以增加节点的属性权重连边与属性矩阵（作用：替代掉之前的拉普拉斯矩阵。 意义？）

### 具体方式

## SEMI-SUPERVISED CLASSIFICATION WITH GRAPH CONVOLUTIONAL NETWORKS

### 意义

1. 针对问题：对于多信息的图提出半监督学习的处理方式

### 理解公式

1. 特征更新： $  H^{(l+1)} = \sigma  ( \widehat {D}^{-\frac {1}{2}}  \widehat {A}  \widehat {D}^{-\frac {1}{2}}  H^{(l)W} (l)) $
    - $\widehat {D}\widehat {A}\widehat {D}$中D相当于sum(A)，故此式是行与列的归一化，这样就更多地关注与节点间的关系，否则有的节点度值为1，而有的为10000，这在传递的过程中赋权就会过多地损失与放大。
