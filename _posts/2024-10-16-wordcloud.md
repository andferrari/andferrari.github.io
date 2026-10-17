---
layout: post
title: wordcloud from bib 💻
date: 2024-10-16
description: Create a wordcloud from bib files in julia
tags: formatting images
categories: sample-posts
thumbnail: assets/img/9.jpg
---

Create a wordcloud from `.bib` file

![Wordcloud](/assets/img/posts/wordcloud.png){: width="400"}

```julia
using Bibliography, WordCloud

function all_words(bib_file)	
	imported_bib = import_bibtex(bib_file)
	words = ""
	for ref in keys(imported_bib)
		words = string(words, lowercase(imported_bib[ref].title), " ")
	end
	words
end

path = "/Users/ferrari/Documents/Sites/andferrari.github.io/_bibliography/"
words = all_words(path*"papers_af.bib")

cl_words = processtext(words, maxnum = 200, minlength = 4, stopwords_extra = ["using", "application"])

wc = wordcloud(cl_words, 
		mask=shape(box, 500 * 2, 350 * 2, cornerradius=10 * 2), 
		fonts = "menlo", colors = :seaborn_dark) 

generate!(wc)
paint(wc, "wordcloud.png")
```
