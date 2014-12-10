---
title: Differential calculus
layout: post
date: 2014-11-30 21:00:00
postTitle: Derivative applications
categories: differential
---

-------

# Equations of normal and tangent lines

--------

## y-intercept of tangent line example

<div class="row">
  <div class="col-sm-6">
    <div id="svg01"></div>
  </div>
  <div class="col-sm-6">
    曲線\(f(x)=\frac{1}{x}\)のある点\((k \ne 0)\)における接線が
    \(y\)軸を横切るときの値を求めよ
    <br>
    \(x=k\)の点の座標は\( (k,\frac{1}{k}) \)
    <br>
    この点を通る接線の傾きは
    $$f(x)=\frac{1}{x}=x^{-1}$$
    $$f'(x)=-x^{-2}=-\frac{1}{x^2}$$
    \(x=k\)のときの傾きは
    $$f'(k)=-\frac{1}{k^2}$$
    接線(tangent line)を\(y=mx+b\)とすると
    <br>
    傾き\(m=\frac{1}{k^2}\)、　ｙ軸との交点のy座標は\(b\)なので
    $$y=-\frac{1}{k^2}x+b$$
   　点\( (k,\frac{1}{k}) \)を通るので
    $$\frac{1}{k}=-\frac{1}{k^2}k+b$$
    $$\frac{1}{k}=-\frac{1}{k}+b$$
    $$b=\frac{1}{k}+\frac{1}{k}=\frac{2}{k}$$
    したがって点\( (k,\frac{1}{k}) \)を通る接線の式は
    $$y=-\frac{1}{k^2}x+\frac{2}{k}$$

  </div>
</div>

-------------

## Equation of normal line(法線)

幾何において __normal__　とは、与えられたオブジェクトに対して垂直な線やベクトルのようなオブジェクトです。

２次元の場合、曲線上の任意の点における接線に対してその点を通る垂直な直線を法線(noramal line)といいます。

<div class="row">
  <div class="col-sm-6">
    <div id="svg02"></div>
  </div>
  <div class="col-sm-6">
  曲線\(f(x)=\frac{e^x}{x^2}\)で\(x=1\)のときの法線の式を求める
  <br>
  \(x=1\)のときの接線の傾きを求めます  
  $$f(x)=\frac{e^x}{x^2}=e^xx^{-2} \quad
  f(1)=\frac{e^1}{1^2}=e$$
  \(f(x)\)を微分します
  $$f'(x)=e^xx^{-2}+e^x(-2x^{-3})$$
  $$f'(1)=e-2e=-e \quad 接線の傾き$$
  法線の傾きは\(-\frac{1}{m}\)なので\(\frac{1}{e}\)
  <br>
  \(y=-\frac{1}{m}x+b\)を法線の式とすると
  $$e=\frac{1}{e}+b \to b=e-\frac{1}{e}$$
  $$y = \frac{1}{e}x+e-\frac{1}{e}$$

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
  var svg02 = d3.select("#svg02")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");


  var xScale01 = d3.scale.linear()
                       .domain([-5,5])
                       .range([50,450]);
  
  var yScale01 = d3.scale.linear()
                       .domain([6,-4])
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
  
  var pathData011 =[];
  var pathData012 =[];
  for (var i=-0.25;i>-5;i=i-0.01){
    pathData011.push(new Point(i,1/i));
  };
  for (var i=0.16;i<5;i=i+0.01){
    pathData012.push(new Point(i,1/i));
  };
  drawPath(svg01,pathData011,{"stroke":"#fff"},xScale01,yScale01);
  drawPath(svg01,pathData012,{"stroke":"#fff"},xScale01,yScale01);

  // graph
  lineData01 = [
    {"x1":1,"y1":1,"x2":0,"y2":2,"stroke":"#0f0"},
    {"x1":1,"y1":1,"x2":2,"y2":0,"stroke":"#0f0"},
  ];
  drawLine(svg01,lineData01,xScale01,yScale01);

  // circle
  var circleData01 = [
    {"cx":1,"cy":1,"r":2,"stroke":"#f0f","fillColor":"#f0f"}
  ];   
  drawCircle(svg01,circleData01,xScale01,yScale01);

  // mathjax   
  foData01 = [
    {"x":5.3,
    "y":1.5,
    "text":"$$x$$",
    "fontSize":"20px"},
    {"x":-0.1,
    "y":8.6,
    "text":"$$y$$",
    "fontSize":"20px"},
    {"x":0.8,
    "y":1,
    "text":"$$k$$",
    "fontSize":"18px"},
    {"x":-0.8,
    "y":2.8,
    "text":"$$\\frac{1}{k}$$",
    "fontSize":"18px"},
    {"x":1,
    "y":5.3,
    "text":"$$f(x)=\\frac{1}{x}$$",
    "fontSize":"18px"}
  ];
 
  drawMathjax(svg01,foData01,xScale01,yScale01);

  var xScale02 = d3.scale.linear()
                       .domain([-3,0])
                       .range([50,450]);
  
  var yScale02 = d3.scale.linear()
                       .domain([1,0])
                       .range([50,450]);       

  // 軸
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
  drawAxes(svg02,axesData02);

  var pathData02 =[];
  for (var i=-3;i<=0;i=i+0.1){
    pathData02.push(new Point(i,func01(i)));
  };
  drawPath(svg02,pathData02,{"stroke":"#fff"},xScale02,yScale02);

  function func01(p){
    return Math.pow(Math.E,p)/Math.pow(p,-2);
  }
</script>
