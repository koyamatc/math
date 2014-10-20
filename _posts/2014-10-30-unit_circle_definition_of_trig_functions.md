---
title: Trigonometry
layout: post
postTitle: Unit circle definition of trig functions
categories: trig
---

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
    $$\overline{AB}の長さと\overline{CD}の長さの比率は$$
    $$\frac{\overline{CD}}{\overline{AB}}=\frac{5}{9}$$
  </div>
</div>

三角形の内角の和は１８０°　→　角Ｂ=90°なので　角Ａ　+ 角Ｃ = 90°

$$ \theta = 90° - \angle C = 90° - 58° = 32°$$

$$cos58°=\frac{BC}{AC}, \quad 
sin32°=\frac{BC}{AC}$$ 
$$\therefore$$
$$sin32°=cos58° \approx 0.53$$

<h3 class="panel">
$$sin\theta = cos(90°-\theta)$$
$$cos\theta = sin(90°-\theta)$$
</h3>

--------

## Secant(sec), cosecant(csc) and cotangent(cot)

<div class="row">
  <div class="col-sm-5">
    <div id="svg04"></div>
  </div>
  <div class="col-sm-7">
    <table class="table">
      <tr>
        <th>$$sin\theta$$</th>
        <th>$$cos\theta$$</th>
        <th>$$tan\theta$$</th>
      </tr>
      <tr>
        <td>$$\frac{opp}{hyp}=\frac{12}{13}$$</td>
        <td>$$\frac{adj}{hyp}=\frac{5}{13}$$</td>
        <td>$$\frac{opp}{adj}=\frac{12}{5}$$</td>
      </tr>
      <tr>
        <th colspan="3">
        Reciprocal trig functions
        </th>
      </tr>
      <tr>
        <th>$$csc\theta$$</th>
        <th>$$sec\theta$$</th>
        <th>$$cot\theta$$</th>
      </tr>
      <tr>
        <td>$$\frac{hyp}{opp}=\frac{13}{12}$$</td>
        <td>$$\frac{hyp}{adj}=\frac{13}{5}$$</td>
        <td>$$\frac{adj}{opp}=\frac{5}{12}$$</td>
      </tr>
    </table>
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


</script>
