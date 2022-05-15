---
layout: post
title: "How to type latex in markdown?"
date: 2022-05-15
---

## Method 1 to use latex in the markdown file
Ref1: https://www.overleaf.com/learn/how-to/Writing_Markdown_in_LaTeX_Documents

Base on what I read, here's what I guess:
* create .md file in latex
* link the overleaf with github repository 

_Comment: this method can create a new repo for an overleaf project, but cannot insert latex into an md file in some folders of some existence repo._ 


## Method 2
Ref2: https://stackoverflow.com/questions/26275645/how-to-support-latex-in-github-pages

* use MathJax
* create a file "_includes/head.html", then add

 <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
      tex2jax: {
        skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'],
        inlineMath: [['$','$']]
      }
    });
  </script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/MathJax.js?config=TeX-MML-AM_CHTML" type="text/javascript"></script> 


Now have a try:

$h_\theta(x) = \Large\frac{1}{1 + \mathcal{e}^{(-\theta^\top x)}}$

*Comment: does not show math symbol, and also make the pages look ugly, so I change the src address.*
* So now I have deleted the head.html file, and check the page, it amazingly displays the math, but the refresh of the webpage seems to be a bit slow. I need to try more


$\sum_{i=1}^m y^{(i)}$









