---
draft: true
date: 2023-03-05T16:16:02-05:00
title: "Dask Tutorial Part 1"
description: ""
tags: 
    - dask
    - python
categories:
    - tutorial
---

## What is Dask?

There are many answers to this question, the one I prefer is this: a Python library for larger-than-memory computation and parallel computation.

Let's see a simple example.

```python
import dask
def add(a, b):
    return a + b

fut = dask.delayed(add)(1, 2)
ret = dask.compute(fut)
```