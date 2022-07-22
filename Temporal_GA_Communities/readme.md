# 如何用自然寻优法找寻社团

---

## An Evolutionary Multiobjective Approach for Community Discovery in Dynamic Networks

这篇论文可谓是这个问题下的鼻祖文章了。

### Highlight

1. 多目标优化，考虑社团在一个快照的模块度Snapshot cost以及社团更替的平滑度Temporal cost。
2. Parameter free：社区数量、cost函数中的α参数都不用咱调。

### 所提方法

- DYNMOGA。用parent矩阵与offspring矩阵来编码表示社团，用遗传算法去优化。
- 试错找出了相对好的突变与交叉rate

### 对比

- 评估指标：NMI、Erro rate
- 在人工生成的网络（3个可变参数）上对比了FaceNet。
- 自身对比：种群数与后代数改变、对目标单目标NMI对比。

---

## A multiobjective discrete cuckoo search algorithm for community detection in dynamic networks

### Highlight

把遗传算法换成了布谷鸟算法

## Analyzing Communities and Their Evolutions in Dynamic Social Networks

### 对比
- 介绍评价指标Bach and Jordan提出的评价指标`Erro rate`,其中Z是算法得出的社团的指标（全是布尔值）矩阵，G是真实的社团指标矩阵。

## Review：Application of natural computation inspired method in community detection

### 评估方法
- 不只是NMI和Q,还有针对符号的SQ、针对重叠的EQ、针对动态网络的HQ
### 自然启发法
- 遗传算法的重要的社区划分发展：2013年一篇文章用相似度初始化、用统计的机器学习结合遗传算法进行划分。
- 免疫算法
- 智能群体：蚁群、粒子群
- 神经网络

## Improved community detection in weighted bipartite networks

|Highlight|方法|对比|展望|
|---|---|---|---|
|提出了针对二分网络的加权模块度|把二分网络邻接矩阵改成带加权的矩阵|用到了后验模块度、NMI评估|
