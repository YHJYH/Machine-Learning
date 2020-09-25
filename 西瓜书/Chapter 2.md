# Chapter 2 模型的评估与选择
## 2.1 经验误差 与 过拟合
error rate: 错误率，分类错误的样本数/样本总数<br>
accuracy: 精度=1-错误率<br>
error: 误差，实际预测输出-样本真实输出<br>
training/empirical error: 训练/经验误差，学习器在训练集上的误差<br>
generalization error: 泛化误差，学习器在新样本上的误差<br>
<br>
目标：得到generalization error小的学习器。<br>
overfitting: 过拟合，将 训练样本的自身特点 当作 潜在样本的一般性质<br>
underfitting: 欠拟合，训练样本的一般性质未习得<br>
<br>
注意：overfitting无法避免<br>
目标：缓解过拟合<br>
<br>
model selection：模型选择，最终模型=学习算法+参数配置<br>
问题：无法获得generalization error，无法直接使用training error（overfitting）<br>
How to access and select model?<br>

## 2.2 模型的评估方法
### 2.2.1 留出法
### 2.2.2 交叉验证法
### 2.2.3 自助法
### 2.2.4 调参 与 最终模型

## 2.3 性能度量
### 2.3.1 错误率 与 精度
### 2.3.2 查准率，查全率 与 F1
### 2.3.3 ROC 与 AUC
### 2.3.4 代价敏感错误率 与 代价曲线

## 2.4 比较检验
### 2.4.1 假设检验
### 2.4.2 交叉验证t检验
### 2.4.3 McNemar检验
### 2.4.4 Friedman检验 与 Nemenyi后续检验

## 2.5 偏差 与 方差






