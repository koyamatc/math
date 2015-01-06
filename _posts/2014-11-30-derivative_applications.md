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
  関数\(f(x)\)の曲線において<br>
  最大値は\((x_{0},f(x_{0}))\)の点でグローバル最大値（global maximum）といいます。
  この点における接線の傾きは0、つまり\(f'(x_{0})=0\)です<br>
  最小値は、マイナスの無限大と考えられるためグローバル最小値は、存在しません<br>
  ローカル最小値は \((x_{1},f(x_{1}))\)の点です。この点における接線の傾きは0、つまり\(f'(x_{1})=0\)です<br>
  ローカル最大値は \((x_{2},f(x_{2}))\)の点です。この点では接線は定義できません、つまり\(f'(x_{2})=undefined\)です<br>
  両端（end points）ではい、\(x=a\)の点で、最大値や最小値がある、<br>
  つまり、\(f'(a)=0\)または\(f'(a)\)は未定義となる点をcritical pointと呼びます
  </div>
  <div class="col-sm-6">
    <div id="svg06"></div>
  </div>
</div>

-----------------

## Finding critical numbers

\\(f(x)=xe^{-2x^2}\\)のクリティカル数を求めます

\\(c\\)を\\(f\\)のクリティカル数とします

\\(f'(c)=0\\) または \\(f'(c)\\)未定義のとき、\\(c\\)はクリティカル数です

\\(f(x)\\)の導関数を求めます

$$f'(x)=\frac{d}{dx}[x]e^{-2x^2}+\frac{d}{dx}[e^{-2x^2}]x$$
$$\quad = e^{-2x^2}+e^{-2x^2}(-4x)x$$
$$\quad =e^{-2x^2}(1-4x^2)$$
$$1-4x^2=0$$
$$1=4x^2$$
$$x=\pm\frac{1}{2}$$
したがって、クリティカル数は\\(\frac{1}{2},-\frac{1}{2}\\)です

-----------------

## Testing critical points for local extrema(極値)

<div class="row">
  <div class="col-sm-6">
    クリティカル・ポイントが、最大値か最小値かを調べるには<br>
    点の前後で傾きの符号がどう変わったかを調べます<br>
    \(x=x_{0}\)では、傾きは正から負へと変わります<br>
    \(x=x_{2}\)でも、傾きは正から負へと変わります<br>
    傾きの符号が正から負に代わる点は最大値です<br>
    \(x=x_{1}\)では、傾きは負から正へと変わります<br>
    傾きの符号が負から正に代わる点は最小値です<br>
    \(x=x_{3}\)では、傾きは負から負です<br>
    この点はクリティカル・ポイントではありません
  </div>
  <div class="col-sm-6">
    <div id="svg07"></div>
  </div>
</div>


-----------------

## Identifying minima and maxima for \\(x^3 - 12x + 2\\)

<div class="row">
  <div class="col-sm-6">
   \(f(x)=x^3 - 12x + 2\) にクリティカル・ポイントがあるか調べます<br>
   \(f(x)\)の導関数を求めます
   $$f'(x)=3x^2-12$$
   $$3x^2-12=0$$
   $$3x^2=12$$
   $$x^2=4$$
   $$x=\pm2$$
   $$f'(2)=0 \quad f'(-2)=0$$
   \(f(x)\)にはクリティカル・ポイントがあります
   $$$$
   \(x=-2\)で、傾きの符号が正から負へ変わるので、最大値です<br>
   \(x=2\)で、傾きの符号が負から正へ変わるので、最小値です<br>
  </div>
  <div class="col-sm-6">
    <div id="svg08"></div>
  </div>
</div>

--------------

# Absolute and relative maxima and minima

--------------

## Extreme value theorem　(極値定理)

<div class="row">
  <div class="col-sm-6">
  関数\(f(x)\)が閉じた区間(\(a,b\)を含む)\([a,b]\)において連続であるならば<br>
  \(f(x)\)には、最大値と最小値が存在する<br>
  \(x=c\)のとき最小値、\(x=d\)のとき最大値とすると
  $$\exists c,d \in [a,b]$$
  $$f(c) \le f(x) \le f(d)$$
  である
  </div>
  <div class="col-sm-6">
    <div id="svg09"></div>
  </div>
</div>
<div class="row">
  <div class="col-sm-6">
  関数\(f(x)\)が不連続の場合、<br>
  \(x=c\)に限りなく近づいて行くと\(f(c)\)に限りなく近づきますがそこには値がありません<br>
  \(x=d\)に限りなく近づいて行くと\(f(d)\)に限りなく近づきますがそこには値がありません<br>
  したがって、不連続の関数では、最大値と最小値が存在するとは限りません。
  </div>
  <div class="col-sm-6">
    <div id="svg091"></div>
  </div>
</div>
<div class="row">
  <div class="col-sm-6">
  開いた（\(a,b\)を含まない）区間\((a,b)\)では、<br>
  \(x=a\)に限りなく近づいて行くと\(f(a)\)に限りなく近づきますがそこには値がありません<br>
  \(x=b\)に限りなく近づいて行くと\(f(b)\)に限りなく近づきますがそこには値がありません<br>
  したがって、開いた区間では関数に、最大値と最小値が存在するとは限りません。
  </div>
  <div class="col-sm-6">
    <div id="svg092"></div>
  </div>
</div>

--------------

## Relative minima and maxima

<div class="row">
  <div class="col-sm-6">
    <div id="svg10"></div>
  </div>
  <div class="col-sm-6">
  関数\(f(x)\)は閉じた区間\([a,b]\)において、\(x=a\)のとき最大であり<br>
  \(x=b\)のとき最少である<br>
  <br>
  \(x=c\)のとはどうでしょうか<br>
  最小値ではないが、\(x=c\)では、その近くの点よりは小さい<br>
  これをrelative minimum または local minimum と呼ぶ
  $$f(c)\le f(x) \quad \forall x \in (c-h,c+h), h \gt 0$$
  \(x=d\)のとはどうでしょうか<br>
  最大値ではないが、\(x=d\)では、その近くの点よりは大きい<br>
  これをrelative maximum または local maximum と呼ぶ
  $$f(d)\ge f(x) \quad \forall x \in (c-h,c+h), h \gt 0$$
  </div>
</div>

--------------

# Concavity and inflection points

---------------

## Concavity, concave upwards and concave downwards intervals

<div class="row">
  <div class="col-sm-6">
    <div id="svg11"></div>
  </div>
  <div class="col-sm-6">
    白線：関数\(f(x)\)<br>
    ピンク：\(f(x)\)の１次導関数\(f'(x)\)<br>
    緑線：\(f(x)\)の２次導関数\(f''(x)\),\(f'(x)\)の１次導関数<br><br>

    関数\(f(x)\)は\(x \ge 0 \)の表示範囲で、最大値と最小値があります<br>
    それらの点はクリティカル・ポイントです<br><br>
    最大値の近くでは\(x\)の小さい方から最大値に近づいていくと、
    その接線の傾きは正の値が徐々に小さくなり、最大値で0となり、それを過ぎると負の値となりさらに小さくなっていきます。<br><br>
    最少値の近くでは\(x\)の小さい方から最少値に近づいていくと、
    その接線の傾きは負の値が徐々に大きくなり、最少値で0となり、それを過ぎると正の値となりさらに大きくなっていきます。<br><br>
    最大値の近くでは、関数\(f(x)\)の描く曲線は下を向いた凹み(concave downward)となります<br>
    最少値の近くでは、関数\(f(x)\)の描く曲線は上を向いた凹み(concave upward)となります<br><br>
    
    クリティカル・ポイントが最大値か最小値かは、凹みの向きを調べればわかります<br>
    
    concave downwardの条件は<br>
    関数\(f(x)\)の接線の傾きが減少していて\(f''(x) \lt 0\)<br>
    この時クリティカル・ポイントは最大値です。<br>
    
    concave upwardの条件は<br>
    関数\(f(x)\)の接線の傾きが増加していて\(f''(x) \gt 0\)<br>
    この時クリティカル・ポイントは最少値です。
  </div>
</div>

--------------

## An inflection point (反曲点)

<div class="row">
  <div class="col-sm-6">
    <div id="svg12"></div>
  </div>
  <div class="col-sm-6">
    関数\(f(x)\)の曲線が、下向きの凹みから上向きの凹み点はどこでしょうか。<br>
    その点は、関数\(f(x)\)の１次導関数\(f'(x)\)の極値を示す点であり<br>
    関数\(f(x)\)の２次導関数\(f''(x)\)の符号が変わる点です。
  </div>
</div>


--------------

# Optimization with calculus

--------------

## Minimizing sum of squares

<div class="row">
  <div class="col-sm-6">
  </div>
  <div class="col-sm-6">
    <div id="svg13"></div>
  </div>
</div>

--------------

##

<div class="row">
  <div class="col-sm-6">
  </div>
  <div class="col-sm-6">
    <div id="svg14"></div>
  </div>
</div>

--------------

##

<div class="row">
  <div class="col-sm-6">
  </div>
  <div class="col-sm-6">
    <div id="svg15"></div>
  </div>
</div>

--------------

##

<div class="row">
  <div class="col-sm-6">
  </div>
  <div class="col-sm-6">
    <div id="svg16"></div>
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
  var svg091 = d3.select("#svg091")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg092 = d3.select("#svg092")
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
                       .domain([7,-1])
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

  var pathData06 = [];
  for (var i=-2;i<=2;i=i+0.1){
    pathData06.push(new Point(i,-5/8*i*i+7/4*i+4));
  };
  for (var i=1.8;i<=6;i=i+0.1){
    pathData06.push(new Point(i,2*Math.cos(i-1.7)+3.12));
  };

  drawPath(svg06,pathData06,{"stroke":"#fff"},xScale06,yScale06);

  var pathData061 = [
    {"x":6,"y":2.3},
    {"x":7,"y":1},
    {"x":9,"y":0.6},
    {"x":10,"y":0.5},
    {"x":11,"y":0.5},
    {"x":12,"y":0},
    {"x":15,"y":-2},
  ];
  drawPath(svg06,pathData061,{"stroke":"#fff","interPolate":"basis"},xScale06,yScale06);

  lineData06 = [
    {"x1":0,"y1":5.25,"x2":3,"y2":5.25,"stroke":"#ccc"}
   ,{"x1":3.9,"y1":1.1,"x2":5.9,"y2":1.1,"stroke":"#ccc"}
   ,{"x1":1.4,"y1":0,"x2":1.4,"y2":5.25,"stroke":"#ccc","opacity":0.7}
   ,{"x1":4.9,"y1":0,"x2":4.9,"y2":1.1,"stroke":"#ccc","opacity":0.7}
   ,{"x1":6,"y1":0,"x2":6,"y2":2.3,"stroke":"#ccc","opacity":0.7}
   ,{"x1":10.5,"y1":0,"x2":10.5,"y2":0.5,"stroke":"#ccc","opacity":0.7}
  ]
  drawLine(svg06,lineData06,xScale06,yScale06);

  circleData06 = [
    {"cx":1.4,"cy":5.25,"r":2,"stroke":"#f0f","fillColor":"#f0f"}
   ,{"cx":4.9,"cy":1.1,"r":2,"stroke":"#f0f","fillColor":"#f0f"}
   ,{"cx":6,"cy":2.3,"r":2,"stroke":"#0f0","fillColor":"#0f0"}
   ,{"cx":10.5,"cy":0.5,"r":2,"stroke":"#0f0","fillColor":"#00f"}
  ];
  drawCircle(svg06,circleData06,xScale06,yScale06);

  // mathjax
  foData06 = [
    {"x":1,
    "y":7,
    "text":"$$global \\quad maximum$$",
    "fontSize":"18px"},
    {"x":5,
    "y":4,
    "text":"$$local \\quad maximum$$",
    "fontSize":"18px"},
    {"x":2,
    "y":2.0,
    "text":"$$local \\quad min$$",
    "fontSize":"18px"},
    {"x":13,
    "y":0.7,
    "text":"$$y=f(x)$$",
    "fontSize":"16px"},
    {"x":1.2,
    "y":1.0,
    "text":"$$x_{0}$$",
    "fontSize":"16px"},
    {"x":5.8,
    "y":1.0,
    "text":"$$x_{2}$$",
    "fontSize":"16px"},
    {"x":4.7,
    "y":1.0,
    "text":"$$x_{1}$$",
    "fontSize":"16px"},
    {"x":10.3,
    "y":1.0,
    "text":"$$x_{3}$$",
    "fontSize":"16px"},
  ];

  drawMathjax(svg06,foData06,xScale06,yScale06);


  drawAxes(svg07,axesData06,xScale06,yScale06);

  drawPath(svg07,pathData06,{"stroke":"#fff"},xScale06,yScale06);

  drawPath(svg07,pathData061,{"stroke":"#fff","interPolate":"basis"},xScale06,yScale06);

  drawLine(svg07,lineData06,xScale06,yScale06);

  drawCircle(svg07,circleData06,xScale06,yScale06);

  drawMathjax(svg07,foData06,xScale06,yScale06);

  // x^3 -12x +2
  var xScale08 = d3.scale.linear()
                       .domain([-3.5,3.5])
                       .range([50,450]);

  var yScale08 = d3.scale.linear()
                       .domain([15,-15])
                       .range([50,450]);

  // 軸
  axesData08 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[-2,2],
    "yTickValues":[],
    "xTickPadding":5,
    "yTickPadding":2,
    "xOrient":["bottom"],
    "yOrient":["left"],
    "stroke":"#ff0",
    "strokeWidth":1,
    "fillColor":"none",
    "xScale":xScale08,
    "yScale":yScale08
  };
  drawAxes(svg08,axesData08,xScale08,yScale08);

  var pathData08 = [];
  for (var i=-3;i<=3;i=i+0.1){
    pathData08.push(new Point(i,3*i*i-12));
  };
  drawPath(svg08,pathData08,{"stroke":"#fff"},xScale08,yScale08);
  var pathData081 = [];
  for (var i=-3;i<=3;i=i+0.1){
    pathData081.push(new Point(i,i*i*i-12*i+2));
  };
  drawPath(svg08,pathData081,{"stroke":"#f0f"},xScale08,yScale08);

  // mathjax
  foData08 = [
    {"x":-1,
    "y":18,
    "text":"$$f(x)$$",
    "fontSize":"18px"},
    {"x":2.5,
    "y":7,
    "text":"$$f'(x)$$",
    "fontSize":"18px"},
  ];

  drawMathjax(svg08,foData08,xScale08,yScale08);

/****
  Absolute and relative maxima and minima
**/
  var xScale09 = d3.scale.linear()
                       .domain([-1,5])
                       .range([50,450]);

  var yScale09 = d3.scale.linear()
                       .domain([5,-1])
                       .range([50,450]);

  // 軸
  axesData09 = {
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
    "xScale":xScale09,
    "yScale":yScale09
  };
  drawAxes(svg09,axesData09);
  drawAxes(svg091,axesData09);
  drawAxes(svg092,axesData09);

  var pathData09 =[];
  function func09(i){
    return 2*Math.cos(2*i)+2.5;
  }
  for (var i=0.5;i<=4;i=i+0.1){
    pathData09.push(new Point(i,func09(i)));
  };
  drawPath(svg09,pathData09,{"stroke":"#fff"},xScale09,yScale09);
  drawPath(svg091,pathData09,{"stroke":"#fff"},xScale09,yScale09);

  // lines
  lineData09 = [
    {"x1":0.5,"y1":0,"x2":0.5,"y2":func09(0.5),"stroke":"#f0f","opacity":0.6},
    {"x1":3.9,"y1":0,"x2":3.9,"y2":func09(3.9),"stroke":"#f0f","opacity":0.6},
    {"x1":1.57,"y1":0,"x2":1.57,"y2":func09(1.57),"stroke":"#ff0","opacity":0.8},
    {"x1":0,"y1":func09(1.57),"x2":1.57,"y2":func09(1.57),"stroke":"#ff0","opacity":0.8},
    {"x1":3.14,"y1":0,"x2":3.14,"y2":func09(3.14),"stroke":"#0ff","opacity":0.8},
    {"x1":0,"y1":func09(3.14),"x2":3.14,"y2":func09(3.14),"stroke":"#0ff","opacity":0.8},
  ];
  drawLine(svg09,lineData09,xScale09,yScale09);
  drawLine(svg091,lineData09,xScale09,yScale09);

  // circle
  var circleData09 = [
    {"cx":3.14/2,"cy":func09(3.14/2),"r":2,"stroke":"#ff0","fillColor":"#ff0"},
    {"cx":3.14,"cy":func09(3.14),"r":2,"stroke":"#0ff","fillColor":"#0ff"}
  ];
  drawCircle(svg09,circleData09,xScale09,yScale09);
  // circle
  circleData091 = [
    {"cx":3.14/2,"cy":func09(3.14/2),"r":3,"stroke":"#fff","fillColor":"#333"},
    {"cx":3.14,"cy":func09(3.14),"r":3,"stroke":"#fff","fillColor":"#333"}
  ];
  drawCircle(svg091,circleData091,xScale09,yScale09);

  // mathjax
  foData09 = [
    {"x":0.4,
    "y":0.7,
    "text":"$$a$$",
    "fontSize":"18px"},
    {"x":3.8,
    "y":0.7,
    "text":"$$b$$",
    "fontSize":"18px"},
    {"x":1.56,
    "y":0.7,
    "text":"$$c$$",
    "fontSize":"18px"},
    {"x":3.13,
    "y":0.7,
    "text":"$$d$$",
    "fontSize":"18px"},
    {"x":-0.5,
    "y":1.3,
    "text":"$$f(c)$$",
    "fontSize":"16px"},
    {"x":-0.5,
    "y":5.3,
    "text":"$$f(d)$$",
    "fontSize":"16px"}
  ];

  drawMathjax(svg09,foData09,xScale09,yScale09);
  drawMathjax(svg091,foData09,xScale09,yScale09);

  // lines
  lineData092 = [
    {"x1":0.5,"y1":1,"x2":4,"y2":4,"stroke":"#fff"},
    {"x1":0.5,"y1":1,"x2":0.5,"y2":0,"stroke":"#f0f","opacity":0.6},
    {"x1":0,"y1":1,"x2":0.5,"y2":1,"stroke":"#f0f","opacity":0.8},
    {"x1":4,"y1":0,"x2":4,"y2":4,"stroke":"#0ff","opacity":0.8},
    {"x1":0,"y1":4,"x2":4,"y2":4,"stroke":"#0ff","opacity":0.8},
  ];
  drawLine(svg092,lineData092,xScale09,yScale09);
  circleData092 = [
    {"cx":0.5,"cy":1,"r":3,"stroke":"#fff","fillColor":"#333"},
    {"cx":4,"cy":4,"r":3,"stroke":"#fff","fillColor":"#333"}
  ];
  drawCircle(svg092,circleData092,xScale09,yScale09);

  // mathjax
  foData092 = [
    {"x":0.4,
    "y":0.7,
    "text":"$$a$$",
    "fontSize":"18px"},
    {"x":3.9,
    "y":0.7,
    "text":"$$b$$",
    "fontSize":"18px"},
    {"x":-0.5,
    "y":2.0,
    "text":"$$f(a)$$",
    "fontSize":"16px"},
    {"x":-0.5,
    "y":5.0,
    "text":"$$f(b)$$",
    "fontSize":"16px"}
  ];

  drawMathjax(svg092,foData092,xScale09,yScale09);

  // Relative minima and maxima
  var xScale10 = d3.scale.linear()
                       .domain([-1,10])
                       .range([50,450]);

  var yScale10 = d3.scale.linear()
                       .domain([10,-1])
                       .range([50,450]);

  // 軸
  axesData10 = {
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
    "xScale":xScale10,
    "yScale":yScale10
  };
  drawAxes(svg10,axesData10);

  var pathData10 =[];
  function func10(i){
    return (-Math.pow(i,3)*7+107*i*i-481*i+813)/48;
  }
  for (var i=1;i<=9;i=i+0.1){
    pathData10.push(new Point(i,func10(i)));
  };
  drawPath(svg10,pathData10,{"stroke":"#fff"},xScale10,yScale10);

  // lines
  lineData10 = [
  {"x1":1,"y1":0,"x2":1,"y2":9,"stroke":"#f0f","opacity":0.6},
  {"x1":0,"y1":9,"x2":1,"y2":9,"stroke":"#f0f","opacity":0.8},
  {"x1":9,"y1":0,"x2":9,"y2":1,"stroke":"#0ff","opacity":0.8},
  {"x1":0,"y1":1,"x2":9,"y2":1,"stroke":"#0ff","opacity":0.8},
  {"x1":3.3,"y1":0,"x2":3.3,"y2":2.9,"stroke":"#ff0","opacity":0.8},
  {"x1":0,"y1":2.9,"x2":3.3,"y2":2.9,"stroke":"#ff0","opacity":0.8},
  {"x1":6.9,"y1":0,"x2":6.9,"y2":6,"stroke":"#ff0","opacity":0.8},
  {"x1":0,"y1":6,"x2":6.9,"y2":6,"stroke":"#ff0","opacity":0.8},
  ];
  drawLine(svg10,lineData10,xScale10,yScale10);

  // mathjax
  foData10 = [
  {"x":0.9,
  "y":1,
  "text":"$$a$$",
  "fontSize":"18px"},
  {"x":8.9,
  "y":1,
  "text":"$$b$$",
  "fontSize":"18px"},
  {"x":3.2,
  "y":1,
  "text":"$$c$$",
  "fontSize":"18px"},
  {"x":6.8,
  "y":1,
  "text":"$$d$$",
  "fontSize":"18px"},
  {"x":-1,
  "y":10.5,
  "text":"$$f(a)$$",
  "fontSize":"16px"},
  {"x":-1,
  "y":2.5,
  "text":"$$f(b)$$",
  "fontSize":"16px"},
  {"x":-1,
  "y":4.5,
  "text":"$$f(c)$$",
  "fontSize":"16px"},
  {"x":-1,
  "y":7.5,
  "text":"$$f(d)$$",
  "fontSize":"16px"},
  {"x":8.9,
  "y":5,
  "text":"$$f(x)$$",
  "fontSize":"16px"}
  ];

  drawMathjax(svg10,foData10,xScale10,yScale10);

  /** CONCAVITY **/
  var xScale11 = d3.scale.linear()
  .domain([-1,8])
  .range([50,450]);

  var yScale11 = d3.scale.linear()
  .domain([10,-10])
  .range([50,450]);
  // 軸
  axesData11 = {
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
    "xScale":xScale11,
    "yScale":yScale11
  };

  drawAxes(svg11,axesData11);
  var pathData11_1 =[];
  var pathData11_2 =[];
  var pathData11_3 =[];
  function func11_1(i){
    return Math.pow(i,3)/3-4*i*i+10*i+4;
  }
  function func11_2(i){
    return Math.pow(i,2)-8*i+10;
  }
  function func11_3(i){
    return 2*i-8;
  }

  for (var i=0;i<=8;i=i+0.1){
    pathData11_1.push(new Point(i,func11_1(i)));
  };
  drawPath(svg11,pathData11_1,{"stroke":"#fff"},xScale11,yScale11);
  for (var i=0;i<=8;i=i+0.1){
    pathData11_2.push(new Point(i,func11_2(i)));
  };
  drawPath(svg11,pathData11_2,{"stroke":"#f0f"},xScale11,yScale11);

  for (var i=0;i<=8;i=i+0.1){
    pathData11_3.push(new Point(i,func11_3(i)));
  };
  drawPath(svg11,pathData11_3,{"stroke":"#0f0"},xScale11,yScale11);

  lineData11 = [
    {"x1":4-Math.sqrt(6),"y1":0,
     "x2":4-Math.sqrt(6),"y2":func11_1(4-Math.sqrt(6)),
     "stroke":"#f0f","opacity":0.5},
    {"x1":4+Math.sqrt(6),"y1":0,
     "x2":4+Math.sqrt(6),"y2":func11_1(4+Math.sqrt(6)),
     "stroke":"#f0f","opacity":0.5},
  ]
  drawLine(svg11,lineData11,xScale11,yScale11);

  circleData11 = [
    {"cx":4-Math.sqrt(6),"cy":func11_1(4-Math.sqrt(6)),
     "r":3,"stroke":"#ff0","fillColor":"#ff0"},
    {"cx":4+Math.sqrt(6),"cy":func11_1(4+Math.sqrt(6)),
     "r":3,"stroke":"#ff0","fillColor":"#ff0"},
  ]
  drawCircle(svg11,circleData11,xScale11,yScale11);

  // mathjax
  foData11 = [
  {"x":0.9,
  "y":-3.3,
  "text":"$$f''(x)$$",
  "fontSize":"18px"},
  {"x":3.2,
  "y":11.5,
  "text":"$$f(x)$$",
  "fontSize":"16px"},
  {"x":7,
  "y":5,
  "text":"$$f'(x)$$",
  "fontSize":"16px"}
  ];

  drawMathjax(svg11,foData11,xScale11,yScale11);

  /** An inflection point **/
  drawAxes(svg12,axesData11);
  drawPath(svg12,pathData11_1,{"stroke":"#fff"},xScale11,yScale11);
  drawPath(svg12,pathData11_2,{"stroke":"#f0f"},xScale11,yScale11);
  drawPath(svg12,pathData11_3,{"stroke":"#0f0"},xScale11,yScale11);
  lineData12 = [
    {"x1":4,"y1":0,
     "x2":4,"y2":func11_1(4),
     "stroke":"#f0f","opacity":0.5},
    {"x1":4,"y1":0,
     "x2":4,"y2":func11_2(4),
     "stroke":"#f0f","opacity":0.5},
  ]
  drawLine(svg12,lineData12,xScale11,yScale11);
  circleData12 = [
    {"cx":4,"cy":func11_1(4),
     "r":3,"stroke":"#ff0","fillColor":"#ff0"},
  ]

  drawCircle(svg12,circleData12,xScale11,yScale11);
  drawMathjax(svg12,foData11,xScale11,yScale11);

  /**
    OPTIMIZATION WITH CALCULUS
  **/

</script>
