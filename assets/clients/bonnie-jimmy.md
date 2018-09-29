---
layout: gallery
custom_css:
   - loadingscreen
permalink: /bonnie-jimmy/
title: "Bonnie and Jimmy"
---
<div class="intro-text">
    <h1 style="color:grey;text-align:center;">Fall Couple Shoot</h1>
    <div class="container">
        <div class="row">
            <div class="col-xs-2 col-sm-2 col-md-2 col-lg-2">
            </div>
            <div class="col-xs-8 col-sm-8 col-md-8 col-lg-8" >
            <i style="color:grey;">"The photo shoot was relaxed and a lot of fun. Linda was able to direct us on how to pose and the photos came out so beautifully. The whole session felt more like a casual outing to go see the foliage. We really enjoyed it!"</i>
            </div>
            <div class="col-xs-2 col-sm-2 col-md-2 col-lg-2">
            </div>
        </div>
    </div>
    <p style="color:grey;text-align:center;">- Bonnie N. & Jimmy C.</p>
</div>
<section class="single-col" id="photos">
{% for image in site.static_files %}
	    {% if image.path contains 'assets/clients/bonnie-jimmy/' %}
    <a href="#index{{forloop.index}}" class="mobile-noclick">
		<img src="{{image.path}}" alt="{{image.name}}" id="index{{forloop.index}}" style="padding-bottom:10px;"/>
	</a>
	 {% endif %}
	{% endfor %}
</section>