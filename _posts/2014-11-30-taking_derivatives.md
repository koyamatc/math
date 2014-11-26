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
  直線の傾き(slope)は、\(x\)の変化量\((\triangle x)\)に対する\(y\)の変化量\((\triangle y)\)で<br>
  $$Slope=m=\frac{\triangle y}{\triangle x}=\frac{y_1 - y_0}{x_1 - x_0}$$
  です
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
    "text":"$$\\triangle x$$",
    "fontSize":"18px"},
    {"x":-1.8,
    "y":5.3,
    "text":"$$\\triangle y$$",
    "fontSize":"18px"}
  ];
 
  drawMathjax(svg01,foData01,xScale01,yScale01);

  var pathData02 = [];
  for (var i=-1;i<=9;i=i+0.1){
    var y =  0.3*Math.pow((i-3),2)+3.5;
    pathData02.push(new Point(i,y));
  }
  drawPath(svg02,pathData02,{"stroke":"#ff0"},xScale01,yScale01);

  // circle
  var circleData02 = [
    {"cx":3,"cy":3.5,"r":2,"stroke":"#f0f","fillColor":"#f0f"}
   ,{"cx":5,"cy":4.7,"r":2,"stroke":"#0f0","fillColor":"#0f0"}
  ];   
  drawCircle(svg02,circleData02,xScale01,yScale01);
 
</script>
