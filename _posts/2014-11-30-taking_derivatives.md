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
  曲線の点\( (x_0,f(x_0)) \)での傾きは、この点での接線(tangent line)の傾き
  <h3>
  $$\lim_{h \to 0} \frac{f(x_0+h)-f(x_0)}{h}$$
  </h3>
  となります
  </div>
</div>

--------

## Calculating slope of tangent line using derivative definition
<div class="row">
  <div class="col-sm-6">
    <div id="svg05"></div>
  </div>
  <div class="col-sm-6">
    \(f(x)=x^2\)です。<br>
    \(x=3\)のとき\(f(3)=9\)でピンクの点\((3,9)\)です<br>
    \(x=3+h\)のとき\(f(3+h)=(3+h)^2\)で黄色の点\((3+h,(3+h)^2))\)です<br>
    \(f'(x)\)を\(f(x)\)の導関数とすると、\(x=3\)のときの接線の傾きは<br>
    $$f'(x)=\lim_{h \to 0} \frac{f(3+h)-f(3)}{h}
    =\lim_{h \to 0} \frac{(3+h)^2-9}{h}$$
    $$\quad=\lim_{h \to 0} \frac{9+6h+h^2-9}{h}
    =\lim_{h \to 0} 6+h=6$$
    一般化すると
    $$f'(x)=\lim_{h \to 0} \frac{f(x+h)-f(x)}{h}
    =\lim_{h \to 0} \frac{(x+h)^2-x^2}{h}$$
    $$\quad=\lim_{h \to 0} \frac{x^2+2hx+h^2-x^2}{h}
    =\lim_{h \to 0} 2x+h=2x$$
    \(2x\)が曲線\(f(x)=x^2\)の各\(x\)における接線の傾きです
  </div>
</div>

## Formal and alternate form of the derivative
<div class="row">
  <div class="col-sm-6">
    <div id="svg06"></div>
  </div>
  <div class="col-sm-6">
  曲線\(y=f(x)\)の\(x=a\)における接線の傾きは
  $$点(a,f(a))とｘ軸方向にhだけ離れた点(a+h,f(a+h))を通る割線において$$
  \(h\)の値が限りなく0に近づいたときに下記の導関数で求められる
  $$f'(a)=\lim_{h \to 0}\frac{f(a+h)-f(a)}{h}$$  
  </div>
</div>
<div class="row">
  <div class="col-sm-6">
    <div id="svg07"></div>
  </div>
  <div class="col-sm-6">
  別の表現をすると
  曲線\(y=f(x)\)の\(x=a\)における接線の傾きは
  $$点(a,f(a))と点(x,f(x))を通る割線において$$
  \(x\)の値が限りなくaに近づいたときに下記の導関数で求められる
  $$f'(x)=\lim_{x \to a}\frac{f(x)-f(a)}{x-a}$$
  2つの導関数は同じことを表している  
  </div>
</div>

-----------

# Visualizing graphs of functionas and their derivatives

-----------

## Derivative intuition
<div class="row">
  <div class="col-sm-6">
    <div id="svg08"></div>
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

  // 
  var svg05 = d3.select("#svg05")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");


  var xScale05 = d3.scale.linear()
                       .domain([-2,7])
                       .range([50,450]);
  
  var yScale05 = d3.scale.linear()
                       .domain([50,-1])
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
  
  gridData05 = 
  {
    "xGrid":true,
    "yGrid":true,
    "xStep":1,
    "yStep":5,
    "stroke":"#0f0",
    "strokeWidth":1,
    "opacity":0.3,
    "xScale":xScale05,
    "yScale":yScale05
  };
  drawGrid(svg05,gridData05);

  // graph
  pathData05 = [];
  for (var i=-2;i<=7;i=i+0.1){
    pathData05.push(new Point(i,i*i));
  }
  drawPath(svg05,pathData05,{"stroke":"#ff0"},xScale05,yScale05);

  lineData05 = [
    {"x1":1,"y1":-9,"x2":7,"y2":45,"stroke":"#f0f"},
    {"x1":0,"y1":-9,"x2":7,"y2":33,"stroke":"lime"},
    {"x1":3,"y1":0,"x2":3,"y2":9,"stroke":"#f0f","opacity":0.4},
    {"x1":0,"y1":9,"x2":3,"y2":9,"stroke":"#f0f","opacity":0.4},
    {"x1":6,"y1":0,"x2":6,"y2":36,"stroke":"#ff0","opacity":0.5},
    {"x1":0,"y1":36,"x2":6,"y2":36,"stroke":"#ff0","opacity":0.5},
  ];
  drawLine(svg05,lineData05,xScale05,yScale05);

  // circle
  var circleData05 = [
    {"cx":3,"cy":9,"r":2,"stroke":"#f0f","fillColor":"#f0f"}
   ,{"cx":6,"cy":36,"r":2,"stroke":"#ff0","fillColor":"#ff0"}
  ];   
  drawCircle(svg05,circleData05,xScale05,yScale05);

  // mathjax   
  foData05 = [
    {"x":7.5,
    "y":5.5,
    "text":"$$x$$",
    "fontSize":"22px"},
    {"x":0.5,
    "y":60.5,
    "text":"$$y=f(x)$$",
    "fontSize":"22px"},
    {"x":2.9,
    "y":5.5,
    "text":"$$3$$",
    "fontSize":"18px"},
    {"x":5.5,
    "y":5.5,
    "text":"$$3+h$$",
    "fontSize":"18px"},
    {"x":-1.2,
    "y":15,
    "text":"$$f(3)$$",
    "fontSize":"18px"},
    {"x":-1.8,
    "y":43,
    "text":"$$f(3+h)$$",
    "fontSize":"18px"},
    {"x":4.2,
    "y":2,
    "text":"$$\\Delta x$$",
    "fontSize":"18px"},
    {"x":-1.8,
    "y":30,
    "text":"$$\\Delta y$$",
    "fontSize":"18px"},
    {"x":1.5,
    "y":32,
    "text":"$$secant \\quad line$$",
    "fontSize":"18px"},
    {"x":4.4,
    "y":24,
    "text":"$$tangent \\quad line$$",
    "fontSize":"18px"}
  ];
 
  drawMathjax(svg05,foData05,xScale05,yScale05);

  // Formal and alternate form of the derivative
  var svg06 = d3.select("#svg06")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg07 = d3.select("#svg07")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");


  var xScale06 = d3.scale.linear()
                       .domain([-1,9])
                       .range([50,450]);
  
  var yScale06 = d3.scale.linear()
                       .domain([3,-3])
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
  drawAxes(svg06,axesData06);
  drawAxes(svg07,axesData06);
  
  gridData06 = 
  {
    "xGrid":true,
    "yGrid":true,
    "xStep":1,
    "yStep":1,
    "stroke":"#0f0",
    "strokeWidth":1,
    "opacity":0.3,
    "xScale":xScale06,
    "yScale":yScale06
  };
  drawGrid(svg06,gridData06);
  drawGrid(svg07,gridData06);

  // graph
  pathData06 = [];
  for (var i=0.05;i<=9;i=i+0.05){
    pathData06.push(new Point(i,Math.log(i)));
  }
  drawPath(svg06,pathData06,{"stroke":"#ff0"},xScale06,yScale06);
  drawPath(svg07,pathData06,{"stroke":"#ff0"},xScale06,yScale06);

  lineData06 = [
    {"x1":-1,"y1":-0.3679,"x2":9,"y2":3.3109,"stroke":"#f0f"},
    {"x1":Math.E,"y1":0,"x2":Math.E,"y2":Math.log(Math.E),"stroke":"#f0f","opacity":0.4},
    {"x1":0,"y1":1,"x2":Math.E,"y2":1,"stroke":"#f0f","opacity":0.4},
    {"x1":5,"y1":0,"x2":5,"y2":Math.log(5),"stroke":"#ff0","opacity":0.5},
    {"x1":0,"y1":Math.log(5),"x2":5,"y2":Math.log(5),"stroke":"#ff0","opacity":0.5},
  ];
  drawLine(svg06,lineData06,xScale06,yScale06);
  drawLine(svg07,lineData06,xScale06,yScale06);

  // circle
  var circleData06 = [
    {"cx":Math.E,"cy":Math.log(Math.E),"r":2,"stroke":"#f0f","fillColor":"#f0f"}
   ,{"cx":5,"cy":Math.log(5),"r":2,"stroke":"#ff0","fillColor":"#ff0"}
  ];   
  drawCircle(svg06,circleData06,xScale06,yScale06);
  drawCircle(svg07,circleData06,xScale06,yScale06);

  // mathjax   
  foData06 = [
    {"x":9.5,
    "y":1.0,
    "text":"$$x$$",
    "fontSize":"22px"},
    {"x":-0.3,
    "y":4.5,
    "text":"$$y$$",
    "fontSize":"22px"},
    {"x":7.5,
    "y":3.5,
    "text":"$$y=f(x)$$",
    "fontSize":"22px"},
    {"x":Math.E-0.1,
    "y":0.5,
    "text":"$$a$$",
    "fontSize":"18px"},
    {"x":4.5,
    "y":0.5,
    "text":"$$a+h$$",
    "fontSize":"18px"},
    {"x":-1,
    "y":1.9,
    "text":"$$f(a)$$",
    "fontSize":"18px"},
    {"x":-2,
    "y":2.5,
    "text":"$$f(a+h)$$",
    "fontSize":"18px"},
  ];
 
  drawMathjax(svg06,foData06,xScale06,yScale06);

  // mathjax   
  foData07 = [
    {"x":9.5,
    "y":1.0,
    "text":"$$x$$",
    "fontSize":"22px"},
    {"x":-0.3,
    "y":4.5,
    "text":"$$y$$",
    "fontSize":"22px"},
    {"x":7.5,
    "y":3.5,
    "text":"$$y=f(x)$$",
    "fontSize":"22px"},
    {"x":Math.E-0.1,
    "y":0.5,
    "text":"$$a$$",
    "fontSize":"18px"},
    {"x":4.9,
    "y":0.5,
    "text":"$$x$$",
    "fontSize":"18px"},
    {"x":-1,
    "y":1.9,
    "text":"$$f(a)$$",
    "fontSize":"18px"},
    {"x":-1,
    "y":2.5,
    "text":"$$f(x)$$",
    "fontSize":"18px"},
  ];
 
  drawMathjax(svg07,foData07,xScale06,yScale06);

</script>
