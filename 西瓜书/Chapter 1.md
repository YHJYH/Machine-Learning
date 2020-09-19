# Chapter 1 Introduction
## 1.1
机器学习(Machine learning): 在计算机上从数据中产生model(模型)的算法，即learning algorithm(学习算法).<br>
形式化定【Mitchell 1997】

## 1.2 基本术语
    data set: 数据集，记录的集合；
    instance/sample: 示例/样本，数据集中的每条记录；
    attribute/feature: 属性/特征，反映事件/对象在某方面的表现/性质；
    attribute value: 属性值；
    attribute/sample space: 属性/样本空间，属性张成的空间；
    feature vector: 特征向量，每个事物在杨蓓空间中的坐标位置，示例；
    dimensionality: 维数，属性个数；
    learning/training: 学习/训练，从数据中学得模型的过程（为了找出和逼近ground-truth）；
    training data: 训练数据，训练过程中使用的数据；
    training sample: 训练样本，训练数据中的每一个样本；
    training set: 训练集，训练样本组成的集合；
    hypothesis: 假设，学得模型对应的关于数据的潜在规律；
    ground-truth: 真相/真实，潜在规律本身；
    learner: 学习器，模型；
    label: 标记，关于instance结果的信息；
    example: 样例，有label的instance；
    label space: 标记/输出空间，所有label的集合；

supervised learning：监督学习<br>
包含<br>
    
    classification分类（预测离散值，包含binary classification【positive/negative class, label space = {0,1} or {-1,+1}】和multi-class classification【|label space| > 2】）

和<br>

    regression回归（预测连续值）（label space = R (real set)）；
 
 unsupervised learning：无监督学习<br>
    
    包含clustering聚类（将training set中的sample分成若干cluster簇，无label）
 <br>
 
    testing：测试，使用学得模型进行预测的过程；
    testing sample：测试样本
    generalization: 泛化能力，学得模型适用于新样本的能力；
    independent and identically distributed: i.i.d. 独立同分布，从全体样本服从的，未知的distribution中获得的每个sample都是独立地从该分布上采样获得的；
    
 ## 1.3 假设空间
 科学推理手段：<br>
 
    induction(归纳)：从特殊到一般，generalization泛化过程；
    deduction(演绎)：从一般到特殊，specialization特化过程；

inductive learning：归纳学习，从example中学习，分为<br>

    广义归纳学习：从example中学习;
    狭义归纳学习：从training data中学得concept(概念)，概念学习/形成;
        
        布尔概念学习：对0/1布尔值的目标概念的学习。
       
version space: 版本空间，与训练集一致的假设集合<br>

## 1.4 归纳偏好
version space中hypothesis的选择：通过训练样本无法判断；<br>
因此，通过学习算法本身的“偏好”进行hypothesis的选择.<br>
inductive bias: 归纳偏好，算法在学习过程中对某种类型hypothesis的偏好；<br>
任何有效的ML算法必有其inductive bias.<br>
<br>
引导algorithm确定"正确"偏好的一般性原则：<br>
Occam's razor: 奥卡姆的剃刀，若有多个假设与观察一致，则选择最简单的那个。<br>
然而其并非平凡原则【假设：什么样的模型更好】<br>
现实问题中：算法的归纳偏好是否与问题本身匹配。<br><br>
结论：总误差与学习算法无关。<br>
证明：<br>
使用算法La，基于training data X，其inductive bias选择hypothesis function h的概率是P(h|X,La);<br>
使f表示ground-truth function；<br>
则La在training data之外的sample上的误差为:<br>
E_ote(La|X,f) = sum(all h)sum(x belongs to sample space-X) P(x)*delta-function(h(x) not equal to f(x))*P(h|X,La)<br>
若delta function内条件达到，delta function等于1，否则为0; <br>
基于书中推导得出（1.1）和（1.2）<br>
关于（1.2）的一个小地方：1/2*2^|X|, 有X个sample，每个sample有两个可能output（0/1），一共有一半的f(x)与h(x)不一致（delta function的限定条件所以只考虑不一致）.<br>

综上：<br>

    No Free Lunch Theorem(NFL): 没有免费的午餐定理<br>
    前提：f的均匀分布。
    
本章重点：现实问题中：算法的归纳偏好是否与问题本身匹配。

## Chapter 1 习题
1.1 <br>
(色泽=青绿；根蒂=蜷缩；敲声=浊响)<br>
(色泽=青绿；根蒂=蜷缩；敲声=*)<br>
(色泽=青绿；根蒂=*；敲声=浊响)<br>
(色泽=*；根蒂=蜷缩；敲声=浊响)<br>
(色泽=*；根蒂=*；敲声=浊响)<br>
(色泽=*；根蒂=蜷缩；敲声=*)<br>
(色泽=青绿；根蒂=*；敲声=*)<br>

1.2<br>



