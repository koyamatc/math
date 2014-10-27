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

## Ratio between concentric arcs

<div class="row">
  <div class="col-sm-5">
    <div id="svg03"></div>
  </div>
  <div class="col-sm-7">
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

  // TEXT
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
  path1Attr02 = {"id":"path1","stroke":"#f00","opacity":"1"};
  path2Attr02 = {"id":"path2","stroke":"#0f0","opacity":"0"};
  path3Attr02 = {"id":"path3","stroke":"#ff0","opacity":"0"};
  path4Attr02 = {"id":"path4","stroke":"#f0f","opacity":"0"};
  drawPath2(svg02,graph1Data02,path1Attr02,xScale02,yScale02);
  drawPath2(svg02,graph2Data02,path2Attr02,xScale02,yScale02);
  drawPath2(svg02,graph3Data02,path3Attr02,xScale02,yScale02);
  drawPath2(svg02,graph4Data02,path4Attr02,xScale02,yScale02);

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
    {"x":15,"y":1.2,"text":"y","stroke":"#ff0","fontSize":"18px"},
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
  drawPath2(svg03,graph1Data03,path1Attr03,xScale03,yScale03);
  drawPath2(svg03,graph2Data03,path2Attr03,xScale03,yScale03);

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


</script>
