# 同群类算法对时序网络的社团结构划分

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
