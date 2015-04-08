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

<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_SVG"></script>
<script src="http://d3js.org/d3.v3.min.js" charset="utf-8"></script>
<script src="{{site.url}}/js/d3draws.js" charset="utf-8"></script>

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

</script>
