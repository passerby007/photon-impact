---
layout: post
title: A Pipeline and Engineering
date: 2015-04-18 16:25:23
categories: Thoughts
tags: VFX
---

Different movie productions have various conditions and needs. Every time people start a new movie project, they will very probably have to face with a new pipeline, slightly or dramatically different from previous one, because of numerous assets, tools, and domain-specific solutions. For example, a new movie may introduce a new tool to generate sort of volumetric effects, and thus new assets and caches should be taken care of. So a flexible pipeline saves a lot of lives.

_Flexible_ means **configurable**, **scalable**, and **dynamic** (is there a word with the \*\*ble form to replace the word dynamic?). Really huge topics. Everything should be considered in one big picture. Basically, it's all about abstraction, and abstraction of abstraction; To be a bit more specific, **rules, interfaces, and their combinations**. Currently many studios use shotgun to manage assets. I am not sure if it's powerful enough to build pipelines with its facilities. It could be a foundation for the pipeline, as it is a database to reference all assets and manage project progress. But I still believe a flexible pipeline is much more than that. Every middle-sized team needs to setup their own flexible pipeline. It involves how to design your pipeline modules. There are mostly three kinds of tools, dcc tools/plugins, pipeline tools, and other in-house tools. I strongly eager to know how to define unified rules and interfaces for these tools, so to make them manageable, but I cannot tell right now.

The software engineering concepts are so applicable here. Building a pipeline is just similar to building a software. At the beginning, you write structural code to directly approach your target, and when things turn more complicated, like the software need to handle more situations, the original straightforward code is no more working, you need make sort of abstraction, to make the code more flexible, or understandable. Soon, this one-level abstraction again fails to work, thus a higher level of abstraction is introduced... That's where the **design pattern** comes from (think about the evolution of  `NewObject()`->`FactoryMode`->`AbstractFactoryMode`, or `Callbacks`->`ObserverMode`, or `Messages`->`Signal/Slot`). My personal abstraction on the methodology of design pattern is:

> Abstraction, and abstraction of abstraction.

The idea is highly general; whereas the implementation is interesting, as it reflects the characteristic of a programming language. After many years of working with C++ with hatred of its template, I finally understand the use of the generic programming, and understand the claim, that you only pay for what you need. It's C++-style abstraction. Everything is carefully defined and 'objectized', the type traits are descriptions on types, the iterator defines how you spot an element in a container; Check out the Boost library to see the real battle. The key point is C++ is a static language, and the meaning of generic programing is to combine these 'abstractions' statically at compiling time, so that to achieve both best flexibility and efficiency. You get rare overhead/pay at runtime. You can even do higher abstraction, that is meta-programming.

However, sadly, a dynamic language is more suitable for a movie pipeline. One reason is the running efficiency is not critical in this case, on the other hand, a dynamic language supports updating the pipeline dynamically. With Python, You don't have to compile the code before it can run, you can hot-update a pipeline when it's in service, simply by pushing and replacing the source code. And you can even generate python code in-place or on the fly accordingly. This is the **Dynamic** principle of our pipeline.

After all these nonsense random thoughts, I could eventually fall into sleep at midnight.
