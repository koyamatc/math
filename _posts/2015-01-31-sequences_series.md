---
title: Differential calculus
layout: post
date: 2015-01-31 20:00:00
postTitle: Sequences, series, and function approximation
categories: integral
---

-------

# Sequences

--------

## Explicit and recursive definitions of sequences

+ finite sequence
$$\\{a\\}_{k=0}^{3}=\\{1,4,7,10\\}
\to a_{0}=1,a_{1}=4,a_{2}=7,a_{3}=10$$
Explicit definition
$$\\{a\\}_{k=0}^{3}=1+3k$$
$$a(k)=1+3k$$
Recursive definition
$$\\{a\\}_{k=0}^{3}においてa_{0}=1 \quad a_{k}=a_{k-1}+3$$ 
+ infinite sequence
$$\\{a_{k}\\}_{k=0}^{\infty}=\\{3,7,11,15, \cdots \\}$$
Explicit definition
$$\\{a_{k}\\}_{k=0}^{\infty}=3+4k$$
$$a(k)=3+4k$$
Recursive definition
$$\\{a\\}_{k=0}^{\infty}においてa_{0}=3 \quad a_{k}=a_{k-1}+4$$ 

## Sequence convergence and divergence

<div class="row">
  <div class="col-sm-12">
    <div class="panel">
      $$ a_{n}=\{1,-\frac{1}{2},\frac{1}{3},-\frac{1}{4},\frac{1}{5}, \cdots \}$$
    </div>
    $$\{a_{n}\}_{1}^{\infty}においてa_{n}=\frac{1}{n}_cdot(-1)^{n+1}
    =\frac{(-1)^{n+1}}{n}$$
    $$\lim_{n \to \infty}a_{n}
    =\lim_{n \to \infty}\frac{(-1)^{n+1}}{n}=0$$
    分母のnは無限大になっても分子は-1と1を繰り返すだけなので限りなく0に近づく（0に収束する）
  </div>
</div>

## Identifying sequence convergence and divergence

<div class="row">
  <div class="col-sm-12">
    <div class="panel">
    $$ a_{n}=\frac{(n+8)(n+1)}{n(n-10)}
    =\frac{n^2+9n+8}{n^2-10n}$$
    </div>
    \(n^2\)は同じように大きくなるので、他の要素を比べると分母が分子より速く大きくなるので
    この式は収束する
    <div class="panel">
    $$ b_{n}=\frac{e^n+1}{e\cdot n+1}$$
    </div>
    分子が分母よりも速く大きくなるので、発散する
    <div class="panel">
    $$ c_{n}=\frac{n^2+1}{n+1000}$$
    </div>
    分子が分母よりも速く大きくなるので、発散する
    <div class="panel">
    $$ d_{n}=(-1)^n$$
    </div>
    -1と1を繰り返して1つの値にはならないので、発散する
  </div>
</div>

## Definition of limit of a sequence and sequence convergence

-----------

# Series

## Sigma notation for sums

<h3>
  $$1+2+3+ \cdots +9+10 = \sum_{i=1}^{10}i$$
  $$1+2+3+ \cdots +99+100 = \sum_{i=1}^{100}i$$
  $$\sum_{i=0}^{50}\pi i^2=\pi 0^2 + \pi 1^2 + \pi 2^2 + \cdots + \pi 49^2 + \pi 50^2$$
</h3> 

## Series as sum of sequence

<h3>
Geometric sequence  
$$\{1,\frac{1}{2},\frac{1}{4},\frac{1}{8}, \cdots\}$$
$$\{a_{n}\}_{n=0}^{\infty}=\frac{1}{2}^n$$

Geometric series
$$1+\frac{1}{2}+\frac{1}{4}+\frac{1}{8}+ \cdots
= \sum_{n=0}^{\infty}\frac{1}{2}^n$$

</h3>

## Writing a series in sigma notation

<div class="panel">
  <h3>
  $$-\frac{5}{3}+\frac{25}{6}-\frac{125}{9} + \cdots $$
  </h3>
  これをシグマで表します
</div>
マイナスが交互に出てくるので
$$(-1)^1, (-1)^2, (-1)^3, \cdots $$
分母は
$$3\cdot1, 3\cdot 2, 3 \cdot3, \cdots$$
分子は
$$5^1,5^2,5^3, \cdots$$
したがって
<h3>
$$\sum_{i=1}^{\infty}(-1)^i \frac{5^i}{3i}$$
</h3>

## Explicitly defining a series

<div class="panel">
  <h3>
  $$\sum_{n=2}^{\infty}\{a_{n}\}=-\frac{8}{5}+\frac{16}{7}-\frac{32}{9} + \cdots $$
  </h3>
</div>
 $$a_{2}=-\frac{8}{5}=\frac{(-2)^3}{2\cdot2+1}$$
 $$a_{3}=\frac{16}{7}=\frac{(-2)^4}{2\cdot3+1}$$
 $$a_{4}=-\frac{32}{9}=\frac{(-2)^5}{2\cdot4+1}$$
<h3>
$$a_{n}=\frac{(-2)^{n+1}}{2n+1}$$
</h3>

## Formula for arithmetic series
<div class="panel">
  <h3>
  Arithmetric sequence  
  $$\{a,a+d,a+2d,a+3d,\cdots a+(n-1)d$$
  $$\{a_{1},a_{2},a_{3},\cdots,a_{n}\}$$
  </h3>
</div>
<div class="panel">
  <h3>
  Arithmetric series  
  $$S_{n}=a\qquad \qquad \quad+a+\qquad \quad d+a+\qquad \quad2d+\cdots +a+(n-1)d$$
  $$S_{n}=a+(n-1)d+a+(n-2)d+a+(n-1)d+\cdots + a$$
  2行を足します
  $$2S_{n}=2a+(n-1)d+2a+(n-1)d+2a+(n-1)d+ \cdots + 2a+(n-1)d$$
  $$2S_{n}=n(2a+(n-1)d)$$
  $$S_{n}=\frac{n(2a+(n-1)d)}{2}=\frac{n(a+a(n-1)d)}{2}$$
  $$\quad a_{1}=a \quad a_{n}= a + (n-1)$$
  $$S_{n}=n\cdot \frac{a_{1}+a_{n}}{2}$$
  </h3>
</div>

-----------

# Geometric series

<h3>
  Geometric sequence
$$a,ar,ar^2,ar^3, \cdots$$
$$r \cdots 比率$$

$$1,-3,9,-27,81,\cdots \qquad r=-3$$
$$3,6,12,24,48, \cdots \qquad r=2$$

  Geometric series
$$1+(-3)+9+(-27)+81+ \cdots$$
$$3+6+12+24+48+ \cdots$$
$$\qquad \downarrow$$
$$\sum_{k=0}^{n}ar^k = ar^0+ar^1+ar^2+ar^3+ \cdots + ar^n$$
</h3>

## Formula for a finite geometric series

<h3>
$$S_{n}=\sum_{k=0}^{n}ar^k = ar^0+ar^1+ar^2+ar^3+ \cdots + ar^n$$
上の式をr倍したものを
$$rS_{n}=\sum_{k=0}^{n}ar^{+1} = ar^1+ar^2+ar^3+ar^4+ \cdots + ar^{n+1}$$
上の式から下の式を引きます
$$S_{n}-rS_{n}=ar^0-ar^{n+1}$$
$$S_{n}(1-r)=a-a^{n+1}$$
$$S_{n}=\sum_{k=0}^{n}ar^k =\frac{a-a^{n+1}}{1-r}$$
</h3>

## Sum of an infinite geometric series

<h3>
$$\sum_{k=0}^{n}ar^k =\frac{a-a^{n+1}}{1-r}$$
$$n \to \inftyのとき$$
$$\lim_{n \to \infty}\sum_{k=0}^{n}ar^k
=\lim_{n \to \infty}\frac{a-a^{n+1}}{1-r}$$
\(r>1\)のときは、発散してしまい極限がない
$$0 \lt |r| \lt 1で$$
\(a^{n+1}\)限りなく小さくなり\(\to 0\)なので
$$\sum_{k=0}^{\infty}ar^k =\frac{a}{1-r}$$
</h3>

---------

# Tests for convergence and divergence

## The nth term divergence test

<div class="panel">
<h3>
$$もし \lim_{n \to \infty}a_{n} \ne 0ならば、
\sum_{n =1}^{\infty}a_{n}は発散する$$
$$0のときは、収束するか発散するかは決定できない$$
</h3>
</div>
<h3>
$$\sum_{n=1}^{\infty}\frac{4n^2-n^3}{7-3n^3}$$
$$\lim_{n \to \infty}\frac{4n^2-n^3}{7-3n^3}
=\lim_{n \to \infty}\frac{\frac{4}{n}-1}{\frac{7}{n^3}-3}=\frac{1}{3}$$
$$\sum_{n=1}^{\infty}\frac{4n^2-n^3}{7-3n^3}は発散する$$
</h3>

## Ratio test

<h3>
<div class="panel">
$$ \sum_{n=k}^{\infty}r^n=r^k+r^{k+1}+r^{k+2}+ \cdots $$
比率は
$$r=\frac{r^{n+1}}{r^n}$$
$$もし|r| \lt 1ならば、収束する$$
</div>
 $$\sum_{n=5}^{\infty}\frac{n^{10}}{n!}は収束するか？$$
 比率は
 $$\frac{(n+1)^{10}}{(n+1)!}\cdot\frac{n!}{n^{10}}
 =\frac{(n+1)^{10}}{(n+1)n^{10}} =\frac{(n+1)^{10}}{n^11+n^{10}}$$
 $$\lim_{n \to \infth}\frac{(n+1)^{10}}{n^11+n^{10}}=0$$

 <div class="panel">
  $$\sum_{n=k}^{\infty}a_{n} で、\lim_{n \to \infty}|\frac{a_{n+1}}{a_{n}}|=Lのとき$$
  $$L \lt 1 \to 収束する$$
  $$L \gt 1 \to 発散する$$
  $$L = 1 \to わからない$$ 
 </div>
</h3>

## Comparison test

<h3>
<div class="panel">
$$\sum_{n=1}^{\infty}a_{n} \quad \sum_{n=1}^{\infty}b_{n}
\quad は、 a_{n},b_{n} \ge 0　かつ a_{n} \le b_{n}のとき$$
$$\sum_{n=1}^{\infty}b_{n}が収束するならば、
\sum_{n=1}^{\infty}a_{n}は収束する$$
$$\sum_{n=1}^{\infty}a_{n}が発散するならば、
\sum_{n=1}^{\infty}b_{n}は発散する$$
</div>
</h3>

## Famous proof that harmonic series diverges



<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_SVG"></script>
<script src="http://d3js.org/d3.v3.min.js" charset="utf-8"></script>
<script src="{{site.url}}/js/d3draws.js" charset="utf-8"></script>

<script>

  y0func = function y0func(x){
    return 0;
  };



</script>
