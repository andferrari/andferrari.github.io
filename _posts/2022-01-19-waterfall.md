---
layout: post
title: Waterfall plot 💻
date: 2021-09-09
description: A simple waterfall julia plot
tags: formatting images
categories: sample-posts
thumbnail: assets/img/9.jpg
---

Simple [Plots.jl](https://github.com/JuliaPlots/Plots.jl) receipe for waterfall plots 
(a la [Unknown Pleasures](https://gist.github.com/andferrari/3e254ffd67629078c1aaad95caf23079) 😀). Install using:
```julia
pkg> add https://github.com/andferrari/WaterFall.jl
```
and
```julia
using WaterFall
x = [exp(-(n - 1e-2*τ^2)^2/τ)  for n in 0:300, τ in 40:10:160]
plotfall(x, w=2)
```
