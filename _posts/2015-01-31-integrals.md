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
    $$\frac{d}{dx}[x^2+c]=2x$$
    すべて\(2x\)となります
  </div>
  <div class="col-sm-6">
    では導関数が\(2x\)となる元の関数は何でしょうか？
    $$x^2,x^2+1,x^2+\pi$$
    などですが
    $$x^2+c$$
    が元の関数となります、これを式
    $$\int 2x dx = x^2 + c$$
    \(\int 2x dx\)を、逆微分とか不定積分といいます
  </div>
</div>

<div class="row">
  <div class="col-sm-6">
    <div id="svg01"></div>
  </div>
  <div class="col-sm-6">

  </div>
</div>

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


/** introduction to  limit */
  var svg01 = d3.select("#svg01")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");

  var xScale01 = d3.scale.linear()
                       .domain([-1.5,1.5])
                       .range([50,450]);
  
  var yScale01 = d3.scale.linear()
                       .domain([1.5,-1.5])
                       .range([50,450]);       

  // 軸
  axesData01 = [
    {"x1":-1.5,"y1":0,"x2":1.5,"y2":0,"stroke":"#ccc"}
   ,{"x1":0,"y1":-1.5,"x2":0,"y2":1.5,"stroke":"#ccc"}
  ];
  drawVectorW(svg01,axesData01,xScale01,yScale01);

  // graph
  lineData01 = [
    // ticks
    {"x1":-1,"y1":0.05,"x2":-1,"y2":-0.05,"stroke":"#ccc"}
   ,{"x1":1,"y1":0.05,"x2":1,"y2":-0.05,"stroke":"#ccc"}
   ,{"x1":-0.05,"y1":-1,"x2":0.05,"y2":-1,"stroke":"#ccc"}
   ,{"x1":-0.05,"y1":1,"x2":0.05,"y2":1,"stroke":"#ccc"}
    // graph
   ,{"x1":-1.5,"y1":1,"x2":1.5,"y2":1,"stroke":"#0f0"}
  ];
  drawLine(svg01,lineData01,xScale01,yScale01);

  // circle
  var circleData01 = [
    {"cx":1,"cy":1,"r":5,"stroke":"#fff","fillColor":"#000"}
  ];   
  drawCircle(svg01,circleData01,xScale01,yScale01);

  // 矢印
  var vecbData01 = [
    {
      "x1":0.5,
      "y1":0.1,
      "x2":1,
      "y2":0.1,
      "stroke":"#f0f"
    },
    {
      "x1":1.3,
      "y1":0.1,
      "x2":1,
      "y2":0.1,
      "stroke":"#f0f"
    }
  ];
  drawVectorB(svg01,vecbData01,xScale01,yScale01);

  // text   
  var textData01 = [
    {"x":1.6,
    "y":-0.1,
    "text":"x",
    "stroke":"#ccc",
    "fontFamily":"メイリオ",
    "fontSize":18},
    {"x":-0.1,
    "y":1.6,
    "text":"y",
    "stroke":"#ccc",
    "fontFamily":"メイリオ",
    "fontSize":18},
    {"x":-1,
    "y":-0.2,
    "text":"-1",
    "stroke":"#ccc",
    "fontFamily":"メイリオ",
    "fontSize":18,
    "anchor":"middle"},
    {"x":1,
    "y":-0.2,
    "text":"1",
    "fontFamily":"メイリオ",
    "stroke":"#ccc",
    "fontSize":18,
    "anchor":"middle"},
    {"x":-0.2,
    "y":-1,
    "text":"-1",
    "stroke":"#ccc",
    "fontFamily":"メイリオ",
    "fontSize":18},
    {"x":-0.1,
    "y":1,
    "text":"1",
    "fontFamily":"メイリオ",
    "stroke":"#ccc",
    "fontSize":18,
    "anchor":"middle"}
      ];

 
  drawText(svg01,textData01,xScale01,yScale01);
 

</script>
