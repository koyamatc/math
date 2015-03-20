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

## Explicit and recursive definitions of sequences



<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_SVG"></script>
<script src="http://d3js.org/d3.v3.min.js" charset="utf-8"></script>
<script src="{{site.url}}/js/d3draws.js" charset="utf-8"></script>

<script>

  var svg01 = d3.select("#svg01")
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

  drawAxes(svg01,axesData01);
  var vecData01 = [
{"x1":0,"y1":0,"x2":5,"y2":0,"stroke":"#00f","strokeWidth":4},
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

</script>
