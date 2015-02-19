---
title: Differential calculus
layout: post
date: 2015-01-31 21:00:00
postTitle: Integration applications
categories: integral
---

-------

# Area between curves

--------

## 例1

<div class="row">
  <div class="col-sm-6">
    <div id="svg01"></div>
  </div>
  <div class="col-sm-6">
    <div class="panel">
      $$f(x)=\sqrt{x} \quad と \quad g(x)=x^2 \quad に挟まれた部分の面積は?$$
    </div>
    $$\int_{0}^{1}(\sqrt{x}-x^2)dx$$
    $$=\int_{0}^{1}(\sqrt{x})dx-\int_{0}^{1}(x^2)dx$$
    $$=\frac{2}{3}x^{\frac{3}{2}}|_{0}^{1} - \frac{1}{3}x^3|_{0}^{1}$$
    $$=\frac{2}{3}-0 -(\frac{1}{3}-0)$$
    $$=\frac{1}{3}$$
  </div>
</div>

## 例2

<div class="row">
  <div class="col-sm-6">
    <div id="svg02"></div>
  </div>
  <div class="col-sm-6">
    <div class="panel">
      $$y=2-x \quad y=\sqrt{x} \quad と \quad y=x^2/4-1$$
      $$に挟まれた部分の面積は?$$
      $$\int_{0}^{1}[\sqrt{x}-(x^2/4-1)]dx 
      +\int_{1}^{2}[2-x-(x^2/4-1)]dx$$
      $$=[\frac{2}{3}x^{3/2}-(x^3/12-x)]_{0}^{1}
        +[2x-x^2/2-(x^3/12-x)]_{1}^{2}$$
      $$=\frac{5}{2}$$  
    </div>
  </div>
</div>

------------

# Average value of a function 

<div class="row">
  <div class="col-sm-6">
    <div id="svg03"></div>
  </div>
  <div class="col-sm-6">
    <div class="panel">
      $$閉じた範囲[a,b]における関数f(x)の平均値を求める$$
    </div>
    $$平均値は[a,b]でyの値の平均値です$$
    $$x軸から曲線までの高さをhとすると、その高さの平均です$$
    関数の下にできる面積で考えると、面積は
    $$\int_{a}^{b}f(x)dx$$
    $$平均の高さをf_{avg}とする長方形で考えると$$
    $$f_{avg} \cdot (b-a) = 　\int_{a}^{b}f(x)dx$$
    $$f_{avg} = \frac{1}{b-a}　\int_{a}^{b}f(x)dx$$

  </div>
</div>

------------

# Arc length

<div class="row">
  <div class="col-sm-6">
    <div id="svg04"></div>
  </div>
  <div class="col-sm-6">
    <div class="panel">
      $$閉じた区間[a,b]における関数f(x)の弧の長さを求める$$
    </div>
    弧の長さは、極短い区間の接線が連なったものと考えられます<br>
    その接線んの長さを\(ds\)とすると、接線の長さは
    $$\int_{a}^{b}ds$$
    ここで　\(ds\) は
    $$ds=\sqrt{(dx)^2 + (dy)^2}$$
    変形します
    $$=\sqrt{(dx)^2(1 + (\frac{dy}{dx})^2)}
    =\sqrt{1 + (\frac{dy}{dx})^2}dx$$
    $$\int_{a}^{b}\sqrt{1 + (\frac{dy}{dx})^2}dx$$
    $$\qquad \frac{dy}{dx}=f'(x)$$
    <div class="panel">
    $$\int_{a}^{b}\sqrt{1 + (f'(x))^2}dx$$
    </div>
  </div>
</div>


------------

# Volume of solids with known cross sections  

<div class="row">
  <div class="col-sm-6">
    <div id="svg05"></div>
  </div>
  <div class="col-sm-6">
    <div class="panel">
      直線x+y=1とx軸、y軸で囲まれた範囲で、x軸に垂直な断面が正三角形の体積を求めよ
    </div>
    正三角形の底辺
    $$1-x$$
    正三角形の高さは
    $$\frac{1-x}{2}\sqrt{3}$$
    正三角形の面積は
    $$\frac{1}{2}(1-x)\frac{1-x}{2}\sqrt{3}=\frac{(1-x)^2\sqrt{3}}{4}$$
    体積は
    $$V(x)=\int_{0}^{1}[\frac{(1-x)^2\sqrt{3}}{4}]dx$$
    $$=\frac{\sqrt{3}}{4}\int_{0}^{1}(1-2x+x^2)dx$$
    $$=\frac{\sqrt{3}}{4}[x-x^2+\frac{x^3}{3}]_{0}^{1}
    =\frac{\sqrt{3}}{4}(1-1+\frac{1}{3}-0)$$
    <div class="panel">
      $$=\frac{\sqrt{3}}{12}$$
    </div>
  </div>
</div>

--------

# Solids of revolution - disc method

## Disk method around x-axis

  <div class="col-sm-6">
    <div id="svg06"></div>
  </div>
  <div class="col-sm-6">
    <div class="panel">
    </div>
    <div class="panel">
    </div>
  </div>
</div>





<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_SVG"></script>
<script src="http://d3js.org/d3.v3.min.js" charset="utf-8"></script>
<script src="{{site.url}}/js/d3draws.js" charset="utf-8"></script>

<script>

  y0func = function y0func(x){
    return 0;
  };


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
                       .domain([0,1.2])
                       .range([50,450]);
  var yScale01 = d3.scale.linear()
                       .domain([1.2,0])
                       .range([50,450]);       

  var xScale02 = d3.scale.linear()
                       .domain([0,2.3])
                       .range([50,450]);
  var yScale02 = d3.scale.linear()
                       .domain([2.3,-1.2])
                       .range([50,450]);       

  var xScale03 = d3.scale.linear()
                       .domain([-1,4])
                       .range([50,450]);
  var yScale03 = d3.scale.linear()
                       .domain([12,0])
                       .range([50,450]);       

  var xScale05 = d3.scale.linear()
                       .domain([0,1.2])
                       .range([50,450]);
  var yScale05 = d3.scale.linear()
                       .domain([1.2,0])
                       .range([50,450]);       

  // 軸
  axesData01 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[1],
    "yTickValues":[1],
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
  
  function func01f(x){
    return Math.sqrt(x);
  };
  func01g = function func01g(x){
    return Math.pow(x,2);
  };

  var pathData01f = [];
  var pathData01g = [];
  var areaData01 = [];

  for (var i = 0; i <= 1.2; i=i+0.02) {
    pathData01f.push(new Point(i,func01f(i)));
    pathData01g.push(new Point(i,func01g(i)));
  };
  for (var i = 0; i <= 1; i=i+0.02) {
    areaData01.push(new Point(i,func01f(i)));
  };

  drawArea(svg01,areaData01,func01g,
    {"fillColor":"#00f","opacity":0.6},xScale01,yScale01); 

  drawPath(svg01,pathData01f,{"stroke":"lime","strokeWidth":2},xScale01,yScale01); 
  drawPath(svg01,pathData01g,{"stroke":"#f0f","strokeWidth":2},xScale01,yScale01); 

  // ex.2 
    // 軸
  axesData02 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[1],
    "yTickValues":[1],
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

  function func02f(x){
    return Math.sqrt(x);
  };
  func02g = function func02g(x){
    return Math.pow(x,2)/4-1;
  };
  func02l = function func02g(x){
    return -x+2;
  };

  var pathData02f = [];
  var pathData02g = [];
  var pathData02l = [];
  var areaData02f = [];
  var areaData02l = [];

  for (var i = 0; i <= 2.3; i=i+0.02) {
    pathData02f.push(new Point(i,func02f(i)));
  };
  for (var i = -0.2; i <= 2.3; i=i+0.02) {
    pathData02g.push(new Point(i,func02g(i)));
    pathData02l.push(new Point(i,func02l(i)));
  };
  for (var i = 0; i <= 1; i=i+0.01) {
    areaData02f.push(new Point(i,func02f(i)));
  };
  for (var i = 1; i <= 2; i=i+0.01) {
    areaData02l.push(new Point(i,func02l(i)));
  };

  drawArea(svg02,areaData02f,func02g,
    {"fillColor":"#00f","opacity":0.6},xScale02,yScale02); 
  drawArea(svg02,areaData02l,func02g,
    {"fillColor":"#00f","opacity":0.6},xScale02,yScale02); 

  drawPath(svg02,pathData02f,{"stroke":"lime","strokeWidth":2},xScale02,yScale02); 
  drawPath(svg02,pathData02g,{"stroke":"#f0f","strokeWidth":2},xScale02,yScale02); 
  drawPath(svg02,pathData02l,{"stroke":"#ff0","strokeWidth":2},xScale02,yScale02); 

  drawAxes(svg02,axesData02);


/** Average value 
                   **/
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
  
  func03 = function func03(x){
    return Math.pow(x,2) + 1;
  };

  var pathData03 = [];
  var pathData031 = [];
  var areaData03 = [];

  for (var i = -1; i <= 4; i=i+0.1) {
    pathData03.push(new Point(i,func03(i)));
  };
  for (var i = 1; i <= 3.1; i=i+0.1) {
    areaData03.push(new Point(i,func03(i)));
  };

  pathData031.push(new Point(1,0));
  pathData031.push(new Point(1,16/3));
  pathData031.push(new Point(0,16/3));
  pathData031.push(new Point(3,16/3));
  pathData031.push(new Point(3,0));

  drawArea(svg03,areaData03,y0func,
    {"fillColor":"#00f","opacity":0.6},xScale03,yScale03); 

  drawPath(svg03,pathData03,{"stroke":"lime","strokeWidth":2},xScale03,yScale03); 
  drawPath(svg03,pathData031,{"stroke":"gold","strokeWidth":2},xScale03,yScale03); 

  drawAxes(svg03,axesData03);

  foData03 = [
    {"x":-0.3,
    "y":14,
    "text":"$$y$$",
    "fontSize":"20px"},
    {"x":4.2,
    "y":1.2,
    "text":"$$x$$",
    "fontSize":"20px"},

    {"x":0.9,
    "y":1.3,
    "text":"$$a$$",
    "fontSize":"18px"},
    {"x":2.9,
    "y":1.3,
    "text":"$$b$$",
    "fontSize":"18px"},

    {"x":2.0,
    "y":14,
    "text":"$$y=f(x)$$",
    "fontSize":"18px"},
    {"x":-0.7,
    "y":22/3,
    "text":"$$f_{avg}$$",
    "fontSize":"18px"},

  ];

  drawMathjax(svg03,foData03,xScale03,yScale03);

  /**
    Arc length
                **/
  
  var pathData04=[];

  for (var i = 1; i <= 3.1; i=i+0.1) {
    pathData04.push(new Point(i,func03(i)));
  };

  lineData04 = [
    {"x1":1,"y1":func03(1),"x2":1,"y2":0,"stroke":"#fff"},
    {"x1":3,"y1":func03(3),"x2":3,"y2":0,"stroke":"#fff"},
    {"x1":2,"y1":func03(2),"x2":2.3,"y2":func03(2),"stroke":"#fff"},
    {"x1":2.3,"y1":func03(2),"x2":2.3,"y2":func03(2.3),"stroke":"#fff"}
  ]

  drawPath(svg04,pathData03,{"stroke":"lime","strokeWidth":2},xScale03,yScale03); 
  drawPath(svg04,pathData04,{"stroke":"#f0f","strokeWidth":3},xScale03,yScale03); 

  drawLine(svg04,lineData04,xScale03,yScale03); 

  drawAxes(svg04,axesData03);

  foData04 = [
    {"x":-0.3,
    "y":14,
    "text":"$$y$$",
    "fontSize":"20px"},
    {"x":4.2,
    "y":1.2,
    "text":"$$x$$",
    "fontSize":"20px"},

    {"x":0.9,
    "y":1.3,
    "text":"$$a$$",
    "fontSize":"18px"},
    {"x":2.9,
    "y":1.3,
    "text":"$$b$$",
    "fontSize":"18px"},

    {"x":2.0,
    "y":14,
    "text":"$$y=f(x)$$",
    "fontSize":"18px"},

    {"x":1.8,
    "y":7.6,
    "text":"$$ds$$",
    "fontSize":"18px"},
    {"x":2.4,
    "y":7.4,
    "text":"$$dy$$",
    "fontSize":"18px"},
    {"x":2,
    "y":6.4,
    "text":"$$dx$$",
    "fontSize":"18px"},

  ];

  drawMathjax(svg04,foData04,xScale03,yScale03);

  /**
    Volume of solid **/

  axesData05 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[1],
    "yTickValues":[1],
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

  function func05(x){
    return 1-x;
  }; 

  lineData05 = [
    {"x1":-.1,"y1":func05(-0.1),"x2":1.1,"y2":func05(1.1),"stroke":"#fff"},
    {"x1":0.7,"y1":0,"x2":0.7,"y2":func05(0.7),
    "stroke":"lime","strokeWidth":4}
  ]

  drawLine(svg05,lineData05,xScale05,yScale05); 

</script>
