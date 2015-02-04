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

## Rectangular and trapezoidal Riemann approximations

<div class="row">
  <div class="col-sm-6">
    <div id="svg061"></div>
  </div>
  <div class="col-sm-6">
    左側の辺を基準にした長方形では
    $$\Delta x = \frac{b-a}{n}$$
    $$\sum_{i=1}^{n}f(x_{i-1})\Delta x$$
  </div>
</div>
<div class="row">
  <div class="col-sm-6">
    <div id="svg062"></div>
  </div>
  <div class="col-sm-6">
    右側の辺を基準にした長方形では
    $$\Delta x = \frac{b-a}{n}$$
    $$\sum_{i=1}^{n}f(x_{i})\Delta x$$
  </div>
</div>
<div class="row">
  <div class="col-sm-6">
    <div id="svg063"></div>
  </div>
  <div class="col-sm-6">
    中間点の高さを基準にした長方形では
    $$\Delta x = \frac{b-a}{n}$$
    $$\sum_{i=1}^{n}\frac{f(x_{i}+x_{i-1})}{2}\Delta x$$
  </div>
</div>
<div class="row">
  <div class="col-sm-6">
    <div id="svg064"></div>
  </div>
  <div class="col-sm-6">
    台形で面積を計算する場合
    $$\Delta x = \frac{b-a}{n}$$
    $$\sum_{i=1}^{n}\frac{f(x_{i})+f(x_{i-1})}{2}\Delta x$$
  </div>
</div>

--------

## Trapezoidal approximation of area under curve

<div class="row">
  <div class="col-sm-6">
    <div id="svg07"></div>
  </div>
  <div class="col-sm-6">
    $$f(x)=\sqrt{x-1}$$
    $$\Delta x = \frac{6-1}{5}=\frac{5}{5}=1$$
    $$
    Area \approx 
    \frac{f(1)+f(2)}{2}\Delta x +
    \frac{f(2)+f(3)}{2}\Delta x +
    \frac{f(3)+f(4)}{2}\Delta x +
    \frac{f(4)+f(5)}{2}\Delta x +
    \frac{f(5)+f(6)}{2}\Delta x 
    $$
    $$
    \quad \approx
    \frac{\Delta x}{2}(f(1)+2f(2)+2f(3)+2f(4)+2f(5)+f(6))
    $$
    $$
    \quad \approx
    \frac{1}{2}(0 + 2 + 2\sqrt{2} + 2\sqrt{3} + 4 + \sqrt{5})
    $$
    $$
    \quae \approx 7.26
    $$

  </div>
</div>

--------

## Riemann sums and integrals

左を基準としたリーマン和は以下のようにあらわせました
$$
区間[a,b]で、\Delta x = \frac{b-a}{n}のとき
\sum_{i=1}^{n}f(x_{i-1})\Delta x
$$
ここで　\\(\Delta x \\)が限りなく小さくなったら、
つまり長方形の数が無限大になったら\\(n \to \infty\\)は、より面積を正確に表せます

$$
\lim_{n \to \infty}\sum_{i=1}^{n}f(x_{i-1})\Delta x
$$

これが積分の定義になります

---------------

## Evaluating definite integral from graph

<div class="row">
  <div class="col-sm-6">
    <div id="svg08"></div>
  </div>
  <div class="col-sm-6">
    $$\int_{-3}^{3}\sqrt{9-x^2}dx$$
    を求めます、これは\(y=\sqrt{9-x^2}\)の曲線の下にできる面積です<br>
    この式に手を加えます
    $$y^2=9-x^2　\to x^2 + y^2 = 9$$
    これは半径が３の円の式で、左図の青く塗りつぶされた部分の面積を求めることになります
    $$\frac{\pi \cdot 3^2}{2}=\frac{9\pi}{2}$$

  </div>
</div>

----------

# Properties of the definite integral

----------

## Integrating scaled version of function

<div class="row">
  <div class="col-sm-6">
    <div id="svg09"></div>
  </div>
  <div class="col-sm-6">
    区間\([a,b]\)で、関数\(y=f(x)\)(緑線)と\(x\)軸との間の面積は
    $$\int_{a}^{b}f(x)dx$$
    \(f(x)\)を\(c\)倍した関数\(y=cf(x)\)(白線)と\(x\)軸との間の面積は
    $$\int_{a}^{b}cf(x)dx$$
    これは縦方向に\(c\)倍長くなった面積です
    <div id="svg092"></div>
    したがって
    $$\int_{a}^{b}cf(x)dx=c\int_{a}^{b}f(x)dx$$
  </div>
</div>

--------

## Integrating sums of functions


<div class="row">
  <div class="col-sm-4">
    <div id="svg101"></div>
    <div class="row">
      <div class="col-sm-offset-5">
        $$\int_{a}^{b}f(x)dx \qquad \qquad+$$
      </div>
    </div>
  </div>
  <div class="col-sm-4">
    <div id="svg102"></div>
    <div class="row">
      <div class="col-sm-offset-5">
        $$\int_{a}^{b}g(x)dx \qquad \qquad =$$
      </div>
    </div>
  </div>
  <div class="col-sm-4">
    <div id="svg103"></div>
    <div class="row">
      <div class="col-sm-offset-4">$$\int_{a}^{b}(f(x)+g(x))dx$$</div>
    </div>

  </div>
</div>

----------

## Definite integral from and to same point

<div class="row">
  <div class="col-sm-6">
    <div id="svg11"></div>
  </div>
  <div class="col-sm-6">
    同じ点から同じ点までの定積分は、
    $$\int_{c}^{c}f(x)dx = 0$$
    高さはあるが、幅は無いので、高さｘ幅=0　となります
  </div>
</div>

------------

## Breaking up integral interval

<div class="row">
  <div class="col-sm-6">
    <div id="svg12"></div>
  </div>
  <div class="col-sm-6">
    $$a \le c \le b$$
    $$\int_{a}^{b}f(x)dx=\int_{a}^{c}f(x)dx+\int_{c}^{b}f(x)dx$$
  </div>
</div>

---------

## Definite integral of shifted function

<div class="row">
  <div class="col-sm-6">
    <div id="svg13"></div>
  </div>
  <div class="col-sm-6">
    $$\int_{a}^{b}f(x)dx=5$$
    とすると
    $$f(x-c)[白線]は、f(x)[緑線]を右へc分移動したものとします$$
    この時
    $$\int_{a+c}^{b+c}f(x-c)dx=\int_{a}^{b}f(x)dx=5$$
  </div>
</div>
--------

## Switching bounds of definite integral

<div class="row">
  <div class="col-sm-6">
    <div id="svg14"></div>
  </div>
  <div class="col-sm-6">
    $$\int_{a}^{b}f(x)dx=\lim_{n\to\infty}\sum_{i=1}^{n}f(x_{i})\Delta x \quad where \quad \Delta x = \frac{b-a}{n}$$
    それでは\(a \to b\) を\(b \to a\)とした場合は
    $$\int_{b}^{a}f(x)dx=\lim_{n\to\infty}\sum_{i=1}^{n}f(x_{i})\Delta x \quad where \quad \Delta x = \frac{a-b}{n}$$
    この場合の\(\Delta x\)は負となります、したがって
    $$\int_{b}^{a}f(x)dx=-\int_{a}^{b}f(x)dx$$
  </div>
</div>

------

# Functions defined by integrals

------

## 

<div class="row">
  <div class="col-sm-6">
    <div id="svg15"></div>
  </div>
  <div class="col-sm-6">
  </div>
</div>
<div class="row">
  <div class="col-sm-6">
    <div id="svg16"></div>
  </div>
  <div class="col-sm-6">
  </div>
</div>

---------

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

## 

<div class="row">
  <div class="col-sm-6">
    <div id="svg19"></div>
  </div>
  <div class="col-sm-6">
  </div>
</div>

--------

## 

<div class="row">
  <div class="col-sm-6">
    <div id="svg20"></div>
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
  var svg061 = d3.select("#svg061")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg062 = d3.select("#svg062")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg063 = d3.select("#svg063")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg064 = d3.select("#svg064")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg07 = d3.select("#svg07")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg08 = d3.select("#svg08")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg09 = d3.select("#svg09")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg092 = d3.select("#svg092")
                .append("svg")
                .attr("height",200)
                .attr("width",200)
                .style("background","#000");
  var svg101 = d3.select("#svg101")
                .append("svg")
                .attr("height",400)
                .attr("width",400)
                .style("background","#000");
  var svg102 = d3.select("#svg102")
                .append("svg")
                .attr("height",400)
                .attr("width",400)
                .style("background","#000");
  var svg103 = d3.select("#svg103")
                .append("svg")
                .attr("height",400)
                .attr("width",400)
                .style("background","#000");
  var svg11 = d3.select("#svg11")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg12 = d3.select("#svg12")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg13 = d3.select("#svg13")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg14 = d3.select("#svg14")
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

  // trapezoid rule
  var xScale06 = d3.scale.linear()
                       .domain([0,10])
                       .range([50,450]);
  
  var yScale06 = d3.scale.linear()
                       .domain([10,0])
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
  drawAxes(svg061,axesData06);
  drawAxes(svg062,axesData06);
  drawAxes(svg063,axesData06);
  drawAxes(svg064,axesData06);

  var pathData06 = [];
  function func06(i){
    return Math.pow(i-3,2)/9+3
  };

  for (var i = 1; i <= 9; i=i+0.1) {
    pathData06.push(new Point(i,func06(i)));
  };
  

  rectData061 = [
    {"x":1,"y":func06(1),"width":0.5*40,"height":func06(1)*40,
    "stroke":"#ff0","fillColor":"#f0f","opacity":0.7},
    {"x":1.5,"y":func06(1.5),"width":0.5*40,"height":func06(1.5)*40,
    "stroke":"#ff0","fillColor":"#f0f","opacity":0.7},
    {"x":2,"y":func06(2),"width":0.5*40,"height":func06(2)*40,
    "stroke":"#ff0","fillColor":"#f0f","opacity":0.7},
    {"x":2.5,"y":func06(2.5),"width":0.5*40,"height":func06(2.5)*40,
    "stroke":"#ff0","fillColor":"#f0f","opacity":0.7},
    {"x":3,"y":func06(3),"width":0.5*40,"height":func06(3)*40,
    "stroke":"#ff0","fillColor":"#f0f","opacity":0.7},
    {"x":3.5,"y":func06(3.5),"width":0.5*40,"height":func06(3.5)*40,
    "stroke":"#ff0","fillColor":"#f0f","opacity":0.7},
    {"x":8,"y":func06(8),"width":0.5*40,"height":func06(8)*40,
    "stroke":"#ff0","fillColor":"#f0f","opacity":0.7},
    {"x":8.5,"y":func06(8.5),"width":0.5*40,"height":func06(8.5)*40,
    "stroke":"#ff0","fillColor":"#f0f","opacity":0.7},

  ];
  drawRect(svg061,rectData061,xScale06,yScale06);

  rectData062 = [
    {"x":1,"y":func06(1.5),"width":0.5*40,"height":func06(1.5)*40,
    "stroke":"#ff0","fillColor":"#f0f","opacity":0.7},
    {"x":1.5,"y":func06(2),"width":0.5*40,"height":func06(2)*40,
    "stroke":"#ff0","fillColor":"#f0f","opacity":0.7},
    {"x":2,"y":func06(2.5),"width":0.5*40,"height":func06(2.5)*40,
    "stroke":"#ff0","fillColor":"#f0f","opacity":0.7},
    {"x":2.5,"y":func06(3),"width":0.5*40,"height":func06(3)*40,
    "stroke":"#ff0","fillColor":"#f0f","opacity":0.7},
    {"x":3,"y":func06(3.5),"width":0.5*40,"height":func06(3.5)*40,
    "stroke":"#ff0","fillColor":"#f0f","opacity":0.7},
    {"x":3.5,"y":func06(4),"width":0.5*40,"height":func06(4)*40,
    "stroke":"#ff0","fillColor":"#f0f","opacity":0.7},
    {"x":8,"y":func06(8.5),"width":0.5*40,"height":func06(8.5)*40,
    "stroke":"#ff0","fillColor":"#f0f","opacity":0.7},
    {"x":8.5,"y":func06(9),"width":0.5*40,"height":func06(9)*40,
    "stroke":"#ff0","fillColor":"#f0f","opacity":0.7},

  ];
  drawRect(svg062,rectData062,xScale06,yScale06);

  rectData063 = [
    {"x":1,"y":func06(1.25),"width":0.5*40,"height":func06(1.25)*40,
    "stroke":"#ff0","fillColor":"#f0f","opacity":0.7},
    {"x":1.5,"y":func06(1.75),"width":0.5*40,"height":func06(1.75)*40,
    "stroke":"#ff0","fillColor":"#f0f","opacity":0.7},
    {"x":2,"y":func06(2.25),"width":0.5*40,"height":func06(2.25)*40,
    "stroke":"#ff0","fillColor":"#f0f","opacity":0.7},
    {"x":2.5,"y":func06(2.75),"width":0.5*40,"height":func06(2.75)*40,
    "stroke":"#ff0","fillColor":"#f0f","opacity":0.7},
    {"x":3,"y":func06(3.25),"width":0.5*40,"height":func06(3.25)*40,
    "stroke":"#ff0","fillColor":"#f0f","opacity":0.7},
    {"x":3.5,"y":func06(3.75),"width":0.5*40,"height":func06(3.75)*40,
    "stroke":"#ff0","fillColor":"#f0f","opacity":0.7},
    {"x":8,"y":func06(8.25),"width":0.5*40,"height":func06(8.25)*40,
    "stroke":"#ff0","fillColor":"#f0f","opacity":0.7},
    {"x":8.5,"y":func06(8.75),"width":0.5*40,"height":func06(8.75)*40,
    "stroke":"#ff0","fillColor":"#f0f","opacity":0.7},

  ];
  drawRect(svg063,rectData063,xScale06,yScale06);

  lineData064 = [
    {"x1":1,"y1":0,"x2":1,"y2":func06(1),"stroke":"gold"},
    {"x1":1.5,"y1":0,"x2":1.5,"y2":func06(1.5),"stroke":"gold"},
    {"x1":2,"y1":0,"x2":2,"y2":func06(2),"stroke":"gold"},
    {"x1":2.5,"y1":0,"x2":2.5,"y2":func06(2.5),"stroke":"gold"},
    {"x1":3,"y1":0,"x2":3,"y2":func06(3),"stroke":"gold"},
    {"x1":3.5,"y1":0,"x2":3.5,"y2":func06(3.5),"stroke":"gold"},
    {"x1":4,"y1":0,"x2":4,"y2":func06(4),"stroke":"gold"},
    {"x1":8,"y1":0,"x2":8,"y2":func06(8),"stroke":"gold"},
    {"x1":8.5,"y1":0,"x2":8.5,"y2":func06(8.5),"stroke":"gold"},
    {"x1":9,"y1":0,"x2":9,"y2":func06(9),"stroke":"gold"},

    {"x1":1,"y1":func06(1),"x2":1.5,"y2":func06(1.5),"stroke":"gold"},
    {"x1":1.5,"y1":func06(1.5),"x2":2,"y2":func06(2),"stroke":"gold"},
    {"x1":2,"y1":func06(2),"x2":2.5,"y2":func06(2.5),"stroke":"gold"},
    {"x1":2.5,"y1":func06(2.5),"x2":3,"y2":func06(3),"stroke":"gold"},
    {"x1":3,"y1":func06(3),"x2":3.5,"y2":func06(3.5),"stroke":"gold"},
    {"x1":3.5,"y1":func06(3.5),"x2":4,"y2":func06(4),"stroke":"gold"},
    {"x1":8,"y1":func06(8),"x2":8.5,"y2":func06(8.5),"stroke":"gold"},
    {"x1":8.5,"y1":func06(8.5),"x2":9,"y2":func06(9),"stroke":"gold"},
  ];

  drawPath(svg064,pathData06,{"stroke":"lime"},xScale06,yScale06);
  drawLine(svg064,lineData064,xScale06,yScale06);

  drawPath(svg061,pathData06,{"stroke":"lime"},xScale06,yScale06);
  drawPath(svg062,pathData06,{"stroke":"lime"},xScale06,yScale06);
  drawPath(svg063,pathData06,{"stroke":"lime"},xScale06,yScale06);

  // text   
  foData06 = [
    {"x":-0.3,
    "y":12,
    "text":"$$y$$",
    "fontSize":"20px"},
    {"x":10,
    "y":1.2,
    "text":"$$x$$",
    "fontSize":"20px"},
    {"x":0.8,
    "y":1,
    "text":"$$x_{0}$$",
    "fontSize":"16px"},
    {"x":1.3,
    "y":1,
    "text":"$$x_{1}$$",
    "fontSize":"16px"},
    {"x":1.8,
    "y":1,
    "text":"$$x_{2}$$",
    "fontSize":"16px"},
    {"x":2.3,
    "y":1,
    "text":"$$x_{3}$$",
    "fontSize":"16px"},
    {"x":2.8,
    "y":1,
    "text":"$$x_{4}$$",
    "fontSize":"16px"},
    {"x":3.3,
    "y":1,
    "text":"$$x_{5}$$",
    "fontSize":"16px"},
    {"x":3.8,
    "y":1,
    "text":"$$x_{6}$$",
    "fontSize":"16px"},

    {"x":8.0,
    "y":1.3,
    "text":"$$x_{n-1}$$",
    "fontSize":"16px"},
    {"x":8.8,
    "y":1,
    "text":"$$x_{n}$$",
    "fontSize":"16px"},

    {"x":0.9,
    "y":0.5,
    "text":"$$a$$",
    "fontSize":"16px"},
    {"x":8.9,
    "y":0.5,
    "text":"$$b$$",
    "fontSize":"16px"},

    {"x":1.1,
    "y":3,
    "text":"$$1$$",
    "fontSize":"20px"},
    {"x":1.6,
    "y":3,
    "text":"$$2$$",
    "fontSize":"20px"},
    {"x":2.1,
    "y":3,
    "text":"$$3$$",
    "fontSize":"20px"},
    {"x":2.6,
    "y":3,
    "text":"$$4$$",
    "fontSize":"20px"},
    {"x":3.1,
    "y":3,
    "text":"$$5$$",
    "fontSize":"20px"},
    {"x":3.6,
    "y":3,
    "text":"$$6$$",
    "fontSize":"20px"},
    {"x":5.6,
    "y":3,
    "text":"$$\\cdots$$",
    "fontSize":"20px"},
    {"x":7.8,
    "y":3,
    "text":"$$n-1$$",
    "fontSize":"12px"},
    {"x":8.6,
    "y":3,
    "text":"$$n$$",
    "fontSize":"20px"},

  ];
 
  drawMathjax(svg061,foData06,xScale06,yScale06);
  drawMathjax(svg062,foData06,xScale06,yScale06);
  drawMathjax(svg063,foData06,xScale06,yScale06);
  drawMathjax(svg064,foData06,xScale06,yScale06);
 
 // Trapezoidal approximation of area under curve
  var xScale07 = d3.scale.linear()
                       .domain([0,7])
                       .range([50,450]);
  
  var yScale07 = d3.scale.linear()
                       .domain([4,0])
                       .range([50,450]);

  // 軸
  axesData07 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[1,2,3,4,5,6],
    "yTickValues":[1,2,3],
    "xTickPadding":5,
    "yTickPadding":2,
    "xOrient":["bottom"],
    "yOrient":["left"],
    "stroke":"#ff0",
    "strokeWidth":1,
    "fillColor":"none",
    "xScale":xScale07,
    "yScale":yScale07
  };
  drawAxes(svg07,axesData07);

  var pathData07 = [];
  function func07(i){
    return Math.sqrt(i-1)
  };

  for (var i = 1; i <= 6.5; i=i+0.05) {
    pathData07.push(new Point(i,func07(i)));
  };
  drawPath(svg07,pathData07,{"stroke":"lime","strokeWidth":3},xScale07,yScale07); 

  lineData07 = [
    {"x1":1,"y1":0,"x2":1,"y2":func07(1),"stroke":"gold"},
    {"x1":2,"y1":0,"x2":2,"y2":func07(2),"stroke":"gold"},
    {"x1":3,"y1":0,"x2":3,"y2":func07(3),"stroke":"gold"},
    {"x1":4,"y1":0,"x2":4,"y2":func07(4),"stroke":"gold"},
    {"x1":5,"y1":0,"x2":5,"y2":func07(5),"stroke":"gold"},
    {"x1":6,"y1":0,"x2":6,"y2":func07(6),"stroke":"gold"},

    {"x1":1,"y1":func07(1),"x2":2,"y2":func07(2),"stroke":"gold"},
    {"x1":2,"y1":func07(2),"x2":3,"y2":func07(3),"stroke":"gold"},
    {"x1":3,"y1":func07(3),"x2":4,"y2":func07(4),"stroke":"gold"},
    {"x1":4,"y1":func07(4),"x2":5,"y2":func07(5),"stroke":"gold"},
    {"x1":5,"y1":func07(5),"x2":6,"y2":func07(6),"stroke":"gold"},
  ];

  drawLine(svg07,lineData07,xScale07,yScale07);

 // Evaluating definite integral from graph
  var xScale08 = d3.scale.linear()
                       .domain([-4,4])
                       .range([50,450]);
  
  var yScale08 = d3.scale.linear()
                       .domain([5,-3])
                       .range([50,450]);

  // 軸
  axesData08 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[-3,3],
    "yTickValues":[1,2,3,4],
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

  var pathData08 = [];
  function func08(i){
    return Math.sqrt(9-i*i)
  };
  y0Func08 = function y0func08(i){
    return 0;
  };

  for (var i = -3; i <= 3; i=i+0.05) {
    pathData08.push(new Point(i,func08(i)));
  };

  drawArea(svg08,pathData08,y0Func08,
    {"fillColor":"#00f","opacity":0.6},xScale08,yScale08); 
  drawPath(svg08,pathData08,{"stroke":"lime","strokeWidth":3},xScale08,yScale08); 
  drawAxes(svg08,axesData08);

 /**Integrating scaled version of function**/
   var xScale09 = d3.scale.linear()
                       .domain([0,7])
                       .range([50,450]);
  
  var yScale09 = d3.scale.linear()
                       .domain([10,0])
                       .range([50,450]);

  // 軸
  axesData09 = {
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
    "xScale":xScale09,
    "yScale":yScale09
  };

  var pathData091 = [];
  var pathData092 = [];
  var areaData093 = [];
  var areaData094 = [];
  function func091(i){
    return Math.sin(i)+i/3 + 1;
  };
  function func092(i){
    return 3*(Math.sin(i)+i/3 + 1);
  };
  y0Func09 = function y0func09(i){
    return 0;
  };

  for (var i = 0; i <= 2*pi; i=i+0.01) {
    pathData091.push(new Point(i,func091(i)));
    pathData092.push(new Point(i,func092(i)));
  };
  for (var i = 1; i <= 2*pi-0.5; i=i+0.01) {
    areaData093.push(new Point(i,func091(i)));
    areaData094.push(new Point(i,func092(i)));
  };

  drawArea(svg09,areaData093,y0Func09,
    {"fillColor":"#00f","opacity":0.4},xScale09,yScale09); 
  drawArea(svg09,areaData094,y0Func09,
    {"fillColor":"#00f","opacity":0.4},xScale09,yScale09); 
  drawPath(svg09,pathData091,{"stroke":"lime","strokeWidth":3},xScale09,yScale09); 
  drawPath(svg09,pathData092,{"stroke":"#fff","strokeWidth":3},xScale09,yScale09); 
  drawAxes(svg09,axesData09);

  // text   
  foData09 = [
    {"x":-0.3,
    "y":12,
    "text":"$$y$$",
    "fontSize":"20px"},
    {"x":7,
    "y":1.2,
    "text":"$$x$$",
    "fontSize":"20px"},

    {"x":2*pi-0.5,
    "y":1.2,
    "text":"$$b$$",
    "fontSize":"18px"},
    {"x":1,
    "y":1.2,
    "text":"$$a$$",
    "fontSize":"18px"},

    {"x":2*pi,
    "y":11,
    "text":"$$y=cf(x)$$",
    "fontSize":"18px"},
    {"x":2*pi,
    "y":5,
    "text":"$$y=f(x)$$",
    "fontSize":"18px"},

    {"x":2,
    "y":6,
    "text":"$$\\int_{a}^{b}cf(x)dx$$",
    "fontSize":"18px"},
    {"x":2,
    "y":3,
    "text":"$$\\int_{a}^{b}f(x)dx$$",
    "fontSize":"18px"},

  ];
 
  drawMathjax(svg09,foData09,xScale09,yScale09);

  rectData092 = [
    {"x":20,"y":110,"width":60,"height":40,"stroke":"#fff"},
    {"x":120,"y":30,"width":60,"height":120,"stroke":"#fff"},
  ]
  drawRect(svg092,rectData092);
  // text   
  foData092 = [
    {"x":0,
    "y":60,
    "text":"$$\\alpha$$",
    "fontSize":"18px"},
    {"x":40,
    "y":100,
    "text":"$$\\beta$$",
    "fontSize":"18px"},
    {"x":30,
    "y":60,
    "text":"$$\\alpha\\beta$$",
    "fontSize":"18px"},

    {"x":95,
    "y":30,
    "text":"$$c\\alpha$$",
    "fontSize":"18px"},
    {"x":140,
    "y":100,
    "text":"$$\\beta$$",
    "fontSize":"18px"},
    {"x":130,
    "y":30,
    "text":"$$c\\alpha\\beta$$",
    "fontSize":"18px"},

  ];
 
  drawMathjax(svg092,foData092);

  /**Integrating sums of functions**/
  var xScale10 = d3.scale.linear()
                       .domain([0,7])
                       .range([20,370]);
  
  var yScale10 = d3.scale.linear()
                       .domain([10,0])
                       .range([20,370]);

  axesData10 = {
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
    "xScale":xScale10,
    "yScale":yScale10
  };

  var pathData101 = [];
  var pathData102 = [];
  var pathData103 = [];
  var areaData101 = [];
  var areaData102 = [];
  var areaData103 = [];

  function func101(i){
    return Math.sin(i)+i/3 + 1;
  };
  function func102(i){
    return i*i/7 + 1;
  };
  y0Func10 = function y0func10(i){
    return 0;
  };

  for (var i = 0; i <= 2*pi; i=i+0.01) {
    pathData101.push(new Point(i,func101(i)));
    pathData102.push(new Point(i,func102(i)));
    pathData103.push(new Point(i,func101(i)+func102(i)));
  };
  for (var i = 1; i <= 2*pi-0.5; i=i+0.01) {
    areaData101.push(new Point(i,func101(i)));
    areaData102.push(new Point(i,func102(i)));
    areaData103.push(new Point(i,func101(i)+func102(i)));
  };

  drawArea(svg101,areaData101,y0Func10,
    {"fillColor":"#00f","opacity":0.4},xScale10,yScale10); 
  drawArea(svg102,areaData102,y0Func10,
    {"fillColor":"#00f","opacity":0.4},xScale10,yScale10); 
  drawArea(svg103,areaData103,y0Func10,
    {"fillColor":"#00f","opacity":0.4},xScale10,yScale10); 

  drawPath(svg101,pathData101,{"stroke":"#fff"},xScale10,yScale10);
  drawPath(svg103,pathData101,{"stroke":"#fff"},xScale10,yScale10);
  drawPath(svg103,pathData103,{"stroke":"#0f0"},xScale10,yScale10);
  drawPath(svg102,pathData102,{"stroke":"#0f0"},xScale10,yScale10);

  drawAxes(svg101,axesData10);
  drawAxes(svg102,axesData10);
  drawAxes(svg103,axesData10);

  // text   
  foData101 = [
    {"x":-0.3,
    "y":12.2,
    "text":"$$y$$",
    "fontSize":"20px"},
    {"x":7,
    "y":1.3,
    "text":"$$x$$",
    "fontSize":"20px"},

    {"x":2*pi-0.6,
    "y":1.3,
    "text":"$$b$$",
    "fontSize":"18px"},
    {"x":1,
    "y":1.3,
    "text":"$$a$$",
    "fontSize":"18px"},

    {"x":2*pi-1,
    "y":5.5,
    "text":"$$y=f(x)$$",
    "fontSize":"18px"},
 
  ];
 

  foData102 = [
    {"x":-0.3,
    "y":12.2,
    "text":"$$y$$",
    "fontSize":"20px"},
    {"x":7,
    "y":1.3,
    "text":"$$x$$",
    "fontSize":"20px"},

    {"x":2*pi-0.6,
    "y":1.3,
    "text":"$$b$$",
    "fontSize":"18px"},
    {"x":1,
    "y":1.3,
    "text":"$$a$$",
    "fontSize":"18px"},

    {"x":2*pi-1,
    "y":9.5,
    "text":"$$y=g(x)$$",
    "fontSize":"18px"},
 
  ];

  foData103 = [
    {"x":-0.3,
    "y":12.2,
    "text":"$$y$$",
    "fontSize":"20px"},
    {"x":7,
    "y":1.3,
    "text":"$$x$$",
    "fontSize":"20px"},

    {"x":2*pi-0.6,
    "y":1.3,
    "text":"$$b$$",
    "fontSize":"18px"},
    {"x":1,
    "y":1.3,
    "text":"$$a$$",
    "fontSize":"18px"},

    {"x":2*pi-2,
    "y":12.2,
    "text":"$$y=f(x)+g(x)$$",
    "fontSize":"18px"},
 
  ];

  drawMathjax(svg101,foData101,xScale10,yScale10);
  drawMathjax(svg102,foData102,xScale10,yScale10);
  drawMathjax(svg103,foData103,xScale10,yScale10);

  /* Definit integral from and to same point **/
  drawPath(svg11,pathData092,{"stroke":"lime","strokeWidth":3},xScale09,yScale09); 
  drawAxes(svg11,axesData09);
  lineData11 = [
    {"x1":2*pi-2.5,"y1":0,"x2":2*pi-2.5,"y2":func092(2*pi-2.5),
    "stroke":"#ff0"}
  ];
  drawLine(svg11,lineData11,xScale09,yScale09);
  // text   
  foData10 = [
    {"x":-0.3,
    "y":12,
    "text":"$$y$$",
    "fontSize":"20px"},
    {"x":7,
    "y":1.2,
    "text":"$$x$$",
    "fontSize":"20px"},

    {"x":2*pi-2.5,
    "y":1.2,
    "text":"$$c$$",
    "fontSize":"18px"},
    {"x":2*pi-0.5,
    "y":1.2,
    "text":"$$b$$",
    "fontSize":"18px"},
    {"x":1,
    "y":1.2,
    "text":"$$a$$",
    "fontSize":"18px"},

    {"x":2*pi,
    "y":11,
    "text":"$$y=f(x)$$",
    "fontSize":"18px"},

  ];
  drawMathjax(svg11,foData10,xScale09,yScale09);

  /** Breaking up integral interval */
  drawArea(svg12,areaData094,y0Func09,
    {"fillColor":"#00f","opacity":0.4},xScale09,yScale09); 
  drawPath(svg12,pathData092,{"stroke":"lime","strokeWidth":3},xScale09,yScale09); 
  drawAxes(svg12,axesData09);
  drawLine(svg12,lineData11,xScale09,yScale09);
  drawMathjax(svg12,foData10,xScale09,yScale09);

/** Definite integral of shifted function */
  var xScale13 = d3.scale.linear()
                       .domain([-2,8])
                       .range([50,450]);
  
  var yScale13 = d3.scale.linear()
                       .domain([10,0])
                       .range([50,450]);

  // 軸
  axesData13 = {
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
    "xScale":xScale13,
    "yScale":yScale13
  };

  var pathData131 = [];
  var pathData132 = [];
  var areaData131 = [];
  var areaData132 = [];
  function func131(i){
  return 3*(Math.sin(i)+i/3 + 1);
  };
  y0Func13 = function y0func13(i){
    return 0;
  };

  for (var i = 0; i <= 2*pi; i=i+0.01) {
    pathData131.push(new Point(i-1.5,func131(i)));
    pathData132.push(new Point(i,func131(i)));
  };
  for (var i = 1; i <= 2*pi-0.5; i=i+0.01) {
    areaData131.push(new Point(i-1.5,func131(i)));
    areaData132.push(new Point(i,func131(i)));
  };

  drawArea(svg13,areaData131,y0Func13,
    {"fillColor":"#00f","opacity":0.6},xScale13,yScale13); 
  drawArea(svg13,areaData132,y0Func13,
    {"fillColor":"#f0f","opacity":0.4},xScale13,yScale13); 
  drawPath(svg13,pathData131,{"stroke":"lime","strokeWidth":3},xScale13,yScale13); 
  drawPath(svg13,pathData132,{"stroke":"#fff","strokeWidth":3},xScale13,yScale13); 
  drawAxes(svg13,axesData13);

  // text   
  foData13 = [
    {"x":-0.3,
    "y":12,
    "text":"$$y$$",
    "fontSize":"20px"},
    {"x":8,
    "y":1.2,
    "text":"$$x$$",
    "fontSize":"20px"},

    {"x":2*pi-2,
    "y":1.2,
    "text":"$$b$$",
    "fontSize":"18px"},
    {"x":1-2,
    "y":1.2,
    "text":"$$a$$",
    "fontSize":"18px"},
    {"x":2*pi-0.5,
    "y":1.2,
    "text":"$$b+c$$",
    "fontSize":"18px"},
    {"x":1,
    "y":1.2,
    "text":"$$a+c$$",
    "fontSize":"18px"},

    {"x":2*pi,
    "y":11,
    "text":"$$y=f(x-c)$$",
    "fontSize":"18px"},
    {"x":pi-.5,
    "y":11,
    "text":"$$y=f(x)$$",
    "fontSize":"18px"},

  ];
 
  drawMathjax(svg13,foData13,xScale13,yScale13);
/** Swich bounds of integral*/
  drawAxes(svg14,axesData06);
  drawPath(svg14,pathData06,{"stroke":"lime"},xScale06,yScale06);
  drawRect(svg14,rectData062,xScale06,yScale06);
  drawMathjax(svg14,foData06,xScale06,yScale06);

</script>
