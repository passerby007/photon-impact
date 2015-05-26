---
layout: post
title: psd and radial basis function
date: 2015-05-26 23:23:05
categories:
tags:
---

RBF is simple, and easy to implement. It is possible to map *n*-dimension keys to *m*-dimension values.

However one thing need to be noticed is the *m*-dimension values are independent from each other,
it might be a good property, but in some cases, like the PSD, might be not.

But one obvious and annoying problem is the weight matrix, which is used to solve a linear system,
may be singular or ill-conditioned (even worse) because of key data distributions.
And the most depressing thing is you still cannot get expected interpolation pattern
after making many tweaks on parameters of the RBFs. I was already resigned to accept these truth.
