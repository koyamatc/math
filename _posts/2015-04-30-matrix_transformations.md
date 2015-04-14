---
title: Linear algebraebra
layout: post
date: 2015-04-30 22:00:00
postTitle: Matrix transformations
categories: linear_algebra
---

-------

# Functions and linear transformations

-------

## A more formal understanding of functions

<div id="svg01"></div>


<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_SVG"></script>
<script src="http://d3js.org/d3.v3.min.js" charset="utf-8"></script>
<script src="{{site.url}}/js/d3draws.js" charset="utf-8"></script>
<script src="{{site.url}}/js/jquery.js" charset="utf-8"></script>

<script>

  var svg01 = d3.select("#svg01")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var xScale01 = d3.scale.linear()
                       .domain([0,400])
                       .range([50,450]);
  var yScale01 = d3.scale.linear()
                       .domain([400,0])
                       .range([50,450]);       


  var pathData01 = [

  ];
  
  pathData01.push(new Point(100,100));
  pathData01.push(new Point(50,300));
  pathData01.push(new Point(200,400));
  pathData01.push(new Point(300,300));
  pathData01.push(new Point(230,50));
 
 drawPath(svg01,pathData01,{"stroke":"#f0f","interPolate":"basis-closed"},xScale01,yScale01)


</script>
