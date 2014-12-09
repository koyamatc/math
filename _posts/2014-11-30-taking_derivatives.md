---
title: Differential calculus
layout: post
date: 2014-11-30 22:00:00
postTitle: Taking derivatives
categories: differential
---

-------

# Using secant line slopes to approximate tangent slope

--------

## Slope of a line secant to a curve

<div class="row">
  <div class="col-sm-6">
    <div id="svg01"></div>
  </div>
  <div class="col-sm-6">
  直線があり、直線上に２点\((x_0,y_0),(x_1,y_1)\)があります<br>
  直線の傾き(slope)は、\(x\)の変化量\((\Delta x)\)に対する\(y\)の変化量\((\Delta y)\)で<br>
  $$Slope=m=\frac{\Delta y}{\Delta x}=\frac{y_1 - y_0}{x_1 - x_0}$$
  です
  </div>
</div>
<div class="row">
  <div class="col-sm-6">
    <div id="svg02"></div>
  </div>
  <div class="col-sm-6">
  曲線の傾きについて考えます<br>
  まず曲線上の２点\((x_0,y_0),(x_1,y_1)\)の傾きを考えます<br>
  $$Slope=m=\frac{\Delta y}{\Delta x}=\frac{y_1 - y_0}{x_1 - x_0}$$
  これは、この範囲において\(x\)に対する\(y\)の変化量の平均です<br>

  いまは、２点を結ぶ直線の傾きを求めています<br>

  この直線のように曲線と交差し２つの部分に分ける線のことを割線(secant line)と呼びます<br>

  点\((x_0,y_0)\)を\((x_1,y_1)\)に近づけてゆくと、傾きの平均値ではなく
  \((x_1,y_1)\)における傾きに近づいていきます

  </div>
</div>

--------

# Introduction to derivatives (導関数)

--------

## Derivative as slope of a tangent line
<div class="row">
  <div class="col-sm-6">
    <div id="svg03"></div>
  </div>
  <div class="col-sm-6">
  緑の直線の傾き(slope)は、
  $$m=\frac{\Delta y}{\Delta x}=\frac{f(b) - f(a)}{b - a}$$
  $$a=2のときf(2)=3, \quad b=5のときf(5)=7 \quad とすると$$
  $$m=\frac{7-3}{5-2}=\frac{4}{3}$$
  </div>
</div>

<div class="row">
  <div class="col-sm-6">
    <div id="svg04"></div>
  </div>
  <div class="col-sm-6">
  曲線\(f(x)\)の傾きを考えます<br>
  曲線の傾きは、曲線上の各々の座標で異なっています<br>
  そこで<br>
  曲線上の１点を\( (x_0,f(x_0)) \)とします<br>
  ２点目を、\(x_0\)に\(h\)を加えた点\((x_0+h,f(x_0+h))\)とします<br>
  この２点を通る曲線\(f(x)\)に対する割線の傾きは
  $$m=\frac{f(x_0+h)-f(x_0)}{x_0+h-x_0}
  =\frac{f(x_0+h)-f(x_0)}{h}$$
  です<br>
  ここで、\(h\)の値を限りなく0に近づけていくと点\( (x_0,f(x_0)) \)での傾きに近づいてゆきます<br>
  曲線の点\( (x_0,f(x_0)) \)での傾きは、この点での接線(tangent line)の傾き
  <h3>
  $$\lim_{h \to 0} \frac{f(x_0+h)-f(x_0)}{h}$$
  </h3>
  となります
  </div>
</div>

--------

## Calculating slope of tangent line using derivative definition
<div class="row">
  <div class="col-sm-6">
    <div id="svg05"></div>
  </div>
  <div class="col-sm-6">
    \(f(x)=x^2\)です。<br>
    \(x=3\)のとき\(f(3)=9\)でピンクの点\((3,9)\)です<br>
    \(x=3+h\)のとき\(f(3+h)=(3+h)^2\)で黄色の点\((3+h,(3+h)^2))\)です<br>
    \(f'(x)\)を\(f(x)\)の導関数とすると、\(x=3\)のときの接線の傾きは<br>
    $$f'(x)=\lim_{h \to 0} \frac{f(3+h)-f(3)}{h}
    =\lim_{h \to 0} \frac{(3+h)^2-9}{h}$$
    $$\quad=\lim_{h \to 0} \frac{9+6h+h^2-9}{h}
    =\lim_{h \to 0} 6+h=6$$
    一般化すると
    $$f'(x)=\lim_{h \to 0} \frac{f(x+h)-f(x)}{h}
    =\lim_{h \to 0} \frac{(x+h)^2-x^2}{h}$$
    $$\quad=\lim_{h \to 0} \frac{x^2+2hx+h^2-x^2}{h}
    =\lim_{h \to 0} 2x+h=2x$$
    \(2x\)が曲線\(f(x)=x^2\)の各\(x\)における接線の傾きです
  </div>
</div>

## Formal and alternate form of the derivative
<div class="row">
  <div class="col-sm-6">
    <div id="svg06"></div>
  </div>
  <div class="col-sm-6">
  曲線\(y=f(x)\)の\(x=a\)における接線の傾きは
  $$点(a,f(a))とｘ軸方向にhだけ離れた点(a+h,f(a+h))を通る割線において$$
  \(h\)の値が限りなく0に近づいたときに下記の導関数で求められる
  $$f'(a)=\lim_{h \to 0}\frac{f(a+h)-f(a)}{h}$$  
  </div>
</div>
<div class="row">
  <div class="col-sm-6">
    <div id="svg07"></div>
  </div>
  <div class="col-sm-6">
  別の表現をすると
  曲線\(y=f(x)\)の\(x=a\)における接線の傾きは
  $$点(a,f(a))と点(x,f(x))を通る割線において$$
  \(x\)の値が限りなくaに近づいたときに下記の導関数で求められる
  $$f'(x)=\lim_{x \to a}\frac{f(x)-f(a)}{x-a}$$
  2つの導関数は同じことを表している  
  </div>
</div>

-----------

# Power rule

-----------

## Power rule

<div class="panel">
 <h3>
 $$f(x)=x^{n},n \ne 0 \to f'(x)= nx^{n-1}$$
 </h3>
</div>

$$f(x)=x^2 \to f'(x)=2x^{2-1}=2x$$
$$g(x)=x^5 \to g'(x)=5x^{5-1}=5x^4$$
$$h(x)=x^-100 \to h'(x)=-100x^{-100-1}=-100x^{-101}$$
$$i(x)=x^2.751 \to i'(x)=2.751x^{2.751-1}=2.751x^{1.751}$$

<div class="row">
  <div class="col-sm-6">
    <div id="svg08"></div>
  </div>
  <div class="col-sm-6">
    $$f(x)=xの導関数は$$
    $$f'(x)=1 \cdot x^{1-1}=x^0=1$$
    $$f(x)の傾きはどの点でも１ということです$$
  </div>
</div>

<div class="row">
  <div class="col-sm-6">
    <div id="svg09"></div>
  </div>
  <div class="col-sm-6">
  $$g(x)=x^2の導関数は$$
  $$g'(x)=2x^{2-1}=2x$$
  $$g(x)の線上の点における傾きは2xです$$ 
  $$g'(-2)=2 \cdot (-2) = -4$$
  $$g'(0)=2 \cdot 0 = 0$$
  $$g'(2)=2 \cdot 2 = 4$$  
  </div>
</div>

-----------------------------

## Derivative properties and polynomial derivatives

<div class="row">
  <div class="col-sm-6">
    <div id="svg10"></div>
  </div>
  <div class="col-sm-6">
    $$\frac{d}{dx}[x^n]=nx^{n-1},n \ne 0$$
    ですが\(n=0\)のときはどうなるでしょうか
    $$\frac{d}{dx}[x^0]=\frac{d}{dx}[1]=0$$
    $$関数f(x)=1つまりy=1の直線で、その傾きは0です$$
    $$y=3の直線も、傾きは0です$$
    
    $$\frac{d}{dx}[A]=0 \quad Aは定数$$
    $$\frac{d}{dx}[Af(x)]=A\frac{d}{dx}[f(x)]=Af'(x)$$
    $$\quad \frac{d}{dx}[2x^5]=2\frac{d}{dx}[x^5]=2 \cdot 5x^{5-1}
    =10x^4$$
    $$\frac{d}{dx}[f(x)+g(x)]
    =\frac{d}{dx}[f(x)]+\frac{d}{dx}[g(x)]=f'(x)+g'(x)$$
    $$\quad \frac{d}{dx}[x^2+x^{-4}]
    =\frac{d}{dx}[x^2]+\frac{d}{dx}[x^{-4}]
    =2x-4x^{-5}$$
    
  </div>
</div>

---------------

## $$Proof:\frac{d}{dx}[x^n]$$

$$\frac{d}{dx}[x^n]=nx^{n-1}$$
を証明します

$$曲線 x^n の任意の点xにおける接線の傾きは$$ 
$$\lim_{\Delta x \to 0}\frac{(x+\Delta x)^n-x^n}{\Delta x}$$
です

これを２項定理を使って展開します
$$\lim_{\Delta x \to 0}
\frac{x^n + 
  \left(
    \begin{array}{c}
      n \\\
      1 \\\
    \end{array}
  \right)
  x^{n-1}\Delta x
  +
  \left(
    \begin{array}{c}
      n \\\
      2 \\\
    \end{array}
  \right)
  x^{n-2}\Delta x^2
  +
  \cdots
  +
  \left(
    \begin{array}{c}
      n \\\
      n \\\
    \end{array}
  \right)
  \Delta x^n
  - x^n
  }
  {\Delta x}
$$
$$
\quad =\lim_{\Delta x \to 0} 
{
  \left(
    \begin{array}{c}
      n \\\
      1 \\\
    \end{array}
  \right)
  x^{n-1}
  +
  \left(
    \begin{array}{c}
      n \\\
      2 \\\
    \end{array}
  \right)
  x^{n-2}\Delta x^3
  +
  \cdots
  +
  \left(
    \begin{array}{c}
      n \\\
      n \\\
    \end{array}
  \right)
  \Delta x^{n-1}
}  
$$
$$\quad = 
{
  \left(
    \begin{array}{c}
      n \\\
      1 \\\
    \end{array}
  \right)
  x^{n-1}
}
=\frac{n!}{(n-1)!1!}x^{n-1}
$$
### $$ \quad =nx^{n-1}$$

---------------------

# Chain rule

---------------------

## Derivatives of \\(\sin x,\cos x, \tan x, e^x\\) and \\(\ln x\\) 

$$\frac{d}{dx}[\sin x] = \cos x$$
$$\frac{d}{dx}[\cos x] = -\sin x$$
$$\frac{d}{dx}[\tan x] = \frac{1}{\cos^2 x}=\sec^2 x$$
<br>
$$\frac{d}{dx}[e^x]=e^x$$
<br>
$$\frac{d}{dx}[\ln x]=\frac{1}{x}=x^{-1}$$

----------------------

## Chain rule introduction

$$h(x)=(\sin x)^2$$
の導関数
$$h'(x)=?$$

$$\frac{d}{dx}[x^2]=2x 
\quad \frac{d}{da}[a^2]=2a
\quad \frac{d}{d\sin x}[(\sin x)^2]=2\sin x$$ 
です

まずは外側の導関数を求めます
$$\frac{d}{d\sin x}[(\sin x)^2]=2\sin x$$
内側の導関数を求めます
$$\frac{d}{dx}[\sin x]=\cos x$$
２つを連結して
$$h'(x)= 2\sin x \cdot \cos x$$
となります

---+---+---+---+---+---+---+---+---+---+---+---+---

２つの関数が組み合わさった関数\\(f(g(x))\\)の導関数を考えます
$$\frac{d}{dx}[f(g(x))]=f'(g(x)) \cdot g'(x)$$
外側の関数f(g(x))の導関数を求め、内側の関数g(x)の導関数と連結します
<br>
\\(\sqrt{3x^2-x}\\)の導関数を求めてみます
$$\frac{d}{dx}[\sqrt{3x^2-x}]=?$$
まず
$$f(x)=\sqrt{x}=x^{\frac{1}{2}} \quad 
g(x)=3x^2-x$$
とします
$$f'(x)=\frac{1}{2}x^{-\frac{1}{2}}$$
$$f'(g(x))=\frac{1}{2}(3x^2-x)^{-\frac{1}{2}}$$
$$g'(x)=6x-1$$
\\(\sqrt{3x^2-x}\\)の導関数は２つを連結して
$$\frac{d}{dx}[\sqrt{3x^2-x}]
=\frac{1}{2}(3x^2-x)^{-\frac{1}{2}} \cdot (6x-1)$$
<br>
\\(2^x\\)の導関数を求めてみます
$$\frac{d}{dx}[2^x]=?$$
まず２を書き換えます
$$2=e^{\ln 2}$$
$$2^x=(e^{\ln 2})^x$$
$$\frac{d}{dx}[2^x]=\frac{d}{dx}[(e^{\ln 2})^x]$$
$$\frac{d}{d\ln 2 \cdot x}[e^{\ln 2 \cdot x}]=e^{\ln 2 \cdot x}$$
$$\frac{d}{dx}[\ln 2 \cdot x]=\ln 2$$
$$\frac{d}{dx}[(e^{\ln 2})^x]
=e^{\ln 2 \cdot x} \cdot \ln 2 
=2^x \cdot \ln 2$$

----------

## Derivative of log with arbitrary base

自然対数の導関数は
$$\frac{d}{dx}[\ln x]=\frac{1}{x}$$

ではbを底とする対数の導関数を求めます\\(\frac{d}{dx}[\log_{b} x]\\)

まず、対数の表現を底b　から底eに変更します
$$\log_{b} x=\frac{\log_{e} x}{\log_{e} x}=\frac{\ln x}{\ln b}$$
したがって
$$\frac{d}{dx}[\log_{b} x]
=\frac{d}{dx}[\frac{1}{\ln b} \cdot \ln x]
=\frac{1}{\ln b}\frac{d}{dx}[\ln x]
=\frac{1}{\ln b} \cdot \frac{1}{x}
=\frac{1}{(\ln b)x}$$

上記に従うと
$$\frac{d}{dx}[\log_{5} x]=\frac{1}{\ln 5 \cdot x}$$
となります

--------------

## Chain rule with triple composition

\\(\sin()\ln(x^2)\\)の導関数を求めます

関数を３つに分けます
$$f(x)=\sin(x)$$
$$g(x)=\ln x$$
$$h(x)=x^2$$

$$\frac{d}{dx}[\sin()\ln(x^2)]=\frac{d}{dx}[f(g(h(x)))]$$
$$ \quad = f'(g(h(x))) \cdot g'(h(x)) \cdot h'(x)$$
$$ \quad = \cos(\ln (x^2)) \cdot \frac{1}{x^2} \cdot 2x$$
例
$$F(x)=\sqrt{\ln(3x)}=(\ln(3x))^{\frac{1}{2}}$$
$$F'(x)=\frac{1}{2}(\ln(3x))^{-\frac{1}{2}} \cdot \frac{1}{3x} \cdot 3$$
$$\quad = \frac{1}{2x\sqrt{\ln(3x)}}$$ 

--------------------------

# Product and quotient rules

---------------------------

## The product rule for derivatives

２つの関数の積の導関数を求める法則は
$$\frac{d}{dx}[f(x)g(x)]=f'(x)g(x)+f(x)g'(x)$$
です
\\(\frac{d}{dx}[x^2\sin x]\\)を求めます
$$f(x)=x^2 \qquad g(x)=\sin x$$
$$f'(x)=2x \qquad g'(x)=\cos x$$
<br>
$$\frac{d}{dx}[x^2\sin x] 
=2x\sin x + x^2\cos x$$  

----------------

## Product rule for more than two functions

$$\frac{d}{dx}[f(x)g(x)h(x)]を求めます$$
まず\\(f(x)とg(x)h(x)\\)に分けて考えると
$$\frac{d}{dx}[f(x)g(x)h(x)]
=\frac{d}{dx}[f(x)]g(x)h(x)+f(x)\frac{d}{dx}[g(x)h(x)]
=f'(x)g(x)h(x)+f(x)g'(x)h(x)+f(x)g(x)'h(x)$$
３つの関数のうちの１つが１回づつ導関数となった積の和なので

関数が４つの場合、４つの関数の積でそのうちの１つが１回筒導関数となった和

ｎ個の関数の場合も同様

-----------------

## Quotient rule from product rule

\\(\frac{d}{dx}[\frac{f(x)}{g(x)}]\\)を求めます
$$\frac{d}{dx}[\frac{f(x)}{g(x)}]
=\frac{d}{dx}[f(x)g(x)^{-1}]$$
puroduct rule と　chain rule を使って
$$=f'(x)g(x)^{-1}+f(x)(-1)g(x)^{-2}g'(x)
=\frac{f'(x)}{g(x)}-\frac{f(x)g'(x)}{g(x)^2}
=\frac{f'(x)g(x)}{g(x)^2}-\frac{f(x)g'(x)}{g(x)^2}$$
$$\quad = \frac{f'(x)g(x)-f(x)g'(x)}{g(x)^2}$$

<br>
quotient ruleを使って　\\(\tan x\\)の導関数を求めます

$$\frac{d}{dx}[\tan x]=\frac{d}{dx}[\frac{\sin x}{\cos x}]
=\frac{\cos x \cos x + \sin x \sin x}{\cos^2 x}$$
$$\quad = \frac{\cos^2 x + \sin^2 x}{\cos^2 x}
=\frac{1}{\cos^2}=(\frac{1}{\cos x})^2=\sec^2 x$$

---------------

# Implicit differentiation

----------------

## Implicit differentiation

<div class="row">
  <div class="col-sm-6">
    単位円上の任意の点\((x,y)\)における接線の傾きを求めます
    <br>
    １つの\(x\)の値に対して\(y\)の値は２つ存在します
    $$x^2 + y^2 = 1$$
    $$y^2=1-x^2 \to y=\pm \sqrt{1-x}$$
    この式を微分して傾きを求めることもできますが、今回はimplicit differentiationと呼ばれる方法を行います
    <br>
    \(x^2 + y^2 = 1\)の両辺を微分します
    $$\frac{d}{dx}[x^2 + y^2]=\frac{d}{dx}[1]$$
    $$\frac{d}{dx}[x^2]+\frac{d}{dx}[y^2]=0$$
    $$2x+\frac{d(y^2)}{dy} \cdot \frac{dy}{dx}=0$$
    $$2x+2y \cdot \frac{dy}{dx}=0$$
    $$\frac{dy}{dx}=\frac{-2x}{2y}$$
    <h3>$$\frac{dy}{dx}=-\frac{x}{y}$$</h3>
  </div>
  <div class="col-sm-6">
    <div id="svg11"></div>
    点\( (\frac{\sqrt{2}}{2},\frac{\sqrt{2}}{2})\)での
    接線の傾きは
    $$-\frac{x}{y}=\frac{\frac{\sqrt{2}}{2}}{\frac{\sqrt{2}}{2}}=-1$$
  </div>
</div>

---------------------

## Showing explicit and implicit differentiation give same result

関数 \\(x\\sqrt{y}=1\\) を明示的に微分すると

$$x\sqrt{y}=1 \to \sqrt{y} = \frac{1}{x}
\quad y=\frac{1}{x^2}=x^{-2}
\quad \frac{dy}{dx}=-2x^{-3}$$

暗黙の微分をすると
$$\frac{d}{dx}[x\sqrt{y}]=\frac{d}{dx}[1]$$
product ruleで
$$\frac{d}{dx}[x]\cdot\sqrt{y}+x\cdot\frac{d}{dx}[\sqrt{y}]=0$$
$$\sqrt{y}+x \cdot \frac{d(\sqrt{y})}{dy}\cdot\frac{dy}{dx}=0$$
$$\sqrt{y}+x \cdot \frac{1}{2}y^{-\frac{1}{2}}\cdot\frac{dy}{dx}=0$$
$$\frac{x}{2\sqrt{y}}\frac{dy}{dx}=-\sqrt{y}$$
$$\frac{dy}{dx}=-\frac{2\sqrt{y}\sqrt{y}}{x}=-\frac{2y}{x}$$
<br>
\\(-2x^{-3}\\)と\\(-\frac{2y}{x}\\)はだいぶ形が違うようですが
<br>
\\(y=x^{-2}\\)を代入すると
$$-\frac{2y}{x}=-\frac{2}{x^2\cdotx}=-2x^{-3}$$

--------------

## Implicit derivative of \\((x-y)^2=x+y-1\\)　

$$\frac{d}{dx}[(x-y)^2]=\frac{d}{dx}[x+y-1]$$
$$\frac{d(x-y)^2}{d(x-y)} \cdot \frac{d(x-y)}{dx} 
=\frac{d}{dx}[x]+\frac{dy}{dx}-\frac{d}{dx}[1]$$
$$2(x-y)(1-\frac{dy}{dx})=1+\frac{dy}{dx}$$
$$(2x-2y)(1-\frac{dy}{dx})=1+\frac{dy}{dx}$$
$$(2x-2y)+(2y-2x)\frac{dy}{dx}=1+\frac{dy}{dx}$$
$$(2y-2x)\frac{dy}{dx}-\frac{dy}{dx}=1-(2x-2y)$$
$$(2y-2x-1)\frac{dy}{dx}=2y-2x+1$$
$$\frac{dy}{dx}=\frac{2y-2x+1}{2y-2x-1}$$

---------

## Implicit derivative of \\(y=\\cos (5x-3y)\\)

$$\frac{dy}{dx}=\frac{d}{dx}[\cos (5x-3y)]$$
$$\frac{dy}{dx}=-\sin(5x-3y) \cdot (5-3\frac{dy}{dx})$$
$$\frac{dy}{dx}=-5\sin(5x-3y)+3\sin(5x-3y)\frac{dy}{dx}$$
$$(1-3\sin(5x-3y))\frac{dy}{dx}=-5\sin(5x-3y)$$
$$\frac{dy}{dx}=\frac{-5\sin(5x-3y)}{1-3\sin(5x-3y)}$$

------------

## Implicit derivative of \\((x^2+y^2)^3=5x^2y^2\\)

$$\frac{d}{dx}[(x^2+y^2)^3]=\frac{d}{dx}[5x^2y^2]$$
$$3(x^2+y^2)^{2}(2x+2y\frac{dy}{dx})=5[2xy^2+x^2 2y\frac{dy}{dx}]$$
$$6x(x^2+y^2)^2+6y(x^2+y^2)^2\frac{dy}{dx}
=10xy^2+10x^2y\frac{dy}{dx}$$
$$6y(x^2+y^2)^2\frac{dy}{dx}-10x^2y\frac{dy}{dx}
=10xy^2-6x(x^2+y^2)^2$$
$$(6y(x^2+y^2)^2-10x^2y)\frac{dy}{dx}=10xy^2-6x(x^2+y^2)^2$$
$$\frac{dy}{dx}=\frac{10xy^2-6x(x^2+y^2)^2}{(6y(x^2+y^2)^2-10x^2y)}$$

--------------

## Finding slope of tangent line with implicit differentiation

\\(x^2+(y-x)^3=28\\)の\\(x=1\\)のときの接線の傾きを求めます

最初に\\(x=1\\)のときの\\(y\\)の値を求めておきます

$$1^2+(y-1)^3=28$$
$$(y-1)^3=27$$
$$y-1=3$$
$$y=4$$
点\\( (1,4) \\)における接線の傾きを求めることになります
$$\frac{d}{dx}[(x^2+(y-x)^3]=\frac{d}{dx}[28]$$
$$2x+3(y-x)^2(\frac{dy}{dx}-1)=0$$
$$2x+3(y-x)^2\frac{dy}{dx}-3(y-x)^2=0$$
$$3(y-x)^2\frac{dy}{dx}=3(y-x)^2-2x$$
$$\frac{dy}{dx}=\frac{3(y-x)^2-2x}{3(y-x)^2}
=\frac{3(4-1)^2-2 \cdot 1}{3(4-1)^2}=\frac{25}{27}$$

---------------

## Implicit derivative of \\(e^{xy^2} = x - y\\)

今回は別の表記法を使って導関数を求めてみます

$$D=\frac{d}{dx} \quad y'=\frac{dy}{dx}$$
とします
$$D[e^{xy^2}] = D[x - y]$$
chain rule
$$e^{xy^2} \cdot D[xy^2]=1-y'$$
product rule
$$e^{xy^2} (y^2+x\cdot 2yy')=1-y'$$
$$y^2e^{xy^2}+2yxe^{xy^2}y'=1-y'$$
$$2yxe^{xy^2}y'+y'=1-y^2e^{xy^2}$$
$$(2yxe^{xy^2}+1)y'=1-y^2e^{xy^2}$$
$$y'=\frac{1-y^2e^{xy^2}}{2xye^{xy^2}+1}$$

-------------

# Derivatives of inverse functions

-------------

## Derivative of inverse sine

\\(y=\sin^{-1} x\\)の導関数を求めます

$$y=\sin^{-1} x \Leftrightarrow \sin y = x$$
なので
$$\frac{d}{dx}[\sin y]=\frac{d}{dx}[x]$$
$$\cos y \frac{dy}{dx}=1$$
$$\frac{dy}{dx}=\frac{1}{\cos y}$$
ここで
$$\sin^2 y + \cos^2 y = 1 \to \cos^2 y = 1 - \sin^2 y 
\to \cos y = \sqrt{1-\sin^2 y}$$
置き換えると
$$\frac{dy}{dx}=\frac{1}{\sqrt{1-\sin^2 y}}
=\frac{1}{\sqrt{1-x^2}}$$

----------------

## Derivative of inverse cosine

\\(y=\cos^{-1} x\\)の導関数を求めます

$$y=\cos^{-1} x \Leftrightarrow \cos y = x$$
なので
$$\frac{d}{dx}[\cos y]=\frac{d}{dx}[x]$$
$$-\sin y \frac{dy}{dx}=1$$
$$\frac{dy}{dx}=-\frac{1}{\sin y}$$
ここで
$$\sin^2 y + \cos^2 y = 1 \to \sin^2 y = 1 - \cos^2 y 
\to \sin y = \sqrt{1-\cos^2 y}$$
置き換えると
$$\frac{dy}{dx}=-\frac{1}{\sqrt{1-\cos^2 y}}
=-\frac{1}{\sqrt{1-x^2}}$$

----------------

## Derivative of inverse tangent

$$\frac{d}{dx}[\tan x]=\sec^2 x = \frac{1}{\cos^2 x}$$
を知っています
$$y=\tan^{-1} x \Leftrightarrow \tan y = x$$
$$\frac{d}{dx}[\tan y]=\frac{d}{dx}[x]$$
$$\frac{1}{\cos^2 y}\frac{dy}{dx}=1$$
$$\frac{dy}{dx}=\cos^2 y$$
ここでテクニックを
$$\frac{dy}{dx}=\frac{\cos^2 y}{\cos^2 y + \sin^2 y}$$
\\(\cos^2 y\\)で分子分母を割ります
$$\frac{dy}{dx}=\frac{1}{1+(\frac{\sin y}{\cos y})^2}$$
$$\frac{dy}{dx}=\frac{1}{1+(\tan y)^2}=\frac{1}{1+x^2}$$

--------------

## Derivative of natural logarithm

$$\frac{d}{dx}[\ln x]=?$$
$$y=\ln x \Leftrightarrow e^y=x$$
$$\frac{d}{dx}[e^y]=\frac{d}{dx}[x]$$
$$e^y\frac{dy}{dx}=1$$
$$\frac{dy}{dx}=\frac{1}{e^y}=\frac{1}{e^{\ln x}}=\frac{1}{x}$$

--------------

## Derivative of \\(x^{x^x}\\)

\\(y=x^x\\)の導関数を求めます

両辺の自然対数をとります
$$\ln y = \ln x^x$$
$$\ln y = x\ln x$$
両辺を微分します
$$\frac{d}{dx}[\ln y]=\frac{d}{dx}[x\ln x]$$
$$\frac{1}{y}\frac{dy}{dx}=\ln x + x\frac{1}{x}$$
$$\frac{1}{y}\frac{dy}{dx}=\ln x + 1$$
$$\frac{dy}{dx}=y(\ln x + 1)$$
$$\frac{dy}{dx}=x^x(\ln x + 1)$$
<br>
上の結果を利用して\\(y=x^{(x^x)}\\)を微分します

両辺の自然対数をとります
$$\ln y = \ln (x^{(x^x)})=x^x\ln x$$
両辺を微分します
$$\frac{d}{dx}[\ln y]=\frac{d}{dx}[x^x\ln x]$$
$$\frac{1}{y}\frac{dy}{dx}=\frac{d}{dx}[x^x]\ln x + x^x\frac{d}{dx}[\ln x]$$
$$\frac{1}{y}\frac{dy}{dx}=x^x(\ln x + 1)\ln x + x^x\frac{1}{x}$$
$$\frac{dy}{dx}=y(x^x(\ln x + 1)\ln x + x^{x-1})$$
$$\frac{dy}{dx}=x^{(x^x)}(x^x(\ln x + 1)\ln x + x^{x-1})$$

---------------

## Derivative using log properties

\\(f(x)=\ln \frac{x+5}{x-1}\\)の導関数\\(f'(x)\\)を求めます

簡単な方法と難しい方法の２通りあります

Easy way

公式 \\(\ln\frac{a}{b}=\ln a - \ln b\\)を使います
$$f(x)=\ln \frac{x+5}{x-1}=\ln(x+5)-\ln(x-1)$$
$$f'(x)=\frac{1}{x+5}-\frac{1}{x-1}$$

Hard way
$$f'(x)=\frac{1}{\frac{x+5}{x-1}}\frac{d}{dx}[\frac{x+5}{x-1}]$$
$$\quad =\frac{x-1}{x+5}\frac{d}{dx}[(x+5)(x-1)^{-1}]$$
$$\quad =\frac{x-1}{x+5}(\frac{1}{x-1}+(x+5)\frac{-1}{(x-1)^2})$$
$$\quad =\frac{1}{x+5}-\frac{1}{x-1}$$





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

  var svg02 = d3.select("#svg02")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");

  var xScale01 = d3.scale.linear()
                       .domain([-1,9])
                       .range([50,450]);
  
  var yScale01 = d3.scale.linear()
                       .domain([9,-1])
                       .range([50,450]);       

  // 軸
  axesData01 = { 
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
    "xScale":xScale01,
    "yScale":yScale01
  };
  drawAxes(svg01,axesData01);
  drawAxes(svg02,axesData01);
  
  gridData01 = 
  {
    "xGrid":true,
    "yGrid":false,
    "xStep":1,
    "yStep":1,
    "stroke":"#0f0",
    "strokeWidth":1,
    "opacity":0.3,
    "xScale":xScale01,
    "yScale":yScale01
  };
  drawGrid(svg01,gridData01);
  drawGrid(svg02,gridData01);

  // graph
  lineData01 = [
    {"x1":-1,"y1":1,"x2":9,"y2":8,"stroke":"#0f0"},
    {"x1":2,"y1":0,"x2":2,"y2":3.1,"stroke":"#f0f","opacity":0.4},
    {"x1":0,"y1":3.1,"x2":2,"y2":3.1,"stroke":"#f0f","opacity":0.4},
    {"x1":4,"y1":0,"x2":4,"y2":4.5,"stroke":"#ff0","opacity":0.5},
    {"x1":0,"y1":4.5,"x2":4,"y2":4.5,"stroke":"#ff0","opacity":0.5},
  ];
  drawLine(svg01,lineData01,xScale01,yScale01);

  // circle
  var circleData01 = [
    {"cx":2,"cy":7*2/10+1.7,"r":2,"stroke":"#f0f","fillColor":"#f0f"}
   ,{"cx":4,"cy":7*4/10+1.7,"r":2,"stroke":"#ff0","fillColor":"#ff0"}
  ];   
  drawCircle(svg01,circleData01,xScale01,yScale01);

  // mathjax   
  foData01 = [
    {"x":9.5,
    "y":1.5,
    "text":"$$x$$",
    "fontSize":"24px"},
    {"x":-0.1,
    "y":11.5,
    "text":"$$y$$",
    "fontSize":"24px"},
    {"x":1.9,
    "y":1,
    "text":"$$x_0$$",
    "fontSize":"18px"},
    {"x":3.9,
    "y":1,
    "text":"$$x_1$$",
    "fontSize":"18px"},
    {"x":-0.8,
    "y":4.8,
    "text":"$$y_0$$",
    "fontSize":"18px"},
    {"x":-0.8,
    "y":6.1,
    "text":"$$y_1$$",
    "fontSize":"18px"},
    {"x":2.7,
    "y":0,
    "text":"$$\\Delta x$$",
    "fontSize":"18px"},
    {"x":-1.8,
    "y":5.3,
    "text":"$$\\Delta y$$",
    "fontSize":"18px"}
  ];
 
  drawMathjax(svg01,foData01,xScale01,yScale01);

  var pathData02 = [];
  for (var i=-1;i<=9;i=i+0.1){
    var y =  0.3*Math.pow((i-3),2)+3.5;
    pathData02.push(new Point(i,y));
  }
  drawPath(svg02,pathData02,{"stroke":"#ff0"},xScale01,yScale01);

  // line
  lineData02 = [
    {"x1":-1,"y1":1.1,"x2":9,"y2":7.1,"stroke":"lime"},
    {"x1":5,"y1":0,"x2":5,"y2":4.7,"stroke":"#0f0","opacity":0.4},
    {"x1":0,"y1":4.7,"x2":5,"y2":4.7,"stroke":"#0f0","opacity":0.4},
    {"x1":3,"y1":0,"x2":3,"y2":3.5,"stroke":"#f0f","opacity":0.5},
    {"x1":0,"y1":3.5,"x2":3,"y2":3.5,"stroke":"#f0f","opacity":0.5},
  ];
  drawLine(svg02,lineData02,xScale01,yScale01);

  // circle
  var circleData02 = [
    {"cx":3,"cy":3.5,"r":2,"stroke":"#f0f","fillColor":"#f0f"}
   ,{"cx":5,"cy":4.7,"r":2,"stroke":"#0f0","fillColor":"#0f0"}
  ];   
  drawCircle(svg02,circleData02,xScale01,yScale01);

  // mathjax   
  foData02 = [
    {"x":9.5,
    "y":1.5,
    "text":"$$x$$",
    "fontSize":"24px"},
    {"x":-0.1,
    "y":11.5,
    "text":"$$y$$",
    "fontSize":"24px"},
    {"x":2.9,
    "y":1,
    "text":"$$x_0$$",
    "fontSize":"18px"},
    {"x":4.9,
    "y":1,
    "text":"$$x_1$$",
    "fontSize":"18px"},
    {"x":-0.8,
    "y":5.0,
    "text":"$$y_0$$",
    "fontSize":"18px"},
    {"x":-0.8,
    "y":6.3,
    "text":"$$y_1$$",
    "fontSize":"18px"},
    {"x":3.7,
    "y":0,
    "text":"$$\\Delta x$$",
    "fontSize":"18px"},
    {"x":-1.8,
    "y":5.5,
    "text":"$$\\Delta y$$",
    "fontSize":"18px"},
    {"x":6,
    "y":6.5,
    "text":"$$secant \\quad line$$",
    "fontSize":"18px"}
  ];
 
  drawMathjax(svg02,foData02,xScale01,yScale01);


// Introduction to derivatives
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


  var xScale03 = d3.scale.linear()
                       .domain([-2,8])
                       .range([50,450]);
  
  var yScale03 = d3.scale.linear()
                       .domain([8,-2])
                       .range([50,450]);       

  // 軸
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
  drawAxes(svg03,axesData03);
  drawAxes(svg04,axesData03);
  
  gridData03 = 
  {
    "xGrid":true,
    "yGrid":true,
    "xStep":1,
    "yStep":1,
    "stroke":"#0f0",
    "strokeWidth":1,
    "opacity":0.3,
    "xScale":xScale03,
    "yScale":yScale03
  };
  drawGrid(svg03,gridData03);
  drawGrid(svg04,gridData03);

  // graph
  lineData03 = [
    {"x1":-2,"y1":func03(-2),"x2":8,"y2":func03(8),"stroke":"#0f0"},
    {"x1":2,"y1":0,"x2":2,"y2":3,"stroke":"#f0f","opacity":0.4},
    {"x1":0,"y1":3,"x2":2,"y2":3,"stroke":"#f0f","opacity":0.4},
    {"x1":5,"y1":0,"x2":5,"y2":7,"stroke":"#ff0","opacity":0.5},
    {"x1":0,"y1":7,"x2":5,"y2":7,"stroke":"#ff0","opacity":0.5},
  ];
  drawLine(svg03,lineData03,xScale03,yScale03);

  // circle
  var circleData03 = [
    {"cx":2,"cy":3,"r":2,"stroke":"#f0f","fillColor":"#f0f"}
   ,{"cx":5,"cy":7,"r":2,"stroke":"#ff0","fillColor":"#ff0"}
  ];   
  drawCircle(svg03,circleData03,xScale03,yScale03);

  // mathjax   
  foData03 = [
    {"x":8.5,
    "y":1.2,
    "text":"$$x$$",
    "fontSize":"22px"},
    {"x":-0.1,
    "y":10.5,
    "text":"$$y=f(x)$$",
    "fontSize":"22px"},
    {"x":1.9,
    "y":1,
    "text":"$$a$$",
    "fontSize":"18px"},
    {"x":4.9,
    "y":1,
    "text":"$$b$$",
    "fontSize":"18px"},
    {"x":-1.2,
    "y":4.5,
    "text":"$$f(a)$$",
    "fontSize":"18px"},
    {"x":-1.2,
    "y":8.5,
    "text":"$$f(b)$$",
    "fontSize":"18px"},
    {"x":3,
    "y":0,
    "text":"$$\\Delta x$$",
    "fontSize":"18px"},
    {"x":-1.8,
    "y":6.3,
    "text":"$$\\Delta y$$",
    "fontSize":"18px"}
  ];
 
  drawMathjax(svg03,foData03,xScale03,yScale03);

  function func03(x){
    return (4*x + 1)/3;
  };

  pathData04 = [];
  for (var i=0;i<=8;i=i+0.1){
    pathData04.push(new Point(i,func04(i)));
  }
  drawPath(svg04,pathData04,{"stroke":"#ff0"},xScale03,yScale03);

  // lines
  lineData04 = [
    {"x1":3,"y1":func04(3),"x2":7,"y2":func04(7),"stroke":"#0f0"},
    {"x1":3,"y1":0,"x2":3,"y2":func04(3),"stroke":"#f0f","opacity":0.4},
    {"x1":0,"y1":func04(3),"x2":3,"y2":func04(3),"stroke":"#f0f","opacity":0.4},
    {"x1":7,"y1":0,"x2":7,"y2":func04(7),"stroke":"#f0f","opacity":0.4},
    {"x1":0,"y1":func04(7),"x2":7,"y2":func04(7),"stroke":"#f0f","opacity":0.4},
  ];
  drawLine(svg04,lineData04,xScale03,yScale03);

  // circle
  var circleData04 = [
    {"cx":3,"cy":func04(3),"r":2,"stroke":"#f0f","fillColor":"#f0f"}
   ,{"cx":7,"cy":func04(7),"r":2,"stroke":"#f0f","fillColor":"#f0f"}
  ];   
  drawCircle(svg04,circleData04,xScale03,yScale03);

  // mathjax   
  foData04 = [
    {"x":8.5,
    "y":1.2,
    "text":"$$x$$",
    "fontSize":"22px"},
    {"x":-0.1,
    "y":10.5,
    "text":"$$f(x)$$",
    "fontSize":"22px"},
    {"x":2.9,
    "y":1,
    "text":"$$x_0$$",
    "fontSize":"18px"},
    {"x":6.2,
    "y":1,
    "text":"$$x_0+h$$",
    "fontSize":"18px"},
    {"x":-1.4,
    "y":3.6,
    "text":"$$f(x_0)$$",
    "fontSize":"18px"},
    {"x":-2.5,
    "y":8.0,
    "text":"$$f(x_0 + h)$$",
    "fontSize":"18px"},
    {"x":5,
    "y":0,
    "text":"$$\\Delta x$$",
    "fontSize":"18px"},
    {"x":-1.8,
    "y":6.0,
    "text":"$$\\Delta y$$",
    "fontSize":"18px"}
  ];
 
  drawMathjax(svg04,foData04,xScale03,yScale03);

  function func04(x){
    return x*x/9 + 1;
  };

  // 
  var svg05 = d3.select("#svg05")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");


  var xScale05 = d3.scale.linear()
                       .domain([-2,7])
                       .range([50,450]);
  
  var yScale05 = d3.scale.linear()
                       .domain([50,-1])
                       .range([50,450]);       

  // 軸
  axesData05 = { 
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
    "xScale":xScale05,
    "yScale":yScale05
  };
  drawAxes(svg05,axesData05);
  
  gridData05 = 
  {
    "xGrid":true,
    "yGrid":true,
    "xStep":1,
    "yStep":5,
    "stroke":"#0f0",
    "strokeWidth":1,
    "opacity":0.3,
    "xScale":xScale05,
    "yScale":yScale05
  };
  drawGrid(svg05,gridData05);

  // graph
  pathData05 = [];
  for (var i=-2;i<=7;i=i+0.1){
    pathData05.push(new Point(i,i*i));
  }
  drawPath(svg05,pathData05,{"stroke":"#ff0"},xScale05,yScale05);

  lineData05 = [
    {"x1":1,"y1":-9,"x2":7,"y2":45,"stroke":"#f0f"},
    {"x1":0,"y1":-9,"x2":7,"y2":33,"stroke":"lime"},
    {"x1":3,"y1":0,"x2":3,"y2":9,"stroke":"#f0f","opacity":0.4},
    {"x1":0,"y1":9,"x2":3,"y2":9,"stroke":"#f0f","opacity":0.4},
    {"x1":6,"y1":0,"x2":6,"y2":36,"stroke":"#ff0","opacity":0.5},
    {"x1":0,"y1":36,"x2":6,"y2":36,"stroke":"#ff0","opacity":0.5},
  ];
  drawLine(svg05,lineData05,xScale05,yScale05);

  // circle
  var circleData05 = [
    {"cx":3,"cy":9,"r":2,"stroke":"#f0f","fillColor":"#f0f"}
   ,{"cx":6,"cy":36,"r":2,"stroke":"#ff0","fillColor":"#ff0"}
  ];   
  drawCircle(svg05,circleData05,xScale05,yScale05);

  // mathjax   
  foData05 = [
    {"x":7.5,
    "y":5.5,
    "text":"$$x$$",
    "fontSize":"22px"},
    {"x":0.5,
    "y":60.5,
    "text":"$$y=f(x)$$",
    "fontSize":"22px"},
    {"x":2.9,
    "y":5.5,
    "text":"$$3$$",
    "fontSize":"18px"},
    {"x":5.5,
    "y":5.5,
    "text":"$$3+h$$",
    "fontSize":"18px"},
    {"x":-1.2,
    "y":15,
    "text":"$$f(3)$$",
    "fontSize":"18px"},
    {"x":-1.8,
    "y":43,
    "text":"$$f(3+h)$$",
    "fontSize":"18px"},
    {"x":4.2,
    "y":2,
    "text":"$$\\Delta x$$",
    "fontSize":"18px"},
    {"x":-1.8,
    "y":30,
    "text":"$$\\Delta y$$",
    "fontSize":"18px"},
    {"x":1.5,
    "y":32,
    "text":"$$secant \\quad line$$",
    "fontSize":"18px"},
    {"x":4.4,
    "y":24,
    "text":"$$tangent \\quad line$$",
    "fontSize":"18px"}
  ];
 
  drawMathjax(svg05,foData05,xScale05,yScale05);

  // Formal and alternate form of the derivative
  var svg06 = d3.select("#svg06")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg07 = d3.select("#svg07")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");


  var xScale06 = d3.scale.linear()
                       .domain([-1,9])
                       .range([50,450]);
  
  var yScale06 = d3.scale.linear()
                       .domain([3,-3])
                       .range([50,450]);       

  // 軸
  axesData06 = { 
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
    "xScale":xScale06,
    "yScale":yScale06
  };
  drawAxes(svg06,axesData06);
  drawAxes(svg07,axesData06);
  
  gridData06 = 
  {
    "xGrid":true,
    "yGrid":true,
    "xStep":1,
    "yStep":1,
    "stroke":"#0f0",
    "strokeWidth":1,
    "opacity":0.3,
    "xScale":xScale06,
    "yScale":yScale06
  };
  drawGrid(svg06,gridData06);
  drawGrid(svg07,gridData06);

  // graph
  pathData06 = [];
  for (var i=0.05;i<=9;i=i+0.05){
    pathData06.push(new Point(i,Math.log(i)));
  }
  drawPath(svg06,pathData06,{"stroke":"#ff0"},xScale06,yScale06);
  drawPath(svg07,pathData06,{"stroke":"#ff0"},xScale06,yScale06);

  lineData06 = [
    {"x1":-1,"y1":-0.3679,"x2":9,"y2":3.3109,"stroke":"#f0f"},
    {"x1":Math.E,"y1":0,"x2":Math.E,"y2":Math.log(Math.E),"stroke":"#f0f","opacity":0.4},
    {"x1":0,"y1":1,"x2":Math.E,"y2":1,"stroke":"#f0f","opacity":0.4},
    {"x1":5,"y1":0,"x2":5,"y2":Math.log(5),"stroke":"#ff0","opacity":0.5},
    {"x1":0,"y1":Math.log(5),"x2":5,"y2":Math.log(5),"stroke":"#ff0","opacity":0.5},
  ];
  drawLine(svg06,lineData06,xScale06,yScale06);
  drawLine(svg07,lineData06,xScale06,yScale06);

  // circle
  var circleData06 = [
    {"cx":Math.E,"cy":Math.log(Math.E),"r":2,"stroke":"#f0f","fillColor":"#f0f"}
   ,{"cx":5,"cy":Math.log(5),"r":2,"stroke":"#ff0","fillColor":"#ff0"}
  ];   
  drawCircle(svg06,circleData06,xScale06,yScale06);
  drawCircle(svg07,circleData06,xScale06,yScale06);

  // mathjax   
  foData06 = [
    {"x":9.5,
    "y":1.0,
    "text":"$$x$$",
    "fontSize":"22px"},
    {"x":-0.3,
    "y":4.5,
    "text":"$$y$$",
    "fontSize":"22px"},
    {"x":7.5,
    "y":3.5,
    "text":"$$y=f(x)$$",
    "fontSize":"22px"},
    {"x":Math.E-0.1,
    "y":0.5,
    "text":"$$a$$",
    "fontSize":"18px"},
    {"x":4.5,
    "y":0.5,
    "text":"$$a+h$$",
    "fontSize":"18px"},
    {"x":-1,
    "y":1.9,
    "text":"$$f(a)$$",
    "fontSize":"18px"},
    {"x":-2,
    "y":2.5,
    "text":"$$f(a+h)$$",
    "fontSize":"18px"},
  ];
 
  drawMathjax(svg06,foData06,xScale06,yScale06);

  // mathjax   
  foData07 = [
    {"x":9.5,
    "y":1.0,
    "text":"$$x$$",
    "fontSize":"22px"},
    {"x":-0.3,
    "y":4.5,
    "text":"$$y$$",
    "fontSize":"22px"},
    {"x":7.5,
    "y":3.5,
    "text":"$$y=f(x)$$",
    "fontSize":"22px"},
    {"x":Math.E-0.1,
    "y":0.5,
    "text":"$$a$$",
    "fontSize":"18px"},
    {"x":4.9,
    "y":0.5,
    "text":"$$x$$",
    "fontSize":"18px"},
    {"x":-1,
    "y":1.9,
    "text":"$$f(a)$$",
    "fontSize":"18px"},
    {"x":-1,
    "y":2.5,
    "text":"$$f(x)$$",
    "fontSize":"18px"},
  ];
 
  drawMathjax(svg07,foData07,xScale06,yScale06);

  // Power rule 
  var svg08 = d3.select("#svg08")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");


  var xScale08 = d3.scale.linear()
                       .domain([-1,5])
                       .range([50,450]);
  
  var yScale08 = d3.scale.linear()
                       .domain([5,-1])
                       .range([50,450]);       

  // 軸
  axesData08 = { 
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
    "xScale":xScale08,
    "yScale":yScale08
  };
  drawAxes(svg08,axesData08);

  gridData08 = 
  {
    "xGrid":true,
    "yGrid":true,
    "xStep":1,
    "yStep":1,
    "stroke":"#0f0",
    "strokeWidth":1,
    "opacity":0.3,
    "xScale":xScale08,
    "yScale":yScale08
  };
  drawGrid(svg08,gridData08);

  lineData08 = [
    {"x1":-1,"y1":-1,"x2":5,"y2":5,"stroke":"#fff"},
    {"x1":-1,"y1":1,"x2":5,"y2":1,"stroke":"#f0f"},
  ];
  drawLine(svg08,lineData08,xScale08,yScale08);

  // mathjax   
  foData08 = [
    {"x":5.5,
    "y":1.0,
    "text":"$$x$$",
    "fontSize":"22px"},
    {"x":-0.3,
    "y":6.5,
    "text":"$$y$$",
    "fontSize":"22px"},
    {"x":3,
    "y":3.5,
    "text":"$$y=f(x)=x$$",
    "fontSize":"18px"},
    {"x":3,
    "y":1.5,
    "text":"$$f'(x)=1$$",
    "fontSize":"18px"},
  ];
 
  drawMathjax(svg08,foData08,xScale08,yScale08);

  // g(x)=x^2
  var svg09 = d3.select("#svg09")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");


  var xScale09 = d3.scale.linear()
                       .domain([-4,4])
                       .range([50,450]);
  
  var yScale09 = d3.scale.linear()
                       .domain([10,-4])
                       .range([50,450]);       

  // 軸
  axesData09 = { 
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[-3,-2,-1,1,2,3],
    "yTickValues":[1,4,9],
    "xTickPadding":5,
    "yTickPadding":2,
    "xOrient":["bottom"],
    "yOrient":["left"],
    "stroke":"#ff0",
    "strokeWidth":1,
    "fillColor":"none",
    "xScale":xScale09,
    "yScale":yScale09
  };
  drawAxes(svg09,axesData09);

  gridData09 = 
  {
    "xGrid":true,
    "yGrid":true,
    "xStep":1,
    "yStep":1,
    "stroke":"#0f0",
    "strokeWidth":1,
    "opacity":0.3,
    "xScale":xScale09,
    "yScale":yScale09
  };
  drawGrid(svg09,gridData09);

  pathData09 =[];
  for (var i=-3.2;i<=3.3;i=i+0.1){
    pathData09.push(new Point(i,i*i));
  }
  drawPath(svg09,pathData09,{"stroke":"#fff"},xScale09,yScale09);


  lineData09 = [
    {"x1":-2,"y1":-4,"x2":4,"y2":8,"stroke":"#f0f"},
  ];
  drawLine(svg09,lineData09,xScale09,yScale09);

  // mathjax   
  foData09 = [
    {"x":4,
    "y":1.0,
    "text":"$$x$$",
    "fontSize":"22px"},
    {"x":-0.3,
    "y":12.5,
    "text":"$$y$$",
    "fontSize":"22px"},
    {"x":2,
    "y":12.5,
    "text":"$$y=g(x)=x^2$$",
    "fontSize":"18px"},
    {"x":2.5,
    "y":6,
    "text":"$$g'(x)=2x$$",
    "fontSize":"18px"},
  ];
 
  drawMathjax(svg09,foData09,xScale09,yScale09);
  
  /*
    derivative properties and polynomial derivatives
  */
  var svg10 = d3.select("#svg10")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");

  drawAxes(svg10,axesData08);

  drawGrid(svg10,gridData08);

  lineData10 = [
    {"x1":-1,"y1":1,"x2":5,"y2":1,"stroke":"#fff"},
    {"x1":-1,"y1":3,"x2":5,"y2":3,"stroke":"#f0f"},
  ];
  drawLine(svg10,lineData10,xScale08,yScale08);

  // mathjax   
  foData10 = [
    {"x":5.5,
    "y":1.0,
    "text":"$$x$$",
    "fontSize":"22px"},
    {"x":-0.3,
    "y":6.5,
    "text":"$$y$$",
    "fontSize":"22px"},
    {"x":2,
    "y":4.2,
    "text":"$$y=3$$",
    "fontSize":"18px"},
    {"x":2,
    "y":2.2,
    "text":"$$y=1$$",
    "fontSize":"18px"},
  ];
 
  drawMathjax(svg10,foData10,xScale08,yScale08);

  // Implicit differentiation
  var svg11 = d3.select("#svg11")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");


  var xScale11 = d3.scale.linear()
                       .domain([-1.2,1.2])
                       .range([50,450]);
  
  var yScale11 = d3.scale.linear()
                       .domain([1.2,-1.2])
                       .range([50,450]);       

  // 軸
  axesData11 = { 
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[-1,1],
    "yTickValues":[-1,1],
    "xTickPadding":5,
    "yTickPadding":2,
    "xOrient":["bottom"],
    "yOrient":["left"],
    "stroke":"#ff0",
    "strokeWidth":1,
    "fillColor":"none",
    "xScale":xScale11,
    "yScale":yScale11
  };
  drawAxes(svg11,axesData11);

  circleData11 = [
    {"cx":0,"cy":0,"r":2000/12,"stroke":"#fff"},
    {"cx":Math.sqrt(2)/2,"cy":Math.sqrt(2)/2,"r":2,"stroke":"#0f0"}
  ];
  drawCircle(svg11,circleData11,xScale11,yScale11)

  lineData11 = [
    {"x1":0,"y1":0,"x2":Math.sqrt(2)/2,"y2":Math.sqrt(2)/2,"stroke":"#fff"},
    {"x1":Math.sqrt(2)/2,"y1":Math.sqrt(2)/2,
    "x2":Math.sqrt(2)/2-0.5,"y2":Math.sqrt(2)/2+0.5,"stroke":"#0f0"},
    {"x1":Math.sqrt(2)/2,"y1":Math.sqrt(2)/2,
    "x2":Math.sqrt(2)/2+0.5,"y2":Math.sqrt(2)/2-0.5,"stroke":"#0f0"},
  ];
  drawLine(svg11,lineData11,xScale11,yScale11);

  // mathjax   
  foData11 = [
    {"x":0.8,
    "y":1.2,
    "text":"$$(\\frac{\\sqrt{2}}{2},\\frac{\\sqrt{2}}{2})$$",
    "fontSize":"18px"},
  ];
 
  drawMathjax(svg11,foData11,xScale11,yScale11);


</script>
