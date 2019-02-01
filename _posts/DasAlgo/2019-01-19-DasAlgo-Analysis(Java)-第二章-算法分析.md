---
layout: post
title: DasAlgo-Analysis(Java) 第二章 算法分析
categories: DasAlgo
tags: DasAlgo
---


### 第二章 算法分析
1. T(N)=O(f(N)) / =o(f(N)) / =\Omega(f(N)) / =\omege(f(N)) / =\Cita(f(N)) 的定义。
![image](https://img-blog.csdn.net/20180507150704920)
2. T(N)=O(f(N))，则f(N)是T(N)的上界，相应的，有下界。
3. 三个法则：<br>
(1)如果T_1(N)=O(f(N))且T_2(N)=O(g(N)),那么：<br>
  (a)T_1(N)+T_2(N)=O(f(N)+g(N))<br>
  (b)T_1(N)*T_2(N)=O(f(N)*g(N))<br>
(2)如果T(N)是一个k次多项式，则T(N)=\Cita(N^k)<br>(3)对任意常数k，log^k{N}=O(N)
4. 通过极限确定两个函数的相对增长率。
```math
lim_{N\to\infty}{\frac{f(N)}{g(N)}}
```
- 极限是0，f(N)=o(g(N))
- 极限是c!=0,f(N)=\Theta(g(N))
- 极限是\infty,g(N)=o(f(N))
- 极限摆动，二者无关
5. if/else语句的运行时间从不超过判断的运行时间再加上S1和S2中运行时间长者的总的运行时间。
6. 分析的基本策略是：从内向外，先析方法调用。
7. 递归的分析：(1)假递归：等效为for循环;(2)求解递推关系。
8. 最小子序列和问题的四种算法。
9. 联机算法都是线性时间，但是其正确性的证明较困难。
10. 具有运行时间的对数特点的三个典型例子：折半查找，欧几里得算法，幂运算
11. 下界的证明一般是最困难的，因为它们不只适用求解某个问题的一个算法而是适用求解该问题的一类算法。<br>

Written by [ZenMoore](https://github.com/ZenMoore "Github")<br>
1/19/2019 20:07:54 PM 