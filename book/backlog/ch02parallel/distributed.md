---
weight: 1204
title: "2.4 分布式计算的基本概念"
bookHidden: true
---

# 2.4 分布式计算的基本概念


关于时间的研究从牛顿到爱因斯坦，直到相对论的发展，我们才知道了光速与观察者无关。
根据这个假设，相对论证明了在一个参考系下同时发生的时间，对于相对此参考系运动的观察者并非同时。
从而对于两个不同的观察者而言，事件顺序可能发生错乱。

分布式计算中，物理上时间的概念也具有不确定性。我们不禁要问，当需要观察某个分布式系统中，
某个确定事件的某些状态是否同时出现。这一点可以体现在并行垃圾回收器中，因为我们不可避免的
需要观察某个对象是否已可以回收，从而需要观察并行线程关于此对象的引用状态以及进程间的通信。

## 分布式时序

一个分布式系统 $P$ 通常由 N 个进程（或线程）$p_i (i=1, 2, ..., N)$ 组成。

## 向量时钟算法

向量时钟算法提供了一个 能够得到与事件时序同构的严格偏序关系 $V$，即有若 V(e) < V(e') 则 e < e'。

设分布式系统中 N 个进程维护自身的时钟 $V_i$，用于给本地事件加时间戳。当进程发送消息时，附带自身维护的时钟。
则在初始情况下 $V_i [j] = 0, i,j = 1, 2, ..., N$。

## 全局状态谓词

## 全局谓词的性质

## 小结

## 许可

&copy; 2018-2020 The [golang.design](https://golang.design) Initiative Authors. Licensed under [CC-BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/).