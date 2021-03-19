---
layout:      post
title:      ".mpipks-note | 02. 朗之万方程和主方程"
keywords:   "mpipks-note"
excerpt:    "这次讨论的主要内容很让我意外地落回了各种数学细节里。"
date:        2021-02-04
categories:  post
milestoneID: 28
---

上周三老板和艾萨鸽了，但是我们还是照常进行了讨论，然后讨论的主要内容很让我意外地落回了各种数学细节里，可能是本科生不在，我们都不好意思形而上的缘故吧。

## 疾病传播的朗之万方程——随机指数传播

两个要点：
1. 在有随机项的情况下，$$ d[log(x(t))] \neq (1/x)(dx/dt) $$
2. 前面 Ito formula 里面的 $$a$$, $$b$$ 和后面 $$a=\mu+\sigma\xi(t)$$ 里的 $$a$$ 容易弄混。

## 维纳过程 (Wiener process)

讨论过程中他们问我有什么问题，我当时正在走神（呃），于是随口问了一句：讲义第4页左侧的式子为什么等于零……老实把表达式展开就知道，是后面一项 $$\left<W_{t_{j+1}}-W_{t_{j}}\right>=0$$

讲义中维纳过程是作为第一讲中的高斯噪音的积分出现的，也就是：$$dW(t)=\xi(t)dt$$，其中高斯噪声满足以下两个条件：
- (1).  $$\left<\xi(t)\right>=0$$
- (2).  $$\left<\xi(t_1)\xi(t_2)\right>=\delta(t_2-t_1)$$

但是[维基百科中的介绍](https://zh.wikipedia.org/wiki/%E7%BB%B4%E7%BA%B3%E8%BF%87%E7%A8%8B)是直接定义了维纳过程本身，它应该是满足如下三个条件的随时间改变的随机变量 $$W(t)$$：
- (1). $$W(0)=0$$
- (2). 映射 $$t\mapsto W(t)$$ 在正实数轴上几乎处处连续
- (3). 对于两个不重叠的时间段 $$0 \leq s_1 < t_1 \leq s_2 < t_2$$, $$W(t_1-s_1)$$ 和 $$W(t_2-s_2)$$ 独立，$$W(t-s)\sim N(0,t-s)$$

这两种定义等价吗？好像是，没仔细想。不过维纳过程的存在是为了对布朗运动进行建模，布朗运动可以看作随机行走在步长趋近于0时的极限；在一年级学过的数学物理方法里，扩散方程的解也可以看作随机行走者经过时间t之后在不同位置出现的概率，也是取步长为0的极限。所以 $$\xi(t)$$ __似乎__ 可以导出 $$W(t)$$，甚至可以不要求 $$\xi(t)$$ 具有高斯分布。

以上似乎有类比谬误的嫌疑，而且假如思路正确的话，会引出一个新的问题——扩散方程的推导来自 Fick 定律，这个过程在何处引入了对随机变量在时间上的积分？

好吧，扯完了之后发现了这个链接：[http://physicallensonthecell.org/advanced-diffusion-and-fokker-planck-picture](http://physicallensonthecell.org/advanced-diffusion-and-fokker-planck-picture)

##  随机变量 vs. 时间变量

对于 $$\xi(t)$$ 函数的第二条性质，我在草纸上顺手写了如下等式：

$$ \left<\xi(t)\xi(t')\right>=\delta(t-t')=\frac{\int_{start}^{end}\int_{start}^{end}\xi(t)\xi(t')dtdt'}{\int_{start}^{end}\int_{start}^{end}dt\ dt'} $$

但是实际上，此处的 $$\left<\right>$$ 应该是随机变量的期望值，也就是

$$ \left<\xi(t)\xi(t')\right>=\int_{-\infty}^{\infty}\int_{-\infty}^{\infty}x_1 x_2 p(\xi(t)=x_1,\xi(t')=x_2)dx_1dx_2 $$

跟 t 没什么关系。在平衡态统计中，系综满足 ergodicity，两者应该是相等的。但在非平衡态下没有这种保证。

随机变量说是变量，实际上需要一个函数来描述，而这个函数的“自变量”是这个随机变量的所有可能取值，这个函数的输入和输出变量之间不是因果关系，这究竟是哥本哈根学派战胜隐变量理论的过人之处，还是新的隐变量理论可能的突破口呢？再往下胡扯存在被当成民科的可能，暂且打住。

## 主方程解得指数分布：随机变量的特征函数 (characteristic function in probability theory)

讲义第 9 页掉落了一件重要装备——解为指数分布的主方程：

$$ \frac{d}{dt}p(n,t) = \lambda \left[p(n-1,t)-p(n,t)\right] $$

上面说随机变量需要用一个函数来描述，但是究竟用哪个函数，却可以有多种选择。最直观的就是中学就学的，离散变量的概率分布函数和连续变量的概率分布密度函数。好处是意思直观，缺点是对于离散变量和连续变量需要分别讨论，两种函数的量纲不同，概率密度的量纲等于随机变量量纲的倒数。

为了统一量纲，所以有了累积分布函数，对离散和连续变量 $$X$$ 的定义都是一样的：$$F(x)=prob(X<x)$$。离散变量的概率分布函数是累积分布函数的差分 (difference)，连续随机变量的概率密度则是累积分布函数的微分 (differential)。

在本节第 9 页的例子里，给出了第三种函数——[特征函数](https://en.wikipedia.org/wiki/Characteristic_function_(probability_theory))，对于一个随机变量 $$X$$ 与其所有的可能取值 $$x$$，特征函数引入新的自变量 $$s$$，由 $$e^{isX}$$ 的期望值给出，也就是说，特征函数是对随机变量的一个 __变换__。

$$ G_X(s) = \left<e^{isX}\right> = \sum_x prob(X=x)e^{ixs}$$

因为指数函数的导数还是指数函数，所以在微分方程里很有用，下面也确实是这么用的。用变换解微分方程的套路，上一节已经遇到了，只不过研究的是动力学，总是拖着一个并未参战的 $$t$$，而且笔记里的形式参数和实际参数并不明确，要是在 C 语言里这么写，是会被测试打死的:
$$G(s,t)_{[笔记里的写法]}:=G_{N或者n[被变换的随机变量]}(s_{[特征函数真正的自变量]},t_{[时间，打酱油的]})$$

## 福克-普朗克方程 (Fokker-Planck equation)

第 10 页，Kramers-Moyal 展开的写法是：

$$ \partial_tp(x,t) = \sum_{n=1}^{\infty}\frac{(-1)^n}{n!}\partial_x^n\alpha_n(x)p(x,t) $$

维基百科上的写法是

$$ \partial_tp(x,t) = \sum_{n=1}^{\infty}\frac{(-1)^n}{n!}\partial_x^n\left[\alpha_n(x)p(x,t)\right] $$

从后一页的算式来看应该是后者，前者写法不规范。



