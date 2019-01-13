# 绪论：初始机器学习
## 什么是机器学习
#### Atrhur Samuel(1959)
**在没有明确设置的情况下使计算机具有学习能力的研究领域**
#### Tom Mitchell(1998)
**一个适当的学习问题定义如下：计算机程序从经验E中学习解决某一任务T以及进行某一性能度量P，通过P测定在T上的因经验E而提高的表现**
针对Tom的观点我们可以来仔细区分一下T、P、E
![](http://47.107.36.172/wp-content/uploads/2019/01/批注-2019-01-11-145241.jpg)
选择第一个选项
- 第一个选项
***区分邮件是不是垃圾邮件***，很显然可以作为T(**作为这个算法的任务T**)
- 第二个选项
***观察你对垃圾邮件的标记***，这个可以当作E(**算法通过比较你标记的垃圾邮件的特征来作为经验E**)
- 第三个选项
***将邮件正确分为垃圾邮件的概率***，这个作为P(**我们可以通过P来知道算法的准确度，来判断算法是否真正到达了我们的预期**)

------------

## 监督学习与无监督学习
### 监督学习(Supervised Learning)
> Supervised learning is the machine learning task of learning a function that maps an input to an output based on example input-output pairs.[[1]]

这段来自Wiki，监督学习的本质是**我们给算法一个数据集，其中包含了正确的答案，而算法的目的就是给出更多正确的答案**
课程中提到了两个问题
![](http://47.107.36.172/wp-content/uploads/2019/01/批注-2019-01-12-212203.jpg)

#### 回归问题
**通过一连串的数据来预测连续的数值输出**，比如说你收集了你家旁边的房价，而你的朋友正打算在你家附近买套房子，正好你可以通过你手边收集的房价数据来预测他所选地段的房价(当然不一定是你来选)
**下面是老师课程中的例子**
![老师课程中的例子](http://47.107.36.172/wp-content/uploads/2019/01/批注-2019-01-12-213613.jpg)

#### 分类问题
就根据吴恩达老师的课程中他与他同事做的乳腺癌的实验来说，通过0 1来判断是否患有乳腺癌，这一类为分类问题，如图
![](http://47.107.36.172/wp-content/uploads/2019/01/批注-2019-01-12-213504.jpg)
*甚至可以变成这样（这个取决于你对变量的规定）*
![](http://47.107.36.172/wp-content/uploads/2019/01/批注-2019-01-12-213537.jpg)

### 无监督学习(Unsupervised Learning)
>Generally, it is wrongly referred to cluster analysis as a branch of machine learning that groups the data that has not been labelled, classified or categorized. Instead of responding to feedback, cluster analysis identifies commonalities in the data and reacts based on the presence or absence of such commonalities in each new piece of data.[[2]]

结合维基百科与课堂上的讲述来说，无监督学习是**将没有标注(labelled)，分类(classification)或者是归档(categorized)的数据中寻找共同点将他们划分开来**

#### 聚类问题
我们所给出的数据中存在相同或者不同的类型与特征，而**聚类算法**所做的事**将具有相同类型的数据分开**，下图就是这个意思
![](https://upload.wikimedia.org/wikipedia/commons/c/c8/Cluster-2.svg)

#### 聚类问题举例
##### 新闻分类
![](http://47.107.36.172/wp-content/uploads/2019/01/批注-2019-01-13-170807.jpg)

当我们在一个大新闻下点击的小标题时，会出现其他新闻社报道的报告，这是聚类的一种体现

##### 基因研究
![](http://47.107.36.172/wp-content/uploads/2019/01/批注-2019-01-13-170904.jpg)

一样的，基因研究来通过区分不同的特性将人分为不同的种类

##### 鸡尾酒问题
>“鸡尾酒会问题”（cocktailparty problem）是在计算机语音识别领域的一个问题，当前语音识别技术已经可以以较高精度识别一个人所讲的话，但是当说话的人数为两人或者多人时，语音识别率就会极大的降低，这一难题被称为鸡尾酒会问题。[[3]]

##### 或者更多方面
![](http://47.107.36.172/wp-content/uploads/2019/01/批注-2019-01-13-171000.jpg)

比如，网络，社交圈，市场份额以及宇宙研究都可以用到聚类算法

[1]: https://en.wikipedia.org/wiki/Supervised_learning "Supervised learning-Wiki"
[2]: https://en.wikipedia.org/wiki/Unsupervised_learning "Unsupervised learning-Wiki"
[3]: http://52opencourse.com/54/coursera%E5%85%AC%E5%BC%80%E8%AF%BE%E7%AC%94%E8%AE%B0-%E6%96%AF%E5%9D%A6%E7%A6%8F%E5%A4%A7%E5%AD%A6%E6%9C%BA%E5%99%A8%E5%AD%A6%E4%B9%A0%E7%AC%AC%E4%B8%80%E8%AF%BE-%E5%BC%95%E8%A8%80-introduction "Coursera公开课笔记: 斯坦福大学机器学习第一课-引言(Introduction)"