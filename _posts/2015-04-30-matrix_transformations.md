---
title: Linear algebraebra
layout: post
date: 2015-04-30 22:00:00
postTitle: Matrix transformations
categories: linear_algebra
---

-------

# Functions and linear transformations

-------

## A more formal understanding of functions

<div class="row">
  <div class="col-sm-6">
    <div id="svg01"></div>
  </div>
  <div class="col-sm-6">
   <h3>
    関数(function)<br>
   １つの集合(X)ともう１つの集合(Y)とを関連づけること
   $$f:X \to Y$$
   集合Xの値が、集合Yの値と関連しているということ<br>
   このことをマップという<br>
   見慣れた関数定義で\(f(x)=x^2\)があります<br>
   今回の定義では\(f:x \to x-2\)<br>
   この関数は実数値を与えると実数値を示します
   $$f:R \to R$$
   関連元の集合をdomain、マッピングされる集合をcodomain（余域）という<br>
   Range : codomain<br>
   レンジは余域の部分集合であり、関数が実際にマッピングする値の集合<br>

    </h3>
  </div>
</div>
<div class="row">
  <div class="col-sm-5">
    <h3>
   例
   $$g:R^2 \to R$$
   $$g(x_{1},x_{2})=2$$
   別の書き方をすると
   $$g:x_{1},x_{2} \to 2$$
   $$Domain:\Bbb{R}^2$$
   $$Codomain:\Bbb{R}$$
   $$Range:2$$
    </h3>
  </div>
  <div class="col-sm-7">
    <h3>
   $$別の例$$
   $$h:\Bbb{R}^2 \to \Bbb{R}^3$$
   高次元へのマッピングです
   $$h(x_{1},x_{2})=(x_{1}+x_{2},x_{2}-x_{1},x_{2}x_{1})$$
   $$$$
   $$f:\Bbb{R}^2 \to \Bbb{R} $$
   $$\quad \text{real valued function / scalor valued function}$$
   $$f:\Bbb{R}^2 \to \Bbb{R}^3$$ 
   $$\quad \text{vector valued function}　$$
   $$\quad \text{１次元より大きいcodomainへ関連付ける関数}$$
    </h3>
  </div>
</div>

## Vector transformations

<div class="row">
  <div class="col-sm-6">
    <div id="svg02"></div>
  </div>
  <div class="col-sm-6">
   <h3>
   </h3>
  </div>
</div>

## Linear transformations

<div class="row">
  <div class="col-sm-6">
    <div id="svg03"></div>
  </div>
  <div class="col-sm-6">
   <h3>
   </h3>
  </div>
</div>

<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_SVG"></script>
<script src="http://d3js.org/d3.v3.min.js" charset="utf-8"></script>
<script src="{{site.url}}/js/d3draws.js" charset="utf-8"></script>
<script src="{{site.url}}/js/jquery.js" charset="utf-8"></script>

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
                       .domain([0,500])
                       .range([50,450]);
  var yScale01 = d3.scale.linear()
                       .domain([500,0])
                       .range([50,450]);       


ellipseData01 = [
  {"cx":100,"cy":250,"rx":70,"ry":120,"stroke":"#fff"},
  {"cx":400,"cy":280,"rx":60,"ry":100,"stroke":"#f00"},
];

drawEllipse(svg01,ellipseData01,xScale01,yScale01);

circleData01 = [
  {"cx":140,"cy":200,"r":5,"stroke":"#fff","fillColor":"#fff"},
  {"cx":380,"cy":210,"r":5,"stroke":"#fff","fillColor":"#fff"},
  {"cx":120,"cy":330,"r":5,"stroke":"#fff","fillColor":"#fff"},
  {"cx":410,"cy":340,"r":5,"stroke":"#fff","fillColor":"#fff"},
];

drawCircle(svg01,circleData01,xScale01,yScale01);

var vecData01 = [
{"x1":140,"y1":200,"x2":380,"y2":210,"stroke":"#0ff","strokeWidth":3},
{"x1":120,"y1":330,"x2":410,"y2":340,"stroke":"#0ff","strokeWidth":3}
];    

drawVectorB(svg01,vecData01,xScale01,yScale01);

var textData01 = [
{"x":90,"y":420,"text":"X",
 "stroke":"#ffF","fontSize":22,"strokeWidth":2,
 "fontFamily":"cursive"},
{"x":390,"y":420,"text":"Y",
 "stroke":"#ffF","fontSize":22,"strokeWidth":2,
 "fontFamily":"cursive"},
{"x":250,"y":180,"text":"map",
 "stroke":"#ffF","fontSize":20,"strokeWidth":2,
 "fontFamily":"cursive"},
{"x":100,"y":70,"text":"domain","anchor":"middle",
 "stroke":"#ffF","fontSize":24,"strokeWidth":2,
 "fontFamily":"cursive"},
{"x":400,"y":130,"text":"codomain","anchor":"middle",
 "stroke":"#ffF","fontSize":24,"strokeWidth":2,
 "fontFamily":"cursive"},
];
drawText(svg01,textData01,xScale01,yScale01);

// Vector transformation
drawEllipse(svg02,ellipseData01,xScale01,yScale01);

circleData01 = [
  {"cx":100,"cy":250,"r":5,"stroke":"#fff","fillColor":"#fff"},
  {"cx":400,"cy":280,"r":5,"stroke":"#fff","fillColor":"#fff"},
];

drawCircle(svg02,circleData01,xScale01,yScale01);

var vecData01 = [
{"x1":100,"y1":250,"x2":400,"y2":280,"stroke":"#0ff","strokeWidth":3},
];    

drawVectorB(svg02,vecData01,xScale01,yScale01);

var foData02 = [
{"x":80,"y":450,"text":"$$\\Bbb{R}^n$$",
 "stroke":"#ffF","fontSize":"24px","strokeWidth":2},
{"x":380,"y":450,"text":"$$\\Bbb{R}^m$$",
 "stroke":"#ffF","fontSize":"24px","strokeWidth":2},
{"x":250,"y":360,"text":"f",
 "stroke":"#ffF","fontSize":"24px","strokeWidth":2},
{"x":60,"y":355,"text":"$$\\vec{x}$$","anchor":"middle",
 "stroke":"#ffF","fontSize":"24px","strokeWidth":2,
 "fontFamily":"cursive"},
{"x":430,"y":380,"text":"$$\\vec{y}$$","anchor":"middle",
 "stroke":"#ffF","fontSize":"24px","strokeWidth":2,
 "fontFamily":"cursive"},
];
drawMathjax(svg02,foData02,xScale01,yScale01);


</script>
