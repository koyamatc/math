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

+ finite sequence (有限数列)
$$\\{a\\}_{k=0}^{3}=\\{1,4,7,10\\}
\to a_{0}=1,a_{1}=4,a_{2}=7,a_{3}=10$$
Explicit definition
$$\\{a\\}_{k=0}^{3}=1+3k$$
$$a(k)=1+3k$$
Recursive definition
$$\\{a\\}_{k=0}^{3}においてa_{0}=1 \quad a_{k}=a_{k-1}+3$$ 
+ infinite sequence (無限数列)
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

# Series　（級数）

## Sigma notation for sums

<h3>
  $$1+2+3+ \cdots +9+10 = \sum_{i=1}^{10}i$$
  $$1+2+3+ \cdots +99+100 = \sum_{i=1}^{100}i$$
  $$\sum_{i=0}^{50}\pi i^2=\pi 0^2 + \pi 1^2 + \pi 2^2 + \cdots + \pi 49^2 + \pi 50^2$$
</h3> 

## Series as sum of sequence

<h3>
Geometric sequence  （等比数列）
$$\{1,\frac{1}{2},\frac{1}{4},\frac{1}{8}, \cdots\}$$
$$\{a_{n}\}_{n=0}^{\infty}=\frac{1}{2}^n$$

Geometric series　（等比級数/幾何級数）
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
  Arithmetric series  （等差級数）
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

# Geometric series　（等比級数）

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
$$S_{n}(1-r)=a-ar^{n+1}$$
$$S_{n}=\sum_{k=0}^{n}ar^k =\frac{a-ar^{n+1}}{1-r}$$
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
 =\frac{(n+1)^{10}}{(n+1)n^{10}} =\frac{(n+1)^{10}}{n^{11}+n^{10}}$$
 $$\lim_{n \to \infty}\frac{(n+1)^{10}}{n^{11}+n^{10}}=0$$

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

<h3>
<div class="panel">
Harmonic series（調和級数）
$$\sum_{n=1}^{\infty}\frac{1}{n}
= 1 + \frac{1}{2}+ \frac{1}{3}+ \frac{1}{4}+ \frac{1}{5}
+ \frac{1}{6}+ \frac{1}{7}+ \frac{1}{8}+ \frac{1}{9} + \cdots$$
は発散する
</div>
上の式から別の式を作成します、各項と\(\frac{1}{2}\)のべき乗とを比べ、項目の値を超えないべき乗の最大値とっていきます
<br>
１と1/2のべき乗では、1が1/2のべき乗の最大値なので1を<br>
1/2と1/2のべき乗では、1/2が1/2のべき乗の最大値なので1/2を<br>
1/3,1/4と1/2のべき乗では、1/4が項目の値を超えないべき乗の最大値なので1/4を<br>
1/5,1/6,1/7,1/8と1/2のべき乗では、1/4が1/2のべき乗の最大値で項目の値を超えないので1/8を<br>
$$S=\quad 1 + \frac{1}{2}
+ \frac{1}{4}+ \frac{1}{4}
+ \frac{1}{8}+ \frac{1}{8}+ \frac{1}{8}+ \frac{1}{8}
+ \frac{1}{16}+ \cdots$$

２つの式の項目を見るとすべて正の数です。そして対応する項目は下の式の値は同じか上の式の項目の値より小さい。<br>
下の式を見ると、\(\frac{1}{4}\)は2つあるので\(\frac{1}{2}\)、
\(\frac{1}{8}\)は4つあるので\(\frac{1}{2}\)、
\(\frac{1}{16}\)は8つあると予想されるので\(\frac{1}{2}\)、
\(S\)を書き換えます
$$S=1 + \frac{1}{2} + \frac{1}{2} + \frac{1}{2} + \cdots = \infty$$
\(S\)は発散します、つまり比較テストの決まりから調和級数は発散します
</h3>

## Comparison test to show convergence

<h3>
<div class="panel">
$$\sum_{n=1}^{\infty}\frac{1}{2^n+n}$$
収束するのか、発散するのか
</div>
$$\sum_{n=1}^{\infty}\frac{1}{2^n+n}
=\frac{1}{3}+\frac{1}{6}+\frac{1}{11}+\frac{1}{20}+ \cdots$$
$$\sum_{n=1}^{\infty}\frac{1}{2^n}
=\frac{1}{2}+\frac{1}{4}+\frac{1}{8}+\frac{1}{16}+ \cdots$$
$$\sum_{n=1}^{\infty}\frac{1}{2^n}
=\sum_{n=1}^{\infty}(\frac{1}{2})^n$$
$$|\frac{1}{2}| \lt 1 \to 
\sum_{n=1}^{\infty}(\frac{1}{2})^n は収束する$$
2つの式の項目はすべて正である、上の式の項目の値は下の式の対応する項目の値以下である、
したがって、下の式が収束するならば、上の式も収束する
</h3>

## Limit comparison test

<h3>
Comparison Test  
$$\sum_{n=1}^{\infty}\frac{1}{2^n+1} \qquad \sum_{n=1}^{\infty}\frac{1}{2^n+1}$$
$$\frac{1}{2^n+1} \ge \frac{1}{2^n+1} \quad n=1,2,3,4,5,\cdots$$
$$um_{n=1}^{\infty}\frac{1}{2^n+1}は収束するので、
\sum_{n=1}^{\infty}\frac{1}{2^n}は収束する$$
<div class="panel">
$$\sum_{n=1}^{\infty}\frac{1}{2^n-1}$$
収束するのか発散するのか？
</div>
$$\frac{1}{2^n-1} \ge \frac{1}{2^n}$$
なので別のテスト方法 Limit comparison test 使います<br>
Limit Comparison Test
$$\sum_{n=k}^{\infty}a_{n} \quad \sum_{n=k}^{\infty}b_{n}$$
$$a_{n} \ge 0, \quad b_{n} \gt 0 \quad すべての n=k,k+1,k+2,\cdots$$
$$\lim_{n=k}^{\infty}\frac{a_{n}}{b_{n}}の値が正で定まれば
両方とも収束するか両方とも発散する$$

$$\lim_{n=1}^{\infty}\frac{\frac{1}{2^n-1}}{\frac{1}{2^n}}
=\lim_{n=1}^{\infty}\frac{2^n}{2^n-1}
=\lim_{n=1}^{\infty}\frac{1}{1-\frac{1}{2^n}}=1$$
$$この値は正であり、\sum_{n=1}^{\infty}\frac{1}{2^n}は収束するので$$
$$\sum_{n=1}^{\infty}\frac{1}{2^n-1}は収束する$$
</h3>

## Alternating series test

<h3>
<div class="panel">
$$\sum_{n=k}^{\infty}a_{n}　\qquad
a_{n}=(-1)^{n}b_{n} \quad or \quad a_{n}=(-1)^{n+1}b_{n}$$
この時
$$1. \quad \lim_{n \to \infty}b_{n}=0$$
$$2. \quad {b_{n}}の数列は、だんだん小さくなる$$
この場合
$$\sum_{n=k}^{\infty}a_{n}\ quad は収束する$$

例
$$\sum_{n=1}^{\infty}\frac{(-1)^{n+1}}{n}
=1-\frac{1}{2}+\frac{1}{3}-\frac{1}{4}+\frac{1}{5}+\cdots$$
$$a_{n}=\frac{(-1)^{n+1}}{n} \qquad b_{n}=\frac{1}{n}$$
$$\lim_{n \to \infty}\frac{1}{n}= 0$$
$${\frac{1}{n}}は小さくなっていく$$
したがって
$$\sum_{n=1}^{\infty}\frac{(-1)^{n+1}}{n}\quad は収束する$$

※上記の条件に適合しない場合は、収束するか発散するかはわからな
</div>
</h3>

## Conditional and absolute convergence

<h3>
$$\sum_{n=1}^{\infty}\frac{(-1)^{n+1}}{n}
=1-\frac{1}{2}+\frac{1}{3}-\frac{1}{4}+\frac{1}{5}+\cdots$$
この式は収束します、では絶対値の総和はどうでしょうか
$$\sum_{n=1}^{\infty}|\frac{(-1)^{n+1}}{n}|
=\sum_{n=1}^{\infty}\frac{1^{n+1}}{n}
=1+\frac{1}{2}+\frac{1}{3}+\frac{1}{4}+\frac{1}{5}+\cdots$$
こちらは発散します（条件付き収束）
$$\sum_{n=1}^{\infty}(-\frac{1}{2})^{n+1} \to 収束します$$
$$\sum_{n=1}^{\infty}|(-\frac{1}{2})^{n+1}|
=\sum_{n=1}^{\infty}(\frac{1}{2})^{n+1} \to 収束します$$
（絶対的収束）
</h3>

## Integral test intuition

<div clas="row">
  <div class="col-sm-6">
    <h3>
      $$\sum_{n=1}^{\infty}\frac{1}{n^2}
      =1+\frac{1}{4}+\frac{1}{9}+\frac{1}{16}+ \cdots$$
      項はすべて正の数で急激に０に近づきます
      $$f(x)=\frac{1}{x^2} \quad を考えます（右のグラフ）$$
      級数の最初の項は、1 x 1 の正方形の面積<br>
      2番目の項は、1 x 1/4 の長方形の面積<br>
      3番目の項は、1 x 1/9 の長方形の面積<br>
      4番目の項は、1 x 1/16 の長方形の面積<br>
      ここで
      $$区間[1.\infty]で、f(x)とx軸の間の面積は$$ 
      $$\int_{1}{\infty}f(x)dx$$
      上の級数の式を書き換えます
      $$\sum_{n=1}^{\infty}\frac{1}{n^2}
      =1+\sum_{n=2}^{\infty}\frac{1}{n^2}
      \lt 1+\int_{1}{\infty}\frac{1}{x^2}dx$$
      四角形は必ずf(x)の下にあります
    </h3>
  </div>
  <div class="col-sm-6">
    <div id="svg01"></div>
  </div>
</div>
<h3>
$$\quad \lim_{t \to \infty}x^{-2}dx=
\lim_{t \to \infty}[-\frac{1}{x}]_{1}^{t}=
\lim_{t \to \infty}(-\frac{1}{t}+1)=1$$
$$\sum_{n=1}^{\infty}\frac{1}{n^2} \lt 2$$
この級数には上限がり無限大になりません、つまり収束します。
</h3>

---*---*---*---*---*---

<h3>
関数\(f(x)\)は、区間\([k,\infty)\)で、正の値をとり、連続で、だんだん小さくなる場合
$$1. \quad \int_{k}^{\infty}f(x)dx \quad が収束するならば \quad
\sum_{n=k}^{\infty}f(n) \quad も収束する$$
$$2. \quad \int_{k}^{\infty}f(x)dx \quad が発散するならば \quad
\sum_{n=k}^{\infty}f(n) \quad も発散する$$
</h3>

---------

# Estimating infinite series

## Using integrals to place bounds on infinite sum

<div class="row">
  <div class="col-sm-6">
    <h3>
      $$S = \sum_{n=1}^{\infty}f(n)
      =\sum_{n=1}^{k}f(n) + \sum_{n=k+1}^{\infty}f(n)$$
      $$ \qquad S_{k}=\sum_{n=1}^{k}f(n) \codts 有限和
         \qquad R_{k}=\sum_{n=k+1}^{\infty}f(n) \cdots 無限和（残りの部分）$$
      $$S = S_{k} + R_{k}$$
      残りの部分の面積は、曲線より下にあるので
      $$R_{k} \le \int_{k}^{\infty}f(x)dx$$
      $$S \le S_{k} + \int_{k}^{\infty}f(x)dx$$
    </h3>

  </div>
  <div class="col-sm-6">
    <div id="svg021"></div>
  </div>
</div>
<div class="row">
  <div class="col-sm-6">
    <h3>
      残りの部分の面積は、曲線より大きいので
      $$R_{k} \le \int_{k+1}^{\infty}f(x)dx$$
      $$S \ge S_{k} + \int_{k+1}^{\infty}f(x)dx$$
      先ほどの結果とあわせて
      $$S_{k} + \int_{k+1}^{\infty}f(x)dx \le S \le
      S_{k} + \int_{k}^{\infty}f(x)dx$$
    </h3>
  </div>
  <div class="col-sm-6">
    <div id="svg022"></div>
  </div>
</div>
<h3>
例
$$S=\sum_{n=1}^{\infty}\frac{1}{n^2}=S_{5}+R_{5}$$
$$S_{5}=\sum_{n=1}^{5}\frac{1}{n^2} \approx 1.464$$
$$R_{5}=\int_{6}^{\infty}\frac{1}{n^2}dx
=\lim_{t \to \infty}\int_{6}^{\infty}\frac{1}{n^2}dx
=\lim_{t \to \infty}[-n^{-1}]_{6}^{\infty}
=\lim_{t \to \infty}(-\frac{1}{t}+\frac{1}{6})=\frac{1}{6}$$
$$R_{5}=\int_{5}^{\infty}\frac{1}{n^2}dx=\frac{1}{5}$$
$$1.464 + \fra{1}{6} \le S \le 1.464 + \frac{1}{5}$$
</h3>

## Alternating series error estimation

<h3>
$$\sum_{n=1}^{\infty}\frac{(-1)^{n+1}}{n^2}
=1 - \frac{1}{4} + \frac{1}{9} -\frac{1}{16} + \frac{1}{25} 
- \frac{1}{36} + \frac{1}{49} - \frac{1}{64} + \cdots$$
|___________|    |___________________| |________________________|  
$$\quad S \qquad = \qquad \qquad S_{4} \qquad  + \qquad \qquad R_{4}$$
$$S_{4}=\frac{115}{144}$$
$$R_{4}=(\frac{1}{25}-\frac{1}{36}) + (\frac{1}{49} - \frac{1}{64}) +() \cdots$$
()の中はすべて＋となるので
$$R_{4} \ge 0$$
$$R_{4}=\frac{1}{25}-(\frac{1}{36}-\frac{1}{49})
                    -(\frac{1}{64})\frac{1}{81}) \cdots$$
()の中はすべて＋となるので、\(\frac{1}{25}\)は超えない
$$R_{4} \le 0.04$$

$$\frac{115}{144} \le S \le \frac{115}{144} + 0.04$$
</h3>

### 例

<h3>
$$\sum_{n=1}^{\infty}\frac{(-1)^{n+1}}{\sqrt{n}}
=1 - \frac{1}{\sqrt{2}}+\frac{1}{\sqrt{3}}-\frac{1}{\sqrt{4}}+ cdots$$
$$S = S_{k} + R_{k}$$
$$|R_{k}| \le 0.001 \quad となる最少のkを求める$$
$$R_{k}=\frac{(-1)^{k+2}}{\sqrt{k+1}}+\frac{(-1)^{k+3}}{\sqrt{k+2}}+\cdots$$
\(R_{k}\)の最初の項を調べる
$$|R_{k}|=|\frac{(-1)^{k+2}}{\sqrt{k+1}}| \le 0.001$$
$$\frac{1}{\sqrt{k+1}} \le 0.001$$
$$1000 = \sqrt{k+1}$$
$$1000000 = k + 1$$
$$999999 = k$$
$$S=S_{999999}-\frac{1}{\sqrt{1000000}}
=S_{999999}-\frac{1}{1000}$$
</h3>

---------

# Power series function representation using algebra

## Power series radius and interval of convergence

### Power series (冪級数)
<h3>
$$f(x)=\sum_{n=0}^{\infty}a_{n}(x-c)^{n}
=a_{0}(x-c)^{0}+a_{1}(x-c)^{1}+a_{2}(x-c)^{2}+a_{3}(x-c)^{3}+ \cdots$$
</h3>

### Geometric series (等比級数)

<h3>
$$g(x)=\sum_{n=0}^{\infty}ax^{n}
=ax^{0}+ax^{1}+ax^{2}+ax^{3}+ax^{4}+ \cdots = \frac{a}{1-x}$$
この式が収束する条件は
$$|x| \lt 1 \to -1 \lt x \lt 1$$
interval of convergence(収束範囲)=2  -1 から　1の範囲<br>
radius of convergence(収束半径)=1<br>
<br>
次の関数について考えます
$$h(x)=\frac{1}{3+x^2}$$
$$=\frac{1}{3(1+\frac{x^2}{3})}=\frac{\frac{1}{3}}{1-(-\frac{x^2}{3})}$$
このことから
$$h(x)=\sum_{n=0}^{\infty}\frac{1}{3}(-\frac{x^2}{3})
=\frac{1}{3}-\frac{1}{9}x^2 + \frac{1}{27}x^4 \cdots $$ 
収束区間は？  収束条件は
$$|(-\frac{x^2}{3})| \lt 1$$
$$x^2 \lt 3 \to |x| \lt \sqrt{3} \to -\sqrt{3} \lt x \lt \sqrt{3}$$
$$h(x)は\quad -\sqrt{3} \lt x \lt \sqrt{3} \quad とき収束する$$
</h3>

## Function as geometric series

<h3>
$$f(x)= 2 -8x^2 + 32x^4 - 128x^6 \cdots$$
$$2 \to  -8x^2 = 2\cdot(-4x^2) \quad -8x^2 \to 32x^4=-8x^2\cdot(-4x^2)$$
比率=(-4x^2) \quad 初項=2
$$f(x)=\sum_{n=0}^{\infty}2(-4x^2)^n$$
収束条件は
$$|-4x^2| \lt 1$$
$$4x^2 \lt 1 \to x^2 \lt \frac{1}{4}$$
$$|x| \lt \frac{1}{2}$$
収束範囲は
$$-\frac{1}{2} \lt x \lt \frac{1}{2}$$
$$f(x)=\sum_{n=0}^{\infty}2(-4x^2)^n=\frac{2}{1-(-4x^2)}
=\frac{2}{1+4x^2}$$
</h3>

-------

# Maclaurin and Taylor series intuition

<div class="row">
  <div class="col-sm-6">
    <div id="svg03"></div>
  </div>
  <div class="col-sm-6">
    関数\(f(x)\)は、多項式で表せます、この関数を１次微分、２次微分、３次微分、４次\(\cdots\)と続けていくと最後に定数が残ります。
    <br>
    では\(x=0\)とした場合
    $$f(0),f'(0),f''(0),f'''(0),f''''(0),\cdots$$
    \(f(0)\)を最後に残った定数とすると\(y=f(0)\)の\(x\)軸に平行な直線です
    <br>
    今度は元の多項式を組み立てていきます
    $$p(0)=f(0)$$
    $$(1)\cdots \quad p(x)=f(0)$$
    １項追加します
    $$p'(0)=f'(0)$$
    $$(2)\cdots \quad p(x)=f(0)+f'(0)x$$
  </div>
</div>
１項追加します
$$p'(x)=f'(0)+f''(0)x$$
$$(3)\cdots \quad p(x)=f(0)+f'(0)x+\frac{1}{2}x^2$$
$$(4)\cdots \quad p(x)=f(0)+f'(0)x+\frac{1}{2}x^2+\frac{1}{2*3}x^3$$
これを続けていくと
$$p(x)=f(0)+f'(0)x+\frac{1}{2}f''(0)x^2+\frac{1}{3*2}f'''(0)x^3
+\frac{1}{4*3*2}f''''(0)x^4+\cdots+
\frac{1}{n!}f^n(0)x^n$$
これをマクローリン級数といい、テイラー級数で\(x=0\)近辺の特別な場合です

<h3>
例1
$$f(x)=\cos x \qquad f(0)=1$$
$$f'(x)=\-sin x \qquad f'(0)=0$$
$$f''(x)=\-cos x \qquad f''(0)=-1$$
$$f'''(x)=\sin x \qquad f'''(0)=0$$
$$f''''(x)=\cos x \qquad f''''(0)=1$$
多項式を組み立てます
$$p(x)=1-\frac{x^2}{2!}+\frac{x^4}{4!}-\frac{x^6}{6!}+\frac{x^8}{8!}
-\frac{x^10}{10!}+\frac{x^12}{12!}\cdots$$
<br>
例2
$$f(x)=\sin x \qquad f(0)=0$$
$$f'(x)=\cos x \qquad f'(0)=1$$
$$f''(x)=\-sin x \qquad f''(0)=0$$
$$f'''(x)=\-cos x \qquad f'''(0)=-1$$
$$f''''(x)=\sin x \qquad f''''(0)=0$$
多項式を組み立てます
$$p(x)=\frac{x^1}{1!}-\frac{x^3}{3!}+\frac{x^5}{5!}-\frac{x^7}{7!}
+\frac{x^9}{9!}-\frac{x^11}{11!}\cdots$$
<br>
例3
$$f(x)=e^x =f'(x)=f''(x)=f^{(3)}(x)=f^{(4)}(x)\cdots$$
$$e^0=1=f'(0)=f''(0)=f^{(3)}(0)=f^{(4)}(0)\cdots$$
$$e^x \approx 1+\frac{x^1}{1!}+\frac{x^2}{2!}+\frac{x^3}{3!}+\frac{x^4}{4!}\cdots$$
$$e \approx 1+\frac{1}{1!}+\frac{1}{2!}+\frac{1}{3!}+\frac{1}{4!}\cdots$$
</h3>

## Euler's formula and Euler's identity

$$e^{ix} \approx 1+ix+\frac{(ix)^{2}}{2!}+\frac{(ix)^{3}}{3!}
+\frac{(ix)^{4}}{4!}+\frac{(ix)^{5}}{5!}+\frac{(ix)^{6}}{6!}+\cdots$$
$$\quad \approx 
1+ix-\frac{x^{2}}{2!}+\frac{ix^{3}}{3!}-\frac{x^{4}}{4!}
+\frac{ix^{5}}{5!}-\frac{x^{6}}{6!}+\frac{ix^{7}}{7!}\cdots$$
実数部と虚数部を分けます
$$e^{ix}=
(1-\frac{x^2}{2!}+\frac{x^4}{4!}-\frac{x^6}{6!}+\cdots)
i(x-\frac{x^3}{3!}+\frac{x^5}{5!}-\frac{x^7}{7!}+\cdots)$$
<h3>
$$e^{ix}=\cos x + i\sin x \cdots オイラーの公式$$
</h3>
$$x=\piのとき$$
$$e^{i\pi}=-1$$
<h3>
$$e^{i\pi}+1=0 \cdots オイラーの等式$$
</h3>

--------

# Taylor series approximations

<div class="row">
  <div class="col-sm-6">
    \(\sin x\)はピンク色の曲線です
    <br>
    \(\sin x\)をマクローリン展開すると
    $$\sin x = x-\frac{x^3}{3!}+\frac{x^5}{5!}-\frac{x^7}{7!}
    +\frac{x^9}{9!}\cdots$$
    最初の項\(x\)の線は　\(\dots\) 青い線
    <br>
    最初から２個の項\(x-\frac{x^3}{3!}\)の線は　\(\dots\) 白い線
    <br>
    最初から３個の項\(x-\frac{x^3}{3!}+\frac{x^5}{5!}\)の線は　\(\dots\) 黄い線
    <br>
    最初から４個の項\(x-\frac{x^3}{3!}+\frac{x^5}{5!}-\frac{x^7}{7!}\)の線は　\(\dots\) 赤の線
    <br>
    最初から5個の項
    \(x-\frac{x^3}{3!}+\frac{x^5}{5!}-\frac{x^7}{7!}
    +\frac{x^9}{9!}\)の線は　\(\dots\) 緑の線
    <br>
    項を増やしていくとだんだんとピンクの線\(\sin x\)に近づいてゆきます
  </div>
  <div class="col-sm-6">
    <div id="svg04"></div>
  </div>
</div>

## Generalized Taylor series approximation

テーラー展開は\\(x=c\\)を中心に展開する場合です
<h3>
$$p(x)=f(c)+f'(c)(x-c)+\frac{f''(c)(x-c)^2}{2!}
+\frac{f^{3}(c)(x-c)^3}{3!}+\frac{f^{4}(c)(x-c)^4}{4!}+\cdots$$
</h3>


<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_SVG"></script>
<script src="http://d3js.org/d3.v3.min.js" charset="utf-8"></script>
<script src="{{site.url}}/js/d3draws.js" charset="utf-8"></script>

<script>

  y0func = function y0func(x){
    return 0;
  };

  var svg01 = d3.select("#svg01")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg021 = d3.select("#svg021")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg022 = d3.select("#svg022")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg03 = d3.select("#svg03")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg04 = d3.select("#svg04")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");

  var xScale01 = d3.scale.linear()
                       .domain([0,4])
                       .range([50,450]);
  var yScale01 = d3.scale.linear()
                       .domain([4,0])
                       .range([50,450]);       

  var xScale02 = d3.scale.linear()
                       .domain([0,6])
                       .range([50,450]);
  var yScale02 = d3.scale.linear()
                       .domain([4,0])
                       .range([50,450]);       

  var xScale03 = d3.scale.linear()
                       .domain([-2,2])
                       .range([50,450]);
  var yScale03 = d3.scale.linear()
                       .domain([2,-2])
                       .range([50,450]);       
  var xScale04 = d3.scale.linear()
                       .domain([-6,6])
                       .range([50,450]);
  var yScale04 = d3.scale.linear()
                       .domain([6,-6])
                       .range([50,450]);       
  // 軸
  axesData01 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[1,2,3],
    "yTickValues":[1],
    "xTickPadding":5,
    "yTickPadding":2,
    "xOrient":["bottom"],
    "yOrient":["left"],
    "stroke":"#ff0",
    "strokeWidth":1,
    "fillColor":"none",
    "xScale":xScale01,
    "yScale":yScale01
  };
  axesData02 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[],
    "yTickValues":[],
    "xTickPadding":5,
    "yTickPadding":2,
    "xOrient":["bottom"],
    "yOrient":["left"],
    "stroke":"#ff0",
    "strokeWidth":1,
    "fillColor":"none",
    "xScale":xScale02,
    "yScale":yScale02
  };
  axesData03 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[],
    "yTickValues":[],
    "xTickPadding":5,
    "yTickPadding":2,
    "xOrient":["bottom"],
    "yOrient":["left"],
    "stroke":"#ff0",
    "strokeWidth":1,
    "fillColor":"none",
    "xScale":xScale03,
    "yScale":yScale03
  };
  axesData04 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[-6,-4,-2,2,4,6],
    "yTickValues":[-6,-4,-2,2,4,6],
    "xTickPadding":5,
    "yTickPadding":2,
    "xOrient":["bottom"],
    "yOrient":["left"],
    "stroke":"#ff0",
    "strokeWidth":1,
    "fillColor":"none",
    "xScale":xScale04,
    "yScale":yScale04
  };

  function func01(x){
    return 1/Math.pow(x,2);
  };

  var pathData01 = [];
  var areaData01 = [];

  for (var i = 0.5; i <= 4; i=i+0.02) {
    pathData01.push(new Point(i,func01(i)));
  };
  for (var i = 1; i <= 4; i=i+0.02) {
    areaData01.push(new Point(i,func01(i)));
  };

  drawArea(svg01,areaData01,y0func,
    {"fillColor":"#00f","opacity":0.6},xScale01,yScale01); 

  drawPath(svg01,pathData01,{"stroke":"lime","strokeWidth":2},xScale01,yScale01);

  lineData01 = [
    {"x1":0,"y1":1,"x2":1,"y2":1,"stroke":"#fff"},
    {"x1":1,"y1":1,"x2":1,"y2":0,"stroke":"#fff"},
    {"x1":1,"y1":1/4,"x2":2,"y2":1/4,"stroke":"#fff"},
    {"x1":2,"y1":1/4,"x2":2,"y2":0,"stroke":"#fff"},
    {"x1":2,"y1":1/9,"x2":3,"y2":1/9,"stroke":"#fff"},
    {"x1":3,"y1":1/9,"x2":3,"y2":0,"stroke":"#fff"},
    {"x1":3,"y1":1/16,"x2":4,"y2":1/16,"stroke":"#fff"},
    {"x1":4,"y1":1/16,"x2":4,"y2":0,"stroke":"#fff"},
  ]

  drawLine(svg01,lineData01,xScale01,yScale01);

  drawAxes(svg01,axesData01);

// 
  function func02(x){
    return 1/x;
  };

  var pathData02 = [];
  var areaData021 = [];
  var areaData022 = [];

  for (var i = 0.3; i <= 6; i=i+0.02) {
    pathData02.push(new Point(i,func02(i)));
  };
  for (var i = 1; i <= 6; i=i+0.02) {
    areaData021.push(new Point(i,func02(i)));
  };
  for (var i = 2; i <= 6; i=i+0.02) {
    areaData022.push(new Point(i,func02(i)));
  };

  drawArea(svg021,areaData021,y0func,
    {"fillColor":"#00f","opacity":0.6},xScale02,yScale02); 
  drawArea(svg022,areaData022,y0func,
    {"fillColor":"#00f","opacity":0.6},xScale02,yScale02); 

  drawPath(svg021,pathData02,{"stroke":"lime","strokeWidth":2},xScale02,yScale02);
  drawPath(svg022,pathData02,{"stroke":"lime","strokeWidth":2},xScale02,yScale02);

  lineData021 = [
    {"x1":1,"y1":0,"x2":1,"y2":1/2,"stroke":"#fff"},
    {"x1":1,"y1":1/2,"x2":2,"y2":1/2,"stroke":"#fff"},
    {"x1":2,"y1":0,"x2":2,"y2":1/2,"stroke":"#fff"},

    {"x1":2,"y1":1/3,"x2":3,"y2":1/3,"stroke":"#fff"},
    {"x1":3,"y1":1/3,"x2":3,"y2":0,"stroke":"#fff"},

    {"x1":3,"y1":1/4,"x2":4,"y2":1/4,"stroke":"#fff"},
    {"x1":4,"y1":1/4,"x2":4,"y2":0,"stroke":"#fff"},

    {"x1":4,"y1":1/5,"x2":5,"y2":1/5,"stroke":"#fff"},
    {"x1":5,"y1":1/5,"x2":5,"y2":0,"stroke":"#fff"},

    {"x1":5,"y1":1/6,"x2":6,"y2":1/6,"stroke":"#fff"},
    {"x1":6,"y1":1/6,"x2":6,"y2":0,"stroke":"#fff"},

  ]
  drawLine(svg021,lineData021,xScale02,yScale02);

  lineData022 = [
    {"x1":2,"y1":0,"x2":2,"y2":1/2,"stroke":"#fff"},
    {"x1":2,"y1":1/2,"x2":3,"y2":1/2,"stroke":"#fff"},
    {"x1":3,"y1":1/2,"x2":3,"y2":0,"stroke":"#fff"},

    {"x1":3,"y1":1/3,"x2":4,"y2":1/3,"stroke":"#fff"},
    {"x1":4,"y1":1/3,"x2":4,"y2":0,"stroke":"#fff"},

    {"x1":4,"y1":1/4,"x2":5,"y2":1/4,"stroke":"#fff"},
    {"x1":5,"y1":1/4,"x2":5,"y2":0,"stroke":"#fff"},

    {"x1":5,"y1":1/5,"x2":6,"y2":1/5,"stroke":"#fff"},
    {"x1":6,"y1":1/5,"x2":6,"y2":0,"stroke":"#fff"},

  ]
  drawLine(svg022,lineData022,xScale02,yScale02);

  drawAxes(svg021,axesData02);
  drawAxes(svg022,axesData02);

  foData02 = [
    {"x":0.9,
    "y":0.4,
    "text":"$$k$$",
    "fontSize":"16px"},
    {"x":1.9,
    "y":0.4,
    "text":"$$k+1$$",
    "fontSize":"16px"},
    {"x":2.9,
    "y":0.4,
    "text":"$$k+2$$",
    "fontSize":"16px"},
    {"x":3.9,
    "y":0.4,
    "text":"$$k+3$$",
    "fontSize":"16px"},
    {"x":4.9,
    "y":0.4,
    "text":"$$k+4$$",
    "fontSize":"16px"},

  ];

  drawMathjax(svg021,foData02,xScale02,yScale02);
  drawMathjax(svg022,foData02,xScale02,yScale02);

  // Maclaurin Sereis
  function func03(x){
    return Math.pow(x,3)/7-2*Math.pow(x,2)/5+x+0.5;
  };

  var pathData03 = [];

  for (var i = -2.0; i <= 2.0; i=i+0.02) {
    pathData03.push(new Point(i,func03(i)));
  };

  drawPath(svg03,pathData03,{"stroke":"lime","strokeWidth":2},xScale03,yScale03);

  drawAxes(svg03,axesData03);
 
  foData03 = [
    {"x":-0.2,
    "y":2.8,
    "text":"$$y$$",
    "fontSize":"18px"},
    {"x":2.1,
    "y":0.5,
    "text":"$$x$$",
    "fontSize":"18px"},
    {"x":2,
    "y":2.5,
    "text":"$$f(x)$$",
    "fontSize":"16px"},
    {"x":-0.4,
    "y":1.2,
    "text":"$$f(0)$$",
    "fontSize":"16px"},

  ];

  drawMathjax(svg03,foData03,xScale03,yScale03);

  // Taylor 
  function func041(x){
    return Math.sin(x);
  };
  function func042(x){
    return x;
  };
  function func043(x){
    return x-Math.pow(x,3)/6;
  };
  function func044(x){
    return x-Math.pow(x,3)/6+Math.pow(x,5)/120;
  };
  function func045(x){
    return x-Math.pow(x,3)/6+Math.pow(x,5)/120-Math.pow(x,7)/5040;
  };
  function func046(x){
    return x-Math.pow(x,3)/6+Math.pow(x,5)/120-Math.pow(x,7)/5040
    +Math.pow(x,9)/362880;
  };
  var pathData041 = [];
  var pathData042 = [];
  var pathData043 = [];
  var pathData044 = [];
  var pathData045 = [];
  var pathData046 = [];

  for (var i = -6.0; i <= 6.0; i=i+0.02) {
    pathData041.push(new Point(i,func041(i)));
    pathData042.push(new Point(i,func042(i)));
    pathData043.push(new Point(i,func043(i)));
    pathData044.push(new Point(i,func044(i)));
    pathData045.push(new Point(i,func045(i)));
    pathData046.push(new Point(i,func046(i)));
  };

  drawPath(svg04,pathData041,{"stroke":"#f0f","strokeWidth":2},xScale04,yScale04);
  drawPath(svg04,pathData042,{"stroke":"#00f","strokeWidth":2},xScale04,yScale04);
  drawPath(svg04,pathData043,{"stroke":"#fff","strokeWidth":2},xScale04,yScale04);
  drawPath(svg04,pathData044,{"stroke":"#ff0","strokeWidth":2},xScale04,yScale04);
  drawPath(svg04,pathData045,{"stroke":"#f00","strokeWidth":2},xScale04,yScale04);
  drawPath(svg04,pathData046,{"stroke":"lime","strokeWidth":2},xScale04,yScale04);

  drawAxes(svg04,axesData04);

</script>
