---
title: Differential calculus
layout: post
date: 2015-01-31 23:00:00
postTitle: Integrals
categories: integral
---

-------

## Antiderivatives and indefinite integrals
<div class="row">
  <div class="col-sm-6">
    導関数
    $$\frac{d}{dx}[x^2]=2x$$
    $$\frac{d}{dx}[x^2+1]=2x$$
    $$\frac{d}{dx}[x^2+\pi]=2x$$
    $$\frac{d}{dx}[x^2+C]=2x$$
    すべて\(2x\)となります
  </div>
  <div class="col-sm-6">
    では導関数が\(2x\)となる元の関数は何でしょうか？
    $$x^2,x^2+1,x^2+\pi$$
    などですが
    $$x^2+C$$
    が元の関数となります、これを式
    $$\int 2x dx = x^2 + C$$
    \(\int 2x dx\)を、逆微分とか不定積分といいます
    <br>
    この値は曲線とx軸の間の面積を表します
  </div>
</div>

----------------

## Indefinite integrals of x raised to a power

$$ \frac{x^{n+1}}{n+1}+C \quad (n \ne -1)の導関数を求めます$$
$$\frac{d}{dx}[\frac{x^{n+1}}{n+1}+c]
=\frac{(n+1)x^n}{n+1}+0=x^n$$
<br>
$$x^nの不定積分を求めます$$
$$\int {x^n} dx=\frac{x^{n+1}}{n+1}+c \quad (n \ne -1)$$

例１
$$\int {x^5} dx=\frac{x^{5+1}}{5+1}+c=\frac{x^6}{6}+C$$
例２
$$\int {5x^{-2}} dx=5\int{x^{-2}}dx=5(\frac{x^{-2+1}}{-2+1}+C)
=5(-x^{-1}+C)=-5x^{-1}+5C$$
$$定数5c \to Cと置き換えて$$
$$=-5x^{-1}+C$$
となります

--------------

## Antiderivative of \\(x^{-1}\\)

<div class="row">
  <div class="col-sm-6">
    $$\int {x^{-1}} dx = \int{\frac{1}{x}} \quad (x \ne 0)$$
    ここで
    $$\frac{d}{dx}[\ln{x}]=\frac{1}{x}$$
    ですから
    $$\int {x^{-1}} dx =　\ln{x}　+ C \quad (x \ne 0)$$
    となりますが、\(\ln{x}　+ C\) は \(x　\gt 0\)　でなければなりません 
    <br>
    しかし\(x\)の範囲は\(0\)を除くすべての\(x\)ですから\(x\)の絶対値をとって
    $$\ln{|x|}を考えます$$
    $$\ln{|x|}=\ln{x}$$
    $$\frac{d}{dx}\ln{|x|}=\frac{d}{dx}\ln{x}=\frac{1}{x}$$
    ピンク線が\(\ln{|x|}\)で、緑線がその導関数\(\frac{1}{x}\quad (x \ne 0)\) です
  </div>
  <div class="col-sm-6">
    <div id="svg01"></div>
  </div>
</div>

---------------

## Basic trig and exponential antiderivatives

$$\int(\sin t + \cos t) dt$$
$$=\int {\sin t} dt + \int {\cos t} dt$$
$$\frac{d}{dt}{-\cos t}=\sin t \quad \frac{d}{dt}{\sin t}=\cos t$$ 
なので
$$=-\cos t + \sin t + C$$
となります

<br>
$$\int (e^{a}+\frac{1}{a}) da$$
$$=\int{e^a} da + \int {\frac{1}{a}}da
=e^a + \ln|a| + C$$

------------

## Antiderivative of hairier expression

$$\int (7x^3 - 5\sqrt{x} + \frac{18\sqrt{x}}{x^3}+x^{-40})dx$$
$$=\int 7x^3 dx - \int 5\sqrt{x}dx + \int \frac{18\sqrt{x}}{x^3} dx + \int x^{-40})dx$$
$$= \frac{7x^4}{4} 
    - \frac{5x^{\frac{3}{2}}}{\frac{3}{2}}
    + \frac{18x^{-\frac{3}{2}}}{-\frac{3}{2}}
    + \frac{x^{-39}}{-39}
    + C
$$
$$=\frac{7}{4}x^4 - \frac{10}{3}x^{\frac{3}{2}} - 12x^{-\frac{3}{2}} - \frac{1}{39}x^{-39} + C$$

-------------

## Velocity and position from acceleration

時間における位置を表す関数を\\(S(t)\\)

これを時間で微分すると\\(\frac{dS}{dt}=V(t)\\)、時間に対する位置の変化、つまり速度です

これを時間で微分すると\\(\frac{dV}{dt}=a(t)\\)、時間に対する速度の変化、加速度です

それでは加速度から初めて、不定積分を求めていきます

$$a(t) \to \int a(t) dt = V(t) \to \int V(t)dt = S(t)$$

ここで
$$a(t)=1m/s^2 \quad V(3)=-3m/s \quad S(2)=-10m$$
とすると
$$V(t)=\int a(t)dt=\int 1dt =t+C$$
$$V(3)=3+C=-3 \to c = -6 \to V(t)=t-6$$
<br>
$$S(t)=\int V(t)dt=\int(t-6)dt=\frac{t^2}{2}-6t+C$$
$$S(2)=2-12+C=-10 \to C=0 \to S(t)=\frac{t^2}{2}-6t$$   





<div class="row">
  <div class="col-sm-6">
    <div id="svg02"></div>
  </div>
  <div class="col-sm-6">
  </div>
</div>

--------

## 

--------

## 

<div class="row">
  <div class="col-sm-6">
    <div id="svg03"></div>
  </div>
  <div class="col-sm-6">
  </div>
</div>

<div class="row">
  <div class="col-sm-6">
    <div id="svg04"></div>
  </div>
  <div class="col-sm-6">
  </div>
</div>

<div class="row">
  <div class="col-sm-6">
    <div id="svg05"></div>
  </div>
  <div class="col-sm-6">
  </div>
</div>

--------

## 

<div class="row">
  <div class="col-sm-6">
    <div id="svg06"></div>
  </div>
  <div class="col-sm-6">
  </div>
</div>

--------

# 

--------

## 

<div class="row">
  <div class="col-sm-6">
    <div id="svg07"></div>
  </div>
  <div class="col-sm-6">
  </div>
</div>

--------

## 


--------

# 

--------

## 

<div class="row">
  <div class="col-sm-6">
    <div id="svg08"></div>
  </div>
  <div class="col-sm-6">
  </div>
</div>
<div class="row">
  <div class="col-sm-6">
    <hr>
    <div id="svg09"></div>
  </div>
  <div class="col-sm-6">
  </div>
</div>
<div class="row">
  <div class="col-sm-6">
    <hr>
    <div id="svg10"></div>
  </div>
  <div class="col-sm-6">
  </div>
</div>
<div class="row">
  <div class="col-sm-6">
    <hr>
    <div id="svg11"></div>
  </div>
  <div class="col-sm-6">
  </div>
</div>
<div class="row">
  <div class="col-sm-6">
    <div id="svg12"></div>
  </div>
  <div class="col-sm-6">
  </div>
</div>
<div class="row">
  <div class="col-sm-6">
    <div id="svg13"></div>
  </div>
  <div class="col-sm-6">
  </div>
</div>
--------

## 

<div class="row">
  <div class="col-sm-3">
  </div>
  <div class="col-sm-3">
  </div>
  <div class="col-sm-6">
  </div>
</div>

------

<div class="row">
  <div class="col-sm-3">
  </div>
  <div class="col-sm-3">
  </div>
  <div class="col-sm-6">
  </div>
</div>
<div class="row">
  <div class="col-sm-6">
    <div id="svg14"></div>
  </div>
  <div class="col-sm-6">
  </div>
</div>

---------

## 

<div class="row">
  <div class="col-sm-6">
    <div id="svg15"></div>
  </div>
  <div class="col-sm-6">
  </div>
</div>

--------

## 

<div class="row">
  <div class="col-sm-6">
    <div id="svg16"></div>
  </div>
  <div class="col-sm-6">
  </div>
</div>

--------

## 

<div class="row">
  <div class="col-sm-6">
    <div id="svg17"></div>
  </div>
  <div class="col-sm-6">
  </div>
</div>

--------

## 

<div class="row">
  <div class="col-sm-6">
    <div id="svg18"></div>
  </div>
  <div class="col-sm-6">
  </div>
</div>

--------

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

  var xScale01 = d3.scale.linear()
                       .domain([-5,5])
                       .range([50,450]);
  
  var yScale01 = d3.scale.linear()
                       .domain([5,-5])
                       .range([50,450]);       

  // 軸
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

  var pathData011=[];
  var pathData012=[];
  var pathData013=[];
  var pathData014=[];
  
  // ln x :x>0
  for (var i = 0.005; i <= 5; i=i+0.01) {
    pathData011.push(new Point(i,Math.log(i)));
  };
  // ln x :x<0
  for (var i = -0.005; i >= -5; i=i-0.01) {
    pathData012.push(new Point(i,Math.log(Math.abs(i))));
  };
  // 1/x :x>0
  for (var i = 0.005; i <= 5; i=i+0.01) {
    pathData013.push(new Point(i,1/i));
  };
  // 1/x :x<0
  for (var i = -0.005; i >= -5; i=i-0.01) {
    pathData014.push(new Point(i,1/i));
  };
  
  drawPath(svg01,pathData011,{"stroke":"#f0f"},xScale01,yScale01);
  drawPath(svg01,pathData012,{"stroke":"#f0f"},xScale01,yScale01);
  drawPath(svg01,pathData013,{"stroke":"#0f0"},xScale01,yScale01);
  drawPath(svg01,pathData014,{"stroke":"#0f0"},xScale01,yScale01);

  // text   
  foData01 = [
    {"x":1.0,
    "y":5,
    "text":"$$\\frac{1}{x} \\quad (x \\gt 0)$$",
    "fontSize":18},
    {"x":-3,
    "y":-3,
    "text":"$$\\frac{1}{x} \\quad (x \\lt 0)$$",
    "fontSize":18},
    {"x":2.0,
    "y":3,
    "text":"$$\\ln{x} \\quad (x \\gt 0)$$",
    "fontSize":18},
    {"x":-4,
    "y":3,
    "text":"$$\\ln{x} \\quad (x \\lt 0)$$",
    "fontSize":18},
  ];
 
  drawMathjax(svg01,foData01,xScale01,yScale01);
 

</script>
