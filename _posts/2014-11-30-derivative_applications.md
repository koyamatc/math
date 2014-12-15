---
title: Differential calculus
layout: post
date: 2014-11-30 21:00:00
postTitle: Derivative applications
categories: differential
---

-------

# Equations of normal and tangent lines

--------

## y-intercept of tangent line example

<div class="row">
  <div class="col-sm-6">
    <div id="svg01"></div>
  </div>
  <div class="col-sm-6">
    曲線\(f(x)=\frac{1}{x}\)のある点\((k \ne 0)\)における接線が
    \(y\)軸を横切るときの値を求めよ
    <br>
    \(x=k\)の点の座標は\( (k,\frac{1}{k}) \)
    <br>
    この点を通る接線の傾きは
    $$f(x)=\frac{1}{x}=x^{-1}$$
    $$f'(x)=-x^{-2}=-\frac{1}{x^2}$$
    \(x=k\)のときの傾きは
    $$f'(k)=-\frac{1}{k^2}$$
    接線(tangent line)を\(y=mx+b\)とすると
    <br>
    傾き\(m=\frac{1}{k^2}\)、　ｙ軸との交点のy座標は\(b\)なので
    $$y=-\frac{1}{k^2}x+b$$
   　点\( (k,\frac{1}{k}) \)を通るので
    $$\frac{1}{k}=-\frac{1}{k^2}k+b$$
    $$\frac{1}{k}=-\frac{1}{k}+b$$
    $$b=\frac{1}{k}+\frac{1}{k}=\frac{2}{k}$$
    したがって点\( (k,\frac{1}{k}) \)を通る接線の式は
    $$y=-\frac{1}{k^2}x+\frac{2}{k}$$

  </div>
</div>

-------------

## Equation of normal line(法線)

幾何において __normal__　とは、与えられたオブジェクトに対して垂直な線やベクトルなどのオブジェクトです。

２次元の場合、曲線上の任意の点における接線に対してその点を通る垂直な直線を法線(noramal line)といいます。

<div class="row">
  <div class="col-sm-6">
    <div id="svg02"></div>
  </div>
  <div class="col-sm-6">
  曲線\(f(x)=\frac{e^x}{x^2}\)で\(x=1\)のときの法線の式を求める
  <br>
  \(x=1\)のときの接線の傾きを求めます  
  $$f(x)=\frac{e^x}{x^2}=e^xx^{-2} \quad
  f(1)=\frac{e^1}{1^2}=e$$
  \(f(x)\)を微分します
  $$f'(x)=e^xx^{-2}+e^x(-2x^{-3})$$
  $$f'(1)=e-2e=-e \quad 接線の傾き$$
  法線の傾きは\(-\frac{1}{m}\)なので\(\frac{1}{e}\)
  <br>
  \(y=-\frac{1}{m}x+b\)を法線の式とすると
  $$e=\frac{1}{e}+b \to b=e-\frac{1}{e}$$
  $$y = \frac{1}{e}x+e-\frac{1}{e}$$

  </div>
</div>

---------------

# Motion along a line

導関数はその瞬間の変化の割合を計算することができます。
時間に対し位置変化の割合が速度(velocity)で、
時間に対し速度変化の割合が加速度(acceleration)です。
この考え方を使って、時間の関数として表される位置にある１次元の粒の動きを分析してみましょう。

-----------

## Total distance traveled by a particle

<div class="row">
  <div class="col-sm-6">
    <div class="panel">
    数直線上をうごく粒子の位置は下記の式で表されるとします
    $$s(t)=\frac{2}{3}t^3-6t^2+10t \quad (t \ge 0)$$
    tは秒を表します
    <br>
    粒子は最初の６秒間に左右に動きます。\(0 \le t \le 6\)の間に粒子が移動する距離の合計はどれだけですか？
    </div>
    右方向に動くときを　＋　、左方向に動くときを　―　で表します。
    <br>
    \(s(t)\)を微分して、速度の変化を表す式を求めます
    $$s'(t)=2t^2-12t+10$$
    \(s'(t)=0\)のとき速度は0で、その時のtを求めます
    $$2t^2-12t+10=0$$
    $$t^2-6t+5=0$$
    $$(t-1)(t-5)=0$$
    したがって\(t=1\)または\(t=5\)のときに速度は0となります。
    <br>
    \(0 \le t \le 1\)で粒子は右方向へ移動し、
    \(1 \le t \le 5\)で粒子は左方向へ移動し、
    \(5 \le t \le 6\)で粒子は右方向へ移動します
    <br>
    １秒後の位置は\(4\frac{2}{3}\)なので移動距離は\(4\frac{2}{3}\)<br>
    5秒後の位置は\(-16\frac{2}{3}\)なので、
    まず\(4\frac{2}{3}\)で最初の位置へ戻りさらに\(16\frac{2}{3}\)移動します<br>
    ６秒後の位置は\(-12\)なので、移動距離は\(4\frac{2}{3}\)<br>
    距離の合計は
    $$4\frac{2}{3}+4\frac{2}{3}+16\frac{2}{3}+4\frac{2}{3}
    =30\frac{2}{3}$$
  </div>
  <div class="col-sm-6">
    <div id="svg03"></div>
    <table class="table">
      <thead>
        <th>\(t\)</th>
        <th>\(s(t)\)</th>
      </thead>
      <tbody>
        <tr>
          <td>0</td>
          <td>0</td>
        </tr>
        <tr>
          <td>1</td>
          <td>\(4\frac{2}{3}\)</td>
        </tr>
        <tr>
          <td>5</td>
          <td>\(-16\frac{2}{3}\)</td>
        </tr>
        <tr>
          <td>6</td>
          <td>-12</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>

----------

## When is a particle speeding up?
<div class="row">
  <div class="col-sm-6">
    数直線上を粒子が左右に行ったり来たりします
    <div id="svg04"></div>
    粒子の位置を時間で表す関数を
    \(s(t)=t^3-6t^2+9t、ｔ \ge 0\)とします<br>
    "スピードアップ"とはどういうことでしょうか<br>
    右方向へスピードアップするとは、速度が正\(v(t) \gt 0\)であり、加速度が正\(a(t) \gt 0\)ということです<br>
    左方向へスピードアップするとは、速度が負\(v(t) \lt 0\)であり、加速度が負\(a(t) \lt 0\)ということです<br>
    速度が正（右向き）のとき、加速度が負（左向き）の場合、スピードは遅くなります、
    速度が負（左向き）のとき、加速度が正（右向き）の場合も、スピードは遅くなります。<br>

    時間に対する位置の変化は位置を表す関数\(s(t)\)の導関数で、それは速度を表しますす
    $$s'(t)=\frac{ds}{dt}=v(t)$$
    $$v(t)=3t^2-12t+9$$
    このグラフを描きます、その時 \(v\)軸との交点は\(v(0)=9\)です<br>
    \(t\)軸との交点は
    $$3t^2-12t+9=0$$
    両辺を３で割ります
    $$t^2-4t+3=0 \to (t-1)(t-3)=0$$
    $$t=1 \quad or \quad t=3$$
    次に、時間に対する速度の変化は\(v(t)\)の導関数で、加速度を表します
    $$s"(t)=v'(t)=a(t)=6t-12$$
    \(v(t)\)の点\((t,v(t))\)における接線の傾きです<br>
    スピードアップの条件は
    $$v(t) \gt 0 \quad and \quad a(t) \gt 0 \quad または \quad 
    v(t) \lt 0 \quad and \quad a(t) \lt 0$$
    よって
    $$1 \lt t \lt 2 \quad or \quad t \gt 3$$ 
  </div>
  <div class="col-sm-6">
    <div id="svg05"></div>
  </div>
</div>

--------------

# Critical points and graphing with calculus

---------------

## Minima, maxima and critical points

<div class="row">
  <div class="col-sm-6">
  </div>
  <div class="col-sm-6">
    <div id="svg06"></div>
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
  var svg03 = d3.select("#svg03")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg04 = d3.select("#svg04")
                .append("svg")
                .attr("height",50)
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


  var xScale01 = d3.scale.linear()
                       .domain([-5,5])
                       .range([50,450]);
  
  var yScale01 = d3.scale.linear()
                       .domain([6,-4])
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
  
  var pathData011 =[];
  var pathData012 =[];
  for (var i=-0.25;i>-5;i=i-0.01){
    pathData011.push(new Point(i,1/i));
  };
  for (var i=0.16;i<5;i=i+0.01){
    pathData012.push(new Point(i,1/i));
  };
  drawPath(svg01,pathData011,{"stroke":"#fff"},xScale01,yScale01);
  drawPath(svg01,pathData012,{"stroke":"#fff"},xScale01,yScale01);

  // graph
  lineData01 = [
    {"x1":1,"y1":1,"x2":0,"y2":2,"stroke":"#0f0"},
    {"x1":1,"y1":1,"x2":2,"y2":0,"stroke":"#0f0"},
  ];
  drawLine(svg01,lineData01,xScale01,yScale01);

  // circle
  var circleData01 = [
    {"cx":1,"cy":1,"r":2,"stroke":"#f0f","fillColor":"#f0f"}
  ];   
  drawCircle(svg01,circleData01,xScale01,yScale01);

  // mathjax   
  foData01 = [
    {"x":5.3,
    "y":1.5,
    "text":"$$x$$",
    "fontSize":"20px"},
    {"x":-0.1,
    "y":8.6,
    "text":"$$y$$",
    "fontSize":"20px"},
    {"x":0.8,
    "y":1,
    "text":"$$k$$",
    "fontSize":"18px"},
    {"x":-0.8,
    "y":2.8,
    "text":"$$\\frac{1}{k}$$",
    "fontSize":"18px"},
    {"x":1,
    "y":5.3,
    "text":"$$f(x)=\\frac{1}{x}$$",
    "fontSize":"18px"}
  ];
 
  drawMathjax(svg01,foData01,xScale01,yScale01);

  var xScale02 = d3.scale.linear()
                       .domain([-1,5])
                       .range([50,450]);
  
  var yScale02 = d3.scale.linear()
                       .domain([6,0])
                       .range([50,450]);       

  // 軸
  axesData02 = { 
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
    "xScale":xScale02,
    "yScale":yScale02
  };
  drawAxes(svg02,axesData02);

  var pathData02 =[];
  for (var i=0.2;i<=5;i=i+0.1){
    pathData02.push(new Point(i,func01(i)));
  };
  drawPath(svg02,pathData02,{"stroke":"#fff"},xScale02,yScale02);

  function func01(p){
    return Math.pow(Math.E,p)/Math.pow(p,2);
  }

  // Lines
  lineData02 = [
    {"x1":0,"y1":2*Math.E,"x2":2,"y2":0,"stroke":"#0f0"},
    {"x1":2,"y1":Math.E+1/Math.E,"x2":-1,"y2":Math.E-2/Math.E,"stroke":"#f0f"},
  ];
  drawLine(svg02,lineData02,xScale02,yScale02);

  // mathjax   
  foData02 = [
    {"x":-1.2,
    "y":3.5,
    "text":"$$normal$$",
    "fontSize":"18px"},
    {"x":1,
    "y":5.3,
    "text":"$$f(x)$$",
    "fontSize":"18px"},
    {"x":2,
    "y":2,
    "text":"$$tangent$$",
    "fontSize":"18px"}
  ];
 
  drawMathjax(svg02,foData02,xScale02,yScale02);



  /*  Total distance traveled by a particle */
  var xScale03 = d3.scale.linear()
                       .domain([0,7])
                       .range([50,450]);
  
  var yScale03 = d3.scale.linear()
                       .domain([11,-9])
                       .range([50,450]);       

  // 軸
  axesData03 = { 
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[1,2,3,4,5,6],
    "yTickValues":[10],
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

  var pathData03 =[];
  for (var i=0;i<=7;i=i+0.1){
    pathData03.push(new Point(i,func03(i)));
  };
  drawPath(svg03,pathData03,{"stroke":"#fff"},xScale03,yScale03);

  function func03(p){
    return 2*p*p-12*p+10;
  }

  // mathjax   
  foData03 = [
    {"x":7,
    "y":1,
    "text":"$$t$$",
    "fontSize":"18px"},
    {"x":-0.5,
    "y":15,
    "text":"$$v$$",
    "fontSize":"18px"},
    {"x":-0.5,
    "y":8,
    "text":"右方向へ",
    "fontSize":"18px"},
    {"x":-0.5,
    "y":-1,
    "text":"左方向へ",
    "fontSize":"18px"},
  ];
 
  drawMathjax(svg03,foData03,xScale03,yScale03);

  // When is a particle speeding up?
  vecData04 = [
    {"x1":0,"y1":25,"x2":500,"y2":25,"stroke":"#fff"}
  ];
  drawVectorW(svg04,vecData04);

  lineData04 = [
    {"x1":200,"y1":20,"x2":200,"y2":30,"stroke":"#fff"}
  ];
  drawLine(svg04,lineData04);
  
  circleData04 = [
    {"cx":200,"cy":25,"r":2,"stroke":"#f0f","fillColor":"#f0f"}
  ];
  drawCircle(svg04,circleData04);

  textData04 = [
    {"x":196,"y":45,"text":"0","stroke":"#fff"}
  ];

  drawText(svg04,textData04);

  var xScale05 = d3.scale.linear()
                       .domain([0,5])
                       .range([50,450]);
  
  var yScale05 = d3.scale.linear()
                       .domain([11,-4])
                       .range([50,450]);       

  // 軸
  axesData05 = { 
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[1,2,3,4],
    "yTickValues":[9],
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

  var pathData05 =[];
  for (var i=0;i<=5;i=i+0.1){
    pathData05.push(new Point(i,func05(i)));
  };
  drawPath(svg05,pathData05,{"stroke":"#fff"},xScale05,yScale05);

  function func05(p){
    return 3*p*p-12*p+9;
  }

  // mathjax   
  foData05 = [
    {"x":5,
    "y":1,
    "text":"$$t$$",
    "fontSize":"18px"},
    {"x":-0.5,
    "y":13.5,
    "text":"$$v$$",
    "fontSize":"18px"},
    {"x":-0.5,
    "y":8,
    "text":"右方向へ",
    "fontSize":"18px"},
    {"x":-0.5,
    "y":-1,
    "text":"左方向へ",
    "fontSize":"18px"},
  ];
 
  drawMathjax(svg05,foData05,xScale05,yScale05);

  // Minima, maxima and critical points
  var xScale06 = d3.scale.linear()
                       .domain([-1,15])
                       .range([50,450]);
  
  var yScale06 = d3.scale.linear()
                       .domain([10,-1])
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
  drawAxes(svg06,axesData06,xScale06,yScale06);

  pathData06 = [];
  for (var i=-2;i<=2;i=i+0.1){
    pathData06.push(new Point(i,-5/8*i*i+7/4*i+4));
  };
  for (var i=1.8;i<=6;i=i+0.1){
    pathData06.push(new Point(i,2*Math.cos(i-1.7)+3.12));
  };
  for (var i=6;i<=11;i=i+0.1){
    pathData06.push(new Point(i,Math.pow(i,3)/(x^2-1));
  };

  drawPath(svg06,pathData06,{"stroke":"#fff"},xScale06,yScale06);

</script>