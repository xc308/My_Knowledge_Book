---
layout: post
title: "How to type latex in markdown?"
date: 2022-05-15
---

## Steps to use latex in the markdown file
Ref1: https://www.overleaf.com/learn/how-to/Writing_Markdown_in_LaTeX_Documents

Base on what I read, here's what I guess:
* create .md file in latex
* link the overleaf with github repository 


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
  <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script> 




