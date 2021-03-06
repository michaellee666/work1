
析过程的报告  
====
1 数据可视化和摘要
------ 
### 数据摘要
#### 读取数据    

  首先导入pandas模块，读取数据。  
  查看表中各列数据类型  
  ![](https://github.com/michaellee666/work1/blob/master/0.gif)    
  根据数据类型具体分析数值属性，标称属性等  
#### 标称属性可能取值的频数  

  选取标称属性，使用`.value_counts() `函数列出该属性可能取值频数并显示  
  ![](https://github.com/michaellee666/work1/blob/master/1.gif)  
#### 数值属性，给出最大、最小、均值、中位数、四分位数及缺失值的个数  
  选取数值属性，分别使用`.max()`,`.min()`,`.mean()`,`.median()`,`.quantile()`等函数获取属性最大、最小、均值、中位数、四分位数。使用`.isnull().sum()`函数获取缺失值个数。  
  ![](https://github.com/michaellee666/work1/blob/master/2.gif)  
### 数据的可视化  
#### 绘制直方图  
  导入`matplotlib.pyplot`模块，用于数据可视化。导入`statsmodels.api`统计分析库，用于用qq图检验其分布。  
  使用`hist(bins = XX)`函数，绘制直方图。  

  使用`qqplot(df,line='45')`绘制qq图检验数据分布是否为正态分布。  
  ![](https://github.com/michaellee666/work1/blob/master/a.png)
  ![](https://github.com/michaellee666/work1/blob/master/a1.png)  
  ![](https://github.com/michaellee666/work1/blob/master/b.png)
  ![](https://github.com/michaellee666/work1/blob/master/b1.png)  
  ![](https://github.com/michaellee666/work1/blob/master/d.png)
  ![](https://github.com/michaellee666/work1/blob/master/d1.png)  
  ![](https://github.com/michaellee666/work1/blob/master/e.png)
  ![](https://github.com/michaellee666/work1/blob/master/e1.png)  
  ![](https://github.com/michaellee666/work1/blob/master/c.png)
  ![](https://github.com/michaellee666/work1/blob/master/c1.png)  
#### 绘制盒图  
  使用`boxplot()`函数，绘制盒图，，对离群值进行识别  
  ![](https://github.com/michaellee666/work1/blob/master/a2.png)
  ![](https://github.com/michaellee666/work1/blob/master/b2.png)  
  ![](https://github.com/michaellee666/work1/blob/master/c2.png)
  ![](https://github.com/michaellee666/work1/blob/master/d2.png)  
  ![](https://github.com/michaellee666/work1/blob/master/e2.png)  
  
## 数据缺失的处理  
使用`isnull().sum()`函数统计数值属性缺失值数量，有针对性的分析其缺失的原因。  
  ![](https://github.com/michaellee666/work1/blob/master/3.gif)  
### 将缺失部分剔除
使用`dropna()`函数将缺失值进行剔除，并用直方图可视化地对比新旧数据集。  
![](https://github.com/michaellee666/work1/blob/master/n0.png)
![](https://github.com/michaellee666/work1/blob/master/n1.png)  
### 用最高频率值来填补缺失值
使用`mode()`函数获取众数，使用`fillna()`函数填补缺失值。填充后的数据输出到`modefill.csv`，并用直方图可视化地对比新旧数据集。  
  ![](https://github.com/michaellee666/work1/blob/master/a.png)
  ![](https://github.com/michaellee666/work1/blob/master/a3.png)  
### 通过属性的相关关系来填补缺失值  
使用`corr()`函数获取数值属性相关系数。并输出到`corr.csv`文件，查看相关关系。根据相关关系进行填充。  
  ![](https://github.com/michaellee666/work1/blob/master/3.gif)  
使用`apply()`函数，对强相关属性进行填充，填充后的数据输出到`corfill.csv`，并用直方图可视化地对比新旧数据集。  
  ![](https://github.com/michaellee666/work1/blob/master/a.png)
  ![](https://github.com/michaellee666/work1/blob/master/a4.png)  
  
# 图中结构为第二个数据集，第一个数据集方法基本一致，分析过程略。




