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

</script>
