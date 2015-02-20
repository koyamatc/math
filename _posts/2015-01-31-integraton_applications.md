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
<div class="row">
  <div class="col-sm-6">
    <div id="svg06"></div>
  </div>
  <div class="col-sm-6">
    <div class="panel">
    $$曲線f(x)=x^2の点からx軸に垂直に引いた線を半径として$$
    $$x軸を中心に描いた円が区間[0,2]に作る図形のの体積は？$$
    </div>
    $$円の半径：r=x^2$$
    $$円の面積：\pi r^2=\pi(x^2)^2$$
    $$図形の体積$$
    $$\int_{0}^{2}\pi (x^2)^2 dx 
    =\pi\int_{0}^{2}x^4 dx$$
    $$=\pi[\frac{x^5}{5}]_{0}^{2}$$
    $$=\pi(\frac{2^5}{5}-0)$$
    <div class="panel">
    $$=\frac{32\pi}{5}$$
    </div>
    一般化すると、図形の体積は
    <div class="panel">
    <h3>
    $$\pi\int_{a}^{b} (f(x))^2 dx $$
    </h3>
    </div>
  </div>
</div>
## Disc method around y-axis
<div class="row">
  <div class="col-sm-6">
    <div id="svg07"></div>
  </div>
  <div class="col-sm-6">
    <div class="panel">
    $$曲線f(x)=x^2の点からy軸に垂直に引いた線を半径として$$
    $$y軸を中心に描いた円がyの区間[1,4]に作る図形のの体積は？$$
    </div>
    $$円の半径：r=\sqrt{y}$$
    $$円の面積：\pi r^2=\pi(\sqrt{y})^2$$
    $$図形の体積$$
    $$\int_{1}^{4}\pi (\sqrt{y})^2 dy 
    =\pi\int_{1}^{4} y dy$$
    $$=\pi[\frac{y^2}{2}]_{1}^{4}$$
    $$=\pi(\frac{4^2}{2}-\frac{1^2}{2})$$
    $$=\pi(\frac{16}{2}-\frac{1}{2})$$
    <div class="panel">
    $$=\frac{15\pi}{2}$$
    </div>
  </div>
</div>

## Disc method (washer method) for rotation around x-axis

<div class="row">
  <div class="col-sm-6">
    <div id="svg08"></div>
  </div>
  <div class="col-sm-6">
    <div class="panel">
      $$y=\sqrt{x}とy=xとに囲まれた部分が$$
      $$x軸を中心に360°回転してできる図形の体積は$$
    </div>
    $$y=\sqrt{x}とy=xの交点は$$
    $$\sqrt{x}=x \to x=x^2 \to x^2-x = 0 \to x(x-1)=0$$
    $$x=0 \quad or \quad x=1$$
    $$y=\sqrt{x}の体積：V_{1}=\pi\int_{0}^{1}(\sqrt{x})^2dx$$
    $$y=xの体積：V_{2}=\pi\int_{0}^{1}x^2 dx$$
    $$回転してできる図形の体積：V_{1}-V_{2}$$
    $$=\pi[\frac{x^2}{2}]_{0}^{1}-\pi[\frac{x^3}{3}]_{0}^{1}$$
    $$=\pi(\frac{1}{2}-0)-(\frac{1}{3}-0))$$
    <div class="panel">
    $$=\frac{1}{6}\pi$$
    </div>
    一般化すると
    $$f(x)=\sqrt{x} \quad g(x)=x \quad として$$
    $$区間を[a,b]とすると$$
    $$\int_{a}^{b}\pi(f(x))^2dx-\int_{a}^{b}\pi(g(x))^2dx$$
    <div class="panel">
      $$\pi\int_{a}^{b}(f(x))^2-(g(x))^2dx$$
    </div>
  </div>
</div>

## Disc method rotation around horizontal line

<div class="row">
  <div class="col-sm-6">
    <div id="svg09"></div>
  </div>
  <div class="col-sm-6">
    <div class="panel">
      $$y=\sqrt{x}とy=1とに囲まれた部分が、区間[1,4]で$$
      $$y=1を中心に360°回転してできる図形の体積は$$
    </div>
    $$V=\pi \int_{1}^{4}(\sqrt{x}-1)^2 dx$$
    $$=\pi \int_{1}^{4}(x-2\sqrt{x}+1) dx$$
    $$=\pi [\frac{x^2}{2}-\frac{4}{3}x^{3}{2}+x]_{1}^{4}$$
    <div class="panel">
    $$=\frac{7}{6}\pi$$
    </div>
  </div>
</div>

## Washer method rotating around non-axis

<div class="row">
  <div class="col-sm-6">
    <div id="svg10"></div>
  </div>
  <div class="col-sm-6">
    <div class="panel">
      $$y=x^2-2xとy=xとに囲まれた部分が、$$
      $$y=4を中心に360°回転してできる図形の体積は$$
    </div>
    $$y=x^2-2xとy=xの交点から区間を求める$$
    $$x^2-2x=x \to x^2-2x-x =0 \to x(x-3)=0$$
    $$区間[0,3]$$
    $$$$
    回転してできた図形の断面積は
    $$A=\pi(外側の円の半径)^2 - \pi(内側の円の半径)^2$$
    $$=\pi[(4-(x^2-2x))^2 - ((4-x)^2)]$$
    図形の体積は
    $$V=\pi \int_{0}^{3}((4-x^2+2x)^2 - (x^2-8x+16)) dx$$
    $$=\pi \int_{0}^{3}(x^4-4x^3-5x^2+24x) dx$$
    $$=\pi [\frac{x^5}{5}-x^4-{5}{3}x^3+12x^2]_{0}^{3}$$
    $$=\pi(\frac{243}{5}-81-45+108 - 0)$$
    <div class="panel">
    $$=\frac{153}{5}\pi$$
    </div>
  </div>
</div>

## Disc method rotating around vertical line

<div class="row">
  <div class="col-sm-6">
    <div id="svg11"></div>
  </div>
  <div class="col-sm-6">
    <div class="panel">
      $$y=x^2-1が区間-1 \le y \le 3 で$$
      $x=-2を軸に360°回転してできる図形の体積は$$
    </div>
    回転してできた図形の断面積は
    $$\qquad y=x^2-1 \to x=\sqrt{y+1}$$
    $$A=\pi(\sqrt{y+1}+2)^2$$
    図形の体積は
    $$V=\pi \int_{-1}^{3}((\sqrt{y+1}+2)^2 dy$$
    $$=\pi \int_{-1}^{3}(y+4\sqrt{y+1}+4) dy$$
    $$=\pi [\frac{y^2}{2}+{8}{3}(y+1)^{\frac{3}{2}}+5y]_{-1}^{3}$$
    $$=\pi(\frac{9}{2}-\frac{64}{3}+15 -(\frac{1}{2}+1))$$
    <div class="panel">
    $$=\frac{136}{3}\pi$$
    </div>
  </div>
</div>

## Washer or ring method for vertical line rotation

<div class="row">
  <div class="col-sm-6">
    <div id="svg12"></div>
  </div>
  <div class="col-sm-6">
    <div class="panel">
      $$y=x^2-1が区間-1 \le y \le 3 で$$
      $x=-2を軸に360°回転してできる図形の体積は$$
    </div>
    回転してできた図形の断面積は
    $$\qquad y=x^2-1 \to x=\sqrt{y+1}$$
    $$A=\pi(\sqrt{y+1}+2)^2$$
    図形の体積は
    $$V=\pi \int_{-1}^{3}((\sqrt{y+1}+2)^2 dy$$
    $$=\pi \int_{-1}^{3}(y+4\sqrt{y+1}+4) dy$$
    $$=\pi [\frac{y^2}{2}+{8}{3}(y+1)^{\frac{3}{2}}+5y]_{-1}^{3}$$
    $$=\pi(\frac{9}{2}-\frac{64}{3}+15 -(\frac{1}{2}+1))$$
    <div class="panel">
    $$=\frac{136}{3}\pi$$
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

  var svg08 = d3.select("#svg08")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");

  var svg09 = d3.select("#svg09")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");

  var svg10 = d3.select("#svg10")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");

  var svg11 = d3.select("#svg11")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");

  var svg12 = d3.select("#svg12")
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

  var xScale06 = d3.scale.linear()
                       .domain([-0.2,2.3])
                       .range([50,450]);
  var yScale06 = d3.scale.linear()
                       .domain([4.5,-4.5])
                       .range([50,450]);       

  var xScale07 = d3.scale.linear()
                       .domain([-2.2,2.2])
                       .range([50,450]);
  var yScale07 = d3.scale.linear()
                       .domain([4.2,-0.5])
                       .range([50,450]);       

  var xScale09 = d3.scale.linear()
                       .domain([-0.2,4.2])
                       .range([50,450]);
  var yScale09 = d3.scale.linear()
                       .domain([2.2,-0.2])
                       .range([50,450]);       

  var xScale10 = d3.scale.linear()
                       .domain([-0.2,3.2])
                       .range([50,450]);
  var yScale10 = d3.scale.linear()
                       .domain([10.2,-1.2])
                       .range([50,450]);       
  var xScale11 = d3.scale.linear()
                       .domain([-6,2])
                       .range([50,450]);
  var yScale11 = d3.scale.linear()
                       .domain([3.5,-1.2])
                       .range([50,450]);       
  var xScale12 = d3.scale.linear()
                       .domain([-0.2,4.2])
                       .range([50,450]);
  var yScale12 = d3.scale.linear()
                       .domain([2,-0.2])
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

/**
  Disc method **/

  axesData06 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[2],
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

  function func061(x){
    return Math.pow(x,2);
  };
  function func062(x){
    return -Math.pow(x,2);
  };

  var pathData061=[];
  var pathData062=[];

  for (var i = -0.2; i <= 2.2; i=i+0.1) {
    pathData061.push(new Point(i,func061(i)));
    pathData062.push(new Point(i,func062(i)));
  };
  drawPath(svg06,pathData061,{"stroke":"#fff","strokeWidth":3},xScale06,yScale06); 
  drawPath(svg06,pathData062,{"stroke":"#0f0","strokeWidth":2},xScale06,yScale06); 

  lineData06 = [
    {"x1":2,"y1":func061(2),"x2":2,"y2":0,"stroke":"#f0f"},
    {"x1":2,"y1":0,"x2":2,"y2":func062(2),"stroke":"#f0f"},
    {"x1":1,"y1":func061(1),"x2":1,"y2":0,"stroke":"#f0f"},
    {"x1":1,"y1":0,"x2":1,"y2":func062(1),"stroke":"#f0f"}
  ]

  drawLine(svg06,lineData06,xScale06,yScale06); 

  // around y-axis
  axesData07 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[2],
    "yTickValues":[],
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

  drawAxes(svg07,axesData07);

  function func07(x){
    return Math.pow(x,2);
  };

  var pathData07=[];

  for (var i = -2.2; i <= 2.2; i=i+0.1) {
    pathData07.push(new Point(i,func07(i)));
  };
  drawPath(svg07,pathData07,{"stroke":"#fff","strokeWidth":3},xScale07,yScale07); 

  lineData07 = [
    {"x1":-1,"y1":func07(-1),"x2":1,"y2":func07(1),"stroke":"#f0f"},
    {"x1":-2,"y1":func07(-2),"x2":2,"y2":func07(2),"stroke":"#f0f"},
  ]

  drawLine(svg07,lineData07,xScale07,yScale07); 

  // washer method
  function func081(x){
    return Math.sqrt(x);
  };
  func082 = function func082(x){
    return x;
  };

  var pathData081=[];
  var pathData082=[];
  var areaData08=[];

  for (var i = 0; i <= 1.2; i=i+0.02) {
    pathData081.push(new Point(i,func081(i)));
    pathData082.push(new Point(i,func082(i)));
  };
  for (var i = 0; i <= 1; i=i+0.02) {
    areaData08.push(new Point(i,func081(i)));
  };

  drawArea(svg08,areaData08,func082,
    {"fillColor":"#00f","opacity":0.6},xScale01,yScale01); 

  drawPath(svg08,pathData081,{"stroke":"#0f0"},xScale01,yScale01); 
  drawPath(svg08,pathData082,{"stroke":"#fff"},xScale01,yScale01); 

  drawAxes(svg08,axesData01);

  // horizontal line

  function func091(x){
    return Math.sqrt(x);
  };
  func092 = function func092(x){
    return 1;
  };
  function func093(x){
    return -Math.sqrt(x)+2;
  };

  var pathData091=[];
  var pathData092=[];
  var pathData093=[];
  var areaData09=[];

  for (var i = 0; i <= 4.2; i=i+0.02) {
    pathData091.push(new Point(i,func091(i)));
    pathData092.push(new Point(i,func092(i)));
  };
  for (var i = 1; i <= 4; i=i+0.02) {
    areaData09.push(new Point(i,func091(i)));
    pathData093.push(new Point(i,func093(i)));
  };

  drawArea(svg09,areaData09,func092,
    {"fillColor":"#00f","opacity":0.6},xScale09,yScale09); 

  drawPath(svg09,pathData091,{"stroke":"#0f0"},xScale09,yScale09); 
  drawPath(svg09,pathData092,{"stroke":"#fff"},xScale09,yScale09); 
  drawPath(svg09,pathData093,{"stroke":"#f0f"},xScale09,yScale09); 


    axesData09 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[1,4],
    "yTickValues":[1],
    "xTickPadding":5,
    "yTickPadding":2,
    "xOrient":["bottom"],
    "yOrient":["left"],
    "stroke":"#ff0",
    "strokeWidth":1,
    "fillColor":"none",
    "xScale":xScale09,
    "yScale":yScale09
  };
  drawAxes(svg09,axesData09);

  //Washer method rotating around non-axis
  function func101(x){
    return x;
  };
  func102 = function func102(x){
    return Math.pow(x,2) - 2*x;
  };
  function func103(x){
    return -Math.pow(x,2) + 2*x + 8;
  };
  func104 =function func104(x){
    return -x + 8;
  };
  function func105(x){
    return 4;
  };

  var pathData101=[];
  var pathData102=[];
  var pathData103=[];
  var pathData104=[];
  var pathData105=[];

  var areaData101=[];
  var areaData102=[];

  for (var i = 0; i <= 3.2; i=i+0.02) {
    pathData101.push(new Point(i,func101(i)));
    pathData102.push(new Point(i,func102(i)));
    pathData105.push(new Point(i,func105(i)));
  };
  for (var i = 0; i <= 3; i=i+0.02) {
    areaData101.push(new Point(i,func101(i)));
    areaData102.push(new Point(i,func103(i)));
    pathData103.push(new Point(i,func103(i)));
    pathData104.push(new Point(i,func104(i)));
  };

  drawArea(svg10,areaData101,func102,
    {"fillColor":"#00f","opacity":0.6},xScale10,yScale10); 
  drawArea(svg10,areaData102,func104,
    {"fillColor":"#00f","opacity":0.6},xScale10,yScale10); 

  drawPath(svg10,pathData101,{"stroke":"#0f0"},xScale10,yScale10); 
  drawPath(svg10,pathData102,{"stroke":"#fff"},xScale10,yScale10); 
  drawPath(svg10,pathData103,{"stroke":"#f0f"},xScale10,yScale10); 
  drawPath(svg10,pathData104,{"stroke":"#f0f"},xScale10,yScale10); 
  drawPath(svg10,pathData105,{"stroke":"#fff"},xScale10,yScale10); 

  axesData10 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[3],
    "yTickValues":[4],
    "xTickPadding":5,
    "yTickPadding":2,
    "xOrient":["bottom"],
    "yOrient":["left"],
    "stroke":"#ff0",
    "strokeWidth":1,
    "fillColor":"none",
    "xScale":xScale10,
    "yScale":yScale10
  };
  drawAxes(svg10,axesData10);

  //Disc method rotating around vertical line
  function func111(x){
    return Math.pow(x,2) - 1;
  };
  function func112(x){
    return Math.sqrt(x+1);
  };

  var pathData111=[];
  var pathData112=[];

  for (var i = 0; i <= 2.1; i=i+0.02) {
    pathData111.push(new Point(i,func111(i)));
  };
  for (var i = -2; i <= 0; i=i+0.02) {
    pathData112.push(new Point(i-4,func111(i)));
  };

  drawPath(svg11,pathData111,{"stroke":"#0f0"},xScale11,yScale11); 
  drawPath(svg11,pathData112,{"stroke":"#f0f"},xScale11,yScale11); 

  lineData11 = [
    {"x1":-4,"y1":-1,"x2":0,"y2":-1,"stroke":"#fff"},
    {"x1":func112(3),"y1":3,"x2":func112(3)-8,"y2":3,"stroke":"#fff"},
    {"x1":-2,"y1":3.5,"x2":-2,"y2":-1.2,"stroke":"#fff"},
  ];

  drawLine(svg11,lineData11,xScale11,yScale11);

  axesData11 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[-2],
    "yTickValues":[3],
    "xTickPadding":5,
    "yTickPadding":2,
    "xOrient":["bottom"],
    "yOrient":["left"],
    "stroke":"#ff0",
    "strokeWidth":1,
    "fillColor":"none",
    "xScale":xScale11,
    "yScale":yScale11
  };
  drawAxes(svg11,axesData11);

  //Washer or ring method for vertical line rotation
  function func121(x){
    return Math.sqrt(x);
  };
  function func122(x){
    return Math.pow(x,2);
  };
  function func124(x){
    return -Math.sqrt(x,2);
  };

  var pathData121=[];
  var pathData122=[];
  var pathData123=[];
  var pathData124=[];

  for (var i = 0; i <= 1.02; i=i+0.02) {
    pathData121.push(new Point(i,func121(i)));
    pathData122.push(new Point(i,func122(i)));
    pathData124.push(new Point(i+3,-func122(i)+1));
  };
  for (var i = -1; i <= 0.02; i=i+0.02) {
    pathData123.push(new Point(i+4,func122(i)));
  };

  drawPath(svg12,pathData121,{"stroke":"#0f0"},xScale12,yScale12); 
  drawPath(svg12,pathData122,{"stroke":"#fff"},xScale12,yScale12); 
  drawPath(svg12,pathData123,{"stroke":"#f0f"},xScale12,yScale12); 
  drawPath(svg12,pathData124,{"stroke":"#f0f"},xScale12,yScale12); 

  lineData12 = [
    {"x1":-4,"y1":-1,"x2":0,"y2":-1,"stroke":"#fff"},
    {"x1":func122(3),"y1":3,"x2":func122(3)-8,"y2":3,"stroke":"#fff"},
    {"x1":-2,"y1":3.5,"x2":-2,"y2":-1.2,"stroke":"#fff"},
  ];

  drawLine(svg12,lineData12,xScale12,yScale12);

  axesData12 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[2],
    "yTickValues":[1],
    "xTickPadding":5,
    "yTickPadding":2,
    "xOrient":["bottom"],
    "yOrient":["left"],
    "stroke":"#ff0",
    "strokeWidth":1,
    "fillColor":"none",
    "xScale":xScale12,
    "yScale":yScale12
  };
  drawAxes(svg12,axesData12);

</script>
