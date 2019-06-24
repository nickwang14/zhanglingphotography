---
layout: gallery
custom_css:
   - loadingscreen
permalink: /diana-family-full/
title: "Diana Family Photo Shoot"
page: "clientworks"
---
<div class="intro-text">
    <h1 style="color:grey;text-align:center;">Family Photo Shoot</h1>
</div>
<section class="single-col" id="photos">
{% for image in site.static_files %}
	    {% if image.path contains 'assets/clientworks/diana-family/' %}
    <a href="#index{{forloop.index}}" class="mobile-noclick">
		<img src="{{image.path}}" alt="{{image.name}}" id="index{{forloop.index}}" style="padding-bottom:10px;"/>
	</a>
	 {% endif %}
	{% endfor %}
</section>