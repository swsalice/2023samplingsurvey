**以下内容为段雨畅所写**

# 5
___


# 统计匹配问题中的辅助变量选择
___


**马塞洛·德奥拉齐奥**

意大利国家统计研究所，意大利罗马

**马尔科·迪齐奥**

意大利国家统计研究所，意大利罗马

**毛罗·斯坎努**

意大利国家统计研究所，意大利罗马

## 内容
5.1 简介

5.2 匹配变量的选择

5.2.1 基于联想的传统方法

5.2.2 通过不确定性选择匹配变量减少

5.2.3 示例

5.2.4 受惩罚的不确定度测量

5.3 欧洲社会调查数据模拟

5.4 结论

参考文献

___

## **5.1简介**
统计匹配（SM，有时称为数据融合或综合匹配）旨在结合所参考的不同样本调查中的可用信息，当两个样本不相交时，分配给相同的目标群体。正式地设Y和Z是两个随机变量；统计匹配技术估计联合概率分布函数（Y，Z）的目标，或其中一个参数（例如列联表或回归系数）

当：

（i）Y和Z不是在调查中共同观察到的，Y是在含有 $n_A$个个体的样本A中观察到，Z是在含有 $n_B$个个体的样本B中观察到；

（ii）A和B是独立的，两个样本中的单位不重叠（不可能使用记录链接）；

（iii）A和B都观察到一组附加变量X。

这个问题最早是在[3]中以三变量(X,Y,Z)的高斯分布为例进行方法学研究的。三变量(X,Y,Z)在高斯分布的情况下，首次从方法上研究了这个问题。关于这个问题缺乏可识别性的研究可以追溯到[24]。缺少可识别性的影响是对联合(Y,Z)分布的多个同样合理的估计是可用的。传统的方法是隐含地或明确地引入假设，使模型可识别，以获得模型参数的唯一估计。通常的假设是在X的条件下，然而，这是一个很强的假设，即鉴于手头的数据，Y和Z的独立性。鉴于手头的数据，这是个很强的假设，不能被检验。为了避免引入假设，使推论更加可信，许多论文已经开始研究如何在考虑到非唯一性的情况下进行推论，考虑到统计匹配中估计的非唯一性，(也见[12])。这些推论是关于找出哪些感兴趣的真实参数与我们所做的观察相一致。这组数值被命名为"不确定性区域"[15]或 "部分识别区域"[31,17]。基于部分识别区域的推理，在其他背景下使用，例如计量经济学[30]和社会科学[20]。值得注意的是，"不确定区域"不应该与 "部分识别区域 "混淆。不应与"置信区间"确定的区域相混淆。在第一种情况下，它们产生于联合分布的部分可识别性；在第二种情况下，区间是由观测的抽样性质决定的,关于这两种不确定性的联合分析的结果在[19]和[28]中有所描述。

在统计匹配中，Rubin[25]定义了一种非正确的贝叶斯方法来探索不确定区域。这种方法在[23]中通过提出适当的贝叶斯方法而得到简化。Moriarty和Scheuren[21]探索了一套同样合理的解决方案，将所有可估计的参数固定为通过一致估计器获得的估计值；这种方法并不完全令人满意，因为有些结果是不可接受的（例如，高斯变量的协方差矩阵为负无限）。使用最大似然估计器来估计可识别的参数，然后找到相应的似然岭（即同样最大似然估计的集合），避免了在这个集合中包括不可接受的解决方案的可能性（见[16]）。使用不确定性一词来描述似然岭的宽度是在[16]中首次提出的。它在不同情况下的属性和它的估计以及对估计者的渐进性质的研究都在[11]。与最小推理概念相关的其他方法在[33]中概述。尽管不确定性是一个有助于描述我们在统计匹配背景下离可识别性有多远的概念，但本章的想法是，它也可以被用来用于操作性目的，也就是用于SM中的变量选择。更确切地说、假设两个调查A和B观察到足够多的共同变量X。大量的共同变量X的情况是很常见的。例如，在社会调查中，许多社会-经济变量 （居住地、年龄、性别、职业、教育和婚姻状况、户主的特征、家庭的特征等等）。等）都是可用的。是否应该将所有这些变量用于匹配目的？可能会出现问题；例如，众所周知，分类变量的数量越多，产生稀疏表格的风险就越大、 也就是每个单元格的观察值很少或为零的表格。更为普遍的是，大量的变量和相应的类别可能会对估计的效率产生影响。对估计的效率产生影响。在这种情况下，主要问题包括同时估计大量可识别的参数,经典的变量选择方法是基于对辅助变量X在(Y,Z)方面的解释能力的分析，例如，通过分析残差，对(Y,Z)的解释能力进行分析。例如，通过分析模型的残差。然而，经典方法需要对(Y,Z)进行联合观测，而在统计匹配的情况下，这些观测是不可用的。统计匹配的情况下无法获得。其结果是，它通常被作为一种次优的方法；也就是说，要分别选择解释Y和Z的变量X。事实上，现有的数据允许在这两个独立的 数据集。在本章中，我们声称可以通过不确定性的概念来找到匹配变量的适当选择，也就是选择那些使不确定性最小的变量那些使不确定性区域最小化的变量。为了避免选择所有可用的共同变量，应该考虑对不确定性的惩罚性措施 应该被考虑在内。在本章中，我们研究了基于表的稀疏性的惩罚。

___
## **5.2匹配变量的选择**

数据源A和B可能共享许多共同的变量X。SM时，不是所有的X变量都会被使用，而只是最重要的那些。选择最相关的  $X_M$（ $X_M$⊆X），称为匹配变量。通常通过咨询主题专家和适当的统计方法来进行（见[14]）。

匹配变量的选择应该在多变量的意义上进行。这就要求有一个数据源，其中(X,Y,Z)被观察到。不幸的是，在基本的SM框架中，这是不可能的，因为(X,Y,Z)从来没有被联合观测过，因此，选择是通过在两个数据集A和B中分别选择变量来进行的。我们的建议是，在选择匹配变量时进行独特的分析，方法是 我们的建议是，在选择匹配变量时进行独特的分析，寻找对减少Y和Z之间的不确定性最有效的共同变量集。匹配变量，避免选择过多的X变量。导致大量的参数需要估计。

### **5.2.1基于联想的传统方法**

变量选择方法一般是基于关联/依赖分析和因变量的残差分析。分析，以及对因变量残差的分析。如前所述，在基本的SM框架中，这是不允许的，因为缺乏 (Y,Z)的联合观测，A只允许研究Y和X之间的关系，而Z和X之间的关系则可以在B中研究。考虑到这些前提，对A和B分别进行了两个分析来选择相应的X变量，然后将这两个独立的分析结果结合起来。然后将两个独立的分析结果结合起来，一般来说，可以应用以下规则：

 $X_Y$ ∩  $X_Z$ ⊆  $X_M$ ⊆  $X_Y$∪  $X_Z$


其中 $X_Y$（ $X_Y$⊆X）和 $X_Z$（ $X_Z$⊆X）是共同变量的子集 分别能更好地解释Y和Z。交叉点 $X_Y$ ∩ $X_Z$提供了如果与 $X_Y$∪ $X_Z$相比，提供了一个较小的匹配变量子集；这是实现解析的一个重要特征。这是实现简明性的重要特征。例如，在一个距离热甲板中，太多的匹配变量会在最终结果中引入不必要的额外噪音。不幸的是， $X_Y$∩ $X_Z$的风险在于一个目标变量的最佳预测因子将被排除，如果它们不在另一个目标变量的预测器子集中，而且，在某些情况下，交集可能会被排除。此外，在某些情况下，交叉点可能是空的。由于这个原因，最终的匹配变量子集匹配变量的最终子集 $X_M$通常是一个折衷的结果，而主题专家和数据分析师的贡献则是 为了确定"最佳"子集，主题专家和数据分析师的贡献是非常重要的"最好的子集"。

识别 $X_Y$的最简单程序是计算Y和每个可用的预测因子X之间的成对相关/关联度。对B也应进行同样的分析，以确定Z的最佳预测因子。为了确定最终的非线性关系，考虑等级（Spearman等级相关系数）可能很方便。一个有趣的建议--可以在[18]中找到--包括查看与回归模型rank(Y)vs. rank(X)相关的调整后的 ${R^{2}}$（未经调整的 ${R^{2}}$ 对应于平方的Spearman等级相关系数）。当X是一个分类的名义变量时，它被认为是回归模型rank(Y )对dummies(X)的调整 ${R^{2}}$ 。

当反应和预测因素都是分类的，那么基于Chi-square的关联度量（Cramer's V）或方差比例减少的度量（见Goodman-Kruskalλ或τ）。可以考虑基于Chiquare的关联测量（Cramer'sV）或按比例减少方差的测量（例如，Goodman-Kruskal λ或τ）。坂本 和Akaike[26]建议使用Akaike信息准则（AIC），也就是说，最好的预测器是能够提供最准确的信息的。即最佳预测器是给出AIC统计量最小的那个。好的 基于AIC的选择程序的优点是，它还可以识别预测器的最佳组合。

有时，可以通过拟合模型来确定重要的预测因子,然后运行程序来选择最佳预测因子。选择子集 $X_Y$也可以要求非参数程序如分类树和回归树[6]，或者更好的是随机森林[7]。它为预测因子提供了一个重要性的衡量标准。然而，随机森林的拟合在计算上要求很高，一些作者警告说，在选择最佳预测因子时不要使用预测因子的重要性衡量标准。(见，例[29]）。

以下内容为杜博玮所做：

### **5.2.4 惩罚性不确定性测量**

在介绍过程之前，让我们引入一些符号。假设Q是所有可用X变量的数量， $H_q$ 是变量 $X_q$ 的类别数。此外， ${D_m}$ 是通过交叉分类共同变量的子集而获得的变量，其中 $HD_m$ 是其类别数；可以创建的子集总数为 $M = (2^{Q}-1)$，而最终子集包括所有Q变量，即 $D_Q= X_1 × X_2 × ... × X_Q$，并且具有 $HD_Q$ 类别数 $（HD_Q = H_1 × H_2 × ... × H_Q）$。匹配变量是与 $D_m$ 相对应的变量，使得在所有可能的变量组合中，d的惩罚度量最小化。更正式地说，假设g是惩罚项，我们寻找最小值 

$\tilde{d_m} = d_m+ g$  (5.3) 

特别地，我们分析了两个替代惩罚度量，两个都基于稀疏性度量。第一种是

$\tilde{d_m}^{(1)}=dm+log(1+\frac{HD_m}{HD_Q})$ (5.4)

的最小值，并且我们搜索˜d的最小值 (1)  m的最小值，使其具有可接受的稀疏程度。
例如，如果稀疏性是由以下因素衡量的

$\bar{n}=min[\frac{n_A}{HD_m×J},\frac{n_B}{HD_m×K}]$ (5.5)

其中， $HD_m×J$和 $HD_m×K$ 分别是表格 $D_m×Y$和 $D_m×Z$ 中的单元格数，因此我们可以要求可接受的子集是那些 $\bar{n}>1$ 的子集。在这个函数中，稀疏性分为两部分，在惩罚项 $log(1+\frac{HD_m}{HD_Q})$ 中考虑了变量X的稀疏性，并在停止规则中要求 $\bar{n}> 1$，即与(Y，X)和(Z，X)相关的稀疏性。引入对数是因为从进行的实验中观察到，这个项的增长速度（不带对数）相对于 $d_m$来说太快了。

第二个惩罚性措施是

$\tilde{d_m}^{(2)}=dm+max[\frac{1}{N_A-HD_m×J},\frac{1}{n_B-HD_m×K}]$  (5.6)

其中， $n_A>(HD_m×J)$ 并且 $n_B>(HD_m×K)$

第二个惩罚项的优点是不依赖于最大表格的所有可用 X 变量的单元数 ( $HD_Q$ )，此时交叉时所得到的。此外，第二个惩罚隐含地包含了这个停止准则，即当 $\bar{n} ≤ 1$ 时停止，表示过于稀疏的列联表的指示。这当然是 $\tilde{d_m}^{(2)}$  的一个积极方面，另一方面， $\tilde{d_m}^{(1)}$ 更加灵活，因为它允许采用不同的稀疏度度量和停止规则中的不同阈值。事实上， $\bar{n}>1$ 的标准是一个主观选择，反映了[2]中关于稀疏性的广泛定义：“当样本大小与单元数的比例相对较小时，列联表被认为是稀疏的”。然而，在文献中，许多其他的方法被提出来衡量稀疏性，例如，基于期望单元频率小于1、5或10的百分比，或者观察到的零频率的百分比。这些指标可以代表惩罚项的替代提案。
当许多共同变量表征问题时，惩罚度量的最小化计算可能是不可行的；因此，提出了一种顺序过程来近似先前的计算。

该过程包括以下步骤：

• 步骤 0 
将 Q 个变量 $X_q$ 按照相对于 $\tilde{d_q}$ 的降序排序。然后选择具有最小 $\tilde{d_q}$ 的变量。 

• 步骤 1 
考虑将一个变量添加到当前已选择的变量集合中得到的所有可能组合，并以 $\tilde{d_m}$ 为标准评估相应的不确定性；例如，在第一次迭代中，将考虑使用步骤 0 中识别的变量与其他变量的所有可能组合。 

• 步骤 2 
选择具有最小 $\tilde{d_m}$ 值的变量组合，然后如果满足以下任一条件之一，则停止：

i) $\tilde{d_m}$  大于前一次迭代对应组合的值，即不存在返回 $\tilde{d_m}$ 下降的变量组合

ii) （仅在使用 $\tilde{d_m}^{(1)}$ 的情况下需要的步骤）稀疏度不可接受，例如使用公式（5.5）中的 $\bar{n} ≤ 1$ ;

否则返回步骤 1。


## **5.3使用欧洲社会调查数据进行模拟**
为了展示选择匹配变量的方法如何工作，考虑一个玩具示例，其中数据来自于欧洲社会调查（ESS，2014）第七轮。数据集仅包括社会人口核心模块的一部分变量，已经排除了缺失值、“不知道”和拒绝回答的样本。总之，共有 n = 28,769 个受访者和 13 个变量（见表5.1）。表5.1中的后两个变量起着目标变量（Y=“hincfel1”和Z=“hinctnta”）的作用，而其他变量则作为可用的共同变量（X）进行处理。最初，我们将使用整个样本来选择匹配变量，在真实的SM应用中不存在这种情况，那里只有包括 (X,Y) 和 (X,Z) 两个独立样本 A 和 B。
在第一步，我们通过计算通常的成对度量来寻找最理想的预测目标变量的最佳预测变量集合，这是通过交叉两个目标变量（即W = Y × Z）获得的，因为它基于（X，Y，Z）的联合分布的全面了解。结果报告在表5.2中。特别地，通过考虑每个可用的X，计算了经过偏差校正的Cramer's V、Theil's U和AIC。


### **TABLE 5.1**

描述所使用模拟中的变量。

| 名称 | 描述 | 
| :----: | :-- | 
| cntry |  居住国家（20个国家） | 
| hhmmb5  | 家庭成员数（1、2、3、4、>4） | 
| gndr | 受访者的性别（1=“男性”，2=“女性”） |
| ageacat | 受访者年龄类别（14-17、18-24、25-44、45-64、65-74、>74） |
| icpart1 | 受访者是否与配偶/伴侣同住（1=“是”，2=“否”） |
| chldhm | 家庭中是否有子女（1=“是”，2=“否”） |
| anypacc | 住房是否存在问题（1=“是”，2=“否”） |
| eisced | 受教育程度最高水平（7个类别） |
| prof2 | 职业状态（1=“有薪工作”，2=“退休”，3=“其他”） |
| crpdwk | 过去7天是否从事过有薪工作（至少1小时）（具有prof2=1或2的人） |
| emplrel | 工作类型（具有prof2=1的人）（1=“雇员”，2=“自雇”，3=“在家庭企业工作”） |
| hinctnta | 家庭总收入的十分位数（1-10） |
| hincfel1 | 是否因当前收入而生活舒适（1=“是”，2=“否”） |


### **TABLE 5.2**

W=(Y × Z)和每个可用的X之间的关联、PRE度量和AIC。 

| X | V' | U | AIC |
| :----: | :----: |:----: |:----: |
| cntry | 0.1117 | 0.0409 | 158818.1 |
| hhmmb5 | 0.2380 | 0.0393 | 158507.0 |
| gndr | 0.0966 | 0.0018 | 164575.4 |
| ageacat | 0.1312 | 0.0153 | 162495.1 |
| icpart1 | 0.3878 | 0.0267 | 160463.2 |
| chldhm | 0.2539 | 0.0119 | 163901.5 |
| anypacc | 0.1479 | 0.0038 | 164231.6 |
| eisced | 0.1785 | 0.0328 | 159653.6 |
| prof2 | 0.2805 | 0.0278 | 160321.4 |
| crpdwk | 0.2606 | 0.0251 | 160771.1 |
| emplrel | 0.0688 | 0.0025 | 164522.7 |

在这个表中，我们看到了每个可用的X与目标变量 $W = (Y × Z)$之间的关联程度、PRE度量和AIC值。其中，偏差校正的Cramer's V表明，与目标变量组合 $（W = Y × Z）$相关性最高的变量是“icpart1”，其次是“prof2”、“crpdwk”、“chldhm”和“hhmmb5”，它们的相关性较低。如果考虑Theil's U或AIC，则可能会得出略有不同的变量子集，特别是“cntry”、“hhmmb5”、“eisced”，以及具有较小值的“icpart1”、“prof2”和“crpdwk”。当使用AIC来识别最佳的X组合来预测 $W = Y × Z$时，返回第一选择的子集只包含变量“hhmmb5”和“cntry”，其次是（“hhmmb5”，“eisced”）和（“hhmmb5”，“cntry”，“icpart1”）。这些结果表明，即使在具有所有变量（X，Y，Z）的唯一数据源中，在不考虑预测因素之间的关系的情况下，成对测量结果会建议选择比必要的预测因素更多的预测因素。

本文介绍了在标准匹配中，当两个不同样本可用时，如何展示基本分析工作的例子。这代表了在标准匹配中的理想情况，其中双变量分布（X，Y）和（X，Z）已知。所有的测量结果（见表5.3）都指出“cntry”和“eisced”是“hincfel1”（Y）的最佳预测变量。相反，当响应变量是“hinctnta”（Z）时，结果不完全一致；如果比较估计的U和AIC，可以确定一个更大的匹配变量子集（“hhmmb5”，“icpart1”，“eisced”，“prof2”，“crpdwk”），而如果比较V 0，则只有一个较小的子集（“icpart1”，“prof2”，“crpdwk”）是最佳选择。
   假设 $X_Y = (“cntry”, “eisced”) $和 $X_Z = (“hhmmb5”, “icpart1”, “eisced”, “prof2”, “crpdwk”)$，它们的交集确定了一个子集，仅包含一个匹配变量 $X_M = “eisced”$；相反，它们的并集返回一个包含六个匹配变量的集合（“cntry”, “hhmmb5”, “icpart1”,“eisced”, “prof2”, “crpdwk”）。


### **TABLE 5.3**

该表格展示了Y（“hincfel1”）和Z（“hinctnta”）对所有可能的X的组合之间的关联（V）、PRE度量和AIC值。

| X | V' | U | AIC | V' | U | AIC | 
| :----: | :----: |:----: |:----: | :----: | :----: | :----: |
| cntry | 0.3567 | 0.1027 | 33427.9 | 0.0898 | 0.0168 | 130381.1 |
| hhmmb5 | 0.0960 | 0.0073 | 36948.6 | 0.2260 | 0.0436 | 126565.4 |
| gndr | 0.0488 | 0.0019 | 37144.6 | 0.0915 | 0.0019 | 132020.9 |
| ageacat | 0.0411 | 0.0014 | 37170.3 | 0.1149 | 0.0150 | 130367.3 |
| icpart1 | 0.1008 | 0.0080 | 36916.6 | 0.3849 | 0.0327 | 127949.7 |
| chldhm | 0.0529 | 0.0022 | 37132.2 | 0.2077 | 0.0097 | 130994.3 |
| anypacc | 0.1096 | 0.0100 | 36844.0 | 0.1285 | 0.0035 | 131815.9 |
| eisced | 0.2385 | 0.0438 | 35593.3 | 0.1715 | 0.0376 | 127395.2 |
| prof2 | 0.1343 | 0.0146 | 36672.0 | 0.2716 | 0.0326 | 127981.4 |
| crpdwk | 0.1143 | 0.0103 | 36834.4 | 0.2596 | 0.0308 | 128211.3 |
| emplrel | 0.0564 | 0.0026 | 37120.1 | 0.0663 | 0.0028 | 131943.9 |


以下内容为王梓帆所做：

很容易看出这些变量的联合分布将产生一个包含12,600个单元格的表格，当添加Y时，表格数量增加了一倍，当添加 Z × $X_M$ 时，表格数量达到了126,000个，这个数量对于只有28,769个样本的可靠估计来说太多了（平均单元格频率“ ${\widetilde n}$ ”为0.2288，远低于1的阈值）。然而，通过AIC确定的联合Y和Z的前3个子集的组合都是Y和Z的最佳预测变量单独考虑后得到的更大的联合预测变量集合的子集。

&emsp;&emsp;使用AIC程序单独考虑每个响应变量来确定“最优”预测变量组合，结果显示 $X_Y^{(AIC)}$  =（“cntry”，“eisced”，“prof2”）和 $X_Z^{(AIC)}$ =（“hhmmb5”，“icpart1”，“eisced”，“prof2”）。交集由两个匹配变量 $X_M$ =（“eisced”，“prof2”）组成，而并集给出了一个包含五个预测变量（“cntry”，“hhmmb5”，“icpart1”，“eisced”，“prof2”）的集合，比使用成对测量后获得的集合略小。同样，通过AIC确定的Y × Z的最佳3个预测变量组合是后者 $X_M$ 的子集。

&emsp;&emsp;通过探索不确定性来选择匹配变量是计算密集型的，但它具有避免单独分析的优点。它需要估计三个列联表：X变量的联合分布、X × Y和X × Z的联合分布。具有唯一样本对应于理想情况，因为从中估计的表格将不会显示在处理两个独立样本时估计的X变量的联合分布中存在的差异。

### **TABLE 5.4**
 
自动选择具有惩罚性措施的匹配变量 ${\widetilde d}_m^{(1)}$。从整个样本中估计的表格。
 
| Comb. of X ( $D_m$ ) | No.of X | $H_{D_m}$ | ${\widetilde d}_m^{(1)}$ | ${\overline n}$ |
| :--- | ---: | ---: | ---: | ---: |
| unconditional | 0 | 2 | 0.100000 | 2876.90 |
| cntry   | 1 | 20 | 0.098797 | 143.85 |
| cntry eisced | 2 | 140 | 0.093235 | 20.55 |
| cntry eisced hhmmb5 | 3 | 700 | 0.087449 | 4.11 |a
| cntry eisced hhmmb5 prof2 | 4 | 2100 | 0.079922 | 1.37 |

 ### **TABLE 5.5**
  
自动选择具有惩罚性措施的匹配变量 ${\widetilde d}_m^{(2)}$。 从整个样本中估计的表格。
 
| Comb. of X ( $D_m$ ) | No.of X | $H_{D_m}$ | ${\widetilde d}_m^{(2)}$ | ${\overline n}$ |
| :--- | ---: | ---: | ---: | ---: |
| unconditional | 0 | 2 | 0.100000 | 2876.90 |
| cntry   | 1 | 20 | 0.098829 | 143.85 |
| cntry eisced | 2 | 140 | 0.093248 | 20.55 |
| cntry eisced hhmmb5 | 3 | 700 | 0.087380 | 4.11 |a
| cntry eisced hhmmb5 prof2 | 4 | 2100 | 0.079704 | 1.37 |

&emsp;&emsp;我们使用第5.2.4节中介绍的算法根据两种替代惩罚测量 ${\widetilde d}_m^{(1)}$ 和 ${\widetilde d}_m^{(2)}$ 选择了匹配变量。结果显示在表5.4和5.5中。在基于惩罚不确定性自动选择匹配变量的过程中，无论惩罚是什么，都提供相同的结果。第二个惩罚项似乎略高于第一个，但这并不影响中间和最终结果。实际上，在两个示例中，最佳匹配变量集合由11个起始共同变量中的4个组成：“cntry”、“hhmmb5”、“eisced”和“prof2”。当考虑目标变量的最佳预测变量的并集( $X_Y$ ∪ $X_Z$ )时，这个子集比基本的单独分析获得的子集(6个变量)小，但比AIC预测Y × Z时确定为“最优”的（“cntry”，“hhmmb5”）略大。

&emsp;&emsp;值得注意的是，这些结果是针对一个“理想”的情况，即在实践中所有变量都可用，即不存在不确定性，也不需要进行统计匹配。为了了解在匹配设置中会发生什么，整个样本被视为一个人工种群，用作模拟的基础。在每次迭代中：
1. 从中不重复地抽取两个独立的简单随机样本A和B。从A中移除变量Z（“hinctnta”），从B中移除变量Y（“hincfel1”）。
2. 使用传统方法（成对测量V0和AIC）和两种基于不确定性的程序进行匹配变量的自动选择，但使用不同的惩罚项。
3. 保存各种已确定的匹配变量子集。

### **TABLE 5.6**

根据传统选择方法，在模拟中确定的匹配变量子集。

<table>
    <tr>
        <td>测度</td> 
        <td>选择的X（匹配变量）</td> 
        <td>(a)</td>
        <td>(b)</td>
        <td>(c)</td>
        <td>(d)</td>
   </tr>
    <tr>
        <td>V'</td> 
        <td>cntry crpdwk eisced hhmmb5 icpart1 prof2</td> 
        <td>100</td> 
        <td>100</td> 
        <td>100</td> 
        <td>100</td> 
    </tr>
    <tr>
        <td rowspan="4">U'</td>    
  		  <td>cntry crpdwk eisced hhmmb5 icpart1 prof2</td> 
      	<td>61</td> 
        <td>70</td> 
        <td>13</td> 
        <td>2</td> 
    </tr>
    <tr>
        <td>cntry crpdwk eisced hhmmb5 prof2</td> 
        <td>7</td> 
        <td>6</td> 
        <td>8</td> 
        <td>10</td>  
    </tr>
    <tr>
        <td>cntry eisced hhmmb5 icpart1 prof2</td> 
        <td>30</td> 
        <td>24</td> 
        <td>79</td> 
        <td>88</td>  
      </tr>
      <tr>
        <td> $Others$ </td> 
        <td>2</td> 
        <td> </td> 
        <td> </td> 
        <td> </td> 
      </tr>
   <tr>
        <td rowspan="4">AIC p.</td>    
  		  <td>cntry eisced hhmmb5 icpart1</td> 
      	<td>55</td> 
        <td>53</td> 
        <td>76</td> 
        <td>61</td> 
    </tr>
    <tr>
        <td>cntry eisced hhmmb5 prof2</td> 
        <td>31</td> 
        <td>35</td> 
        <td>22</td> 
        <td>39</td>  
    </tr>
    <tr>
        <td>cntry hhmmb5 icpart1 prof2</td> 
        <td>8</td> 
        <td>8</td> 
        <td>2</td> 
        <td> </td>  
      </tr>
      <tr>
        <td> $Others$ </td> 
        <td>6</td> 
        <td>4</td> 
        <td> </td> 
        <td> </td> 
      </tr>
     <tr>
        <td rowspan="6">AIC c.</td>    
  		  <td>cntry hhmmb5 icpart1 prof2</td> 
      	<td>10</td> 
        <td>6</td> 
        <td> </td> 
        <td> </td> 
    </tr>
    <tr>
        <td>cntry eisced icpart1 prof2</td> 
        <td>21</td> 
        <td>85</td> 
        <td>100</td> 
        <td>99</td>  
    </tr>
    <tr>
        <td>cntry eisced icpart1</td> 
        <td>34</td> 
        <td> </td> 
        <td> </td> 
        <td> </td>  
      </tr>
     <tr>
        <td>cntry hhmmb5 prof2</td> 
        <td>24</td> 
        <td>3</td> 
        <td> </td> 
        <td> </td>  
      </tr>
      <tr>
        <td>cntry icpart1 prof2</td> 
        <td>5</td> 
        <td> </td> 
        <td> </td> 
        <td> </td>  
      </tr>
      <tr>
        <td> $Others$ </td> 
        <td>6</td> 
        <td>6</td> 
        <td> </td> 
        <td>1</td> 
      </tr>
</table>

&emsp;&emsp;针对以下不同的 $n_A$ 和 $n_B$ 的组合，进行了100次迭代的操作：(a) $n_A$ = 1000， $n_B$  = 3000; (b) $n_A$ = 2000， $n_B$ = 4000; (c) $n_A$ = 5000， $n_B$ = 10000; (d) $n_A$ = 10000， $n_B$ = 15000。

&emsp;&emsp;表5.6显示了传统程序选择匹配变量的模拟结果；具体而言，结果是关于与Y和Z具有最高关联性或最佳预测性的变量的并集。仅在情况(a)中，即在样本最小的情况下，成对测量才会产生可变结果，但V'例外，它总是确定一组6个匹配变量，与在完整样本分析中确定的一样。当考虑Theil's U时，仅在情况(c)和(d)中，由5个变量组成的子集比更大的子集更受欢迎。在表5.6中表示为“AIC p”的AIC惩罚倾向于支持较小的匹配变量子集；最常见的差别仅在于这四个变量中的一个。最后，当匹配变量由与Y和Z的最佳预测组合的并集确定时，如由AIC确定的，表5.6中表示为“AIC c”，结果在情况(a)中表现出非常高的异质性，表明相对于需要估计的单元数，此程序的样本过小。从情况(b)开始，异质性消失，几乎所有模拟都喜欢四个变量集合（“cntry”，“eisced”，“hhmmb5”，“prof2”）。

### **TABLE 5.7**

在不同的模拟情况下，选择一组匹配变量的次数。

<table>
     <tr>
        <td>情况</td> 
        <td> <b>选定的匹配变量<b> </td> 
        <td> <b>Freq. <b> </td>
        <td>$$\sqrt { ( M S E ( d ) } / d ^ { * }$$</td>
     </tr>
     <tr>
        <td rowspan="4">(a)</td>    
  		  <td>chldhm cntry eisced</td> 
      	<td>19</td> 
        <td>0.02%</td>
     </tr>
     <tr>
        <td>cntry eisced gndr</td> 
        <td>23</td> 
        <td>0.02%</td>   
     </tr>
     <tr>
        <td> $cntry$ $eisced$ $icpart1$ </td> 
        <td>57</td> 
        <td>0.02%</td>
      </tr>
      <tr>
        <td>cntry gndr hhmmb5</td> 
        <td>1</td> 
        <td> </td>
      </tr>
   <tr>
        <td rowspan="3">(b)</td>    
  		  <td>chldhm cntry eisced</td> 
      	<td>8</td> 
        <td>0.01%</td>
     </tr>
     <tr>
        <td>cntry eisced gndr</td> 
        <td>6</td> 
        <td>0.01%</td>   
     </tr>
     <tr>
        <td> $cntry$ $eisced$ $icpart1$ </td> 
        <td>86</td> 
        <td>0.01%</td>
      </tr>
      <tr>
        <td rowspan="2">(c)</td>    
  		  <td>ageacat cntry eisced</td> 
      	<td>1</td> 
        <td> </td>
      </tr>
      <tr>
        <td> <b>cntry eisced hhmmb5<b> </td> 
        <td>99</td> 
        <td>0.01%</td>   
     </tr>
      <tr>
        <td rowspan="2">(d)</td>    
  		  <td>ageacat cntry eisced</td> 
      	<td>1</td> 
        <td> </td>
      </tr>
      <tr>
        <td> $cntry$ $eisced$ $gndr$ $hhmmb5$ </td> 
        <td>99</td> 
        <td>0.00%</td>   
     </tr>
</table>

&emsp;&emsp;总之，少量的模拟结果表明，传统的选择匹配变量的方法倾向于提供比实际需要更广泛的变量集。只有基于AIC的选择程序，考虑到与要估计的参数数量相关的惩罚，才倾向于识别较小的匹配变量集。如预期的，相对较小的样本（ $n_A$ = 1000 和 $n_B$ = 3000）具有高度的结果异质性。一般来说，用传统的选择程序识别的匹配变量集倾向于比在理想情况下（所有变量均可用）确定的最佳组合更大。

&emsp;&emsp;现在让我们来看一下基于不确定性选择匹配变量的模拟结果（见表5.7）。对于每个样本大小的组合，在100次迭代中，有一个特定的匹配变量组合更频繁地出现（样本大小越大，在表中以斜体显示的频率越高）。只有在 $n_A$ =5000和 $n_B$ =10000的组合中，所选的匹配变量与整个数据集上执行的分析一致（在表中以粗体和斜体显示）；其他组合也包括其他变量（如“icpart1”或“gndr”）。这可能是因为多元关联是最难估计的方面。不管怎样，一旦做出选择， $\widehat{d}$ 的均方误差得到控制，并且其相对于已知参考值 d* 的平方根急剧趋近于零。在模拟设置中， d* 是在整个ESS样本上计算的d，该样本被视为选定各个样本的目标总体。

&emsp;&emsp;正如预期的那样，基于不确定性的程序比基于成对测量的传统程序更为简洁，即使与包括惩罚项的AIC方法相比也是如此。

## **5.4 结论**           
           
&emsp;&emsp;本文概述了在统计匹配应用中选择匹配变量的方法。在分析大规模调查时，这是一个非常耗时的阶段。比较这两种工作方式，这两种方式在简单性和计算工作量方面都非常不同。对于我们处理的分类变量的情况，即家庭调查非常普遍的情况，基于成对关联/预测误差(PRE)度量的传统程序非常简单，计算工作量非常低，但是往往会提供太多的匹配变量，特别是在考虑Cramer's V或Theil's U时。当考虑AIC时，由于惩罚项有利于简化模型，因此选择的变量子集较小。而那些基于不确定性探索的带惩罚项的程序则选择更小而有效的匹配变量子集，但是这些程序计算量较大。一般来说，基于不确定性探索的匹配变量集合往往是基于传统成对度量方法所确定的集合的一个子集。这个结果表明，在存在多个共同变量X的数据源的情况下，可以使用两步程序：在第一步中，使用传统度量方法来确定最相关的共同变量子集，然后在第二步中，可以使用不确定性探索来从第一步所确定的X的子集开始确定匹配变量集。这个复杂的过程将结合两种方法的优点，即传统程序的简单性和基于不确定性的程序的简洁性，并且，由于从可能的变量X的较小子集开始应用不确定性探索，从而减少计算工作量。
