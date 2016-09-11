---
tags:
  - 机器学习
layout: post
title: '机器学习简介'
category: 学习
---

机器学习似乎很火，我也开始研究机器学习了~

<!--more-->

那什么是机器学习呢？ 搜集到的定义有：

* “机器学习是一门人工智能的科学，该领域的主要研究对象是人工智能，特别是如何在经验学习中改善具体算法的性能”。
* “机器学习是对能通过经验自动改进的计算机算法的研究”。 
* “机器学习是用数据或以往的经验，以此优化计算机程序的性能标准。” 
* “A computer program is said to learn from experience E with respect to some class of tasks T and performance measure P, if its performance at tasks in T, as measured by P, improves with experience E.”


看着头大的定义先不管了。。。

用一个例子或许可以更好地阐述机器学习，比较经典的是垃圾邮件的检测。侦测一个单词是否存在并没有太大的作用，然而当某几个特定单词同时出现时，再辅以考察邮件长度及其他因素，人们就可以更准确地判定该邮件是否为垃圾邮件。在这种意义下，机器学习就是把无序的数据转换成有用的信息。




### 机器学习的任务：

***

机器学习的任务主要有三类：分类、回归、聚类和密度估计，涉及到的算法以后再说。


### 模型需要用到的概念：

***

* 假设空间 $ F $：输入空间到输出空间的映射的集合。
* 损失函数：用于度量预测错误的程度。设输入为 $X$，输出为 $Y$，$f \in F$，损失函数记为 $L(Y,f(x))$，常用的损失函数有：
 * 0-1 损失函数：$$ \begin{eqnarray}L(Y,f(X))=
\begin{cases}
1,Y \neq f(X) \cr 0,Y = f(X)
\end{cases}
\end{eqnarray} $$
 * 平方损失函数：$$ L(Y,f(X))=(Y-f(X))^2 $$
 * 绝对损失函数：$$ L(Y,f(X))= \vert Y-f(X) \vert $$
 * 对数损失函数或对数似然损失函数：$$ L(Y,f(X))= -\log P(Y \vert X) $$

  损失函数越小，模型就越好。

* 经验风险：模型 $f(X)$ 关于训练数据集 $ T={(x _1,y _1),(x _2,y _2),\cdots,(x _N,y _N)} $ 的平均损失称为经验风险，记作 $ R _{emp}(f) $ ： $$ R _{emp}(f)=\frac{1}{N} \sum _{i=1}^N L(y _i,f(x _i)),(x _i,y _i)\in T $$
