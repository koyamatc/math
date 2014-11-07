---
title: math
layout: default
---

#Mathematics

- - -

忘れてしまっている数学のメモです。

__Khan Academy__ で勉強したことなどをまとめています。

===

###index

<div class="row">
	<div class="col-sm-4">
		<h3><span class="label label-info">Trigonometry(三角法)</span></h3>
		<ol class="post-list">
 			{% for post in site.categories.trig %}
   				<li><a href="{{ post.url }}">{{ post.postTitle }}</a></li>
 			{% endfor %}
		</ol>			
	</div>
	<div class="col-sm-4">
		<h3><span class="label label-info">Differential calculus</span></h3>
		<ol class="post-list">
 			{% for post in site.categories.differential %}
   				<li><a href="{{ post.url }}">{{ post.postTitle }}</a></li>
 			{% endfor %}
		</ol>			
	</div>
	<div class="col-sm-4">
		<h3><span class="label label-info"></span></h3>
		<ol class="post-list">
 			{% for post in site.categories. %}
   				<li><a href="{{ post.url }}">{{ post.postTitle }}</a></li>
 			{% endfor %}
		</ol>			
	</div>


</div>