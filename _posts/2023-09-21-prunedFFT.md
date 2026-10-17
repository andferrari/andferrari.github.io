---
layout: post
title: PrunedFFT 💻
date: 2021-09-09
description: Fast subset of a 2D FFT
tags: formatting images
categories: sample-posts
thumbnail: assets/img/9.jpg
---

You need to compute a **subset** of the outputs of a 2D FFT 
with a **large zero padding**? Try [PrunedFFT.jl](https://github.com/andferrari/PrunedFFT.jl). It works also on GPU🔥

```julia
using PrunedFFT

n = 128
x = rand(n, n)
n_pad = 1024
k_span = collect(512:612)

f = pruned_fft(x, n_pad, k_span)
```

If `CUDA.jl` is installed
```julia
using CUDA

xc = cu(x)
f = pruned_fft(xc, n_pad, k_span)
```

For a very large zero padding, GPU🔥 acceleration is a must!
```
julia> @time f1 = pruned_fft(xc, n_pad^2, k_span);
 0.713510 seconds (78.25 k allocations: 1.792 GiB, 17.73% gc time)

julia> @time f1 = pruned_fft(x, n_pad^2, k_span);
19.362908 seconds (2.25 k allocations: 9.985 GiB, 3.82% gc time)
```