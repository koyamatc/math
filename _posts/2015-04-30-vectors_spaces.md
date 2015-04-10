---
title: Linear algebraebra
layout: post
date: 2015-04-30 23:00:00
postTitle: Vectors and spaces
categories: linear_algebra
---

-------

## Vector intro for linear algebra

<div class="row">
  <div class="col-sm-7">
    <h3>
    $$
    Vector=
    \underbrace
    {\underbrace{magnitude}_{\cfrac{5mph}{speed \to scalor}}
    +\underbrace{direction}_{\cfrac{east}{}}}
    _{veocity \to vector}
    $$
    </h3>
    ベクトルの表現
    $$
    \vec{v}=(5,0)
    =\left[
        \begin{matrix}
        5 \\
        0 \\
        \end{matrix}
    \right]
    \qquad
    \vec{a}
    =\left[
        \begin{matrix}
        4 \\
        3 \\
        \end{matrix}
    \right]

    $$
  </div>
  <div class="col-sm-5">
    <div id="svg01"></div>
  </div>
</div>

--------

## Adding vectors　（加算）

<div class="row">
  <div class="col-sm-7">
    <h3>
    $$
    \vec{a}
    =\left[
        \begin{matrix}
        6 \\
        -2 \\
        \end{matrix}
    \right]
    \qquad
    \vec{b}
    =\left[
        \begin{matrix}
        -4 \\
        4 \\
        \end{matrix}
    \right]
    $$
    $$
    \vec{a}+\vec{b}
    =\left[
        \begin{matrix}
        2 \\
        2 \\
        \end{matrix}
    \right]
    $$    

    </h3>
  </div>
  <div class="col-sm-5">
    <div id="svg02"></div>
  </div>
</div>

--------

## Multiplying a vector by a scalar　（乗算）

<div class="row">
  <div class="col-sm-7">
    <h3>
    $$
    \vec{a}
    =\left[
        \begin{matrix}
        2 \\
        1 \\
        \end{matrix}
    \right]
    \qquad
    3\vec{a}
    =3\left[
        \begin{matrix}
        2 \\
        1 \\
        \end{matrix}
    \right]
    =\left[
        \begin{matrix}
        3 \cdot 2 \\
        3 \cdot 1 \\
        \end{matrix}
    \right]
    =\left[
        \begin{matrix}
        6 \\
        3 \\
        \end{matrix}
    \right]
    $$
    $$
    -1\vec{a}
    =\left[
        \begin{matrix}
        -2 \\
        -1 \\
        \end{matrix}
    \right]
    
    $$

    </h3>
  </div>
  <div class="col-sm-5">
    <div id="svg03"></div>
  </div>
</div>

## Unit vector notation

<div class="row">
  <div class="col-sm-7">
    <h3>
    $$
    \vec{v}
    =\left[
        \begin{matrix}
        2 \\
        3 \\
        \end{matrix}
    \right]
    $$
    単位ベクトル
    $$
    \hat{\imath}
    =\left[
        \begin{matrix}
        1 \\
        0 \\
        \end{matrix}
    \right]
    \qquad
    \hat{\jmath}
    =\left[
        \begin{matrix}
        0 \\
        1 \\
        \end{matrix}
    \right]
    $$
    $$\vec{v}を単位ベクトルで表すと\qquad \vec{v}=2\hat{\imath}+3\hat{\jmath}$$
    $$
    \vec{b}=-\hat{\imath} + 4\hat{\jmath}
    $$
    $$
    \vec{v}+\vec{b}=(2-1)\hat{\imath}+(3+4)\hat{\jmath}=\hat{\imath}+7\hat{\jmath}
    $$

    </h3>
  </div>
  <div class="col-sm-5">
    <div id="svg04"></div>
  </div>
</div>

## unit vector

<div class="row">
  <div class="col-sm-7">
    <h3>
      大きさが１のベクトルを単位ベクトルといいます<br>
      これを\(\hat{u}\) と表し \(||\vec{u}||=1\)
      <br>
      \(\vec{a}=(3,4)\) の単位べくとルを求める
      $$||\vec{a}|| = \sqrt{3^2+4^2}=\sqrt{25}=5$$
      $$\hat{u}=\frac{\vec{a}}{||\vec{a}||}
      =\frac{1}{5}(3,4)=(\frac{3}{5},\frac{4}{5})$$ 

    </h3>
  </div>
  <div class="col-sm-5">
    <div id="svg05"></div>
  </div>
</div>

----------

## Parametric representations of lines

### 線をパラメータ形式で表します

<div class="row">
  <div class="col-sm-6">
    <h3>
      ベクトルを定義します
      $$
      \vec{V}=
        \left[
        \begin{matrix}
          2  \\
          1  \\
        \end{matrix}
        \right]
      $$
      <button id="btn06-1" class="btn btn-lg btn-primary">
        グラフに描く
      </button>
      <br>
      すべての\(\vec{V}\)の集合を\(c\)を実数の定数として表すと
      $$S=\{ c\vec{V} \mid c \in \Bbb{R}\}$$
      $$c=2 \text{ ならば　} c\vec{V}
      =2\left[
        \begin{matrix}
          2  \\
          1  \\
        \end{matrix}
        \right]
        =\left[
        \begin{matrix}
          4  \\
          2  \\
        \end{matrix}
        \right]
      $$  

      <button id="btn06-2" class="btn btn-lg btn-primary">
        グラフに描く
      </button>
      <br><br>
      Sを位置ベクトルの集合とすると、傾き1/2　で原点を通る直線となる
    </h3>
  </div>
  <div class="col-sm-6">
    <div id="svg061"></div>
    <button id="btnReset06" class="btn btn-lg btn-warning">
      Reset
    </button>
  </div>
</div>

<h3>
  点\((2,4)\) を通る、上記の直線と並行な直線を考える
  
  $$
    \vec{x}=
      \left[
        \begin{matrix}
          2  \\
          4  \\
        \end{matrix}
      \right]
  $$

  <button id="btn06-3" class="btn btn-lg btn-primary">
    グラフに描く
  </button>

  <button id="btn06-4" class="btn btn-lg btn-primary">
    ベクトル群をグラフに描く
  </button>
  <button id="btn06-5" class="btn btn-lg btn-primary">
    直線をグラフに描く
  </button>
  <div id="exp06-5">
    この直線は \(c\vec{V}\) に \(\vec{x}\) を加えたものです

    $$L=\{ \vec{x}+t\vec{V} \mid t \in \Bbb{R} \}$$
    直線を表すのに代数では　\(y=mx+b\)　がありますが、
    この式は２次元のときしか使えません<br>
    ベクトルでのの定義は、直線を一般化したもので、次元の拡張にも対応します
  </div>

</h3>

<div class="row">
  <div class="col-sm-6">
    <h3>
      ２つのベクトルを定義します
      $$
      \vec{a}=
        \left[
        \begin{matrix}
          2  \\
          1  \\
        \end{matrix}
        \right]
      
      \qquad
      
      \vec{b}=
        \left[
        \begin{matrix}
          0  \\
          3  \\
        \end{matrix}
        \right]
      $$
      $$\vec{b}-\vec{a}=
        \left[
        \begin{matrix}
          -2  \\
          2  \\
        \end{matrix}
        \right]
      $$  
      <button id="btn062-1" class="btn btn-lg btn-primary">
        (\(\vec{b}-\vec{a}\))をグラフに描く
      </button>
      <br>
      $$t(\vec{b}-\vec{a}) \mid t \in \Bbb{R} 
      \text{ は、原点を通る直線を表す}$$
      $$\vec{b}と\vec{a}\text{　を位置ベクトルとすると２点を通る直線は}$$
      $$L=\{\vec{b}+t(\vec{b}-\vec{a})\mid t \in \Bbb{R}\}$$
      または
      $$L=\{\vec{a}+t(\vec{b}-\vec{a})\mid t \in \Bbb{R}\}$$
      $$これは\quad t(\vec{b}-\vec{a})を \vec{b} または \vec{a} 分
      平行移動したもの$$
      $$L=
        \left[
        \begin{matrix}
          0  \\
          3  \\
        \end{matrix}
        \right]
      + t
        \left[
        \begin{matrix}
          -2  \\
          2  \\
        \end{matrix}
        \right]
        \mid t \in \Bbb{R}
      $$ 
      $$
        L_{i}=
        \left[
        \begin{matrix}
          x軸  \\
          y軸  \\
        \end{matrix}
        \right]

      $$
      $$x=-2t$$
      $$y=2t+3$$ 
      <button id="btn062-2" class="btn btn-lg btn-primary">
        ２点を通る直線をグラフに描く
      </button>

    </h3>
  </div>
  <div class="col-sm-6">
    <div id="svg062"></div>
    <button id="btnReset062" class="btn btn-lg btn-warning">
      Reset
    </button>
  </div>
</div>

<h3>
それでは２点が３次元にあるとします、２点のベクトルは
$$
  \vec{p}_{1}=
        \left[
        \begin{matrix}
          -1  \\
           2  \\
           7  \\
        \end{matrix}
        \right]
  \qquad      
  \vec{p}_{2}=
        \left[
        \begin{matrix}
           0  \\
           3  \\
           4  \\
        \end{matrix}
        \right]
$$
$$ \Bbb{R}^3 \text{　で、この２点を通る線の式（線の集合は）}$$
$$L=\{ 
    \vec{p}_{1}+t(\vec{p}_{1}-\vec{p}_{2}) \mid t \in \Bbb{R}^3
    
    \}
$$ 
$$
  \vec{p}_{1}-\vec{p}_{2}= 
        \left[
        \begin{matrix}
          -1  \\
          -1  \\
           3  \\
        \end{matrix}
        \right]
$$
$$
  L=\{
        \left[
        \begin{matrix}
          -1  \\
           2  \\
           7  \\
        \end{matrix}
        \right]
   + t
        \left[
        \begin{matrix}
          -1  \\
          -1  \\
           3  \\
        \end{matrix}
        \right]
   \mid t \in \Bbb{R}^3        

  \}        
$$
$$x=-t-1$$
$$y=-t+2$$
$$z=3t+7$$
パラメータでの表現は、もっと多くの次元にも対応できます
</h3>

-------------

# Linear combinations and span

--------------

## Linear combination(線型結合)　とは

###  ベクトルの線形結合は

<h3>
  いくつかのベクトルがあります
  $$v_{1},v_{2},v_{3}, \cdots ,v_{n} \in \Bbb{R}$$
  <strong>この加算を意味します</strong><br>

  各ベクトルにはスカラー値（実数）倍されています
  $$c_{1}v_{1}+c_{2}v_{2}+c_{3}v_{3}+ \cdots +c_{n}v_{n} 
  \mid c \in \Bbb{R}$$
</h3>

### 例

<div class="row">
  <div class="col-sm-6">
    <h3>
      ベクトルを定義します
      $$
      \vec{a}=
        \left[
        \begin{matrix}
          1  \\
          2  \\
        \end{matrix}
        \right]
      
      \qquad
      
      \vec{b}=
        \left[
        \begin{matrix}
          0  \\
          3  \\
        \end{matrix}
        \right]
      $$
      定数が　0　のとき
      $$
      0\vec{a}+0\vec{b}=
        \left[
        \begin{matrix}
          0  \\
          0  \\
        \end{matrix}
        \right]
      = \large{0}
      \quad \text{0 ベクトル}
      $$
      次の場合
      $$
      3\vec{a}+(-2)\vec{b}=
        \left[
        \begin{matrix}
          3  \\
          0  \\
        \end{matrix}
        \right]
      $$
      定数は様々な値をとり続けることができます。<br>
      これが線型結合です<br>
      つまり多くの\(\vec{a}\)　と　\(\vec{b}\)の線型結合があります
      <br>
      ３つ目のベクトル
      $$
      \vec{c}=
        \left[
        \begin{matrix}
          7  \\
          2  \\
        \end{matrix}
        \right]
      $$
      があり、これを　\(8\vec{c}\)として、加えることができます
      $$3\vec{a}+(-2)\vec{b}+ 8\vec{c}$$ 
    </h3>
  </div>
  <div class="col-sm-6"></div>
</div>

## グラフに描いてみましょう
<div class="row">
  <div class="col-sm-6">
    <div id="svg071"></div>
      <button id="btnReset071" class="btn btn-lg btn-warning">
        Reset
      </button>
 
  </div>
  <div class="col-sm-6">
    <h3>
      <button id="btn071-1" class="btn btn-lg btn-primary">
        $$\vec{a} \text{ を描く}$$
      </button>
      <button id="btn071-2" class="btn btn-lg btn-primary">
        $$\vec{b} \text{ を描く}$$
      </button>
      <button id="btn071-3" class="btn btn-lg btn-primary">
        $$3\vec{a} \text{ を描く}$$
      </button>
      <button id="btn071-4" class="btn btn-lg btn-primary">
        $$-2\vec{b} \text{ を描く}$$
      </button>
      <br><br>
      <button id="btn071-5" class="btn btn-lg btn-primary">
        $$3\vec{a}-2\vec{b} \text{ を描く}$$
      </button>
      <button id="btn071-6" class="btn btn-lg btn-primary">
        $$\frac{11}{2}\vec{a}-2\vec{b} \text{ を描く}$$
      </button>
      <br><br>
      <button id="btn071-7" class="btn btn-lg btn-primary">
        $$色々な定数でベクトルを描く$$
      </button>
    </h3>
  </div>
</div>

<h3>
$$
c_{1}\vec{a}+c_{2}\vec{b} 
\text{ で、２次元平面上のすべての点を表すことができます}
$$
この２つのベクトルと定数で表すことのできる空間を<strong>ベクトル空間(span)</strong>
といいます。
$$Span(\vec{a},\vec{b})=\Bbb{R}^2$$
</h3>

<div class="row">
  <div class="col-sm-6">
    <div id="svg072"></div>
      <button id="btnReset072" class="btn btn-lg btn-warning">
        Reset
      </button>
   </div>
  <div class="col-sm-6">
    <h3>
      次の２つのベクトルの場合を見ましょう
      $$
      \vec{a}=
        \left[
        \begin{matrix}
          2  \\
          2  \\
        \end{matrix}
        \right]
      
      \qquad
      
      \vec{b}=
        \left[
        \begin{matrix}
          -2  \\
          -2  \\
        \end{matrix}
        \right]
      $$
      <button id="btn072-1" class="btn btn-lg btn-primary">
        $$\vec{a} \text{ を描く}$$
      </button>
      <button id="btn072-2" class="btn btn-lg btn-primary">
        $$\vec{b} \text{ を描く}$$
      </button>
      <button id="btn072-3" class="btn btn-lg btn-primary">
        $$c_{1}\vec{a} \text{ を描く}$$
      </button>
      <button id="btn072-4" class="btn btn-lg btn-primary">
        $$c_{2}\vec{b} \text{ を描く}$$
      </button>

    </h3>
  </div>
</div>
<h3>
$$
c_{1}\vec{a}+c_{2}\vec{b} 
\text{　今回のベクトル空間は１本の線上です、平面全体を表していません}
$$
２つのベクトルが同一線上にある場合には、面全体を表すことはできません。
<br>
また　０ベクトルも面全体を表せません
<br><br>
$$Span(v_{1},v_{2},v_{3},\cdots,v_{n})=
\{c_{1}v_{1}+c_{2}v_{2}+c_{3}v_{3}+\cdots+c_{n}v_{n}\}
\mid c_{i} \in \Bbb{R}^{n} \quad 1 \ge i \ge n
$$
</h3>

---------

# Linear dependence and independence

---------

## 

<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_SVG"></script>
<script src="http://d3js.org/d3.v3.min.js" charset="utf-8"></script>
<script src="{{site.url}}/js/d3draws.js" charset="utf-8"></script>
<script src="{{site.url}}/js/jquery.js" charset="utf-8"></script>

<script>

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

  var svg071 = d3.select("#svg071")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg072 = d3.select("#svg072")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");

  var xScale01 = d3.scale.linear()
                       .domain([-1,6])
                       .range([50,450]);
  var yScale01 = d3.scale.linear()
                       .domain([6,-1])
                       .range([50,450]);       
  var xScale02 = d3.scale.linear()
                       .domain([-7,7])
                       .range([50,450]);
  var yScale02 = d3.scale.linear()
                       .domain([7,-7])
                       .range([50,450]);       

  var xScale04 = d3.scale.linear()
                       .domain([0,4])
                       .range([50,450]);
  var yScale04 = d3.scale.linear()
                       .domain([4,0])
                       .range([50,450]);       

  var xScale05 = d3.scale.linear()
                       .domain([0,5])
                       .range([50,450]);
  var yScale05 = d3.scale.linear()
                       .domain([5,0])
                       .range([50,450]);       

  var xScale06 = d3.scale.linear()
                       .domain([-10,10])
                       .range([20,480]);
  var yScale06 = d3.scale.linear()
                       .domain([6,-6])
                       .range([20,480]);       
  var xScale07 = d3.scale.linear()
                       .domain([-10,10])
                       .range([20,480]);
  var yScale07 = d3.scale.linear()
                       .domain([10,-10])
                       .range([20,480]);       

  // 軸
  axesData01 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[1,2,3,4,5,6],
    "yTickValues":[1,2,3,4,5,6],
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
  axesData06 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[-10,-8,-6,-4,-2,2,4,6,8,10],
    "yTickValues":[-10,-8,-6,-4,-2,2,4,6,8,10],
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

  axesData07 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[-10,-8,-6,-4,-2,2,4,6,8,10],
    "yTickValues":[-10,-8,-6,-4,-2,2,4,6,8,10],
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

  drawAxes(svg01,axesData01);
  var vecData01 = [
{"x1":0,"y1":0,"x2":5,"y2":0,"stroke":"#0f0","strokeWidth":4},
{"x1":0,"y1":0,"x2":4,"y2":3,"stroke":"#f0f","strokeWidth":4}
];    
drawVectorB(svg01,vecData01,xScale01,yScale01);

foData01 = [
    {"x":-0.5,
    "y":7.5,
    "text":"$$y$$",
    "fontSize":"18px"},
    {"x":6.2,
    "y":0.5,
    "text":"$$x$$",
    "fontSize":"18px"},
    {"x":2.5,
    "y":1.5,
    "text":"$$\\vec{v}$$",
    "fontSize":"16px"},
    {"x":2,
    "y":3,
    "text":"$$\\vec{a}$$",
    "fontSize":"16px"},

  ];

  drawMathjax(svg01,foData01,xScale01,yScale01);

  // Adding
  var vecData02 = [
{"x1":0,"y1":0,"x2":6,"y2":-2,"stroke":"#0f0","strokeWidth":4},
{"x1":0,"y1":0,"x2":-4,"y2":4,"stroke":"#f0f","strokeWidth":4},
{"x1":0,"y1":0,"x2":2,"y2":2,"stroke":"#ff0","strokeWidth":4},
{"x1":6,"y1":-2,"x2":2,"y2":2,"stroke":"#f0f","strokeWidth":4},
];    
drawVectorB(svg02,vecData02,xScale02,yScale02);
drawAxes(svg02,axesData02);

foData02 = [
    {"x":-0.5,
    "y":9,
    "text":"$$y$$",
    "fontSize":"18px"},
    {"x":7.2,
    "y":1,
    "text":"$$x$$",
    "fontSize":"18px"},
    {"x":2.5,
    "y":0.5,
    "text":"$$\\vec{a}$$",
    "fontSize":"16px"},
    {"x":-3,
    "y":3.5,
    "text":"$$\\vec{b}$$",
    "fontSize":"16px"},
    {"x":3.5,
    "y":3.5,
    "text":"$$\\vec{b^{'}}$$",
    "fontSize":"16px"},

  ];

  drawMathjax(svg02,foData02,xScale02,yScale02);

// Multiplying 

var vecData03 = [
{"x1":0,"y1":0,"x2":6,"y2":3,"stroke":"#0f0","strokeWidth":6},
{"x1":0,"y1":0,"x2":2,"y2":1,"stroke":"#f0f","strokeWidth":2},
{"x1":0,"y1":0,"x2":-2,"y2":-1,"stroke":"#ff0","strokeWidth":4}
]; 

drawVectorB(svg03,vecData03,xScale02,yScale02);

drawAxes(svg03,axesData02);

// Unit vectors notation
var vecData04 = [
{"x1":0,"y1":0,"x2":2,"y2":0,"stroke":"#fff","strokeWidth":5},
{"x1":2,"y1":0,"x2":2,"y2":3,"stroke":"#fff","strokeWidth":5},
{"x1":0,"y1":0,"x2":2,"y2":3,"stroke":"#f0f","strokeWidth":5},
{"x1":0,"y1":0,"x2":1,"y2":0,"stroke":"#0f0","strokeWidth":3},
{"x1":0,"y1":0,"x2":0,"y2":1,"stroke":"#0f0","strokeWidth":3}
]; 

drawVectorB(svg04,vecData04,xScale04,yScale04);

foData04 = [
    {"x":1,
    "y":2.5,
    "text":"$$\\vec{v}$$",
    "fontSize":"16px"},
    {"x":0.5,
    "y":0.4,
    "text":"$$\\hat{\\imath}$$",
    "fontSize":"16px"},
    {"x":-0.2,
    "y":1,
    "text":"$$\\hat{\\jmath}$$",
    "fontSize":"16px"},
    {"x":1.2,
    "y":0.4,
    "text":"$$2$$",
    "fontSize":"16px"},
    {"x":2.2,
    "y":2.0,
    "text":"$$3$$",
    "fontSize":"18px"},

  ];

  drawMathjax(svg04,foData04,xScale04,yScale04);

  // unit vector
var vecData05 = [
{"x1":0,"y1":0,"x2":3,"y2":0,"stroke":"#fff","strokeWidth":5},
{"x1":3,"y1":0,"x2":3,"y2":4,"stroke":"#fff","strokeWidth":5},
{"x1":0,"y1":0,"x2":3,"y2":4,"stroke":"#f0f","strokeWidth":5},
{"x1":0,"y1":0,"x2":3/5,"y2":4/5,"stroke":"#0f0","strokeWidth":3},
]; 

drawVectorB(svg05,vecData05,xScale05,yScale05);

foData05 = [
    {"x":1.5,
    "y":3.5,
    "text":"$$\\vec{a}$$",
    "fontSize":"16px"},
    {"x":0.1,
    "y":1.4,
    "text":"$$\\hat{u}$$",
    "fontSize":"16px"},
    {"x":1.5,
    "y":0.4,
    "text":"$$3$$",
    "fontSize":"16px"},
    {"x":3.2,
    "y":2.0,
    "text":"$$4$$",
    "fontSize":"18px"},

  ];

  drawMathjax(svg05,foData05,xScale05,yScale05);

  // Parametric representation of line

  var vecData061 = [];
  var pathData061 = [];
  
  init06();

  // Object
  function func061(x,y,c,stroke,sWidth){
    this.x1 = 0;
    this.y1 = 0;
    this.x2 = x*c;
    this.y2 = y*c;
    this.stroke = stroke?stroke:"#fff";
    this.strokeWidth = sWidth?sWidth:2;
    return this;
  };
  function func0612(x,y,c,stroke,sWidth){
    this.x1 = x*c;
    this.y1 = y*c;
    this.x2 = x*c+2;
    this.y2 = y*c+4;
    this.stroke = stroke?stroke:"#fff";
    this.strokeWidth = sWidth?sWidth:2;
    pathData061.push(new Point(this.x2,this.y2))
    return this;
  };


  d3.select("#btn06-1").on("click", function(){
    vecData061.push(new func061(2,1,1,"#0f0"));

    drawVectorB(svg061,vecData061,xScale06,yScale06);
    $("#btn06-2").removeClass("disabled");
  });     

  d3.select("#btn06-2").on("click", function(){

    for (var i = -10; i<= 10; i=i+0.5){
      vecData061.push(new func061(2,1,i,"",1));
    };

    drawVectorB(svg061,vecData061,xScale06,yScale06);
    $("#btn06-3").removeClass("disabled");
  });     

  d3.select("#btn06-3").on("click", function(){

    vecData061.push(new func061(2,4,1,"#0f0"));

    drawVectorB(svg061,vecData061,xScale06,yScale06);
    $("#btn06-4").removeClass("disabled");
  });     

  d3.select("#btn06-4").on("click", function(){

    for (var i = -10; i<= 10; i=i+0.5){
      vecData061.push(new func0612(2,1,i,"#f0f",1));
    };

    drawVectorB(svg061,vecData061,xScale06,yScale06);


    $("#btn06-5").removeClass("disabled");
  });     
  d3.select("#btn06-5").on("click", function(){

    drawPath(svg061,pathData061,{"stroke":"#f0f"},xScale06,yScale06)
    $("#exp06-5").removeClass("hidden");;
    //$("#btn06-5").removeClass("disabled");
  });     
  
  d3.select("#btnReset06").on("click", function(){
    init06();
  });     

  function init06(){
    
    vecData061 = [];

    $("#btn06-2").addClass("disabled");
    $("#btn06-3").addClass("disabled");
    $("#btn06-4").addClass("disabled");
    $("#btn06-5").addClass("disabled");
    $("#exp06-5").addClass("hidden");

    svg061.selectAll("svg g").remove();
    svg061.selectAll("svg path").remove();
    svg061.selectAll("svg line").remove();

    drawAxes(svg061,axesData06); 
  };

  // svg062
  var vecData062 = [];
  
  init062();


  d3.select("#btn062-1").on("click", function(){

    vecData062.push(new func061(-2,2,1,"#ff0",3));

    drawVectorB(svg062,vecData062,xScale06,yScale06);
    $("#btn062-2").removeClass("disabled");
  });  

  d3.select("#btn062-2").on("click", function(){

    lineData062 = [
      {"x1":-10,"y1":10+3,"x2":10,"y2":-10+3,"stroke":"#ff0"}
    ];

    drawLine(svg062,lineData062,xScale06,yScale06);
  });     

  d3.select("#btnReset062").on("click", function(){
    init062();
  });     

  function init062(){
  
    $("#btn062-2").addClass("disabled");

    svg062.selectAll("svg g").remove();
    svg062.selectAll("svg path").remove();
    svg062.selectAll("svg line").remove();

    vecData062=[];
    drawAxes(svg062,axesData06); 
    vecData062.push(new func061(2,1,1,"#0f0",3));
    vecData062.push(new func061(0,3,1,"#f0f",3));
    drawVectorB(svg062,vecData062,xScale06,yScale06);

  };

/* Linear combinations and span*/
  // Object
  function vecObj(ax,ay,bx,by,c1,c2,stroke,sWidth){
    this.x1 = 0;
    this.y1 = 0;
    this.x2 = ax*c1 + bx*c2;
    this.y2 = ay*c1 + by*c2;
    this.stroke = stroke?stroke:"#fff";
    this.strokeWidth = sWidth?sWidth:2;
    return this;
  };

gridData07 = 
{
"xGrid":true,
"yGrid":true,
"xStep":2,
"yStep":2,
"stroke":"#0f0",
"strokeWidth":1,
"opacity":0.3,
"xScale":xScale07,
"yScale":yScale07
};

  var vecData071 = [];
  
  init071();

  d3.select("#btn071-1").on("click", function(){

    vecData071.push(new vecObj(1,2,0,0,1,1,"#fff",3));

    drawVectorB(svg071,vecData071,xScale07,yScale07);
    $("#btn071-2").removeClass("disabled");
  });  
  
  d3.select("#btn071-2").on("click", function(){

    vecData071.push(new vecObj(0,0,0,3,1,1,"#f00",3));

    drawVectorB(svg071,vecData071,xScale07,yScale07);
    $("#btn071-3").removeClass("disabled");
  });  

  d3.select("#btn071-3").on("click", function(){

    vecData071.push(new vecObj(1,2,0,0,3,1,"#ccc",2));

    drawVectorB(svg071,vecData071,xScale07,yScale07);
    $("#btn071-4").removeClass("disabled");
  });  

  d3.select("#btn071-4").on("click", function(){

    vecData071.push(new vecObj(0,0,0,3,1,-2,"#f0f",2));

    drawVectorB(svg071,vecData071,xScale07,yScale07);
    $("#btn071-5").removeClass("disabled");
  });  

  d3.select("#btn071-5").on("click", function(){

    vecData071.push(new vecObj(1,2,0,3,3,-2,"#0f0",4));

    drawVectorB(svg071,vecData071,xScale07,yScale07);
    $("#btn071-6").removeClass("disabled");
  });  

  d3.select("#btn071-6").on("click", function(){

    vecData071.push(new vecObj(1,2,0,3,11/2,-2,"#0f0",4));

    drawVectorB(svg071,vecData071,xScale07,yScale07);
    $("#btn071-7").removeClass("disabled");

  });  

  d3.select("#btn071-7").on("click", function(){

    var x2,y2;
    for (var i=0;i<90;i++){

      x2 = Math.random() * 10 * Math.pow(-1,Math.floor(Math.random()*2)+1);
      y2 = Math.random() * 10 * Math.pow(-1,Math.floor(Math.random()*2)+1);
      vecData071.push(new vecObj(x2,y2,0,0,1,1,"#f0f",1));
    };

    drawVectorB(svg071,vecData071,xScale07,yScale07);
    $("#btn071-5").removeClass("disabled");

  });  

  d3.select("#btnReset071").on("click", function(){
    init071();
  });     
function init071(){

  $("#btn071-2").addClass("disabled");
  $("#btn071-3").addClass("disabled");
  $("#btn071-4").addClass("disabled");
  $("#btn071-5").addClass("disabled");
  $("#btn071-6").addClass("disabled");
  $("#btn071-7").addClass("disabled");

  svg071.selectAll("svg g").remove();
  svg071.selectAll("svg path").remove();
  svg071.selectAll("svg line").remove();

  vecData071=[];

  drawAxes(svg071,axesData07);   
  drawGrid(svg071,gridData07); 
}

  //  
  
  var vecData072 = [];
  
  init072();

  d3.select("#btn072-1").on("click", function(){

    vecData072.push(new vecObj(2,2,0,0,1,1,"#fff",3));

    drawVectorB(svg072,vecData072,xScale07,yScale07);
    $("#btn072-2").removeClass("disabled");
  });  
  
  d3.select("#btn072-2").on("click", function(){

    vecData072.push(new vecObj(0,0,-2,-2,1,1,"#f00",3));

    drawVectorB(svg072,vecData072,xScale07,yScale07);
    $("#btn072-3").removeClass("disabled");
  });  

  d3.select("#btn072-3").on("click", function(){

    for (var i=-10;i<10;i=i+0.5){
      vecData072.push(new vecObj(2,2,0,0,i,1,"#ccc",2));
    };

    drawVectorB(svg072,vecData072,xScale07,yScale07);
    $("#btn072-4").removeClass("disabled");
  });  

  d3.select("#btn072-4").on("click", function(){

    for (var i=-10;i<10;i=i+0.5){
      vecData072.push(new vecObj(0,0,-2,-2,1,i,"#f0f",2));
    };

    drawVectorB(svg072,vecData072,xScale07,yScale07);
    $("#btn072-5").removeClass("disabled");
  });  

  d3.select("#btn072-5").on("click", function(){

    vecData072.push(new vecObj(1,2,0,3,3,-2,"#0f0",4));

    drawVectorB(svg072,vecData072,xScale07,yScale07);
    $("#btn072-6").removeClass("disabled");
  });  

  d3.select("#btn072-6").on("click", function(){

    vecData072.push(new vecObj(1,2,0,3,11/2,-2,"#0f0",4));

    drawVectorB(svg072,vecData072,xScale07,yScale07);
    $("#btn072-7").removeClass("disabled");

  });  

  d3.select("#btn072-7").on("click", function(){

    var x2,y2;
    for (var i=0;i<90;i++){

      x2 = Math.random() * 10 * Math.pow(-1,Math.floor(Math.random()*2)+1);
      y2 = Math.random() * 10 * Math.pow(-1,Math.floor(Math.random()*2)+1);
      vecData072.push(new vecObj(x2,y2,0,0,1,1,"#f0f",1));
    };

    drawVectorB(svg072,vecData072,xScale07,yScale07);
    $("#btn072-5").removeClass("disabled");

  });  

  d3.select("#btnReset072").on("click", function(){
    init072();
  });     


function init072(){

  $("#btn072-2").addClass("disabled");
  $("#btn072-3").addClass("disabled");
  $("#btn072-4").addClass("disabled");
  $("#btn072-5").addClass("disabled");
  $("#btn072-6").addClass("disabled");
  $("#btn072-7").addClass("disabled");

  svg072.selectAll("svg g").remove();
  svg072.selectAll("svg path").remove();
  svg072.selectAll("svg line").remove();

  vecData072=[];

  drawAxes(svg072,axesData07);   
  drawGrid(svg072,gridData07); 
}

</script>
