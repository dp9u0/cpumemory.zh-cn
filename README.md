# What Every Programmer Should Know About Memory

本文翻译自文章[What Every Programmer Should Know About Memory](https://people.freebsd.org/~lstewart/articles/cpumemory.pdf)

## 目录

1. [Introduction](01.introduction.md) : 前言
2. [Commodity Hardware Today](02.commodity-hardware-today.md) : 现代商用硬件
3. [CPU Caches](03.cpu-caches.md) : CPU缓存
4. [Virtual Memory](04.virtual-memory.md) : 虚拟内存
5. [NUMA Support](05.numa-support.md) : NUMA支持
6. [What Programmers Can Do](06.what-programmers-can-do.md) : 程序员可以做什么
7. [Memory Performance Tools](07.memory-performance-tools.md) : 内存工具
8. [Upcoming Technology](08.upcoming-technology.md) : 未来的技术
9. 附录
* A. [Examples and Benchmark Programs](A.examples-and-benchmark-programs.md)
* B. [Some OProfile Tips](B.some-oprofile-tips.md) : 一些性能分析的建议
* C. [Memory Types](C.memory-types.md)
* D. [libNUMA Introduction](D.libnuma-introduction.md)
* E. [Index](E.index.md)
* F. [Bibliography](F.bibliography.md)
* G. [Revision History](G.revision-history.md)

## 词汇表

* memory: 内存
* memory controller: 内存控制器
* virtual memory: 虚拟内存
* main memory: 主存
* Direct Memory Access,DMA: 直接内存存取
* mass storage: 大容量存储设备
* cache: 缓存
* Random-Access Memory,RAM: 随机存取内存
* Non-Uniform Memory Access,NUMA: 非统一内存访问

## 说明

1. 关于注释: 注释原文与翻译被统一放在文档的最后,并提供锚点跳转功能,方便查看和回退
2. 关于专有名词等由于翻译可能导致有所歧义的词汇,翻译过程中将尽可能的提供原文词汇作为参考: 例如 mass storage 将翻译为: 大容量存储设备(*mass storage*),并在后面用斜体字标注原文.
3. 标点符号: 尽可能使用半角标点
4. 对于习惯使用的词汇不会进行翻译,例如RAM ,ROM 等

## Reference

* [What Every Programmer Should Know About Memory](https://people.freebsd.org/~lstewart/articles/cpumemory.pdf)
* [系列文章](https://lwn.net/Articles/250967/)
