# 客户数据分析项目

数据集包含2010年12月到2011年11月约一年的某电商平台订单记录，共计54万多条数据，8个属性，涉及用户ID、下单时间、地点（国别）、下单商品数量、商品单价、商品代码和描述。

本篇内容主要为拿到数据集后，没有明确问题导向下进行的探索性分析。整体思路是按照“人-货-场”的分析框架展开，文章结构如下：

1.  数据概览和清洗 
2.  年度数据总览 
3.  产品类别探索 
4.  用户细分 
5.  销售的时间序列分析 
6.  总结


* 商品描述、顾客ID和国别存在缺失值，下单时间不是时间格式，由于顾客ID缺失，缺失用户相关的回购率复购率及分类指标均无法对应，我在这里选择删除顾客ID缺失的数据

* 订单号列：一般为6位数，清洗完后发现大部分不符合格式的，前面跟了个C，表示canceled，即为退单号。

* 产品号列：主要由数字构成，但其中有纯英文构成的，筛选出这部分数据，发现是商品产生的附加费用，如邮费、人工费等，这部分由于不是商品，也要进行剔除。

参考文档：

![hpIBa4](https://upiclw.oss-cn-beijing.aliyuncs.com/uPic/hpIBa4.png)

https://www.kaggle.com/carrie1/ecommerce-data

https://github.com/Sillians/E-Commerce-Customer-Segmentation-Project/blob/master/E-Commerce%20Customer%20Segmentation.ipynb

https://github.com/abakliwal12/ML-Hackathon/blob/master/Customer_Segmentation.ipynb
