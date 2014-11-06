---
title: Trigonometry
layout: post
postTitle: Unit circle definition of trig functions
categories: trig
---

-------
## 角度の表し方　度数（degrees）と弧度（radians）

<div class="row">
  <div class="col-sm-5">
    <div id="svg00"></div>
  </div>
  <div class="col-sm-7">
    <h3>
    １　radianとは、半径rの円で、円弧の長さが r となる角度。
    </h3>
    $$\theta = 1(radian)$$
  </div>
</div>
<div class="row">
  <div class="col-sm-5">
    <div id="svg01"></div>
  </div>
  <div class="col-sm-7">
   <table class="table">
      <tr>
        <th>angle</th><th>degrees</th><th>radians</th>
      </tr>
      <tr>
        <td>$$a$$</td><td>$$360$$</td><td>$$\quad2\pi$$</td>
      </tr>
      <tr>
        <td>$$b$$</td><td>$$180$$</td><td>$$\quad\pi$$</td>
      </tr>
      <tr>
        <td>$$c$$</td><td>$$ 90$$</td><td>$$\quad \frac{\pi}{2}$$</td>
      </tr>
      <tr>
        <td></td><td>$$\quad 0$$</td><td>$$\quad 0$$</td>
      </tr>
      <tr>
        <td>$$d$$</td><td>$$-90$$</td><td>$$-\frac{\pi}{2}$$</td>
      </tr>
    </table>
    弧度と度数の変換
    $$1°=\frac{\pi}{180}$$
    $$1_{(rad)}=\frac{180}{\pi}$$
    <h3 class="text-gold">
    $$radians = degrees \times \frac{\pi}{180} $$
    </h3>
  </div>
</div>

--------

## Finding arc length from radian angle measure

<div class="row">
  <div class="col-sm-5">
    <div id="svg02"></div>
  </div>
  <div class="col-sm-7">
    <p>
      半径１単位の円で、0.4(rad)の角度が作る円弧の長さは0.4 radii である。
    </p>
    <p>
      半径５単位の円で、角度 0.4(rad)が作る円弧の長さは
    </p>
    $$5\frac{units}{radii} \times 0.4 radii = 2 \quad units$$
    となる。   
  </div>
</div>

--------

## Ratio between concentric arcs

<div class="row">
  <div class="col-sm-5">
    <div id="svg03"></div>
  </div>
  <div class="col-sm-7">
    x radians の円弧が２つあり<br>
    小さいほうの円弧の半径は　5<br>
    大きいほうの円弧の半径は　9<br>
    この時
    $$\stackrel{\frown}{AB}の長さと\stackrel{\frown}{CD}の長さの比率は$$
    $$\frac{\stackrel{\frown}{CD}}{\stackrel{\frown}{AB}}=\frac{5}{9}$$
    ここで
    $$\stackrel{\frown}{CD}の長さを\frac{25}{8}$$
    だとすると
    $$5x=\frac{25}{8}$$
    $$x=\frac{5}{8}\quad radians$$
    となります。したがって
    $$\stackrel{\frown}{AB}=9 \times \frac{5}{8} = \frac{45}{8}$$
    です。 
  </div>
</div>

--------

## Unit circle

<div class="row">
  <div class="col-sm-5">
    <div id="svg04"></div>
  </div>
  <div class="col-sm-7">
    <p>
      Unit circle(単位円)は、半径が　１　の円です。
    </p>
    $$cos\theta = \frac{a}{1}= a$$
    $$sin\theta = \frac{b}{1}= b$$
    <div class="panel">
      <h3>$$a=cos\theta\cdots(x座標)$$</h3>
      <h3>$$b=sin\theta\cdots(y座標)$$</h3>
    </div>
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
    $$\angle BAD = \frac{\pi}{4} \quad radiansです$$
    $$\angle ABD = ?$$
    $$三角形の内角の和は 180^\circなので$$　
    $$\angle ABD + \frac{\pi}{4} + \frac{\pi}{2} = \pi$$
    $$\angle ABD　= \pi - \frac{\pi}{4}-\frac{\pi}{2}
    = \frac{4\pi-\pi-2\pi}{4}=\frac{\pi}{4}$$
    $$２つの角が同じ三角形は２等辺三角形なので$$
    $$x=y$$
    $$x^2+y^2=1 \rightarrow x^2+x^2=1$$
    $$2x^2=1$$
    $$x^2=\frac{1}{2}$$
    $$x = \frac{1}{\sqrt{2}}=\frac{1}{\sqrt{2}}\cdot\frac{\sqrt{2}}{\sqrt{2}}
    =\frac{\sqrt{2}}{2}$$
    $$y=\frac{\sqrt{2}}{2}$$
    $$sin\frac{\pi}{4}=\frac{y}{1}=\frac{\sqrt{2}}{2}$$
    $$cos\frac{\pi}{4}=\frac{x}{1}=\frac{\sqrt{2}}{2}$$
    $$tan\frac{\pi}{4}=\frac{y}{x}
    =\frac{\frac{\sqrt{2}}{2}}{\frac{\sqrt{2}}{2}}=1$$
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

  var height = 400;
  var width = 400;
  

/**  */
  var svg00 = d3.select("#svg00")
                .append("svg")
                .attr("height",height)
                .attr("width",width)
                .style("background","#000");

  var svg01 = d3.select("#svg01")
                .append("svg")
                .attr("height",height)
                .attr("width",width)
                .style("background","#000");

  var xScale01 = d3.scale.linear()
                       .domain([-1.1,1.1])
                       .range([50,350]);
  
  var yScale01 = d3.scale.linear()
                       .domain([1.1,-1.1])
                       .range([50,350]);       

  // 軸
  axesData01 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[],
    "yTickValues":[],
    "stroke":"#ff0",
    "strokeWidth":1,
    "xScale":xScale01,
    "yScale":yScale01
  };
  
  drawAxes(svg00,axesData01);
  drawAxes(svg01,axesData01);

  // circle
  var circleData01 = [
    {"cx":0,"cy":0,"r":135,"stroke":"#fff","strokeWidth":4,"fillColor":"none"}
  ];   

  drawCircle(svg00,circleData01,xScale01,yScale01);
  drawCircle(svg01,circleData01,xScale01,yScale01);

  // Arc
  var arcData00 = [
    {
      "startPos":90,
      "endPos":135/pi,
      "innerRadius":0,
      "outerRadius":135,
      "stroke":"#0f0",
      "strokeWidth":4,
      "fillColor":"none"
    }
   ,{
      "startPos":90,
      "endPos":135/pi,
      "innerRadius":30,
      "outerRadius":30,
      "stroke":"#f00",
      "strokeWidth":2,
      "fillColor":"none"
    }
  ];
  var arcData01 = [
    {
      "startPos":0,
      "endPos":90,
      "innerRadius":90,
      "outerRadius":90,
      "stroke":"#0f0"
    },
    {
      "startPos":-90,
      "endPos":90,
      "innerRadius":60,
      "outerRadius":60,
      "stroke":"#ff0"
    },
    {
      "startPos":0,
      "endPos":360,
      "innerRadius":30,
      "outerRadius":30,
      "stroke":"#f00"
    },
    {
      "startPos":90,
      "endPos":180,
      "innerRadius":75,
      "outerRadius":75,
      "stroke":"#ccc"
    }

  ];
  drawArc(svg00,arcData00,xScale01,yScale01);
  drawArc(svg01,arcData01,xScale01,yScale01);

  // 矢印
  var vecbData01 = [
    {
      "x1":0.01,
      "y1":0.66,
      "x2":0,
      "y2":0.66,
      "stroke":"#0f0"
    },
    {
      "x1":-0.44,
      "y1":0.01,
      "x2":-0.44,
      "y2":0,
      "stroke":"#ff0"
    },
    {
      "x1":0.22,
      "y1":-0.01,
      "x2":0.22,
      "y2":0,
      "stroke":"#f00"
    },
    {
      "x1":0.01,
      "y1":-0.55,
      "x2":0,
      "y2":-0.55,
      "stroke":"#ccc"
    }
  ];
  drawVectorB(svg01,vecbData01,xScale01,yScale01);

  // text   
  var textData00 = [
    {"x":0.5,
    "y":-0.25,
    "text":"r",
    "stroke":"#fff",
    "fontFamily":"メイリオ",
    "fontSize":18},
    {"x":1,
    "y":0.4,
    "text":"r",
    "stroke":"#fff",
    "fontFamily":"メイリオ",
    "fontSize":18},
    {"x":0.25,
    "y":0.1,
    "text":"Θ",
    "stroke":"#f00",
    "fontFamily":"メイリオ",
    "fontSize":18}

      ];
  var textData01 = [
    {"x":-0.25,
    "y":-0.25,
    "text":"a",
    "stroke":"#f00",
    "fontFamily":"メイリオ",
    "fontSize":18},
    {"x":-0.4,
    "y":0.4,
    "text":"b",
    "stroke":"#ff0",
    "fontFamily":"メイリオ",
    "fontSize":18},
    {"x":0.5,
    "y":0.5,
    "text":"c",
    "stroke":"#0f0",
    "fontFamily":"メイリオ",
    "fontSize":18},
    {"x":0.45,
    "y":-0.5,
    "text":"d",
    "fontFamily":"メイリオ",
    "stroke":"#ccc",
    "fontSize":18}
      ];

  drawText(svg00,textData00,xScale01,yScale01);
  drawText(svg01,textData01,xScale01,yScale01);
 
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
  var arcData02 = [
    {
      "startPos":-20,
      "endPos":60,
      "innerRadius":300,
      "outerRadius":300,
      "stroke":"#ccc"
    },
    {
      "startPos":20,
      "endPos":0.4*300/pi,
      "innerRadius":0,
      "outerRadius":300,
      "stroke":"#ff0",
      "fillColor":"none"
    },
    {
      "startPos":20,
      "endPos":0.4*300/pi,
      "innerRadius":50,
      "outerRadius":50,
      "stroke":"#f00",
      "fillColor":"none"
    }
  ];
  var foData02 = [
    {
      "x":0.8,
      "y":5,
      "text":"$$5$$"
    },
    {
      "x":0.8,
      "y":3.5,
      "text":"$$0.4$$"
    },
    {
      "x":4,
      "y":9,
      "text":"$$2=5 \\times 0.4$$"
    },
    {
      "x":0,
      "y":1,
      "text":"$$P$$"
    },
    {
      "x":2.5,
      "y":9.5,
      "text":"$$A$$"
    },
    {
      "x":5,
      "y":8,
      "text":"$$B$$"
    },
  ];
  drawArc(svg02,arcData02,xScale02,yScale02);
  drawMathjax(svg02,foData02,xScale02,yScale02);

/**  Ratio between concentric arcs */
  var svg03 = d3.select("#svg03")
                .append("svg")
                .attr("height",height)
                .attr("width",width)
                .style("background","#000");

  var xScale03 = d3.scale.linear()
                       .domain([-1,7])
                       .range([50,350]);
  
  var yScale03 = d3.scale.linear()
                       .domain([8,0])
                       .range([50,350]);                       
  var arcData03 = [
    {
      "startPos":0,
      "endPos":70,
      "innerRadius":300,
      "outerRadius":300,
      "stroke":"#ccc"
    },
    {
      "startPos":10,
      "endPos":0.6*300/pi,
      "innerRadius":0,
      "outerRadius":300,
      "stroke":"#ff0",
      "fillColor":"none"
    },
    {
      "startPos":10,
      "endPos":0.6*300/pi,
      "innerRadius":50,
      "outerRadius":50,
      "stroke":"#f00",
      "fillColor":"none"
    }
   ,{
      "startPos":10,
      "endPos":0.6*300/pi,
      "innerRadius":500/3,
      "outerRadius":500/3,
      "stroke":"#ccc",
      "fillColor":"none"
    }
  ];
  var foData03 = [
    {
      "x":0,
      "y":4,
      "text":"$$5$$"
    },
    {
      "x":0.5,
      "y":8,
      "text":"$$4$$"
    },
    {
      "x":0.7,
      "y":3,
      "text":"$$x$$"
    },
    {
      "x":4,
      "y":9,
      "text":"$$9x$$"
    },
    {
      "x":2.5,
      "y":5.6,
      "text":"$$5x$$"
    },
    {
      "x":0,
      "y":1,
      "text":"$$P$$"
    },
    {
      "x":1.3,
      "y":9.8,
      "text":"$$A$$"
    },
    {
      "x":7,
      "y":6,
      "text":"$$B$$"
    },
    {
      "x":0.4,
      "y":6,
      "text":"$$C$$"
    },
    {
      "x":3.8,
      "y":3.8,
      "text":"$$D$$"
    },
  ];
  drawArc(svg03,arcData03,xScale03,yScale03);
  drawMathjax(svg03,foData03,xScale03,yScale03);

/**  Unit circle */
  var svg04 = d3.select("#svg04")
                .append("svg")
                .attr("height",height)
                .attr("width",width)
                .style("background","#000");

  drawAxes(svg04,axesData01);

  // circle
  drawCircle(svg04,circleData01,xScale01,yScale01);

  var vecData04 = [
    {
      "x1":0,
      "y1":0,
      "angles":0,
      "length":1.2,
      "stroke":"#ff0"
    }
   ,{
      "x1":0,
      "y1":0,
      "angles":60,
      "length":1.2,
      "stroke":"#ff0"
    }
  ];
  drawVectorA(svg04,vecData04,xScale01,yScale01);

  var lineData04 = [
    {
      "x1":Math.cos(pi/3),
      "y1":Math.sin(pi/3),
      "x2":Math.cos(pi/3),
      "y2":0,
      "stroke":"#0f0"
    }
   ,{
      "x1":Math.cos(pi/3),
      "y1":0,
      "x2":0,
      "y2":0,
      "stroke":"#f0f"
    }
  ];
  drawLine(svg04,lineData04,xScale01,yScale01);

  // right angle
  var pathData04 = [
    {"x":Math.cos(pi/3)-0.1,
     "y":0
    },
    {"x":Math.cos(pi/3)-0.1,
     "y":0.1
    },
    {"x":Math.cos(pi/3),
     "y":0.1
    }
  ];
  drawPath(svg04,pathData04,{"stroke":"#fff"},xScale01,yScale01);

  var foData04 = [
    {
      "x":0,
      "y":0.3,
      "text":"$$O$$"
    },
    {
      "x":0.15,
      "y":0.9,
      "text":"$$1$$"
    },
    {
      "x":0.55,
      "y":0.8,
      "text":"$$b$$"
    },
    {
      "x":0.25,
      "y":0.3,
      "text":"$$a$$"
    },
    {
      "x":0.1,
      "y":0.5,
      "text":"$$\\theta$$"
    },
    {
      "x":0,
      "y":1.5,
      "text":"$$(0,1)$$"
    },
    {
      "x":0,
      "y":-0.7,
      "text":"$$(0,-1)$$"
    },
    {
      "x":1,
      "y":0.3,
      "text":"$$(1,0)$$"
    },
    {
      "x":-1.4,
      "y":0.3,
      "text":"$$(-1,0)$$"
    },
    {
      "x":0.55,
      "y":1.3,
      "text":"$$(a, b)$$"
    }

  ];
  drawMathjax(svg04,foData04,xScale01,yScale01);

/**
    Solving triangle in unit circle  
                                      */
  var svg05 = d3.select("#svg05")
                .append("svg")
                .attr("height",height)
                .attr("width",width)
                .style("background","#000");


  var xScale05 = d3.scale.linear()
                       .domain([-1,1])
                       .range([20,380]);
  
  var yScale05 = d3.scale.linear()
                       .domain([1,-1])
                       .range([20,380]);       

  // 軸
  axesData05 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[-1,1],
    "yTickValues":[-1,1],
    "yPadding":10,
    "stroke":"#ff0",
    "strokeWidth":1,
    "xScale":xScale05,
    "yScale":yScale05
  };

  drawAxes(svg05,axesData05);

  // circle
  var circleData05 = [
    {"cx":0,"cy":0,"r":180,"stroke":"#999","strokeWidth":2,"fillColor":"none"}
 ];   
  drawCircle(svg05,circleData05,xScale05,yScale05);

  var vecData05 = [
    {
      "x1":0,
      "y1":0,
      "angles":0,
      "length":1.2,
      "stroke":"#ff0"
    }
   ,{
      "x1":0,
      "y1":0,
      "angles":45,
      "length":1.5,
      "stroke":"#ff0"
    }
  ];
  drawVectorA(svg05,vecData05,xScale05,yScale05);

  var lineData05 = [
    {
      "x1":Math.cos(pi/4),
      "y1":Math.sin(pi/4),
      "x2":Math.cos(pi/4),
      "y2":0,
      "stroke":"#0f0"
    }
   ,{
      "x1":Math.cos(pi/4),
      "y1":0,
      "x2":0,
      "y2":0,
      "stroke":"#f0f"
    }
  ];
  drawLine(svg05,lineData05,xScale05,yScale05);

  // right angle
  var pathData05 = [
    {"x":Math.cos(pi/4)-0.1,
     "y":0
    },
    {"x":Math.cos(pi/4)-0.1,
     "y":0.1
    },
    {"x":Math.cos(pi/4),
     "y":0.1
    }
  ];
  drawPath(svg05,pathData05,{"stroke":"#fff"},xScale05,yScale05);

  var foData05 = [
    {
      "x":0,
      "y":0.23,
      "text":"$$A$$"
    },
    {
      "x":0.65,
      "y":1.12,
      "text":"$$B$$"
    },
    {
      "x":1.05,
      "y":0.23,
      "text":"$$C$$"
    },
    {
      "x":0.7,
      "y":0.23,
      "text":"$$D$$"
    },
    {
      "x":0.2,
      "y":0.7,
      "text":"$$1$$"
    },
    {
      "x":0.75,
      "y":0.7,
      "text":"$$y$$"
    },
    {
      "x":0.3,
      "y":0.23,
      "text":"$$x$$"
    },
    {
      "x":0.15,
      "y":0.4,
      "text":"$$\\frac{\\pi}{4}$$"
    },
    {
      "x":0.75,
      "y":1.0,
      "text":"$$(x, y)$$"
    }

  ];
  drawMathjax(svg05,foData05,xScale05,yScale05);

/**
    Finding trig functions ...  
                                      */
  var svg06 = d3.select("#svg06")
                .append("svg")
                .attr("height",height)
                .attr("width",width)
                .style("background","#000");

 var polyData06 = [
  {"cx":0,"cy":0,"r":1,"sides":3,"start":90,"stroke":"#ff0"},
 ];

  drawPolygon(svg06,polyData06,xScale05,yScale05);

  // line
  var lineData06 = [
    {
      "x1":0,
      "y1":1,
      "x2":0,
      "y2":-0.5,
      "stroke":"#0f0"
    }
   ,{
      "x1":-0.1,
      "y1":-0.4,
      "x2":-0.1,
      "y2":-0.5,
      "stroke":"#fff"
    }
   ,{
      "x1":-0.1,
      "y1":-0.4,
      "x2":0,
      "y2":-0.4,
      "stroke":"#fff"
    }
  ];
  drawLine(svg06,lineData06,xScale05,yScale05);

  var foData06 = [
    {
      "x":-0.1,
      "y":1.1,
      "text":"$$\\alpha$$"
    },
    {
      "x":-0.8,
      "y":-0.15,
      "text":"$$\\beta$$"
    },
    {
      "x":-0.45,
      "y":0.7,
      "text":"$$2$$"
    },
    {
      "x":0.45,
      "y":0.7,
      "text":"$$2$$"
    },
    {
      "x":0.1,
      "y":0.4,
      "text":"$$a$$"
    },
    {
      "x":0.6,
      "y":-0.0,
      "text":"$$\\frac{\\pi}{3}$$"
    },
    {
      "x":-0.5,
      "y":-0.3,
      "text":"$$b$$"
    }

  ];
  drawMathjax(svg06,foData06,xScale05,yScale05);

/**
    arcsin  
                                      */
  var svg07 = d3.select("#svg07")
                .append("svg")
                .attr("height",height)
                .attr("width",width)
                .style("background","#000");

  // axess    
   axesData07 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[],
    "yTickValues":[],
    "yPadding":10,
    "stroke":"#ff0",
    "strokeWidth":1,
    "xScale":xScale05,
    "yScale":yScale05
  };

  drawAxes(svg07,axesData07);                
  // circle
  drawCircle(svg07,circleData05,xScale05,yScale05);
  // line
  var lineData07 = [
    {
      "x1":Math.cos(pi/4),
      "y1":Math.sin(pi/4),
      "x2":Math.cos(pi/4),
      "y2":0,
      "stroke":"#0f0"
    }
   ,{
      "x1":Math.cos(pi/4),
      "y1":0,
      "x2":0,
      "y2":0,
      "stroke":"#f0f"
    }
   ,{
      "x1":Math.cos(pi/4),
      "y1":Math.sin(pi/4),
      "x2":0,
      "y2":0,
      "stroke":"#ff0"
    }
   ,{
      "x1":Math.cos(-pi/3),
      "y1":Math.sin(-pi/3),
      "x2":Math.cos(-pi/3),
      "y2":0,
      "stroke":"#0f0"
    }
   ,{
      "x1":Math.cos(-pi/3),
      "y1":0,
      "x2":0,
      "y2":0,
      "stroke":"#f0f"
    }
   ,{
      "x1":Math.cos(-pi/3),
      "y1":Math.sin(-pi/3),
      "x2":0,
      "y2":0,
      "stroke":"#ff0"
    }
   ,{
      "x1":Math.cos(-pi/3)-0.1,
      "y1":0,
      "x2":Math.cos(-pi/3)-0.1,
      "y2":-0.1,
      "stroke":"#fff"
    }
   ,{
      "x1":Math.cos(-pi/3)-0.1,
      "y1":-0.1,
      "x2":Math.cos(-pi/3),
      "y2":-0.1,
      "stroke":"#fff"
    }
  ];
  drawLine(svg07,lineData07,xScale05,yScale05);

  // right angle
  var pathData07 = [
    {"x":Math.cos(pi/4)-0.1,
     "y":0
    },
    {"x":Math.cos(pi/4)-0.1,
     "y":0.1
    },
    {"x":Math.cos(pi/4),
     "y":0.1
    }
  ];
  drawPath(svg07,pathData07,{"stroke":"#fff"},xScale05,yScale05);

  var foData07 = [
    {
      "x":0.2,
      "y":0.7,
      "text":"$$1$$"
    },
    {
      "x":0.75,
      "y":0.7,
      "text":"$$y$$"
    },
    {
      "x":0.6,
      "y":0.23,
      "text":"$$x$$"
    },
    {
      "x":0.15,
      "y":0.4,
      "text":"$$\\frac{\\pi}{4}$$"
    },
    {
      "x":0.75,
      "y":1.2,
      "text":"$$(\\frac{\\sqrt{2}}{2}, \\frac{\\sqrt{2}}{2})$$"
    },
    {
      "x":0.5,
      "y":-0.6,
      "text":"$$(\\frac{1}{2}, -\\frac{\\sqrt{3}}{2})$$"
    }

  ];
  drawMathjax(svg07,foData07,xScale05,yScale05);

/**
    arccos  
                                      */
  var svg08 = d3.select("#svg08")
                .append("svg")
                .attr("height",height)
                .attr("width",width)
                .style("background","#000");

  // axes
  drawAxes(svg08,axesData07);
  // circle
  drawCircle(svg08,circleData05,xScale05,yScale05);                
  // line
  var lineData08 = [
    {
      "x1":Math.cos(pi*2/3),
      "y1":Math.sin(pi*2/3),
      "x2":Math.cos(pi*2/3),
      "y2":0,
      "stroke":"#0f0"
    }
   ,{
      "x1":Math.cos(pi*2/3),
      "y1":0,
      "x2":0,
      "y2":0,
      "stroke":"#f0f"
    }
   ,{
      "x1":Math.cos(pi*2/3),
      "y1":Math.sin(pi*2/3),
      "x2":0,
      "y2":0,
      "stroke":"#ff0"
    }
   ,{
      "x1":Math.cos(pi*2/3)+0.1,
      "y1":0,
      "x2":Math.cos(pi*2/3)+0.1,
      "y2":0.1,
      "stroke":"#fff"
    }
   ,{
      "x1":Math.cos(pi*2/3)+0.1,
      "y1":0.1,
      "x2":Math.cos(pi*2/3),
      "y2":0.1,
      "stroke":"#fff"
    }
  ];
  drawLine(svg08,lineData08,xScale05,yScale05);
  // arc
  var arcData08 = [
    {
      "startPos":90,
      "endPos":-30,
      "innerRadius":50,
      "outerRadius":50,
      "stroke":"#f0f"
    },
    {
      "startPos":-30,
      "endPos":-90,
      "innerRadius":30,
      "outerRadius":30,
      "stroke":"#00f"
    },
  ];
  // MathJax
  var foData08 = [
    {
      "x":0.05,
      "y":0.4,
      "text":"$$\\theta$$"
    },
    {
      "x":-0.2,
      "y":0.4,
      "text":"$$\\alpha$$"
    },
    {
      "x":-0.6,
      "y":0.2,
      "text":"$$-\\frac{1}{2}$$"
    },
  ];
  drawArc(svg08,arcData08,xScale05,yScale05);
  drawMathjax(svg08,foData08,xScale05,yScale05);

/**
    arctan  
                                      */
  var svg09 = d3.select("#svg09")
                .append("svg")
                .attr("height",height)
                .attr("width",width)
                .style("background","#000");
  // 軸                
  drawAxes(svg09,axesData07);
  // circle
  drawCircle(svg09,circleData05,xScale05,yScale05);                
  // line
  var lineData09 = [
    {
      "x1":Math.cos(-pi/4),
      "y1":Math.sin(-pi/4),
      "x2":Math.cos(-pi/4),
      "y2":0,
      "stroke":"#0f0"
    }
   ,{
      "x1":Math.cos(-pi/4),
      "y1":0,
      "x2":0,
      "y2":0,
      "stroke":"#f0f"
    }
   ,{ // slope
      "x1":Math.cos(pi*3/4),
      "y1":Math.sin(pi*3/4),
      "x2":Math.cos(-pi/4),
      "y2":Math.sin(-pi/4),
      "stroke":"#ff0"
    }
   ,{ // right angle
      "x1":Math.cos(-pi/4)-0.1,
      "y1":0,
      "x2":Math.cos(-pi/4)-0.1,
      "y2":-0.1,
      "stroke":"#fff"
    }
   ,{
      "x1":Math.cos(-pi/4)-0.1,
      "y1":-0.1,
      "x2":Math.cos(-pi/4),
      "y2":-0.1,
      "stroke":"#fff"
    }
  ];
  drawLine(svg09,lineData09,xScale05,yScale05);
  // arc
  var arcData09 = [
    {
      "startPos":90,
      "endPos":135,
      "innerRadius":30,
      "outerRadius":30,
      "stroke":"#f0f"
    },
  ];
  // MathJax
  var foData09 = [
    {
      "x":0.17,
      "y":0.2,
      "text":"$$\\theta$$"
    },
    {
      "x":0.3,
      "y":0.35,
      "text":"$$x$$"
    },
    {
      "x":0.75,
      "y":0,
      "text":"$$y$$"
    },
  ];
  drawArc(svg09,arcData09,xScale05,yScale05);
  drawMathjax(svg09,foData09,xScale05,yScale05);

/**
    Restricting domain of trig function ....  
                                      */
  var svg10 = d3.select("#svg10")
                .append("svg")
                .attr("height",height)
                .attr("width",width)
                .style("background","#000");

  // ellipse
  var ellipseData10 = [
    {
      "cx":120,
      "cy":200,
      "ry":150,
      "rx":70,
      "stroke":"#0f0"
    }
    ,
    {
      "cx":280,
      "cy":200,
      "ry":150,
      "rx":70,
      "stroke":"#f0f"
    }
  ];
  drawEllipse(svg10,ellipseData10);

  //circle
  var circleData10 = [
    {"cx":120,"cy":150,"r":10,"fillColor":"#0f0"},
    {"cx":120,"cy":220,"r":10,"fillColor":"#0f0"},
    {"cx":120,"cy":260,"r":10,"fillColor":"#0f0"},
    {"cx":280,"cy":150,"r":10,"fillColor":"#f0f"},
    {"cx":280,"cy":240,"r":10,"fillColor":"#f0f"},
  ];
  drawCircle(svg10,circleData10);

  //vector
  var vecData10 = [
    {"x1":130,"y1":140,"x2":270,"y2":145,"stroke":"#0f0"},
    {"x1":130,"y1":220,"x2":270,"y2":230,"stroke":"#0f0"},
    {"x1":130,"y1":260,"x2":270,"y2":250,"stroke":"#0f0"},
    {"x1":270,"y1":160,"x2":130,"y2":155,"stroke":"#f0f"},
    {"x1":270,"y1":240,"x2":170,"y2":240,"stroke":"#f0f"}
  ];
  drawVectorB(svg10,vecData10);

  // MathJax
  var foData10 = [
    {
      "x":70,
      "y":-20,
      "text":"$$Domain$$",
      "fontSize":"1.5em"
    },
    {
      "x":250,
      "y":-20,
      "text":"$$Range$$",
      "fontSize":"1.5em"
    },
    {
      "x":150,
      "y":60,
      "text":"$$f$$",
      "fontSize":"1.1em"
    },
    {
      "x":220,
      "y":110,
      "text":"$$f^{-1}$$",
      "fontSize":"1.1em"
    },
    {
      "x":150,
      "y":140,
      "text":"$$f$$",
      "fontSize":"1.1em"
    },
    {
      "x":150,
      "y":210,
      "text":"$$f$$",
      "fontSize":"1.1em"
    },
    {
      "x":150,
      "y":175,
      "text":"$$?$$",
      "fontSize":"1.1em"
    }
  ];
  drawMathjax(svg10,foData10);

  var svg11 = d3.select("#svg11")
                .append("svg")
                .attr("height",height)
                .attr("width",width)
                .style("background","#000");

  var xScale11 = d3.scale.linear()
                       .domain([-200,360])
                       .range([20,380]);
  
  var yScale11 = d3.scale.linear()
                       .domain([1.2,-1.2])
                       .range([20,380]);       

  // axes
  axesData11 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[],
    "yTickValues":[],
    "yPadding":10,
    "stroke":"#ff0",
    "strokeWidth":1,
    "xScale":xScale11,
    "yScale":yScale11
  };

  drawAxes(svg11,axesData11);

  // graph
  var pi = Math.PI;
  var aDegree = pi / 180;
  var graphData11 = [];

  for (var i=-200;i<=340;i++){

    graphData11.push(new Point(i+50,Math.cos(aDegree*i)));
  };
  drawPath(svg11,graphData11,{"stroke":"#f00"},xScale11,yScale11);

  // lines
  var lineData11 = [
    {"x1":-200,
     "y1":0.5,
     "x2":370,
     "y2":0.5,
     "stroke":"aqua",
     "strokeWidth":1
    },
    {"x1":50,
     "y1":-1.1,
     "x2":50,
     "y2":1.1,
     "stroke":"#0f0",
     "strokeWidth":1
    },
    {"x1":230,
     "y1":-1.1,
     "x2":230,
     "y2":1.1,
     "stroke":"#0f0",
     "strokeWidth":1
    }
  ];
  drawLine(svg11,lineData11,xScale11,yScale11);

  // vector
  var vecData11 = [
    {"x1":50,
     "y1":0,
     "x2":230,
     "y2":0,
     "stroke":"#f0f",
     "strokeWidth":5
    }
  ];
  drawVectorW(svg11,vecData11,xScale11,yScale11);

  // MathJax
  var foData11 = [
    {
      "x":-150,
      "y":0.8,
      "text":"$$0.5$$",
      "fontSize":"1.1em"
    }
  ];
  drawMathjax(svg11,foData11,xScale11,yScale11);

</script>
