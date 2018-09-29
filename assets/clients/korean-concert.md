---
layout: gallery
custom_css:
   - loadingscreen
permalink: /korean-concert/
title: "Korean Concert"
---
<div class="intro-text">
    <h1 style="color:grey;text-align:center;">KTMAC Reminiscence Concert</h1>
    <div class="container">
        <div class="row">
            <div class="col-xs-2 col-sm-2 col-md-2 col-lg-2">
            </div>
            <div class="col-xs-8 col-sm-8 col-md-8 col-lg-8" >
            <i style="color:grey;">"Punctual and professional. Great action shots and an eye for composition. Excellent communication throughout the post-production phase. A pleasure to work with regardless of how involved you want to be in the artistic process."</i>
            </div>
            <div class="col-xs-2 col-sm-2 col-md-2 col-lg-2">
            </div>
        </div>
    </div>
    <p style="color:grey;text-align:center;">- John L. (President, Korean Traditional Music Association)</p>
</div>
<section class="single-col" id="photos">
{% for image in site.static_files %}
	    {% if image.path contains 'assets/clients/korean-concert/' %}
    <a href="#index{{forloop.index}}" class="mobile-noclick">
		<img src="{{image.path}}" alt="{{image.name}}" id="index{{forloop.index}}" style="padding-bottom:10px;"/>
	</a>
	 {% endif %}
	{% endfor %}
</section>