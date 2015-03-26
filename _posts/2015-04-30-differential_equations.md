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

<h3>
<div class="panel">
$$\frac{dy}{dx}=\frac{-x}{ye^{x^2}}$$
この答えとなる関数は(0,1)を通ります、その関数を求めよ
</div>
左辺にyを、右辺にxを集めます(2つに分けることからseparable)
$$y \cdot dy = -x e^{-x^2}\cdot dx$$
両辺を積分します
$$\int y \, dy = \int -x e^{-x^2}\, dx$$
$$\frac{y^2}{2} + C_{1}=\frac{1}{2} \int -2xe^{-x^2}\, dx$$
$$ \frac{y^2}{2} + C_{1}=\frac{1}{2}e^{-x^2}+C_{2}$$
両辺から\(C_{1}\)を引きます、右辺の定数は\(C_{2}-C_{1}=C\)とおけます
$$\frac{y^2}{2}=\frac{1}{2}e^{-x^2}+C$$
通過点(0,1)を代入する
$$\frac{1}{2}=\frac{1}{2}+C \to C=0$$
$$\frac{y^2}{2}=\frac{1}{2}e^{-x^2}$$
$$y^2=e^{-x^2}$$
両辺の平方根をとる
$$y=\pm \sqrt{e^{-x^2}}$$
yはプラスなので
$$y=e^{\frac{-x^2}{2}}$$
</h3>
<br>
<h3>
例
<div class="panel">
$$\frac{dy}{dx}=2y^2$$
\((1,-1)\)を通る関数を求める
</div>
$$\frac{dy}{2y^2}=dx$$
$$\int \frac{1}{2}y^{-2}\,dy=\int\,dx$$
$$-\frac{1}{2}y^{-1}=x+C$$
$$\frac{1}{y}=-2x+C$$
$$y=\frac{1}{c-2x}$$
$$-1=\frac{1}{c-2}$$
$$2-c=1$$
$$c=1$$
$$y=\frac{1}{-2x+1}$$ 
</h3>

--------

# Modeling with differential equations

## Modeling population with simple differential equation
<h3>
<div class="panel">
人口に関してモデル化してみます<br>
変数を定義します<br>
P:人口　　t:時間（日数）<br>
人口の変化率は
$$\frac{dP}{dt}=kP$$
この一般解を求めよ
</div>
$$\frac{1}{P}dP=kdt$$
$$\int \frac{1}{P}dP=\int kdt$$
$$\ln |P|=kt+C_{1}$$
$$|P|=e^{kt+C_{1}}$$
$$|P|=e^{kt}e^{c_{1}}$$
$$e^{c_{1}}は定数となりますからCとします$$
$$|P|=Ce^{kt}$$
Pは人口で正の数ですから
$$P=Ce^{kt}$$
</h3>

## Particular solution given initial conditions for population

<h3>
<div class="panel">
初期情報を与えます
$$t=0 \qquad P=100$$
$$t=50 \qquad P=200$$
これでCとkは求められるでしょうか
</div>
$$100=Ce^{0k}$$
$$200=Ce^{50k}$$
$$C=100$$
$$200=100e^{50k} \to 2=e^{50k} \to \ln\,2=50k \to k= \frac{\ln 2}{50}$$
$$P(t)=100e^{(\frac{\ln2}{50})t}$$
</h3>

## Newton's law of Cooling

<h3>
<div class="panel">
物体の温度が周囲の温度によってどう変化していくかをモデル化します
$$T:物体の温度 \qquad T_{a}:周囲の温度(ambient temperature)$$
温度の時間による変化を
$$\frac{dT}{dt}=k(T-T_{a})$$
$$k>0\quadで、T \ge t_{a} \quad のとき\quad \frac{dT}{dt}\le 0$$
なので
$$\frac{dT}{dt}=-k(T-T_{a})$$
この一般解を求めます
</div>
$$\frac{1}{T-T_{a}}\,dT = -k\,dt$$
両辺を積分します
$$\int \frac{1}{T-T_{a}}\,dT = \int -k\,dt$$
$$\ln |T-T_{a}|=-kt+C_{1}$$
$$|T-T_{a}|=e^{-kt+C_{1}} \to |T-T_{a}|=e^{-kt}e^{C_{1}}$$
$$|T-T_{a}|=Ce^{-kt}$$
$$T \ge T_{a} \qquad T(t)=Ce^{-kt}+T_{a}$$ 
$$T \lt T_{a} \qquad T(t)=T_{a}-Ce^{-kt}$$ 
</h3>

---------

# Logistic differential equation and function

## Modeling population as an exponential function



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
