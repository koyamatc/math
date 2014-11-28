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
  曲線の点\( (x_0,f(x_0)) \)での傾きは
  <h3>
  $$\lim_{h \to 0} \frac{f(x_0+h)-f(x_0)}{h}$$
  </h3>
  となります


  </div>
</div>

--------

## 
<div class="row">
  <div class="col-sm-6">
    <div id="svg05"></div>
  </div>
  <div class="col-sm-6">
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

</script>
