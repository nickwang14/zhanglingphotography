---
layout: gallery
custom_css:
   - loadingscreen
permalink: /elaine-ollie-full/
title: "Elaine and Ollie"
page: "clientworks"
---
<section class="single-col" id="photos">
{% for image in site.static_files %}
	    {% if image.path contains 'assets/clientworks/elaine-ollie/' %}
    <a href="#index{{forloop.index}}" class="mobile-noclick">
		<img src="{{image.path}}" alt="{{image.name}}" id="index{{forloop.index}}" style="padding-bottom:10px;"/>
	</a>
	 {% endif %}
	{% endfor %}
</section>