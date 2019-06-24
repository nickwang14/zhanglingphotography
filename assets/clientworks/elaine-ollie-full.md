---
layout: gallery
custom_css:
   - loadingscreen
permalink: /elaine-ollie-full/
title: "Elaine and Ollie"
page: "clientworks"
---
<div class="intro-text">
    <h1 style="color:grey;text-align:center;">School Daze: Love Story</h1>
    <div class="container">
        <div class="row">
            <div class="col-xs-2 col-sm-2 col-md-2 col-lg-2">
            </div>
            <div class="col-xs-8 col-sm-8 col-md-8 col-lg-8" >
            <i style="color:grey;">"We didn't have any expectations for our engagement shoot and let Linda boss us around. She did a great job telling our story through photography and she listened when we said we wanted to highlight our fur baby. Really love the ones of our pup, she got really cute pictures of her smile!"</i>
            </div>
            <div class="col-xs-2 col-sm-2 col-md-2 col-lg-2">
            </div>
        </div>
    </div>
    <p style="color:grey;text-align:center;">- Elaine & Ollie</p>
</div>
<section class="single-col" id="photos">
{% for image in site.static_files %}
	    {% if image.path contains 'assets/clientworks/elaine-ollie/' %}
    <a href="#index{{forloop.index}}" class="mobile-noclick">
		<img src="{{image.path}}" alt="{{image.name}}" id="index{{forloop.index}}" style="padding-bottom:10px;"/>
	</a>
	 {% endif %}
	{% endfor %}
</section>