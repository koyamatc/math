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

-------

# U-substitution

-------

不定積分
$$\int (3x^2+2x)e^{(x^3+x^2)} dx$$
これの解き方としてu-substitutionというテクニックを使います

注目するのは\\(3x^2+2x\\) は \\(x^3+x^2\\) の導関数という点です

$$u=x^3+x^2$$
$$\frac{du}{dx}=3x^2+2x \to du = (3x^2+2x)dx$$
とします

問題の不定積分を書き換えます
$$\int (3x^2+2x)e^{(x^3+x^2)} dx = \int (3x^2+2x)dx e^{(x^3+x^2)}
= \int du e^{u} = \int e^{u}du $$
$$\quad = e^{u} + C = e^{x^3+x^2} + C$$

例１

<div class="panel">
$$\int \frac{4x^3}{x^4 + 7}dx$$
</div>

$$u=x^4 + 7$$
$$\frac{du}{dx}=4x^3 \to du=4x^3dx$$
問題を書き換えます
$$\int \frac{4x^3}{x^4 + 7}dx=\int \frac{4x^3dx}{x^4 + 7}
=\int \frac{du}{u}=\frac{1}{u}du$$
$$\quad = ln|u| + C = ln|x^4 + 7| + C$$

例2
<div class="panel">
$$\int \sqrt{7x+9}dx$$
</div>
$$u=7x+9$$
$$\frac{du}{dx}=7 \to du=7dx$$

ここで７という数字を使うために少し工夫します
$$\int \frac{1}{7}\cdot 7\sqrt{7x+9}dx 
=\frac{1}{7} \int 7dx\sqrt{7x+9}$$
$$\quad = \frac{1}{7} \int \sqrt{u}du 
= \frac{1}{7} \int u^{\frac{1}{2}}du 
=\frac{1}{7}(\frac{2}{3}u^{\frac{3}{2}}+C)
=\frac{2}{21}u^{\frac{3}{2}} + C$$
$$\quad = \frac{2}{21}(7x+9)^{\frac{3}{2}} + C$$

例3
<div class="panel">
$$\int \frac{\pi}{x\ln x}dx$$
</div>
$$u=\ln x$$
$$\frac{du}{dx}=\frac{1}{x} \to du={1}{x}dx$$
問題を書き換えます
$$\int \frac{\pi}{x\ln x}dx
=\pi \int \frac{1}{\ln x}\frac{1}{x}dx
=\pi \int \frac{1}{u}du$$
$$ \quad
=\pi ln|u| + C
=\pi ln|\ln x| + C$$

例4
<div class="panel">
$$\int_{0}^{1}x^2 2^{x^{3}} dx$$
</div>
$$\frac{d}{dx}e^x=e^x$$
$$\int e^x dx = e^x + C$$
$$2=e^{\ln2} \to 2^{x^3}=(e^{\ln2})^{x^3}=e^{x^{3}\ln2}$$
問題を書き換えます
$$\int_{0}^{1}x^2 e^{x^{3}\ln2} dx$$
u-subsutitution
$$u=x^{3}\ln2$$
$$\frac{du}{dx}=3x^2 \ln2=x^2 3\ln2 =x^2 \ln2^3 = \ln8 x^2
\to du=\ln8 x^2dx$$
$$\intx^2 e^{x^{3}\ln2} dx
=\frac{1}{\ln8} \int \ln8 x^2 e^{x^{3}\ln2} dx
=\frac{1}{\ln8} \int e^{u}du
=\frac{1}{\ln8}e^{u}+C=\frac{1}{\ln8}e^{x^{3}\ln2}+C$$
$$\int_{0}^{1}x^2 2^{x^{3}} dx
=\frac{1}{\ln8}e^{1^{3}\ln2}-\frac{1}{\ln8}e^{0^{3}\ln2}
=\frac{1}{\ln8}*2 - \frac{1}{\ln8}*1
=\frac{1}{\ln8}$$

例5
<div class="panel">
$$\int \frac{2^{\ln x}}{x} dx = \int \frac{1}{x}2^{\ln x}dx$$
</div>
$$u=\ln x$$
$$du = \frac{1}{x}dx$$

$$\int \frac{1}{x}2^{\ln x}dx
=\int 2^{u}du
=\int (e^{\ln2})^{u}du
=\int (e^{(\ln2)u}du$$
$$\qquad \int e^{au}du=\frac{1}{a}e^{au}+C$$
$$=\frac{1}{\ln2}e^{u\ln2}+C$$
$$ \qquad a\ln b = \ln b^a \to u\ln2=\ln 2^{u}$$
$$=\frac{1}{\ln2}2^{u}+C$$
$$=\frac{1}{\ln2}2^{\ln x}+C$$

例6
<div class="panel">
$$\int (x+3)(x-1)^5 dx $$
</div>
$$u=x-1 \to x= u+1$$
$$du = dx$$

$$\int (x+3)(x-1)^5 dx
=\int (u+1+3)u^5 du
=\int (u+4)u^5 du
=\int (u^6+4u^5) du
=\frac{u^7}{7}+\frac{4u^6}{6} + C$$
$$=\frac{(x-1)^7}{7}+\frac{2}{3}(x-1)^6 + C$$

例7
<div class="panel">
$$\int_{0}^{\sqrt{\pi}}x\sin(x^2)dx$$
</div>
$$u=x^2$$
$$du = 2xdx$$
置き換えます
$$\frac{1}{2}\int_{0}^{\sqrt{\pi}}2x\sin(x^2)dx
=\frac{1}{2}\int_{u=0}^{u=\pi}\sin(u)du
=\frac{1}{2}[-\cos u ]_{0}^{\pi}$$
$$=\frac{1}{2}[-\cos \pi + \cos 0]
=\frac{1}{2}[1 + 1]=1$$

例8
<div class="panel">
$$\int \frac{\cos(5x)}{e^{\sin(5x)}}dx$$
</div>
$$u=\sin(5x)$$
$$\frac{d}{dx}=5\cos(5x) \to du=5\cos(5x)dx$$

置き換えると
$$\int \frac{\cos(5x)}{e^{\sin(5x)}}dx
=\frac{1}{5}\int \frac{5\cos(5x)}{e^{\sin(5x)}}dx
=\frac{1}{5}\int \frac{1}{e^u}du
=\frac{1}{5}\int e^{-u}du
$$
ここで-uを
$$w=-u$$
$$dw=-du$$

置き換えます
$$
=(-1)\frac{1}{5}\int e^{-u}du(-1)
=-\frac{1}{5}\int e^{w}dw
=-\frac{1}{5}e^{w}+C
=-\frac{1}{5}e^{-u}+C
=-\frac{1}{5}e^{-\sin(5x)}+C
$$

---------


## u-substitution and back substitution




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
