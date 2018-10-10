---
layout: post
category: "machine learning"
title:  "CUDA GPU加速"
tags: [CUDA,GPU加速]
---

1. An Even Easier Introduction to CUDA

https://devblogs.nvidia.com/even-easier-introduction-cuda/
	
	a. nvidia编译： nvcc add.cu -o add_cuda
		cuda file extension with '.cu'
	b. 度量kernel运行效率: nvprof
		nvprof ./add_cuda

	GPU bandwidth throughput是如何计算的？

2. CUDA C Best Practices Guide

https://docs.nvidia.com/cuda/cuda-c-best-practices-guide/index.html#abstract

	Assess -> Parallelize -> Optimize -> Deploy

	Assess: 评估
	对于现有项目，第一步是评估应用程序以找到负责大部分执行时间的代码部分。有了这些知识，开发人员可以评估这些瓶颈以实现并行化并开始研究GPU加速。

	通过了解最终用户的要求和约束，并应用Amdahl和Gustafson定律，开发人员可以通过加速应用程序的已识别部分来确定性能改进的上限。