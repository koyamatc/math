---
title: Trigonometry
layout: post
postTitle: Symmetry and periodicity trig functions 
categories: trig
---

# Symmetry and periodicity of trig functions

------

## Symmetry of trig values

<div class="row">
  <div class="col-sm-9">
    <div id="svg01"></div>
  </div>
  <div class="col-sm-3">
    <p>単位円において、４本のベクトルが単位円と交わる点の相互関係</p>
  </div>
</div>

--------

## Relating trig functions through angle rotations

<div class="row">
  <div class="col-sm-8">
    <div id="svg02"></div>
  </div>
  <div class="col-sm-4">
    $$角度\thetaのベクトルを反時計回りに\frac{\pi}{2}回転する$$
    $$２つの単位円との交点の関係を表すと$$
    $$\cos(\theta)=\sin(\frac{\pi}{2}+\theta)$$
    $$\sin(\theta)=-\cos(\frac{\pi}{2}+\theta)$$
    $$\tan(\theta)=-\frac{1}{\tan(\frac{\pi}{2}+\theta)}$$  
    $$\quad \tan(\frac{\pi}{2}+\theta)
    =\frac{\sin(\frac{\pi}{2}+\theta)}{\cos(\frac{\pi}{2}+\theta)}$$
    $$\qquad =\frac{\cos(\theta)}{-\sin(\theta)}
    =-\frac{1}{\tan(\theta)}$$

  </div>
</div>

--------

# Pythagorean identity 

------

## Pythagorean trig identity from soh cah toa

<div class="row">
  <div class="col-sm-6">
    <div id="svg03"></div>
  </div>
  <div class="col-sm-6">
    正三角形があります各辺を a, b, c とすると
    $$a^2 + b^2 = c^2 \quad です$$
    $$\angle acを\thetaとすると$$
    $$\sin\theta = \frac{b}{c} \quad \cos\theta = \frac{a}{c} \to
    \sin^2\theta = \frac{b^2}{c^2} \quad \cos^2\theta = \frac{a^2}{c^2}$$
    $$\sin^2\theta + \cos^2\theta = \frac{b^2}{c^2} + \frac{a^2}{c^2}
    =\frac{b^2 + a^2}{c^2}=\frac{c^2}{c^2}=1$$
    <div class="panel">
      <h3>$$\sin^2\theta + \cos^2\theta = 1$$</h3>
    </div>
  </div>
</div>

--------

## Pythagorean trig identity from unit circle

<div class="row">
  <div class="col-sm-6">
    <div id="svg04"></div>
  </div>
  <div class="col-sm-6">
    $$x=\cos\theta \quad y=\sin\theta$$
    $$x^2 + y^2 = 1$$
    $$\sin^2\theta + \cos^2\theta = 1$$


  </div>
</div>


--------
# Angle addition formulas
--------

## Applying angle addition formula for sin

<div class="row">
  <div class="col-sm-6">
    <div id="svg05"></div>
  </div>
  <div class="col-sm-6">
  </div>
</div>



<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_SVG"></script>
<script src="http://d3js.org/d3.v3.min.js" charset="utf-8"></script>
<script src="{{site.url}}/js/d3draws.js" charset="utf-8"></script>

<script>

  var height = 500;
  var width = 800;
  

/**  */
  var svg01 = d3.select("#svg01")
                .append("svg")
                .attr("height",height)
                .attr("width",800)
                .style("background","#000");

  var xScale01 = d3.scale.linear()
                       .domain([-1,1])
                       .range([200,600]);
  
  var yScale01 = d3.scale.linear()
                       .domain([1,-1])
                       .range([50,450]);       

  // 軸
  axesData01 = [
    {
      "x1":-1.1,
      "y1":0,
      "x2":1.1,
      "y2":0,
      "stroke":"#fff"
    },
    {
      "x1":0,
      "y1":-1.1,
      "x2":0,
      "y2":1.1,
      "stroke":"#fff"
    }
  ];
  drawVectorW(svg01,axesData01,xScale01,yScale01);

  // unit circle
  circleData01 = [
    {"cx":0,"cy":0,"r":200,"stroke":"#ff0"}
  ];
  drawCircle(svg01,circleData01,xScale01,yScale01); 

  // path
  pathData01 = [
    {"x":Math.cos(pi/6),"y":Math.sin(pi/6)},
    {"x":Math.cos(-pi/6),"y":Math.sin(-pi/6)},
    {"x":Math.cos(pi+pi/6),"y":Math.sin(pi+pi/6)},
    {"x":Math.cos(pi-pi/6),"y":Math.sin(pi-pi/6)},
    {"x":Math.cos(pi/6),"y":Math.sin(pi/6)},
  ];
  drawPath(svg01,pathData01,{"stroke":"#ccc","strokeWidth":1},xScale01,yScale01);
 
  // vector
  vecData01 = [
    {"x1":0,"y1":0,"angles":30,"length":1.2,"stroke":"lime"}
   ,{"x1":0,"y1":0,"angles":-30,"length":1.2,"stroke":"purple"}
   ,{"x1":0,"y1":0,"angles":150,"length":1.2,"stroke":"red"}
   ,{"x1":0,"y1":0,"angles":210,"length":1.2,"stroke":"orange"}
  ]
  drawVectorA(svg01,vecData01,xScale01,yScale01);

  // mathjax
  var foData01 = [
    {"x":0,"y":1.5,"text":"$$y$$","fontSize":"20px"},
    {"x":1.2,"y":0.3,"text":"$$x$$","fontSize":"20px"},
    {"x":0.15,"y":0.33,"text":"$$\\theta$$","fontSize":"16px"},
    {"x":-0.2,"y":0.33,"text":"$$\\theta$$","fontSize":"16px"},
    {"x":-0.2,"y":0.23,"text":"$$\\theta$$","fontSize":"16px"},
    {"x":0.15,"y":0.22,"text":"$$-\\theta$$","fontSize":"16px"},
    {"x":-0.4,"y":0.85,"text":"$$\\pi-\\theta$$","fontSize":"16px"},
    {"x":-0.7,"y":0.1,"text":"$$\\pi+\\theta$$","fontSize":"16px"},

    {"x":0.9,"y":0.8,
      "text":"$$(\\cos(\\theta),\\sin (\\theta))$$","fontSize":"16px"},
    {"x":0.9,"y":-0.2,
      "text":"$$(\\cos(-\\theta),\\sin (-\\theta))$$","fontSize":"16px"},  
    {"x":-1.9,"y":0.8,
      "text":"$$(\\cos(\\pi-\\theta),\\sin (\\pi-\\theta))$$","fontSize":"16px"},
    {"x":-1.9,"y":-0.2,
      "text":"$$(\\cos(\\pi+\\theta),\\sin (\\pi+\\theta))$$","fontSize":"16px"},  

    {"x":-1.8,"y":1.25,
      "text":"$$\\cos(\\pi-\\theta)=-\\cos (\\theta)$$","fontSize":"16px"},  
    {"x":-1.8,"y":1.1,
      "text":"$$\\sin(\\pi-\\theta)=\\sin (\\theta)$$","fontSize":"16px"},  
    {"x":-1.8,"y":0.95,
      "text":"$$\\tan(\\pi-\\theta)=-\\tan (\\theta)$$","fontSize":"16px"},  

    {"x":-1.8,"y":-0.4,
      "text":"$$\\cos(\\pi+\\theta)=-\\cos (\\theta)$$","fontSize":"16px"},  
    {"x":-1.8,"y":-0.55,
      "text":"$$\\sin(\\pi+\\theta)=-\\sin (\\theta)$$","fontSize":"16px"},  
    {"x":-1.8,"y":-0.7,
      "text":"$$\\tan(\\pi+\\theta)=\\tan (\\theta)$$","fontSize":"16px"},  

    {"x":1.0,"y":-0.4,
      "text":"$$\\cos(-\\theta)=\\cos (\\theta)$$","fontSize":"16px"},  
    {"x":1.0,"y":-0.55,
      "text":"$$\\sin(-\\theta)=-\\sin (\\theta)$$","fontSize":"16px"},  
    {"x":1.0,"y":-0.7,
      "text":"$$\\tan(-\\theta)=-\\tan (\\theta)$$","fontSize":"16px"},  

  ];
  drawMathjax(svg01,foData01,xScale01,yScale01);

  // arc
  arcData01 = [
    {"startPos":90,"endPos":60,
    "innerRadius":50,"outerRadius":50,
    "stroke":"lime"},
    {"startPos":90,"endPos":120,
    "innerRadius":50,"outerRadius":50,
    "stroke":"purple"},
    {"startPos":90,"endPos":-60,
    "innerRadius":100,"outerRadius":100,
    "stroke":"red"},
    {"startPos":90,"endPos":-120,
    "innerRadius":80,"outerRadius":80,
    "stroke":"orange"}


  ];
  drawArc(svg01,arcData01,xScale01,yScale01);


/**  rotations  */
  var svg02 = d3.select("#svg02")
                .append("svg")
                .attr("height",height)
                .attr("width",width)
                .style("background","#000");

  // 軸
  drawVectorW(svg02,axesData01,xScale01,yScale01);

  // unit circle
  drawCircle(svg02,circleData01,xScale01,yScale01); 

  // vector
  vecData02 = [
    {"x1":0,"y1":0,"angles":30,"length":1.2,"stroke":"lime"}
   ,{"x1":0,"y1":0,"angles":120,"length":1.2,"stroke":"lime"}
  ]
  drawVectorA(svg02,vecData02,xScale01,yScale01);

  // lines
  lineData02 = [
    {
      "x1":Math.cos(30*aDegree),
      "y1":Math.sin(30*aDegree),
      "x2":Math.cos(30*aDegree),
      "y2":0,
      "stroke":"#999"
    }
   ,{
      "x1":Math.cos(120*aDegree),
      "y1":Math.sin(120*aDegree),
      "x2":0,
      "y2":Math.sin(120*aDegree),
      "stroke":"#999"
    }
   ,{
      "x1":0,
      "y1":0,
      "x2":Math.cos(30*aDegree),
      "y2":0,
      "stroke":"#f0f"
    }
   ,{
      "x1":0,
      "y1":0,
      "x2":0,
      "y2":Math.sin(120*aDegree),
      "stroke":"#f0f"
    }
  ]
  drawLine(svg02,lineData02,xScale01,yScale01);

  // arc
  arcData02 = [
    {
      "startPos":60,
      "endPos":-30,
      "innerRadius":40,
      "outerRadius":40,
      "stroke":"red"
    }
  ];
  drawArc(svg02,arcData02,xScale01,yScale01);

  // arrow head
  headData02 = [
   {
     "x1":Math.cos(120*aDegree)/5+0.00001,
     "y1":Math.sin(120*aDegree)/5+0.00001,
     "x2":Math.cos(120*aDegree)/5,
     "y2":Math.sin(120*aDegree)/5,
     "stroke":"red"}
  ]
  drawVectorB(svg02,headData02,xScale01,yScale01);

  // mathjax
  var foData02 = [
    {"x":0,"y":1.5,"text":"$$y$$","fontSize":"20px"},
    {"x":1.2,"y":0.3,"text":"$$x$$","fontSize":"20px"},
    
    {"x":0.15,"y":0.33,"text":"$$\\theta$$","fontSize":"16px"},

    {"x":0.9,"y":0.5,
      "text":"$$\\sin (\\theta)$$","fontSize":"16px"},
    {"x":0.4,"y":0.2,
      "text":"$$\\cos(\\theta)$$","fontSize":"16px"},

    {"x":0.9,"y":0.8,
      "text":"$$(\\cos(\\theta),\\sin (\\theta))$$","fontSize":"16px"},
    {"x":-1.7,"y":1.2,
      "text":"$$(\\cos(\\frac{\\pi}{2}+\\theta),\\sin (\\frac{\\pi}{2}+\\theta))$$",
      "fontSize":"16px"},
    {"x":0.05,"y":0.8,
      "text":"$$\\sin (\\frac{\\pi}{2}+\\theta)$$","fontSize":"16px"},
    {"x":-0.5,"y":1.4,
      "text":"$$\\cos (\\frac{\\pi}{2}+\\theta)$$","fontSize":"16px"},


  ];
  drawMathjax(svg02,foData02,xScale01,yScale01);
 


/**  Intersections of sine curve and cosine curve  */
  var svg03 = d3.select("#svg03")
                .append("svg")
                .attr("height",height)
                .attr("width",500)
                .style("background","#000");

  var xScale03 = d3.scale.linear()
                       .domain([50,450])
                       .range([50,450]);
  
  var yScale03 = d3.scale.linear()
                       .domain([450,50])
                       .range([50,450]);  

  //  right Triangle
  triData003 = [
    {"x1":100,"y1":150,
     "angle":0,"adjacent":300,"theta":35,
     "stroke":"#ff0","rightMark":true}
  ]                          
  drawRTriangle(svg03,triData003,xScale03,yScale03);

  // TEXT
  var foData03 = [
    {"x":250,"y":200,"text":"$$a$$","fontSize":"22px"},
    {"x":410,"y":290,"text":"$$b$$","fontSize":"22px"},
    {"x":250,"y":350,"text":"$$c$$","fontSize":"22px"},

    {"x":130,"y":225,"text":"$$\\theta$$","fontSize":"20px"},
  ];
  drawMathjax(svg03,foData03,xScale03,yScale03);
 

  //
  var svg04 = d3.select("#svg04")
                .append("svg")
                .attr("height",height)
                .attr("width",500)
                .style("background","#000");

  var xScale04 = d3.scale.linear()
                       .domain([-1,1])
                       .range([50,450]);
  
  var yScale04 = d3.scale.linear()
                       .domain([1,-1])
                       .range([50,450]);       

  // 軸
  drawVectorW(svg04,axesData01,xScale04,yScale04);

  // unit circle
  circleData04 = [{
    "cx":0,
    "cy":0,
    "r":200,
    "stroke":"#fff",
    "strokeWidth":3
  }];

  drawCircle(svg04,circleData04,xScale04,yScale04);

  // lines and vectors
  vecData04 = [
    {"x1":0,"y1":0,"angles":35,"length":1.2,"stroke":"lime"}
  ];
  drawVectorA(svg04,vecData04,xScale04,yScale04);

  lineData04 = [
    { 
      "x1":0,
      "y1":0,
      "x2":Math.cos(35*aDegree),
      "y2":0,
      "stroke":"#f0f","strokeWidth":3
    },
    { 
      "x1":Math.cos(35*aDegree),
      "y1":Math.sin(35*aDegree),
      "x2":Math.cos(35*aDegree),
      "y2":0,
      "stroke":"#ff0","strokeWidth":3
    },
  ];
  drawLine(svg04,lineData04,xScale04,yScale04);
 // mathjax
 var foData04 = [
    {"x":0,"y":1.5,"text":"$$y$$","fontSize":"18px"},
    {"x":1.1,"y":0.3,"text":"$$x$$","fontSize":"18px"},
    
    {"x":0.3,"y":0.2,"text":"$$\\cos\\theta$$","fontSize":"18px"},
    {"x":0.9,"y":0.6,"text":"$$\\sin\\theta$$","fontSize":"18px"},
    
    {"x":0.15,"y":0.32,"text":"$$\\theta$$","fontSize":"16px"},
  ];
 drawMathjax(svg04,foData04,xScale04,yScale04);


 /** 
    
                      */

  var svg05 = d3.select("#svg05")
                .append("svg")
                .attr("height",height)
                .attr("width",500)
                .style("background","#000");

  var xScale05 = d3.scale.linear()
                       .domain([-360,360])
                       .range([20,480]);
  
  var yScale05 = d3.scale.linear()
                       .domain([4,-4])
                       .range([20,480]);

</script>
