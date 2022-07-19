# 单图的社团如何划分？

## Community detection using Local Group Assimilation

### 方法

LGA：
1.每个节点选最相似节点合并成簇
2.每个簇由簇间边密度公式选最大的簇合并
3.用模块度再进行合并

### 公式

- 簇间边密度

## A hypergraph-based framework for personalized recommendations via user

### 超图

- Hyperedge所连的两个节点是同类型的则为同质图，否则为异构图
- 超图构建：  
```` python
定义用户集向量U、项目集向量I
ei为Ui连到I的集合向量，E为ei的集合
W存放每个ei的权值,通过度值来归一
则超图Hg=(V,E,W), V=U+I
定义评分矩阵R与同维的邻接矩阵H
````