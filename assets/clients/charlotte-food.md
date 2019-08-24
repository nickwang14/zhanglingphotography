---
layout: gallery
custom_css:
   - customimagegrid
   - loadingscreen
permalink: /charlotte-food/
title: "Charsiubaobao Food Blog"
images: 
    - charlotte-food01.jpg
    - charlotte-food03.jpg
    - charlotte-food06.jpg
    - charlotte-food07.jpg
    - charlotte-food14.jpg
    - charlotte-food16.jpg
    - charlotte-food04.jpg
    - charlotte-food12.jpg
    - charlotte-food11.jpg
    - charlotte-food08.jpg
    - charlotte-food15.jpg
    - charlotte-food17.jpg
    - charlotte-food05.jpg
    - charlotte-food09.jpg
    - charlotte-food10.jpg
    - charlotte-food13.jpg
    - charlotte-food18.jpg
    - charlotte-food19.jpg

---
<div class="intro-text">
    <h1 style="color:grey;text-align:center;">Charsiubaobao Food Blog</h1>
    <div class="container">
        <div class="row">
            <div class="col-xs-2 col-sm-2 col-md-2 col-lg-2">
            </div>
            <div class="col-xs-8 col-sm-8 col-md-8 col-lg-8" >
            <i style="color:grey;">"Some nice words. Some more nice words. Even more nice words. All about Linda. Because Linda is great. Linda should take ALL the photos. And I'll feed her as payment. It's a beautiful friendship."</i>
            </div>
            <div class="col-xs-2 col-sm-2 col-md-2 col-lg-2">
            </div>
        </div>
    </div>
    <p style="color:grey;text-align:center;">- Charlotte S.</p>
</div>
<section class="mobile-photos">
{% for image in site.static_files %}
	{% if image.path contains 'assets/clients/charlotte-food/' %}
		<img src="{{image.path}}" alt="{{image.name}}" id="index{{forloop.index}}" class="mobile-photos mobile-noclick"/>
	{% endif %}
{% endfor %}
</section>
<section id="modal">
	{% for link in page.images %}
    <div class="modal fade" tabindex="-1" role="dialog" id="index{{forloop.index}}">
        <div class="modal-dialog modal-lg">
        <div class="modal-content">
            <div class="modal-header">
                <button type="button" class="close" data-dismiss="modal" aria-label="Close"><span aria-hidden="true">&times;</span></button>
            </div>
           <img src="/assets/clients{{ page.permalink }}{{ link }}" id="{{image.path}}"/>
        </div><!-- /.modal-content -->
        </div><!-- /.modal-dialog -->
    </div><!-- /.modal -->
	{% endfor %}
</section>
<section id="photos" class="photos">
{% for link in page.images %}
	 <a href="#index{{forloop.index}}" data-toggle="modal" data-target="#index{{forloop.index}}" class="mobile-noclick">
		<img src="/assets/clients{{ page.permalink }}{{ link }}" id="index{{forloop.index}}"/>
	</a>
{% endfor %}
</section>