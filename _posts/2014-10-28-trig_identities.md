---
title: Trigonometry
layout: post
postTitle: Symmetry and periodicity trig functions 
categories: trig
---

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

## Angle addition formula for sine

<div class="row">
  <div class="col-sm-6">
    <div id="svg05"></div>
  </div>
  <div class="col-sm-6">
    <div class="panel">
      $$\sin(x+y) = \sin(x)\cos(y) + \cos(x)\sin(y)$$
    </div>
    $$\sin(x+y) = \overline{DF}
    =\overline{DE}+\overline{EF}
    =\overline{DE}+\overline{CB}$$
    $$\overline{EC} \parallel \overline{AB}$$
    $$\angle ECA = y, \quad
    90^{\circ}-\angle DCE = \angle CDE = y$$
    $$\overline{AC}=\cos(x)$$
    $$\sin(y)=\frac{\overline{CB}}{\overline{AC}}
    =\frac{\overline{CB}}{\cos{x}}
    \to \overline{CB}= \cos(x)\sin(y)$$
    $$\overline{DC}=\sin(x)$$
    $$\cos(y)=\frac{\overline{DE}}{\overline{DC}}
    =\frac{\overline{DE}}{\sin(x)}
    \to \overline{DE}= \sin(x)\cos(y)$$
    <h3>
      $$\sin(x+y) = \sin(x)\cos(y) + \cos(x)\sin(y)$$
    </h3>

  </div>
</div>

## Angle addition formula for cosine

<div class="row">
  <div class="col-sm-6">
    <div id="svg06"></div>
  </div>
  <div class="col-sm-6">
  <div class="panel">
    $$\cos(x+y) = \cos(x)\cos(y) - \sin(x)\sin(y)$$
  </div>
  $$\cos(x+y) = \overline{AF} = \overline{AB}-\overline{FB}
  =\overline{AB}-\overline{EC}$$
  $$\cos(y)=\frac{\overline{AB}}{\overline{AC}}
  =\frac{\overline{AB}}{\cos(x)}
  \to \overline{AB}=\cos(x)\cos(y)$$

  $$\sin(y)=\frac{\overline{EC}}{\overline{DC}}
  =\frac{\overline{EC}}{\sin(x)}
  \to \overline{EC}=\sin(x)\sin(y)$$
  <h3>
    $$\cos(x+y) = \cos(x)\cos(y) - \sin(x)\sin(y)$$
  </h3>

  </div>
</div>

--------
# Law of cosines and law of sines
--------

## Law of cosines 

<div class="row">
  <div class="col-sm-6">
    <div id="svg07"></div>
  </div>
  <div class="col-sm-6">
    緑の辺　b　と　c　に挟まれた角が　θ　のとき以下の法則が成り立つ
    <div class="panel">
      <h3>$$a^2=b^2+c^2-2bc\cos\theta$$</h3>
    </div>
    $$a^2=12^2+9^2-2(12)(9)\cos87^{\circ}$$
    $$\quad = 225-216\cos87^{\circ}$$
    $$a=\sqrt{225-216\cos87^{\circ}}\approx14.6$$
  </div>
</div>

## Law of sines 

<div class="row">
  <div class="col-sm-6">
    <div id="svg08"></div>
  </div>
  <div class="col-sm-6">
    左図のような三角形で
    <div class="panel">
      $$\frac{\sin30^{\circ}}{2}
      =\frac{\sin105^{\circ}}{a}
      =\frac{\sin45^{\circ}}{b}$$
    </div>
    が成り立つ
    $$\frac{\sin30^{\circ}}{2}=\frac{\frac{1}{2}}{2}=\frac{1}{4}$$
    なので
    $$\frac{\sin105^{\circ}}{a}=\frac{1}{4} \to 
    a=4 \cdot \sin105^{\circ}\approx 3.86$$
    $$\frac{\sin45^{\circ}}{b}=\frac{1}{4} \to 
    b=4 \cdot \sin45^{\circ} \approx1.83$$
  </div>
</div>

## Proof : Law of cosines 

<div class="row">
  <div class="col-sm-6">
    <div id="svg09"></div>
  </div>
  <div class="col-sm-6">
    <div class="panel">
      <h3>$$a^2=b^2+c^2-2bc\cos\theta$$</h3>
    </div>
    $$\cos \theta = \frac{d}{b} \to d=b\cos \theta$$
    $$e = c - d = c - b\cos \theta$$
    $$\sin \theta = \frac{m}{b} \to m=b\sin \theta$$
    $$a^2 = m^2 + e^2$$
    $$\quad = (b\sin\theta)^2 + (c - b\cos \theta)^2$$
    $$\quad = b^2\sin^2\theta + c^2 - 2bc\cos\theta + b^2\cos^2\theta$$
    $$\quad = b^2(\sin^2\theta + \cos^2\theta) + c^2 - 2bc\cos\theta$$
    $$\sin^2\theta + \cos^2\theta=1なので$$
    $$\underline{a^2 = b^2 + c^2 - 2bc\cos\theta}$$
  </div>
</div>

## Proof : Law of sines 

<div class="row">
  <div class="col-sm-6">
    <div id="svg10"></div>
  </div>
  <div class="col-sm-6">
    <div class="panel">
      <h3>$$\frac{\sin\alpha}{A}=\frac{\sin\beta}{B}$$</h3>
    </div>
    $$\sin\alpha = \frac{x}{B} \to B\sin\alpha = x$$
    $$\sin\beta = \frac{x}{A} \to A\sin\beta = x$$
    $$B\sin\alpha = A\sin\beta$$
    $$\underline{\frac{\sin\alpha}{A} = \frac{\sin\beta}{B}}$$
  </div>
</div>

## Trig identities review and fun
<div>
<h3>
<div class="panel">
$$\sin(a+b)=\sin(a) \cdot \cos(b) + \sin(b) \cdot \cos(a)$$
</div>
$$\sin(a+(-b))=\sin(a) \cdot \cos(-b) + \sin(-b) \cdot \cos(a)$$
$$\quad \cos(-b)=\cos(b), \quad \sin(-b)=-\sin(b)なので$$
<div class="panel">
$$\sin(a-b)=\sin(a) \cdot \cos(b) - \sin(b) \cdot \cos(a)$$
</div>
<div class="panel">
$$\sin(2a)=\sin(a+a)=2\sin(a)\cos(a)$$
</div>
<div class="panel">
$$\cos(a+b)=\cos(a) \cdot \cos(b) - \sin(a) \cdot \sin(b)$$
</div>
<div class="panel">
$$\cos(a-b)=\cos(a) \cdot \cos(b) + \sin(a) \cdot \sin(b)$$
</div>
<div class="panel">
$$\cos(2a)=\cos(a+a)=\cos^2(a) - \sin^2(a)$$
</div>

</h3>
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
   addition formula for sin 
                            */

  var svg05 = d3.select("#svg05")
                .append("svg")
                .attr("height",height)
                .attr("width",500)
                .style("background","#000");

  var xScale05 = d3.scale.linear()
                       .domain([0,1])
                       .range([50,450]);
  
  var yScale05 = d3.scale.linear()
                       .domain([1,0])
                       .range([50,450]);

  triangleData05 = [
    {"x1":0,"y1":0,"angle":0,"adjacent":400,"theta":30,"stroke":"#0f0","strokeWidth":3,"rightMark":true},
    {"x1":0,"y1":0,"angle":30,"adjacent":462,"theta":25,"stroke":"#f0f","strokeWidth":3,"rightMark":true},
    {"x1":0.728,"y1":1.038,"angle":-90,"adjacent":181,"theta":30,"stroke":"#f0f","strokeWidth":3,"rightMark":true},
    {"x1":0,"y1":0,"angle":0,"adjacent":291,"theta":55,"stroke":"#ff0","strokeWidth":3,"rightMark":true}

  ];

  drawRTriangle(svg05,triangleData05,xScale05,yScale05);                       

  // mathjax
  foData05 = [
    {"x":-0.05,"y":0.09,"text":"$$A$$","fontSize":"18px"}
   ,{"x":1.02,"y":0.1,"text":"$$B$$","fontSize":"18px"}
   ,{"x":1.02,"y":0.75,"text":"$$C$$","fontSize":"18px"}
   ,{"x":0.7,"y":1.23,"text":"$$D$$","fontSize":"18px"}
   ,{"x":0.65,"y":0.75,"text":"$$E$$","fontSize":"18px"}
   ,{"x":0.7,"y":0.09,"text":"$$F$$","fontSize":"18px"}
   ,{"x":0.08,"y":0.25,"text":"$$x$$","fontSize":"18px"}
   ,{"x":0.09,"y":0.19,"text":"$$y$$","fontSize":"18px"}
   ,{"x":0.93,"y":0.72,"text":"$$y$$","fontSize":"18px"}
   ,{"x":0.73,"y":1.12,"text":"$$y$$","fontSize":"18px"}
   ,{"x":0.37,"y":0.75,"text":"$$1$$","fontSize":"18px"}
   ,{"x":0.5,"y":0.5,"text":"$$1$$","fontSize":"18px"}
  ];
  drawMathjax(svg05,foData05,xScale05,yScale05);

 /** 
   addition formula for cos 
                            */

  var svg06 = d3.select("#svg06")
                .append("svg")
                .attr("height",height)
                .attr("width",500)
                .style("background","#000");

  drawRTriangle(svg06,triangleData05,xScale05,yScale05);
  drawMathjax(svg06,foData05,xScale05,yScale05);

 /** 
   Law of cosine and sine 
                            */

  var svg07 = d3.select("#svg07")
                .append("svg")
                .attr("height",300)
                .attr("width",500)
                .style("background","#000");

  var xScale07 = d3.scale.linear()
                       .domain([0,15])
                       .range([50,450]);
  
  var yScale07 = d3.scale.linear()
                       .domain([7.5,0])
                       .range([50,250]);

  lineData07 = [
     {"x1":0,"y1":0,"x2":14.6,"y2":0,"stroke":"#f00"}
    ,{"x1":0,"y1":0,"x2":9.46,"y2":7.38,"stroke":"#0f0"}
    ,{"x1":14.6,"y1":0,"x2":9.46,"y2":7.38,"stroke":"#0f0"}
  ];

  drawLine(svg07,lineData07,xScale07,yScale07);

  // mathjax
  foData07 = [
    {"x":7,"y":1,"text":"$$a=?$$","fontSize":"18px"}
   ,{"x":2,"y":6,"text":"$$b=12$$","fontSize":"18px"}
   ,{"x":13,"y":6,"text":"$$c=9$$","fontSize":"18px"}
   ,{"x":9,"y":9,"text":"$$\\theta$$","fontSize":"18px"}
   ,{"x":8.5,"y":8,"text":"$$87^{\\circ}$$","fontSize":"18px"}
     ];
  drawMathjax(svg07,foData07,xScale07,yScale07);

  // vector
  vecData07 = [
    {"x1":9,"y1":5,"x2":8,"y2":1,"stroke":"#f00"}
  ];
  drawVectorB(svg07,vecData07,xScale07,yScale07);


  var svg08 = d3.select("#svg08")
                .append("svg")
                .attr("height",height)
                .attr("width",500)
                .style("background","#000");

  var xScale08 = d3.scale.linear()
                       .domain([-2.5,2.5])
                       .range([100,500]);
  
  var yScale08 = d3.scale.linear()
                       .domain([2.5,-2.5])
                       .range([50,450]);

  lineData08 = [
     {"x1":0,"y1":0,"x2":0,"y2":2,"stroke":"#f00"}
    ,{"x1":0,"y1":0,"x2":-2.15,"y2":-1.84,"stroke":"#0f0"}
    ,{"x1":0,"y1":2,"x2":-2.15,"y2":-1.84,"stroke":"#0f0"}
  ];

  drawLine(svg08,lineData08,xScale08,yScale08);

  // mathjax
  foData08 = [
    {"x":-1.3,"y":1,"text":"$$a$$","fontSize":"18px"}
   ,{"x":-0.9,"y":-0.2,"text":"$$b$$","fontSize":"18px"}
   ,{"x":0.2,"y":1.8,"text":"$$2$$","fontSize":"18px"}
   ,{"x":-1.72,"y":-0.5,"text":"$$30^{\\circ}$$","fontSize":"16px"}
   ,{"x":-0.33,"y":2,"text":"$$45^{\\circ}$$","fontSize":"16px"}
   ,{"x":-0.5,"y":0.8,"text":"$$105^{\\circ}$$","fontSize":"16px"}
  ];
  drawMathjax(svg08,foData08,xScale08,yScale08);

 /** 
   Proof :Law of cosines  
                            */

  var svg09 = d3.select("#svg09")
                .append("svg")
                .attr("height",300)
                .attr("width",500)
                .style("background","#000");

  var xScale09 = d3.scale.linear()
                       .domain([0,15])
                       .range([50,450]);
  
  var yScale09 = d3.scale.linear()
                       .domain([7.5,0])
                       .range([50,250]);

  lineData09 = [
     {"x1":0,"y1":0,"x2":14.6,"y2":0,"stroke":"#0f0"}
    ,{"x1":0,"y1":0,"x2":9.46,"y2":7.38,"stroke":"#0f0"}
    ,{"x1":14.6,"y1":0,"x2":9.46,"y2":7.38,"stroke":"#f00"}
    ,{"x1":9.46,"y1":0,"x2":9.46,"y2":7.38,"stroke":"#999"}
    // right angle
    ,{"x1":9.46,"y1":0.5,"x2":9.,"y2":0.5,"stroke":"#999"}
    ,{"x1":9,"y1":0,"x2":9.,"y2":0.5,"stroke":"#999"}
  ];

  drawLine(svg09,lineData09,xScale09,yScale09);

  // mathjax
  foData09 = [
    {"x":7,"y":1.5,"text":"$$c$$","fontSize":"18px"}
   ,{"x":3,"y":6.5,"text":"$$b$$","fontSize":"18px"}
   ,{"x":13,"y":7,"text":"$$a$$","fontSize":"18px"}
   ,{"x":1.5,"y":2.8,"text":"$$\\theta$$","fontSize":"18px"}
   ,{"x":8.5,"y":6,"text":"$$m$$","fontSize":"18px"}
   ,{"x":5,"y":2.8,"text":"$$d$$","fontSize":"18px"}
   ,{"x":12,"y":2.8,"text":"$$e$$","fontSize":"18px"}
     ];
  drawMathjax(svg09,foData09,xScale09,yScale09);

 /** 
   Proof :Law of sines  
                            */
  var svg10 = d3.select("#svg10")
                .append("svg")
                .attr("height",300)
                .attr("width",500)
                .style("background","#000");

  var xScale10 = d3.scale.linear()
                       .domain([0,15])
                       .range([50,450]);
  
  var yScale10 = d3.scale.linear()
                       .domain([7.5,0])
                       .range([50,250]);

  lineData10 = [
     {"x1":0,"y1":0,"x2":14.6,"y2":0,"stroke":"#0f0"}
    ,{"x1":0,"y1":0,"x2":9.46,"y2":7.38,"stroke":"#0f0"}
    ,{"x1":14.6,"y1":0,"x2":9.46,"y2":7.38,"stroke":"#f00"}
    ,{"x1":9.46,"y1":0,"x2":9.46,"y2":7.38,"stroke":"#999"}
    // right angle
    ,{"x1":9.46,"y1":0.5,"x2":9.,"y2":0.5,"stroke":"#999"}
    ,{"x1":9,"y1":0,"x2":9.,"y2":0.5,"stroke":"#999"}
  ];

  drawLine(svg10,lineData10,xScale10,yScale10);

  // mathjax
  foData10 = [
    {"x":7,"y":1.5,"text":"$$C$$","fontSize":"18px"}
   ,{"x":3,"y":6.5,"text":"$$B$$","fontSize":"18px"}
   ,{"x":13,"y":7,"text":"$$A$$","fontSize":"18px"}
   ,{"x":1.2,"y":2.8,"text":"$$\\alpha$$","fontSize":"18px"}
   ,{"x":13.4,"y":2.8,"text":"$$\\beta$$","fontSize":"18px"}
   ,{"x":8.5,"y":6,"text":"$$x$$","fontSize":"18px"}
   ,{"x":8.7,"y":8.5,"text":"$$\\theta$$","fontSize":"18px"}
  ];
  drawMathjax(svg10,foData10,xScale10,yScale10);



</script>
