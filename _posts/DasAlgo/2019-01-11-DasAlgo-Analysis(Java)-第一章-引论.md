---
layout: post
title: 2019-1-11-DasAlgo_Analysis(Java)_第一章_引论
categories: DasAlgo
tags: DasAlgo
---


### 第一章 引论
1. 选择问题和字谜问题。
2. 系列公式：
```math

(0) log 1024=10\ |\  log1048576=20

\text{几何级数}

(1)\ \sum_{i=0}^N{2^i}=2^{N+1}-1

(2)\ \sum_{i=0}^N{A^i}=\frac{A^{N+1}-1}{A-1}

(3)\ \sum_{i=0}^N{A^i}\leqslant\frac{1}{1-A}\ (0<A<1)

(4)\ S=\sum_{i=0}^\infty{A^i}=\frac{1}{1-A}\ (0<A<1)\text{(证明可以使用错位相减法)}

(5)\ S=\sum_{i=1}^\infty{\frac{i}{2^i}}=2

\text{算术级数}

(6)\ \sum_{i=1}^N{i}=\frac{N(N+1)}{2}

(7)\ \sum_{i=1}^N{i^k}\approx\frac{N^{k+1}}{|k+1|}\ (k\neq -1)

(8)\ \sum_{i=1}^N{i^2}=\frac{N(N+1)(2N+1)}{6}\approx\frac{N^3}{3}

\text{调和数，调和和}

(9) H_N=\sum_{i=1}^N\frac{1}{i}\approx\ln{N}

(10) \lambda=\lim_{n->\infty}[(\sum_{k=1}^N\frac{1}{k})-\ln{N}]\approx0.57721566\text{(9 式误差趋于常数，即欧拉常数lambda)}
```

3. 概念：程序瓶颈，(数项)级数，收敛和发散，模运算(尽量避免模运算)。
4. 对于无穷级数，只有收敛级数可以采用错位相减法。
5. 证明的方法：<br>
(1)归纳法证明：基准情形->归纳假设->归纳推理
(2)反证法证明<br>
6. 递归简论：一个函数用它自己来定义。<br>
(0)数学依据：归纳法<br>
(1)基准情形原则。<br>
(2)不断推进原则。<br>
(3)设计法则：假设所有的递归调用都能运行。<br>
(4)合成效益法则：去除重复性规则。<br>
7. 泛型机制<br>
(0)概念：泛型实现，类型参数，特定类型的参数表，显式泛型方法，原始类，擦除类型。<br>
(1)使用 Object 实现泛型：a.类型转换问题 b.基本类型问题(使用不可变的包装类解决)。<br>
(2)使用接口类型实现泛型：a.用户定义接口与库类问题 b.final 类问题(可以使用函数对象来解决)。<br>
(3)与数组：数组具有协变性，而泛型具有不可变性(类型兼容的数组称为协变数组类型；数组具有协变性，故通过编译，运行时报ArrayStoreException.)；数组是具体化的，而泛型是可擦除的。<br>
(4)泛型的意义在于：将运行时错误提前到编译错误。<br>
(5)失去协变性也就失去了一定的灵活性。<br>
(6)类型限界：
```
public static <T extends Comparable>...
//使用父接口方法是，并不能确定操作对象类型。

public static <T extends Comparable<T>>...
//逻辑错误：T_par实现了Comparable<T_par>,T extends T_par,T IS-A Comparable<T_par> IS-NOT-A Comparable<T>

public static <T extends Comparable<? super T>>...
//最终结果
```
(7)对泛型的限制：a.基本类型不能用作类型参数; b.instanceof 检测和类型转换只对原始类型进行; c.static 语境; d.泛型类型的实例化 e.泛型数组对象 f.参数化类型的数组
8. 函数对象：没有数据只有一个方法的类的实例化，一个函数通过将其放在一个对象内部而被传递。函数对象的意义在于进行方法的传递。
　　　　　　　　　　　　　　　　　　　　　　　　　Written by [ZenMoore](https://github.com/ZenMoore "Github")<br>
　　　　　　　　　　　　　　　　　　　　　　　　　1/11/2019 20:22:54 PM 

