[<h1 align = "center">:helicopter: Bagging :running:</h1>][1]

## Bagging（Booststrap AGGregatING）

 - **基于并行策略**：基学习器之间不存在依赖关系，可同时生成
 - **基本思路**
    - 利用`自助采样法`对训练集随机采样，重复进行 T 次；
    - 基于每个采样集训练一个基学习器，并得到 T 个基学习器；
    - 预测时，集体**投票决策****
        > `自助采样法`：对 m 个样本的训练集，有放回的采样 m 次；此时，样本在 m 次采样中始终没被采样的概率约为
         0.368，即每次自助采样只能采样到全部样本的 63% 左右<br>
         ![pic1](pic/公式_20180902220459.png)
 - **特点**
    - 训练每个基学习器时只使用一部分样本；
    - 偏好`不稳定的学习器`作为基学习器；所谓`不稳定的学习器`，指的是对样本分布较为敏感的学习器。

![bagging][2]
---
[1]: http://blog.csdn.net/good_boyzq/article/details/54730004
[2]: http://img.blog.csdn.net/20170208160930513
