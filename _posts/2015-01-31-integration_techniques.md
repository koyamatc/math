---
title: Differential calculus
layout: post
date: 2015-01-31 22:00:00
postTitle: Integration techniques
categories: integral
---

-------

# Integration by parts

--------

## Deriving integration by parts formula

微分におけるproduct rule　を思い出しましょう
<div class="panel">
$$\frac{d}{dx}(f(x)g(x))=f'(x)g(x)+f(x)g'(x)$$
</div>

\\(f(x)g(x)\\)は右辺を積分したものになりますから
$$f(x)g(x)=\int f'(x)g(x)dx + \int f(x)g'(x)dx$$
両辺から\\(\int f'(x)g(x)dx\\)を引きます
$$f(x)g(x)-\int f'(x)g(x)dx = \int f(x)g'(x)dx$$
両辺を入れ替えます
<div class="panel">
$$\int f(x)g'(x)dx = f(x)g(x)-\int f'(x)g(x)dx$$
</div>

この規則を使って積分を行います

例1

$$\int x \cos x dx=?$$
$$f(x)=x \quad f'(x)=1 \quad g(x)= \sin x \quad g'(x)= \cos x$$
これから
$$\int x \cos x dx=x \cdot \sin x - \int (1 \cdot \sin x)dx$$
$$\quad = x \cdot \sin x - (-\cos x) 
= x \cdot \sin x + \cos x + C$$

例2

$$\int (\ln x) dx=?$$
これを書き換えます
$$\int (\ln x) dx=\int (\ln x \cdot 1) dx$$
$$f(x)=\ln x \quad f'(x)=\frac{1}{x} \quad g(x)= x \quad g'(x)=1$$
これから
$$\int (\ln x \cdot 1) dx 
=x \cdot \ln x - \int (\frac{1}{x} \cdot x)dx
=x \cdot \ln x - x + C$$

例3

$$\int (x^2e^x) dx=?$$
$$f(x)=x^2 \quad f'(x)=2x \quad g(x)= e^x \quad g'(x)=e^x$$
これから
$$\int (x^2e^x) dx=x^2e^x-\int (2xe^x) dx
=x^2e^x-2\int (xe^x) dx$$
\\(\int (xe^x) dx\\)について規則から
$$f(x)=x \quad f'(x)=1 \quad g(x)= e^x \quad g'(x)=e^x$$
したがって
$$\int (x^2e^x) dx=x^2e^x-\int (2xe^x) dx
=\int (x^2e^x) dx=x^2e^x-2\int (xe^x) dx
=x^2e^x - (2xe^x-2\int (1 \cdot e^x)dx) 
=x^2e^x - 2xe^x + 2e^x+C$$

例4

$$\\int (e^x \cos x) dx=?$$
$$f(x)=e^x \quad f'(x)=e^x \quad g(x)= \sin x \quad g'(x)=\cos x$$
よって
$$\int (e^x \cos x) dx=e^x \sin x - \int (e^x \sin x)dx$$
ここで
$$\int (e^x \sin x)dx=?$$
$$f(x)=e^x \quad f'(x)=e^x \quad g(x)= -\cos x \quad g'(x)=\sin x$$
$$\int (e^x \sin x)dx=-e^x\cos x +\int (e^x \cos x)$$
$$\int (e^x \cos x) dx=e^x \sin x - \int (e^x \sin x)dx
=e^x \sin x + e^x\cos x - \int (e^x \cos x)$$
$$2\int (e^x \cos x) dx=e^x \sin x + e^x\cos x$$
$$\int (e^x \cos x) dx=\frac{e^x \sin x + e^x\cos x}{2}+C$$

<div class="row">
  <div class="col-sm-6">
    <div id="svg01"></div>
  </div>
  <div class="col-sm-6">
    <div class="panel">
    </div>
  </div>
</div>



<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_SVG"></script>
<script src="http://d3js.org/d3.v3.min.js" charset="utf-8"></script>
<script src="{{site.url}}/js/d3draws.js" charset="utf-8"></script>

<script>


/**  */
  var svg01 = d3.select("#svg01")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");


</script>
