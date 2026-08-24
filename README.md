# 认知行为的计算原理

## Acknowledgment

* 感谢教育部高等学校心理学类专业教学指导委员会教育教学改革项目的支持
* Our project is supported by the GitBook's free community plan. We deeply appreciate GitBook's help.

## 书名

《认知行为计算原理》

## 目标

本书主要针对国内心理学本科/硕士/博士学生，目标成为心理学科本科或者研究生相关课程的教科书。本书希望介绍计算认知科学和认知神经科学中常用的计算建模思想和方法，本书内容也希望帮助到计算机等工科希望从事交叉科学研究学生，以及精神病学、神经科学和基础医学的学生。

## 教学材料

本书基于张洳源过去几年在上海交通大学和华东师范大学的教学实践，主要基于以下两门课程

* 《计算认知与人工智能》，上海交通大学，心理学，研究生选修课，[课程链接](https://ruyuanzhang.github.io/teaching/CompCogAI/CompCogAI.html)
  * <mark style="color:purple;">2023年春季学期上海交通大学全校全门类1619门课中学生教学评价排名第1</mark>
* 《数学建模》，华东师范大学，心理学，本科生专业选修课，[课程链接](https://ruyuanzhang.github.io/teaching/MathModel/MathematicalModeling.html)

## 作者列表

主要负责人：张洳源，北京大学心理与认知科学学院

学术委员会：胡传鹏(南京师范大学)，胡啸(北京师范大学)，胡扬(华东师范大学)，胡捷(华东师范大学)

## 写作形式

本书采取众筹的形式，每一个章节指定一名章节负责人，可以是老师或者学生。并且每一个章节招募1-3名学生志愿作者。由志愿学生撰写主要内容，章节负责人润色和审核。

* 第一章: 高雨燕(负责人)，王晓霞，葛威
* 第二章: 施稚霖(负责人)，陆新泉，谭启瑶
* 第三章: 林也(负责人)，吴国伟，陈怀雪
* 第四章: 胡啸(负责人)，郑玮琦，邹季言，徐心怡
* 第五章: 游毓琦(负责人), 申雨菡，谭敬斌
* 第六章: 胡传鹏(负责人), 孙宇鸿，苏瑞，方圆，夏澍恺
* 第七章: 郭鸣谦(负责人)，许扬
* 第八章: 王滢洁(负责人), 程练， 赵洒洒，李凌宇
* 第九章: 夏澍恺(负责人)
* 第十章: 黄尚晶(负责人), 陈率, 雷晓璇，路子童

另招募1-2名具有美术设计功底，会photoshop，illustrator等工具的人员

* 温秀娟



## 写作的一些格式原则

### 文字

* 每一个页面，都用H1, H2依次排列下面的子标题，不要用数字标题。

### 思考题

当需要提出一些思考题时，可以用hint的格式

{% hint style="info" icon="question" %}
请问学习率是越高越好么？
{% endhint %}

### 图

* 请用(章节号-图号)来表明每一个章节图。例如，第二章节的第10张图，用“图2-10”来表示。

### 公式

* 请用(章节号-公式号)来表明每一个章节图。例如，第二章节的第5个公式，用公式2-5来表示。
* 在写公式的时候，用 \qquad (2-5)来表示，例如

$$
f(x) = x * e^{2 pi i \xi x} \qquad (2-5)
$$

## 代码块和结果

我们的代码块和运行结果，都用code block的格式，只不过一般代码用python的语法格式，运行结果用plain的语法格式，如下图

{% code overflow="wrap" %}
```python
import numpy as np
a = np.random.rand(3,4)
print(a.shape)
```
{% endcode %}

{% code overflow="wrap" %}
```
(3,4)
```
{% endcode %}

### 参考文献

* 每个章节的参考文献请统一放到后面的Appendix里面
* 参考文献一律用数字来表示，引用格式为nature系列杂志投稿格式，例如

> Klaholz, B. P., Myasnikov, A. G. & Van Heel, M. Visualization of release factor 3 on the ribosome during termination of protein synthesis. Nature 427, 862–865 (2004).
