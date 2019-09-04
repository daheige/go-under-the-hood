<div align="center">
<img src="book/assets/header.png" alt="logo" />
<br/><br/>
<a href="./README.en-us.md"><img src="https://img.shields.io/badge/lang-English-blue.svg?longCache=true&style=flat-square" alt="en-us"/></a>
<a href="./README.md"><img src="https://img.shields.io/badge/lang-简体中文-red.svg?longCache=true&style=flat-square" alt="zh-cn"/></a>
<a href="./LICENSE"><img src="https://img.shields.io/github/license/changkun/go-under-the-hood.svg?style=flat-square"/></a>
<a href="./LICENSE"><img src="https://img.shields.io/badge/license-CC%20BY--NC--ND%204.0-lightgrey.svg?style=flat-square"/></a>
<a href="https://www.paypal.me/changkunde/4.99eur"><img src="https://img.shields.io/badge/donate-PayPal-104098.svg?style=popout-square&logo=PayPal"/></a>
<a href="https://t.me/joinchat/FEeulA4zgj2DsBbudBqMcQ"><img src="https://img.shields.io/badge/chat-telegram-%232CA5E0.svg?logo=telegram&logoColor=white&style=flat-square"/></a>
<br/><br/>
<p>Go 语言源码研究 | 基于 <code>go1.13</code></p>
</div>

---

<img src="book/assets/cover-cn.png" alt="logo" height="550" align="right" />

## 致读者

Go 语言从 2009 年诞生之初已有十年的历史。
在这十年的过程中，Go 语言的热度逐渐上升，Go 语言团队也在持续不断的每隔六个月的时间就发布一个全新的 Go 版本。
纵观大多数编程语言的历史进程，令人惊讶的是 Go 语言自身在进化的这十年间，
语言本身并未发生太大变化，Go 语言的用户能够持续不断写出向后兼容的应用。
从语言设计的角度而言，作为一门从诞生之初就考虑低成本高并发、简洁等原则的语言，
很难让人不对其简洁设计背后的各项实现机制以及具体工作原理所好奇。
本书就是一本关于 Go 语言源码分析的书籍。

读者可能会好奇，设计总在演进、源码总在变化，为什么要费力气研究实际工作中可能永远不会接触的源码？
笔者以为不然，因为 "软件工程发生在代码被非原作者阅读之时"，
在阅读源码的过程中，我们除了能进一步加深对语言本身的理解，
更重要的则是理解某个设计背后所使用的根本原理，以及当其他人在实现这个设计的过程中发生的工程实践与技巧。

另外也能会有读者问，源码分析的文章这么多，为什么还要专门写关于源码分析的书？
一个很重要的原因在于笔者在开始阅读 Go 源码并查阅部分资料时，
发现已经存在的资料大多已经存在一定程度上的过时，同时在分析源码的过程中并没有
细致到介绍某段代码的的产生背景、相关知识以及发展历程。
而且 Go 运行时的开发是相当活跃的，因此笔者希望能够通过自己阅读源码这个过程，
在了解到最新版本的动态的同时，也能对整个 Go 源码的演进历史有一定了解。

## 组织结构

本书内容涵盖整个 Go 语言的核心源码，这包括但不限于用户端能直接接触的 Go 运行时 `runtime`、与关键语言特性相关的编译器 `cmd/compile`、
诸多重要的标准库 `sync`/`reflect`/`errors` 等等。
在极少数情况下，本书会讨论不同平台下的实现差异，主要以 Linux/Darwin amd64，以及 Go 1.11 中引入的 WebAssembly 为主。

本书共分为四个部分，第一部分简要回顾了与 Go 运行时及编译器相关的基础理论，并在其最后一章中简要讨论了 Go 程序的生命周期。
第二部分着重关注 Go 的运行时机制，这包括调度器、内存分配器、垃圾回收期、调试机制以及程序的 ABI 等。
第三部分则着眼于 Go 的编译器机制，包括 Go 编译器对关键字的翻译行为，对 cgo 程序的翻译过程，以及链接器等。
最后一个部分则讨论了一些依赖运行时和编译器的标准库，本书只介绍这些标准库与运行时和编译器之间的配合，并不会完整的整个包的源码进行分析。

## 开始阅读

- [🇨🇳 简体中文](./book/zh-cn/TOC.md)
- [🇬🇧 English](./book/en-us/TOC.md)

## 致谢

作者的时间和语言技能均有限。因此如果读者在阅读本书的过程中发现任何错误或可提升的语言表述，欢迎您提交 [Issues](https://github.com/changkun/go-under-the-hood/issues/new/choose) 或 [Pull request](https://github.com/changkun/go-under-the-hood/pulls)，
其具体细节请参考[如何参与贡献](./CONTRIBUTING.md)。
如果您想要关注本仓库的更新情况，可以点击仓库的 `Watch`。如果您喜欢本书，我们也非常高兴能够收到您的 `Star`。

作者特别希望感谢 [@egonelbre](https://github.com/egonelbre/gophers) 所提供的 gopher 图片设计。

---

<div align="center">
<p></p>
<p><a href="https://github.com/changkun/go-under-the-hood">Go under the hood</a> &copy; 2018 - 2019 <a href="https://changkun.de">Changkun Ou</a></p>
</div>



