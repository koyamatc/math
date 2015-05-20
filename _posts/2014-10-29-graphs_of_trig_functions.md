---
title: Trigonometry
layout: post
postTitle: Graphs of trig functions
categories: trig
---

------

## Midline, amplitude and period of a function

<div class="row">
  <div class="col-sm-6">
    <div id="svg01"></div>
  </div>
  <div class="col-sm-6">
    <h3>midline</h3>
    最大値と最小値の中間値を通る線（左図　y=1の緑の直線）
    <h3>amplitude（振幅）</h3>
    中間値から最大値または最小値までの長さ（左図ピンクの線）
    <h3>period（周期）</h3>
    <p>
    繰り返される曲線の中で、ある位置から次の同じ位置までの長さ
    </p>
    <p>y=1の点で見ると、x=0の次のプラス方向の点はx=1のときですが、
      x=0では曲線はyの値が増加する方向に進み、x=1では減少する方向に進んでいます。
      なので、x=0の次の同じ位置の点はx=2のときになります。
    </p>
  </div>
</div>

--------

## Example of amplitude and period

<div class="row">
  <div class="col-sm-6">
    <div id="svg02"></div>
  </div>
  <div class="col-sm-6">
    $$左図の赤い曲線は y = sin(x) です$$
    <div class="btn-group-vertical">
      ボタンを押してください。
      <button type="button" id="runPath2" class="btn btn-primary" data-toggle="button"><h3>$$y = -sin(x)$$</h3></button>
      <button type="button" id="runPath3" class="btn btn-primary" data-toggle="button"><h3>$$y = 2sin(x)$$<h3></button>
      <button type="button" id="runPath4" class="btn btn-primary" data-toggle="button"><h3>$$y = sin(3x)$$<h3></button>
    </div>
  </div>
</div>

--------

## Intersection of sine and cosine 

<div class="row">
  <div class="col-sm-6">
    <div id="svg03"></div>
  </div>
  <div class="col-sm-6">
    $$0 \ge \theta \ge 2\piのとき$$
    $$y=sin\theta とy=cos\theta が交差する点はいくつか？$$
    $$左図を見ると２か所$$
    $$0 \ge \theta \ge \frac{\pi}{2}の間と
    \pi\ge\theta\ge\frac{3}{4}\piの間$$
  </div>
</div>

<div class="row">
  <div class="col-sm-6">
    <div id="svg04"></div>
  </div>
  <div class="col-sm-6">
    単位円でみてみると
    $$交点の１つは、0 \ge \theta \ge \frac{\pi}{2}で
    \theta=\frac{\pi}{4}radで、$$
    $$\sin\theta = \cos\thetaなので y = x = a　とすると$$
    $$ a^2 + a^2 = 1^2(ピタゴラスの定理)$$
    $$2a^2 = 1$$
    $$a^2 = \frac{1}{2}$$
    $$a = \frac{1}{\sqrt{2}}
    =\frac{1}{\sqrt{2}} \cdot \frac{\sqrt{2}}{\sqrt{2}}
    =\frac{\sqrt{2}}{2}$$
    $$（\frac{\sqrt{2}}{2},\frac{\sqrt{2}}{2})の点です$$
    $$もう１つの交点は、\pi\ge\theta\ge\frac{3}{4}\piで、
    \theta=\pi + \frac{\pi}{4}=\frac{5\pi}{4}rad$$
    $$（-\frac{\sqrt{2}}{2},-\frac{\sqrt{2}}{2})の点です$$

  </div>
</div>

--------

## Tangent graph

<div class="row">
  <div class="col-sm-6">
    <div id="svg05"></div>
  </div>
  <div class="col-sm-6">
    $$y=\tan\theta=\frac{\sin\theta}{\cos\theta}$$
    $$単位円でみれば、角度\thetaのベクトルの傾きです\frac{\triangle y}{\triangle x}$$
    $$\thetaが\frac{\pi}{2}に近づいていくと傾きは限りなく大きくなり\inftyに近づく$$
    $$\thetaが-\frac{\pi}{2}に近づいていくと傾きは限りなく小さくなり-\inftyに近づく$$
    $$-\frac{\pi}{2}\lt \theta \lt \frac{\pi}{2}において
    -\infty \lt\tan \theta \lt \inftyである$$
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
  drawPath(svg01,graphData01,{"stroke":"#f00"},xScale01,yScale01);
 
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

  // TEXT
  var textData01 = [
    {"x":-450,"y":-0.4,"text":"2.5","stroke":"#ff0","fontSize":"18px","anchor":"middle"},
    {"x":-360,"y":-0.4,"text":"2.0","stroke":"#ff0","fontSize":"18px","anchor":"middle"},
    {"x":-270,"y":-0.4,"text":"1.5","stroke":"#ff0","fontSize":"18px","anchor":"middle"},
    {"x":-180,"y":-0.4,"text":"1.0","stroke":"#ff0","fontSize":"18px","anchor":"middle"},
    {"x":-90,"y":-0.4,"text":"-0.5","stroke":"#ff0","fontSize":"18px","anchor":"middle"},
    {"x":90,"y":-0.4,"text":"0.5","stroke":"#ff0","fontSize":"18px","anchor":"middle"},
    {"x":180,"y":-0.4,"text":"1.0","stroke":"#ff0","fontSize":"18px","anchor":"middle"},
    {"x":270,"y":-0.4,"text":"1.5","stroke":"#ff0","fontSize":"18px","anchor":"middle"},
    {"x":360,"y":-0.4,"text":"2.0","stroke":"#ff0","fontSize":"18px","anchor":"middle"},
    {"x":450,"y":-0.4,"text":"2.5","stroke":"#ff0","fontSize":"18px","anchor":"middle"},
    {"x":540,"y":-0.4,"text":"3.0","stroke":"#ff0","fontSize":"18px","anchor":"middle"},
  ];
  drawText(svg01,textData01,xScale01,yScale01);

/**  Example of amplitude and period  */
  var svg02 = d3.select("#svg02")
                .append("svg")
                .attr("height",height)
                .attr("width",width)
                .style("background","#000");

  var xScale02 = d3.scale.linear()
                       .domain([-360,360])
                       .range([20,480]);
  
  var yScale02 = d3.scale.linear()
                       .domain([2,-2])
                       .range([20,480]);       

  // 軸
  axesData02 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[],
    "yTickValues":[-2,-1,-0.5,0.5,1,1.5,2],
    "stroke":"#ff0",
    "strokeWidth":1,
    "xScale":xScale02,
    "yScale":yScale02
  };
  
  drawAxes(svg02,axesData02);

  // mathjax
  var foData02 = [
    {"x":15,"y":2.4,"text":"y","stroke":"#ff0","fontSize":"18px"},
    {"x":360,"y":0.5,"text":"x","stroke":"#ff0","fontSize":"18px"},
    {"x":-380,"y":0.25,"text":"$$-2\\pi$$","stroke":"#ff0","fontSize":"16px"},
    {"x":-310,"y":0.25,"text":"$$-\\frac{3}{4}\\pi$$","stroke":"#ff0","fontSize":"16px"},
    {"x":-200,"y":0.25,"text":"$$-\\pi$$","stroke":"#ff0","fontSize":"16px"},
    {"x":-130,"y":0.25,"text":"$$-\\frac{\\pi}{2}$$","stroke":"#ff0","fontSize":"16px"},
    {"x":80,"y":0.25,"text":"$$\\frac{\\pi}{2}$$","stroke":"#ff0","fontSize":"16px"},
    {"x":170,"y":0.25,"text":"$$\\pi$$","stroke":"#ff0","fontSize":"16px"},
    {"x":260,"y":0.25,"text":"$$\\frac{3}{4}\\pi$$","stroke":"#ff0","fontSize":"16px"},
    {"x":350,"y":0.25,"text":"$$2\\pi$$","stroke":"#ff0","fontSize":"16px"}
  ];
  drawMathjax(svg02,foData02,xScale02,yScale02);
 
  // graph
  var graph1Data02 = [];   
  var graph2Data02 = [];   
  var graph3Data02 = [];  
  var graph4Data02 = [];   

  for (var i=-360;i<=360;i++){
    graph1Data02.push(new Point(i,Math.sin(aDegree*i)));
    graph2Data02.push(new Point(i,-Math.sin(aDegree*i)));
    graph3Data02.push(new Point(i,Math.sin(aDegree*i)*2));
    graph4Data02.push(new Point(i,Math.sin(aDegree*i*3)));
  };
  path1Attr02 = {"_id":"path1","stroke":"#f00","opacity":"1"};
  path2Attr02 = {"_id":"path2","stroke":"#0f0","opacity":"0"};
  path3Attr02 = {"_id":"path3","stroke":"#ff0","opacity":"0"};
  path4Attr02 = {"_id":"path4","stroke":"#f0f","opacity":"0"};
  drawPath(svg02,graph1Data02,path1Attr02,xScale02,yScale02);
  drawPath(svg02,graph2Data02,path2Attr02,xScale02,yScale02);
  drawPath(svg02,graph3Data02,path3Attr02,xScale02,yScale02);
  drawPath(svg02,graph4Data02,path4Attr02,xScale02,yScale02);

  var gridData02 = 
  {
    "xGrid":true,
    "yGrid":true,
    "xStep":90,
    "yStep":1,
    "stroke":"#0f0",
    "strokeWidth":1,
    "opacity":0.3,
    "xScale":xScale02,
    "yScale":yScale02
    };
  drawGrid(svg02,gridData02);

  d3.select("#runPath2").on("click",function(){
    var btnState =  svg02.select("#path2").attr("opacity")==0?true:false;
    if (btnState){
      svg02.select("#path2")
        .transition()
        .duration(1000)
        .attr("opacity",1);
    } else {
      svg02.select("#path2")
        .transition()
        .duration(1000)
        .attr("opacity",0);
    } 
  });
  d3.select("#runPath3").on("click",function(){
    var btnState =  svg02.select("#path3").attr("opacity")==0?true:false;
    if (btnState){
      svg02.select("#path3")
        .transition()
        .duration(1000)
        .attr("opacity",1);
    } else {
      svg02.select("#path3")
        .transition()
        .duration(1000)
        .attr("opacity",0);
    } 
  });
  d3.select("#runPath4").on("click",function(){
    var btnState =  svg02.select("#path4").attr("opacity")==0?true:false;
    if (btnState){
      svg02.select("#path4")
        .transition()
        .duration(1000)
        .attr("opacity",1);
    } else {
      svg02.select("#path4")
        .transition()
        .duration(1000)
        .attr("opacity",0);
    } 
  });

/**  Intersections of sine curve and cosine curve  */
  var svg03 = d3.select("#svg03")
                .append("svg")
                .attr("height",height)
                .attr("width",width)
                .style("background","#000");

  var xScale03 = d3.scale.linear()
                       .domain([0,360])
                       .range([50,450]);
  
  var yScale03 = d3.scale.linear()
                       .domain([1,-1])
                       .range([50,450]);       

  // 軸
  axesData03 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[],
    "yTickValues":[-1,-0.5,0.5,1],
    "stroke":"#ff0",
    "strokeWidth":1,
    "xScale":xScale03,
    "yScale":yScale03
  };
  
  drawAxes(svg03,axesData03);

  // TEXT
  var foData03 = [
    {"x":0,"y":1.5,"text":"$$y$$","stroke":"#ff0","fontSize":"18px"},
    {"x":380,"y":0.3,"text":"$$\\theta$$","stroke":"#ff0","fontSize":"18px"},
    {"x":80,"y":0.2,"text":"$$\\frac{\\pi}{2}$$","stroke":"#ff0","fontSize":"16px"},
    {"x":170,"y":0.2,"text":"$$\\pi$$","stroke":"#ff0","fontSize":"16px"},
    {"x":260,"y":0.2,"text":"$$\\frac{3}{4}\\pi$$","stroke":"#ff0","fontSize":"16px"},
    {"x":350,"y":0.2,"text":"$$2\\pi$$","stroke":"#ff0","fontSize":"16px"},
    {"x":150,"y":1.0,"text":"$$y=sin\\theta$$","stroke":"#ff0","fontSize":"16px"},
    {"x":320,"y":1.0,"text":"$$y=cos\\theta$$","stroke":"#ff0","fontSize":"16px"}
  ];
  drawMathjax(svg03,foData03,xScale03,yScale03);
 
  // graph
  var graph1Data03 = [];   
  var graph2Data03 = [];   

  for (var i=0;i<=360;i++){
    graph1Data03.push(new Point(i,Math.sin(aDegree*i)));
    graph2Data03.push(new Point(i,Math.cos(aDegree*i)));
  };
  path1Attr03 = {"id":"path1","stroke":"#f00"};
  path2Attr03 = {"id":"path2","stroke":"#0f0"};
  drawPath(svg03,graph1Data03,path1Attr03,xScale03,yScale03);
  drawPath(svg03,graph2Data03,path2Attr03,xScale03,yScale03);

  var gridData03 = 
  {
    "xGrid":true,
    "yGrid":true,
    "xStep":90,
    "yStep":0.2,
    "stroke":"#0f0",
    "strokeWidth":1,
    "opacity":0.3,
    "xScale":xScale03,
    "yScale":yScale03
    };
  drawGrid(svg03,gridData03);

  var svg04 = d3.select("#svg04")
                .append("svg")
                .attr("height",height)
                .attr("width",width)
                .style("background","#000");

  var xScale04 = d3.scale.linear()
                       .domain([-1,1])
                       .range([50,450]);
  
  var yScale04 = d3.scale.linear()
                       .domain([1,-1])
                       .range([50,450]);       

  // 軸
  axesData04 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[-1,1],
    "yTickValues":[-1,1],
    "stroke":"#ff0",
    "strokeWidth":1,
    "xScale":xScale04,
    "yScale":yScale04
  };
  
  drawAxes(svg04,axesData04);

  // unit circle
  circleData04 = [{
    "cx":0,
    "cy":0,
    "r":200,
    "stroke":"#fff",
    "strokeWidth":3
  }];

  drawCircle(svg04,circleData04,xScale04,yScale04);

  //path
  pathData04 = [
    {"x":Math.sqrt(2)/2,"y":0},
    {"x":Math.sqrt(2)/2,"y":Math.sqrt(2)/2},
    {"x":-Math.sqrt(2)/2,"y":-Math.sqrt(2)/2},
    {"x":-Math.sqrt(2)/2,"y":0}
  ];

  drawPath(svg04,pathData04,{"stroke":"#ff0"},xScale04,yScale04);

 // mathjax
 var foData04 = [
    {"x":0,"y":1.4,"text":"$$y$$","fontSize":"18px"},
    {"x":1.1,"y":0.3,"text":"$$x$$","fontSize":"18px"},
    {"x":0.3,"y":0.2,"text":"$$a$$","fontSize":"18px"},
    {"x":0.75,"y":0.6,"text":"$$a$$","fontSize":"18px"},
    {"x":0.1,"y":0.35,"text":"$$45^\\circ$$","fontSize":"16px"},
    {"x":-0.5,"y":0.5,"text":"$$225^\\circ$$","fontSize":"16px"},
    {"x":-1.2,"y":-0.6,
    "text":"$$（-\\frac{\\sqrt{2}}{2},-\\frac{\\sqrt{2}}{2})$$","fontSize":"12px"},
    {"x":0.7,"y":1.1,
    "text":"$$（\\frac{\\sqrt{2}}{2},\\frac{\\sqrt{2}}{2})$$","fontSize":"12px"},
  ];
 drawMathjax(svg04,foData04,xScale04,yScale04);

 arcData04 = [
  { 
    "startPos":90,
    "endPos":45,
    "innerRadius":50,
    "outerRadius":50,
    "stroke":"#f00"}
  ,{ 
    "startPos":90,
    "endPos":-135,
    "innerRadius":80,
    "outerRadius":80,
    "stroke":"#0f0"}
 ];
 drawArc(svg04,arcData04,xScale04,yScale04);

 /** 
    graph of tangent
                      */

  var svg05 = d3.select("#svg05")
                .append("svg")
                .attr("height",height)
                .attr("width",width)
                .style("background","#000");

  var xScale05 = d3.scale.linear()
                       .domain([-360,360])
                       .range([20,480]);
  
  var yScale05 = d3.scale.linear()
                       .domain([4,-4])
                       .range([20,480]);

  var gridData05 = 
  {
    "xGrid":true,
    "yGrid":true,
    "xStep":90,
    "yStep":1,
    "stroke":"#0f0",
    "strokeWidth":1,
    "opacity":0.3,
    "xScale":xScale05,
    "yScale":yScale05
    };
  drawGrid(svg05,gridData05);

  // 軸
  axesData05 = {
    "xAxis":true,
    "yAxis":true,
    "xTickValues":[],
    "yTickValues":[-4,-2,2,4],
    "stroke":"#ff0",
    "strokeWidth":1,
    "xScale":xScale05,
    "yScale":yScale05
  };


  drawAxes(svg05,axesData05);
  
  var tan1Data05 = [];
  var tan2Data05 = [];
  var tan3Data05 = [];
  var tan4Data05 = [];
  var tan5Data05 = [];

  for (var i = -89; i < 90; i++) {
       tan1Data05.push(new Point(i-180,Math.tan((i-180)*aDegree)));
       tan2Data05.push(new Point(i,Math.tan(i*aDegree)));
       tan3Data05.push(new Point(i+180,Math.tan((i+180)*aDegree)));
       tan4Data05.push(new Point(i+360,Math.tan((i+360)*aDegree)));
       tan5Data05.push(new Point(i-360,Math.tan((i-360)*aDegree)));
  };              

  drawPath(svg05,tan1Data05,{"stroke":"#f0f"},xScale05,yScale05);
  drawPath(svg05,tan2Data05,{"stroke":"#f0f"},xScale05,yScale05);
  drawPath(svg05,tan3Data05,{"stroke":"#f0f"},xScale05,yScale05);
  drawPath(svg05,tan4Data05,{"stroke":"#f0f"},xScale05,yScale05);
  drawPath(svg05,tan5Data05,{"stroke":"#f0f"},xScale05,yScale05);

  // mathjax
  var foData05 = [
    {"x":15,"y":4.9,"text":"$$y$$","stroke":"#ff0","fontSize":"18px"},
    {"x":360,"y":0.8,"text":"$$\\theta$$","stroke":"#ff0","fontSize":"18px"},
    {"x":-380,"y":0.25,"text":"$$-2\\pi$$","stroke":"#ff0","fontSize":"16px"},
    {"x":-310,"y":0.25,"text":"$$-\\frac{3}{4}\\pi$$","stroke":"#ff0","fontSize":"16px"},
    {"x":-200,"y":0.25,"text":"$$-\\pi$$","stroke":"#ff0","fontSize":"16px"},
    {"x":-130,"y":0.25,"text":"$$-\\frac{\\pi}{2}$$","stroke":"#ff0","fontSize":"16px"},
    {"x":80,"y":0.25,"text":"$$\\frac{\\pi}{2}$$","stroke":"#ff0","fontSize":"16px"},
    {"x":170,"y":0.25,"text":"$$\\pi$$","stroke":"#ff0","fontSize":"16px"},
    {"x":260,"y":0.25,"text":"$$\\frac{3}{4}\\pi$$","stroke":"#ff0","fontSize":"16px"},
    {"x":350,"y":0.25,"text":"$$2\\pi$$","stroke":"#ff0","fontSize":"16px"}
  ];

  drawMathjax(svg05,foData05,xScale05,yScale05);
</script>
