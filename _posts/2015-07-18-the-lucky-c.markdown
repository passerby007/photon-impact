---
layout: post
title: The Lucky C++
date: 2015-07-18 23:49:35
categories:
tags:
---

C++一度处境不妙，事实上感觉是越来越处境不妙，因为越来越多的程序员，越来越多的工作岗位，集中在web，
app development上。这些领域通常来讲，都是通过平台专用语言，或是脚本框架来完成。于是，从整体比例
来看，人们也越来越不倾向于学习和使用C++。虽然C++1x终于让这门语言变的现代化了，但是似乎为时已晚，
反而让批评和否定C++的程序员增加了一个理由：然并卵，C++更复杂了。。。

不过，很搞笑的是，可能C++比大家认为的情况要幸运一点。世界上最赚钱的移动平台iOS，使用Object-C/
Swift，而世界上使用人数最多的移动平台Android，使用Java。两个平台的原生开发语言，老死不相往来;
instead, C++ is natively supported on both platoforms! On ios, Object-C++ is used
to bridge the gap between Obj-C and C++, and Android directly provide NDK for C++
development. Because no ambitious team would ignore either of these two platforms,
so we see many of them adopting the solution that uses C++ to develop core modules,
and uses native languages to develop the GUI part. When you add new features to
the core, or fix bugs in the core, usually they can be applied to all platforms
at the same time. If consider the feature of low runtime cost, as claimed by C++
committee, we can expect to gain performance benefit from this solution.

C++ is still cool~
