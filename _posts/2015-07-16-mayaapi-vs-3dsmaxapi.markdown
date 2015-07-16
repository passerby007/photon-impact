---
layout: post
title: MayaAPI vs 3dsMaxAPI
date: 2015-07-16 23:46:24
categories:
tags:
---

3dsMax API流露的是浓浓的90年代气息，GetCoreInterface(), GetCoreInterface1(), GetCoreInterface2()...
是在太坑爹。就像是一台年久失修的老机器，没法把它砸了重来，又不得不维护，只好捏着鼻子往上加各种补丁。

Maya API刚好走了另一个极端，坚决贯彻数据（MObject）和方法（MFn）分离的思路，凡事皆是MObject，
但是后果就是你往往不知道MObject到底是什么。当所有的方法都是返回MObject的时候，你将无法直接从返回
类型一目了然地知道实际数据是什么。而且，过度封装的后果就是，严重影响运行效率。
