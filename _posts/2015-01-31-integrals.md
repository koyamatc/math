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

---------

# Area under a rate function as net change

-------

## Area under rate function

<div class="row">
  <div class="col-sm-6">
    時間に対して移動する距離の割合を表す関数\(r(t)\)があります
    $$r(t)=\frac{距離の変化}{時間の変化}=\frac{\Delta s}{\Delta t}
    \to \Delta s = r(t) \cdot \Delta t$$
    $$r(t)=5m/s \quad t=4s$$
    のとき、移動距離はどのくらいでしょう
    $$ \Delta s = r(t) \cdot \Delta t $$
    $$\quad = 5m/s \cdot 4s = 20m$$ 
    右のグラフでいうと、直線\(r=5\)と\(t=4\)に囲まれた面積と同じになります
  </div>
  <div class="col-sm-6">
    <div id="svg02"></div>
  </div>
</div>

<div class="row">
  <div class="col-sm-6">
  条件が
  $$0 \le t \le 2 \quad r=2m/s$$
  $$t \gt 2 \quad r=5m/s$$
  $$ t=5s$$
  のときはどうでしょうか
  $$2 \cdot 2 + 5 \cdot 3 = 4 + 15 = 19m$$ 
  </div>
  <div class="col-sm-6">
    <div id="svg03"></div>
  </div>
</div>

--------

# Riemann sums (リーマン和)

--------

## Simple Riemann approximation using rectangles

<div class="row">
  <div class="col-sm-6">
    <div id="svg04"></div>
  </div>
  <div class="col-sm-6">
    <div class="panel">
      関数\(f(x)=x^2+1\)で\(x \in[1,3]\)において、曲線の下側にできる面積を求める
    </div>
    グラフのように、\(x\)を等間隔に分割した長方形を描きます<br>
    その長方形の面積の合計を求めます<br>
    曲線と長方形の間には隙間がありますが、\(x\)の間隔を小さくしていくことで、隙間も小さくなります<br>
    今回は４個の長方形で求めてみます<br>
    $$xの幅: \Delta x = \frac{3-1}{4} = \frac{1}{2}$$
    $$おおよその面積=
    f(1)\cdot\Delta x +
    f(1.5)\cdot\Delta x +
    f(2)\cdot\Delta x +
    f(2.5)\cdot\Delta x
    $$
    $$
    = 
    2\cdot\frac{1}{2} +
    3.25\cdot\frac{1}{2} +
    5\cdot\frac{1}{2} +
    7.25\cdot\frac{1}{2}
    =
    8.75
    $$
  </div>
</div>

--------

## Generalizing a left Riemann sum with equally spaced rectangles

<div class="row">
  <div class="col-sm-6">
    <div id="svg05"></div>
  </div>
  <div class="col-sm-6">
    前のことを一般化します<br>
    関数\(f(x)でx \in[a,b]\)の範囲で、曲線の下側にできる面積を求めます<br>
    長方形は左側の境界線を元に描きます
    $$xの幅:\Delta x = \frac{b-a}{n}$$
    $$
    面積\approx 
    f(x_{0})\Delta x +
    f(x_{1})\Delta x +
    f(x_{2})\Delta x +
    f(x_{3})\Delta x +
    \cdots +
    f(x_{n-1})\Delta x
    $$
    $$\approx \sum_{i=1}^{n}f(x_{n-1})\Delta x$$
    となります
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
  var svg02 = d3.select("#svg02")
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
  var svg05 = d3.select("#svg05")
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
 
  /** Area under rate function **/
  var xScale02 = d3.scale.linear()
                       .domain([0,6])
                       .range([50,450]);
  
  var yScale02 = d3.scale.linear()
                       .domain([6,0])
                       .range([50,450]);       

  // 軸
  axesData02 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[1,2,3,4,5],
    "yTickValues":[1,2,3,4,5],
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
  drawAxes(svg02,axesData02);

  rectData02 = [
    {"x":0,"y":5,"width":4*400/6,"height":5*400/6,
    "fillColor":"#f0f","opacity":0.3}
  ];
  drawRect(svg02,rectData02,xScale02,yScale02);

  lineData02 = [
    {"x1":0,"y1":5,"x2":6,"y2":5,"stroke":"gold"},
    {"x1":4,"y1":0,"x2":4,"y2":5,"stroke":"lime"},
  ];

  drawLine(svg02,lineData02,xScale02,yScale02);

  // text   
  foData02 = [
    {"x":0,
    "y":7.3,
    "text":"$$r$$",
    "fontSize":"24px"},
    {"x":6.2,
    "y":1,
    "text":"$$t$$",
    "fontSize":"24px"},
    {"x":1.5,
    "y":4,
    "text":"$$20$$",
    "fontSize":"48px"},
  ];
 
  drawMathjax(svg02,foData02,xScale02,yScale02);

  drawAxes(svg03,axesData02);

  rectData03 = [
    {"x":0,"y":2,"width":2*400/6,"height":2*400/6,
    "fillColor":"#f0f","opacity":0.3}
   ,{"x":2,"y":5,"width":3*400/6,"height":5*400/6,
    "fillColor":"#f0f","opacity":0.3}
  ];
  drawRect(svg03,rectData03,xScale02,yScale02);

  lineData03 = [
    {"x1":0,"y1":2,"x2":2,"y2":2,"stroke":"gold"},
    {"x1":2,"y1":5,"x2":5,"y2":5,"stroke":"gold"},
    {"x1":2,"y1":0,"x2":2,"y2":2,"stroke":"lime"},
    {"x1":5,"y1":0,"x2":5,"y2":5,"stroke":"lime"},
  ];

  drawLine(svg03,lineData03,xScale02,yScale02);

  // text   
  foData03 = [
    {"x":0,
    "y":7.3,
    "text":"$$r$$",
    "fontSize":"24px"},
    {"x":6.2,
    "y":1,
    "text":"$$t$$",
    "fontSize":"24px"},
    {"x":2.5,
    "y":4,
    "text":"$$19$$",
    "fontSize":"48px"},
  ];
 
  drawMathjax(svg03,foData03,xScale02,yScale02);

/** Riemann sums **/
  var xScale04 = d3.scale.linear()
                       .domain([0,3.5])
                       .range([50,450]);
  
  var yScale04 = d3.scale.linear()
                       .domain([11,0])
                       .range([50,450]);

  // 軸
  axesData04 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[1,2,3],
    "yTickValues":[5,10],
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
  drawAxes(svg04,axesData04);

  var pathData04 = [];
  function func04(i){
    return i*i + 1;
  };

  // x^2 + 1
  for (var i = 0; i <= 3.5; i=i+0.1) {
    pathData04.push(new Point(i,func04(i)));
  };
  
  drawPath(svg04,pathData04,{"stroke":"lime"},xScale04,yScale04);


  rectData04 = [
    {"x":1,"y":func04(1),"width":0.5*400/3.5,"height":func04(1)*400/11,
    "fillColor":"#f0f","opacity":0.3},
    {"x":1.5,"y":func04(1.5),"width":0.5*400/3.5,"height":func04(1.5)*400/11,
    "fillColor":"#f0f","opacity":0.3},
    {"x":2,"y":func04(2),"width":0.5*400/3.5,"height":func04(2)*400/11,
    "fillColor":"#f0f","opacity":0.3},
    {"x":2.5,"y":func04(2.5),"width":0.5*400/3.5,"height":func04(2.5)*400/11,
    "fillColor":"#f0f","opacity":0.3}
  ];
  
  drawRect(svg04,rectData04,xScale04,yScale04);

  lineData04 = [
    {"x1":1,"y1":0,"x2":1,"y2":func04(1),"stroke":"gold"},
    {"x1":1.5,"y1":0,"x2":1.5,"y2":func04(1.5),"stroke":"gold"},
    {"x1":2,"y1":0,"x2":2,"y2":func04(2),"stroke":"gold"},
    {"x1":2.5,"y1":0,"x2":2.5,"y2":func04(2.5),"stroke":"gold"},
    {"x1":3,"y1":0,"x2":3,"y2":func04(3),"stroke":"gold"},
  ];

  drawLine(svg04,lineData04,xScale04,yScale04);

  // text   
  foData04 = [
    {"x":0,
    "y":14,
    "text":"$$y$$",
    "fontSize":"24px"},
    {"x":3.5,
    "y":1.5,
    "text":"$$x$$",
    "fontSize":"24px"},
  ];
 
  drawMathjax(svg04,foData04,xScale04,yScale04);

/** Genralizing left Riemann sum **/
  var xScale05 = d3.scale.linear()
                       .domain([0,7])
                       .range([50,450]);
  
  var yScale05 = d3.scale.linear()
                       .domain([2,0])
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

  var pathData05 = [];
  function func05(i){
    return Math.cos(i-0.4)/2 + 1;
  };

  // x^2 + 1
  for (var i = 0; i <= 7; i=i+0.1) {
    pathData05.push(new Point(i,func05(i)));
  };
  
  drawPath(svg05,pathData05,{"stroke":"lime"},xScale05,yScale05);


  rectData05 = [
    {"x":1,"y":func05(1),"width":0.5*400/7,"height":func05(1)*400/2,
    "fillColor":"#f0f","opacity":0.3},
    {"x":1.5,"y":func05(1.5),"width":0.5*400/7,"height":func05(1.5)*400/2,
    "fillColor":"#f0f","opacity":0.3},
    {"x":2,"y":func05(2),"width":0.5*400/7,"height":func05(2)*400/2,
    "fillColor":"#f0f","opacity":0.3},
    {"x":2.5,"y":func05(2.5),"width":0.5*400/7,"height":func05(2.5)*400/2,
    "fillColor":"#f0f","opacity":0.3},
    {"x":5.5,"y":func05(5.5),"width":0.5*400/7,"height":func05(5.5)*400/2,
    "fillColor":"#f0f","opacity":0.3}
  ];
  
  drawRect(svg05,rectData05,xScale05,yScale05);

  lineData05 = [
    {"x1":1,"y1":0,"x2":1,"y2":func05(1),"stroke":"gold"},
    {"x1":1.5,"y1":0,"x2":1.5,"y2":func05(1.5),"stroke":"gold"},
    {"x1":2,"y1":0,"x2":2,"y2":func05(2),"stroke":"gold"},
    {"x1":2.5,"y1":0,"x2":2.5,"y2":func05(2.5),"stroke":"gold"},
    {"x1":3,"y1":0,"x2":3,"y2":func05(3),"stroke":"gold"},
    {"x1":5.5,"y1":0,"x2":5.5,"y2":func05(5.5),"stroke":"gold"},
    {"x1":6,"y1":0,"x2":6,"y2":func05(6),"stroke":"gold"},
  ];

  drawLine(svg05,lineData05,xScale05,yScale05);

  // text   
  foData05 = [
    {"x":6.3,
    "y":2,
    "text":"$$y=f(x)$$",
    "fontSize":"18px"},
    {"x":0,
    "y":2.5,
    "text":"$$y$$",
    "fontSize":"20px"},
    {"x":7,
    "y":0.2,
    "text":"$$x$$",
    "fontSize":"20px"},
    {"x":0.8,
    "y":0.25,
    "text":"$$x_{0}$$",
    "fontSize":"18px"},
    {"x":1.3,
    "y":0.25,
    "text":"$$x_{1}$$",
    "fontSize":"18px"},
    {"x":1.8,
    "y":0.25,
    "text":"$$x_{2}$$",
    "fontSize":"18px"},
    {"x":2.3,
    "y":0.25,
    "text":"$$x_{3}$$",
    "fontSize":"18px"},
    {"x":2.8,
    "y":0.25,
    "text":"$$x_{4}$$",
    "fontSize":"18px"},
    {"x":5.0,
    "y":0.25,
    "text":"$$x_{n-1}$$",
    "fontSize":"18px"},
    {"x":5.8,
    "y":0.25,
    "text":"$$x_{n}$$",
    "fontSize":"18px"},

    {"x":0.9,
    "y":0.15,
    "text":"$$a$$",
    "fontSize":"18px"},
    {"x":5.9,
    "y":0.15,
    "text":"$$b$$",
    "fontSize":"18px"},

    {"x":1.1,
    "y":0.5,
    "text":"$$1$$",
    "fontSize":"22px"},
    {"x":1.6,
    "y":0.5,
    "text":"$$2$$",
    "fontSize":"22px"},
    {"x":2.1,
    "y":0.5,
    "text":"$$3$$",
    "fontSize":"22px"},
    {"x":2.6,
    "y":0.5,
    "text":"$$4$$",
    "fontSize":"22px"},
    {"x":4.1,
    "y":0.5,
    "text":"$$\\cdots$$",
    "fontSize":"22px"},
    {"x":5.6,
    "y":0.5,
    "text":"$$n$$",
    "fontSize":"22px"},

  ];
 
  drawMathjax(svg05,foData05,xScale05,yScale05);

</script>
