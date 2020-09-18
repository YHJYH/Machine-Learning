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
  *包含
        *classification分类（预测离散值，包含binary classification【positive/negative class, label space = {0,1} or {-1,+1}】和multi-class classification【|label space| > 2】）
和<br>
        *regression回归（预测连续值）（label space = R (real set)）；
 unsupervised learning：无监督学习<br>
  *包含clustering聚类（将training set中的sample分成若干cluster簇，无label）

    testing：测试，使用学得模型进行预测的过程；
    testing sample：测试样本

