---
title: Trigonometry
layout: post
postTitle: Graphs of trig functions
categories: trig
---

## Midline, amplitude and period of a function

<div class="row">
  <div class="col-sm-6">
    <div id="svg01"></div>
  </div>
  <div class="col-sm-6">
  </div>
</div>

--------

## Finding arc length from radian angle measure

<div class="row">
  <div class="col-sm-5">
    <div id="svg02"></div>
  </div>
  <div class="col-sm-7">
  </div>
</div>

--------

## Ratio between concentric arcs

<div class="row">
  <div class="col-sm-5">
    <div id="svg03"></div>
  </div>
  <div class="col-sm-7">
  </div>
</div>

--------

## Unit circle

<div class="row">
  <div class="col-sm-5">
    <div id="svg04"></div>
  </div>
  <div class="col-sm-7">
  </div>
</div>

--------

# Trig functions of special angles

## Solving triangle in unit circle

<div class="row">
  <div class="col-sm-5">
    <div id="svg05"></div>
  </div>
  <div class="col-sm-7">
  </div>
</div>

---------

## Finding trig functions of special angles

<div class="row">
  <div class="col-sm-5">
    <div id="svg06"></div>
  </div>
  <div class="col-sm-7">
    $$三角形の２辺は長さが２で同じなので、この三角形は２等辺三角形である$$
    $$したがって$$
    $$\beta=\frac{\pi}{3}$$
    $$\alpha+\frac{\pi}{3}+\frac{\pi}{2}=\pi
    \rightarrow \alpha = \pi-\frac{\pi}{3}-\frac{\pi}{2}
    = \frac{6\pi-2\pi-3\pi}{6}=\frac{\pi}{6}$$
    $$この三角形の３つの内角はすべて\frac{\pi}{3}であるので、この三角形は正三角形である$$
    $$底辺に対する頂点から降ろされた垂線は底辺を２等分するので$$
    $$b=1$$
    $$a^2+b^2=2^2 \rightarrow a^2+1^2=4$$
    $$a^2=4-1=3$$
    $$a=\sqrt{3}$$
    <table class="table">
      <tr>
        <th>$$sin\frac{\pi}{3}$$</th>
        <th>$$cos\frac{\pi}{3}$$</th>
        <th>$$tan\frac{\pi}{3}$$</th>
      </tr>
      <tr>
        <td>$$\frac{\sqrt{3}}{2}$$</td>
        <td>$$\frac{1}{2}$$</td>
        <td>$$\sqrt{3}$$</td>
      </tr>
      <tr>
        <th>$$sin\frac{\pi}{6}$$</th>
        <th>$$cos\frac{\pi}{6}$$</th>
        <th>$$tan\frac{\pi}{6}$$</th>
      <tr>
        <td>$$\frac{1}{2}$$</td>
        <td>$$\frac{\sqrt{3}}{2}$$</td>
        <td>$$\frac{1}{\sqrt{3}}=\frac{\sqrt{3}}{3}$$</td>
      </tr>
      </tr>
    </table>
  </div>
</div>

--------

# Invrse trig functions

## $$\arcsin$$

<div class="row">
  <div class="col-sm-5">
    <div id="svg07"></div>
  </div>
  <div class="col-sm-7">
  $$sin\frac{\pi}{4}=\frac{\sqrt{2}}{2}$$
  $$では、sin\theta = \frac{\sqrt{2}}{2} のとき、\theta の角度は?$$
  $$arcsin\frac{\sqrt{2}}{2}=\theta \quad
  または \quad
  sin^{-1}\frac{\sqrt{2}}{2}=\theta$$
  $$という関数を使います$$
  $$ただし$$
  $$-1 \le y \le 1 \quad 
  で \quad 
  -\frac{\pi}{2} \le \theta \le \frac{\pi}{2}
  \quad という制限を設けます$$ 
  $$arcsin\frac{\sqrt{2}}{2}=\frac{\pi}{4}$$
  $$$$
  $$arcsin\frac{-\sqrt{3}}{2}=? \to -\frac{\pi}{3}$$
  $$$$
  $$\arcsin(\sin\theta)=\arcsin(y)=\theta$$
  $$\sin(\arcsin y)=\sin \theta = y$$
  </div>
</div>

--------

## $$\arccos$$

<div class="row">
  <div class="col-sm-5">
    <div id="svg08"></div>
  </div>
  <div class="col-sm-7">
  $$\cos\theta = x \to 
  \arccos x= \theta ,\quad  \cos^{-1}x= \theta$$
  $$$$
  $$\arccos (-\frac{1}{2})=\theta? \to \cos\theta = (-\frac{1}{2})
  \to x = -\frac{1}{2}$$
  $$Domain:-1 \le x \le 1$$
  $$Range \quad restrict:0 \le \theta \le \pi$$
  $$\alpha = \arccos (\frac{1}{2}) = \frac{\pi}{3}$$
  $$\theta = \pi - \alpha = \pi - \frac{\pi}{3} = \frac{2\pi}{3}$$
  $$$$
  $$\arccos(\cos\theta)=\arccos(x)=\theta$$
  $$\cos(\arccos x)=\cos \theta = x$$
  </div>
</div>

-------

## $$\arctan$$

<div class="row">
  <div class="col-sm-5">
    <div id="svg09"></div>
  </div>
  <div class="col-sm-7">
  $$\tan \theta = x \to \arctan x = \theta, \quad \tan^{-1}x=\theta$$
  $$\tan \theta = \frac{\sin \theta}{\cos \theta} 
  \to \frac{y-value}{x-value} \to slope(傾き)$$
  $$\arctan(-1)=\theta?$$
  $$\tan \theta = -1 \to 傾きが　-1 \to 長さx = 長さy$$
  $$Domain:-\infty \lt y \lt \infty$$
  $$Range \quad restrict:-\frac{\pi}{2} \lt \theta \lt \frac{\pi}{2}$$
  $$\theta = -45^\circ = -\frac{\pi}{4}rad$$

  </div>
</div>

-------

## Restricting domain of trig function to make invertible

<div class="row">
  <div class="col-sm-5">
    <div id="svg10"></div>
  </div>
  <div class="col-sm-7">
  $$関数fは、domainの要素を元にrangeの要素を示します$$
  $$逆関数f^{-1}は、rangeの要素を元にdomainの要素を示します$$
  $$上側のrangeの要素は１つのdomainの要素から指し示されています$$
  $$この場合、逆関数f^{-1}はdomainの要素を特定できます$$
  $$一方、下側のrangeの要素は２つのdomain要素から指し示されています$$
  $$こちらの場合、逆関数f^{-1}はdomainの要素を特定できません$$
  $$そのため、domainに制限を与えて、$$
  $$domainの要素とrangeの要素が１対１となるようにします$$
  </div>
</div>

<div class="row">
  <div class="col-sm-5">
    <div id="svg11"></div>
  </div>
  <div class="col-sm-7">
    $$グラフの　値0.5の青線は赤い曲線と３か所で交わっています。$$
    $$赤い曲線を表す関数f(x)には、f(x)=0.5となるxが複数存在するということです。$$
    $$この場合f(x)の逆関数f^{-1}(0.5)は、xを特定できません。$$
    $$そこで、xのとる値ををピンクの矢印の範囲に限定することで$$
    $$逆関数f^{-1}(0.5)は値を特定することができます$$
  </div>
</div>

<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_SVG"></script>
<script src="http://d3js.org/d3.v3.min.js" charset="utf-8"></script>
<script src="{{site.url}}/js/d3draws.js" charset="utf-8"></script>

<script>

  var height = 500;
  var width = 500;
  

/**  */
  var svg01 = d3.select("#svg01")
                .append("svg")
                .attr("height",height)
                .attr("width",width)
                .style("background","#000");

  var xScale01 = d3.scale.linear()
                       .domain([-540,540])
                       .range([20,480]);
  
  var yScale01 = d3.scale.linear()
                       .domain([5,-3])
                       .range([20,480]);       

  // 軸
  axesData01 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[],
    "yTickValues":[-3,-2.5,-2,-1,-0.5,0.5,1,1.5,2,2.5,3,3.5,4,4.5,5],
    "stroke":"#ff0",
    "strokeWidth":1,
    "xScale":xScale01,
    "yScale":yScale01
  };
  
  drawAxes(svg01,axesData01);

 
  // graph
  var graphData01 = [];   

  for (var i=-630;i<=450;i++){
    graphData01.push(new Point(i+90,Math.cos(aDegree*i)*3+1));
  };
  drawPath(svg01,graphData01,"#f00",2,"none",xScale01,yScale01);
 
  var gridData01 = 
  {
    "xGrid":true,
    "yGrid":true,
    "xStep":90,
    "yStep":1,
    "stroke":"#0f0",
    "strokeWidth":1,
    "opacity":0.3,
    "xScale":xScale01,
    "yScale":yScale01
    };
  drawGrid(svg01,gridData01);

  // line
  var lineData01 = [
    {
      "x1":-540,
      "y1":1,
      "x2":540,
      "y2":1,
      "stroke":"lime",
      "strokeWidth":4
    }
   ,{
      "x1":90,
      "y1":4,
      "x2":90,
      "y2":1,
      "stroke":"#f0f",
      "strokeWidth":4
    }
  ];
  drawLine(svg01,lineData01,xScale01,yScale01);

  // vector
  var vecData01 = [
    {
      "x1":90,
      "y1":4.2,
      "x2":450,
      "y2":4.2,
      "stroke":"#ff0",
      "strokeWidth":3
    }
  ];
  drawVectorW(svg01,vecData01,xScale01,yScale01);

/**  Finding arc length from .... */
  var svg02 = d3.select("#svg02")
                .append("svg")
                .attr("height",height)
                .attr("width",width)
                .style("background","#000");

  var xScale02 = d3.scale.linear()
                       .domain([-2,6])
                       .range([50,350]);
  
  var yScale02 = d3.scale.linear()
                       .domain([8,0])
                       .range([50,350]);                       

</script>
