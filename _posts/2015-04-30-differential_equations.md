---
title: Differential Equations
layout: post
date: 2015-04-30 23:00:00
postTitle: First order differential equations
categories: differential_equations
---

# Intro to differential equations
-------

## Differential equation introduction 

Differential equations (微分方程式)

ある出来事を、モデル化したりシミュレートするのに便利

どのようなものなのか

例
$$y''+2y' = 3y$$
$$f''(x)+2f'(x)=3f(x)$$
$$\frac{d^2y}{dx^2}+2\frac{dy}{dx}=3y$$
３つとも同じことを表しています

そしてこの答えは、関数、または関数の組合せ、関数のクラスとなります

Algebraic equations(代数方程式)では
$$x^2+3x+2=0$$
この答えは数字または数字の組合せとなります
$$x=-1 \quad まては \quad x=-2$$

微分方程式では、答えは複数ある場合もあります

答え1
$$y_{1}(x)=e^{-3x}$$
$$y'_{1}=-3e^{-3x}$$
$$y''_{1}=9e^{-3x}$$
$$y''+2y' = 3y \to 9e^{-3x}-6e^{-3x}=3e^{-3x}$$

答え2
$$y_{2}(x)=e^{x}$$
$$y'_{2}(x)=e^{x}$$
$$y''_{2}(x)=e^{x}$$
$$y''+2y' = 3y \to e^{x}+2e^{x}=3e^{x}$$

$$y_{1}とy_{2}どちらもこの微分方程式の答えです$$ 

## Finding particular linear solution to differential equation

$$\frac{dy}{dx}=-2x+3y-5$$
があります、ヒントとして答えは
$$y=mx+b$$
という直線の式とします、まずこの式を微分します
$$\frac{dy}{dx}=m \qquad 定数$$
$$m=-2x+3(mx+b)-5$$
$$m=-2x+3mx+3b-5$$
$$m=(3m-2)x+3b-5$$
mは定数なので
$$3m-2=0 \quad m=3b-5$$
$$m=\frac{2}{3}$$
$$\frac{2}{3}=3b-5$$
$$b=\frac{17}{9}$$
$$y=\frac{2}{3}+\frac{17}{9}$$ 

## Creating a slope field



<div class="row">
  <div class="col-sm-6">
    <h3>
    $$\frac{dy}{dx}=\frac{-x}{y}$$
$$
\begin{array}{r|r|r}
x & y & \frac{dy}{dx} \\
\hline
0 & 1 & 0  \\
1 & 1 & -1  \\
1 & 0 & undefined \\
1 & -1 & 1 \\
-1 & 1 & 1 \\
-1 & -1 & -1 \\  
\end{array}
$$
これをもとに、右の平面に傾きの線を描きます
<br>
これらが連なったものをスロープフィールドといいます
    </h3>
  </div>
  <div class="col-sm-6">
    <div id="svg01"></div>
  </div>
</div>

--------

# Separable equations

## Separable differential equations introduction



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
                       .domain([-2.5,2.5])
                       .range([50,450]);
  var yScale01 = d3.scale.linear()
                       .domain([2.5,-2.5])
                       .range([50,450]);       

  // 軸
  axesData01 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[-2,-1,1,2],
    "yTickValues":[-2,-1,1,2],
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
  function func011(x,m,b){
    return m*(x+0.2)+b;
  };
  function func012(x,m,b){
    return m*(x-0.2)+b;
  }
  ;
  var lineData01 = [
{"x1":-.2,"y1":1,
 "x2":0.2,"y2":1,"stroke":"#0f0","strokeWidth":4},
{"x1":0.8,"y1":func012(1,-1,2),
 "x2":1.2,"y2":func011(1,-1,2),"stroke":"#0f0","strokeWidth":4},
{"x1":0.8,"y1":func012(1,1,-2),
 "x2":1.2,"y2":func011(1,1,-2),"stroke":"#0f0","strokeWidth":4},
{"x1":-1.2,"y1":func012(-1,1,2),
 "x2":-0.8,"y2":func011(-1,1,2),"stroke":"#0f0","strokeWidth":4},
{"x1":-1.2,"y1":func012(-1,-1,-2),
 "x2":-0.8,"y2":func011(-1,-1,-2),"stroke":"#0f0","strokeWidth":4},

{"x1":1.8,"y1":func012(2,-1,4), 
 "x2":2.2,"y2":func011(2,-1,4),"stroke":"#f0f","strokeWidth":4},
{"x1":1.8,"y1":func012(2,1,-4),
 "x2":2.2,"y2":func011(2,1,-4),"stroke":"#f0f","strokeWidth":4},
{"x1":-2.2,"y1":func012(-2,1,4),
 "x2":-1.8,"y2":func011(-2,1,4),"stroke":"#f0f","strokeWidth":4},
{"x1":-2.2,"y1":func012(-2,-1,-4),
 "x2":-1.8,"y2":func011(-2,-1,-4),"stroke":"#f0f","strokeWidth":4},
];    
drawLine(svg01,lineData01,xScale01,yScale01);

foData01 = [
    {"x":-0.5,
    "y":3.5,
    "text":"$$y$$",
    "fontSize":"18px"},
    {"x":2.7,
    "y":0.5,
    "text":"$$x$$",
    "fontSize":"18px"},
  ];

  drawMathjax(svg01,foData01,xScale01,yScale01);

</script>
