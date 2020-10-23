---
layout:      post
title:      ".py | matplotlib笔记：两种API"
keywords:   ""
excerpt:    "import matplotlib.pyplot as plt"
date:        2020-10-04
categories:  post
milestoneID: 19
---

“图”这个字在英语中可以对应好几个词，picture, image, figure, plot... 其中的 plot，意思是展示两组或两组以上的数据之间关系的图像。用时髦一点的话说，就是数据可视化的产物。  

所谓`matplotlib`，顾名思义，~~`mat` 表示山寨 MATLAB~~，`plot` 的含义如上所述，`lib` 表示这是 python 的[一个第三方库 (library)，而不是某种领域专用的编程语言 (domain specific languange, DSL)](http://www.yinwang.org/blog-cn/2017/05/25/dsl)。

所谓 API，全称是 application programming interface, 应用程序接口，约等于在你有了自己的数据，想调用 matplotlib 来画图的时候，那些需要写在你自己代码里的语句的语法规则。

因为是代码库，所以在一切开始之前，需要在你的 python 代码开头声明引入

```python
import matplotlib.pyplot as plt
```

`plt` 可以换成你喜欢并且不和其他代码冲突的名字，但是这三个字母是大家的约定俗成的，网上的绝大多数示例代码都这么写，~~照抄就完事了。~~

## `matplotlib` 的两种 API

`matplotlib` 有两种 API，（其实还有第 3 种 `pylab`，但它没能经得起时间的检验，已经处于官方极不推荐的状态），分别是：

- 基于状态的 (state-based)
- 面向对象的 (object-oriented)

两种风格混用的话大概率没法玩得转，会产生各种出人意料的输出结果，新手 debug 的能力又比较差，所以最好先选边站队，有时间再学剩下的一个。

对于有 MATLAB 基础的朋友，基于状态的 API 语法和 MATLAB 几乎一模一样，几乎可以直接上手，当年 python 算是后起之秀，这一招当初就是为了从 MATLAB 那里吸引用户， ~~相当歹毒。~~ 这套接口本身也比较简单，适合在调试程序的时候快速看一下结果，检查错误。

对于一般的初学者，matplotlib 的代码本身就是用面向对象的编程范式写成的，学习这套 API 可以更好的理解代码，知道自己究竟在干什么，顺便还可以熟悉一下面向对象的编程范式。现在学 python 之前就会 MATLAB 的人越来越少，网上 ~~可供复制粘贴~~ 的示例代码越来越多地使用面向对象的语法，学习面向对象的接口也更加实用。

## 两种 API 的相同任务

{% maincolumn "assets/photos/2020-10-04_figure-and-axes.png" "" %}

上图来自网上随便找的一篇论文，可以看到，一般我们会把信息相关的几幅小图放在一起，在文章排版的时候，这张组合在一起的图片算作一个单位。在 matplotlib 里面，这样一个基本单位叫做 `figure`，而每一幅小图叫做 `axis` （变量名常简写作 `ax`）。平时的单图可以看作只有一个 `axis` 的 `figure`，多图的时候往往用一个 tuple `axes` 的 `__getitem__()` 方法来控制每个子图。

{% maincolumn "assets/photos/2020-10-04_anatomy-of-figure.png" "" %}

上图[来自官网](https://matplotlib.org/gallery/showcase/anatomy.html#anatomy-of-a-figure)，图中的蓝字就是 matplotlib 认为的一张只有一个 axis 的 figure 所包含的元素。

两种 API 要做的事情，就是建立 `figure` 和 `axis`，然后提供函数/方法来生成或者改变各个元素。

## 基于状态 (state-based)

所谓基于状态的 API，不太好解释，前面已经说过，在每个函数前面加上 plt，剩下的就和写 MATLAB 几乎完全一样。

看[官网给出的教程](https://matplotlib.org/tutorials/introductory/pyplot.html#sphx-glr-tutorials-introductory-pyplot-py)，可以观察到两个有趣的现象：

- 几乎没有赋值运算符 `=`
- 几乎所有的 `.` 前面都是 `plt`

也就是说，与 matplotlib 相关的命令都是函数，而且不需要将返回值赋给任何变量。`figure` 和 `axis` 的概念被隐藏起来了，`plt.figure()` 建立一个 figure；`plt.subplot()`建立多个 axes，并且将程序的注意力放到函数参数指定的子图上；紧跟着的设定各种元素的函数都会作用到之前最新一个 `plt.subplot()` 所指定的子图上。

没有赋值说明函数的返回值并不重要，这些函数都会作用在后台维护的 figure 和 axis 的状态机上面，也就是说这些函数都有副作用，不是纯函数。

## 面向对象 (object-oriented)

[作为对比](https://matplotlib.org/gallery/showcase/anatomy.html#anatomy-of-a-figure)：

- 头几句会有赋值运算符 `=`，被赋值的变量名一般就是 `fig` 和 `ax`。
- `.` 前面都是 `fig` 和 `ax`，其中 `ax` 居多。

`fig` 和 `ax` 分别是 `matplotlib.figure.Figure` 和 `matplotlib.axes.Axes` 两种对象的实例，画图和调整都是在调用两种对象的方法，主要是 `ax` 的方法。

## 不同之处 Cheat Sheet

绝大多数命令，在两种 API 之下的名字都一样，差别就在于开头究竟是 `plt.` 还是 `ax.`，但是少数命令不同，下面做了一个表格，进行一个不完全的列举：

| State-Based | 任务 | Object-Oriented |
|---|---|---|
|`plt.figure(**args)`|__新建 figure__|`fig = plt.figure(**args)`|
|`plt.subplot(**args)`|__新建 axis__|`ax = fig.add_subplot(**args)`|
|好像没有|__同时新建 figure 和复数 axes__|`fig,axes = plt.subplots(**args)`|
|`plt.title(**args)`|__设置 figrue 标题__|`ax.set_title(**args)`|
|`plt.xlabel(**args)`|__设置 x 轴名称__|`ax.set_xlabel(**args)`|
|`plt.ylabel(**args)`|__设置 y 轴名称__|`ax.set_ylabel(**args)`|
|`plt.xlim(**args)`|__设置 x 轴范围__|`ax.set_xlim(**args)`|
|`plt.ylim(**args)`|__设置 y 轴范围__|`ax.set_ylim(**args)`|

其他不同的命令，以后用到的时候会随手更新。
