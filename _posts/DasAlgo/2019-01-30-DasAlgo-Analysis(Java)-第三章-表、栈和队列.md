---
layout: post
title: DasAlgo-Analysis(Java) 第三章 表、栈和队列
categories: DasAlgo
tags: DasAlgo
---

### 第三章 表、栈和队列
1. ADT 抽象数据类型
2. A_i 后继 A_{i-1}, A_{i-1} 前驱 A_i, 前驱元和后继元。
3. 表的实现：简单数组实现和链表实现。
- 链表的每个节点包括表元素和链(next链)。
- 双链表
4. Collections API:
- Collection<T> extends Iterable<T>
- Iterable: remove()删除由next()最新返回的项
- 使用Iterable.remove()的两重原因
	- 知道删除项的准确位置，效率更高。
	- 针对 ConcurrentModificationException 的保护机制。
- List ADT 的两种实现方式：ArrayList 和 LinkedList
	- ArrayList 是可增长数组实现
	- LinkedList 是双链表实现
	- ArrayList 的数据域 ensureCapacity 和 trimToSize() 方法
5. 示例：remove方法对LinkedList的应用：删除偶数值项
- 优化一：避免拷贝
- 优化二：get方法改为迭代器
6. 泛型数组的创建是违法的，不可避免地：创建泛型类型限界地数组之后采用类型转换。
7. 内部类、嵌套类的区分在于是否静态。
8. 示例：迭代器优化
- 初始：MyArrayList 和 ArrayListIterator 是平行的类：迭代器无法使用表的数据
- 优化一：迭代器构造时传入表对象：表的数据域的可见性问题
- 优化二：嵌套类：编译器无法计算得出迭代所针对的表的对象
- 优化三：内部类
9. 当声明一个内部类时，编译器则添加对外部类对象的一个**隐式引用**，该对象引起内部类对象的构造。
10. 在每一个内部类的对象都恰好与外部类对象的一个实例相关联的情况下，内部类是有用的。在这种情况下，内部类的对象在没有外部类对象与其关联时是永远不可能存在的。
