# Chapter 2 模型的评估与选择
## 2.1 经验误差 与 过拟合
    error rate: 错误率，分类错误的样本数/样本总数
    accuracy: 精度=1-错误率
    error: 误差，实际预测输出-样本真实输出
    training/empirical error: 训练/经验误差，学习器在训练集上的误差
    generalization error: 泛化误差，学习器在新样本上的误差
目标：得到generalization error小的学习器。<br>

    overfitting: 过拟合，将 训练样本的自身特点 当作 潜在样本的一般性质
    underfitting: 欠拟合，训练样本的一般性质未习得
注意：overfitting无法避免<br>
目标：缓解过拟合<br>
 
    model selection：模型选择，最终模型=学习算法+参数配置
问题：无法获得generalization error，无法直接使用training error（overfitting）<br>
**How to access and select model?**<br>
>补充:<br>
P问题：可以算出答案的问题<br>
NP问题：可以验证答案正确性的问题<br>
NP完全问题：一个问题A如果被称为NP完全问题，则符合以下两条件：第一，A属于NP问题；第二，所有问题可以通过解决A问题得到解决<br>
NP难问题：满足NP完全问题第二个条件，但不满足第一个条件的问题<br>

## 2.2 模型的评估方法（data set的划分）
>本节目录
>1. 留出法<br>
>2. 交叉验证法<br>
>3. 自助法<br>
>4. 调参 与 最终模型<br>

        testing set: 测试集，测试学习器对新样本的判别能力
        testing error：测试误差，作为泛化误差的近似
    
### 2.2.1 留出法（hold-out）
hold-out: 将数据集D划分为两个互斥的集合：训练集S和测试集T<br>
即，D=S∪T，S∩T=0<br>
<br>
注意：<br>
1. S和T的划分要尽可能保证数据分布的一致性，即保持样本的类别比例相似（stratified sampling分层采样）；<br>
2. 采用若干次随机划分+重复进行试验评估后取平均值作为hold-out的评估结果.<br>
<br>

>Q：若S大，则T小，模型更接近于D但评估结果不stable；若T大S小，模型与D差异更大，降低了模型的fidelity（保真度）.<br>
>A：S:T = 2:1或者4:1<br>

### 2.2.2 交叉验证法（k-fold cross validation）
cross validation: 将D划分为k个大小相等的互斥子集，每个子集通过stratified sampling得到（保持数据分布一致性）；每次使用k-1个子集的并集作为训练集，剩下的作为测试集；最终返回k个测试结果的均值.<br>
即，D=D1∪D2∪...∪Dk, Di∩Dj=0<br>
<br>
评估结果的**稳定性**和**保真度**取决于k<br>
k常用值：5，10，20<br>
<br>
>特殊情况:k=D中的样本数量<br>
>Leave-One-Out(LOO): 留一法<br>
>优点：更为准确的评估结果<br>
>缺点: 数据量大的时候费时费力<br>

### 2.2.3 自助法（bootstrapping）
bootstrapping: 以bootstrap sampling（自助采样法）为基础：每次从包含m个样本的数据集D中抽取一个样本放入新数据集D'再将其放回，重复m次，则最终有包含m个样本是数据集D'.<br>
样本在m次采样中始终不被采到的概率是（1- 1/m）^m, 取极限m to infinity得0.368.<br>
将D'作为S，D-D'作为T<br>
out-of-bag estimate: 包外估计，由此产生的测试结果<br>
<br>
>适用于数据集较小，难以有效划分S和T的时候；<br>
>优点：same size，适用于集成学习<br>
>缺点：D'改变了初始数据的分布，由此引入估计偏差<br>

### 2.2.4 调参 与 最终模型
    parameter: 参数，学习算法中的参数配置将影响最终的学得模型
    parameter tuning：调参
    validation set：验证集，基于验证集上的性能来进行模型选择和调参,用于评估测试的数据集
    
调参的问题：参数数量多，单个参数取值多；<br>
解决方法：对每个参数选择范围和变化步长<br>

最终模型：使用完整数据集D重新训练模型<br>

## 2.3 性能度量（performance measure）
>本节目录<br>
>1. 错误率 与 精度<br>
>2. 查准率，查全率 与 F1<br>
>3. ROC 与 AUC<br>
>4. 代价敏感错误率 与 代价曲线<br>

模型的好坏取决于：算法，数据，任务需求<br>
performance measure：反映任务需求<br>

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






