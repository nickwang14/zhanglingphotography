---
layout: gallery
custom_css:
   - customimagegrid
   - loadingscreen
permalink: /cat-mike/
title: "Catherine & Michael"
images: 
    - catmike00.jpg
    - catmike10.jpg
    - catmike09.jpg
    - catmike08.jpg
    - catmike13.jpg
    - catmike14.jpg
    - catmike17.jpg
    - catmike01.jpg
    - catmike03.jpg
    - catmike06.jpg
    - catmike11.jpg
    - catmike15.jpg
    - catmike16.jpg
    - catmike18.jpg
    - catmike02.jpg
    - catmike04.jpg
    - catmike05.jpg
    - catmike07.jpg
    - catmike12.jpg
    - catmike19.jpg
    - catmike20.jpg
---
<div class="intro-text">
    <h1 style="color:grey;text-align:center;">Catherine & Michael</h1>
</div>
<section class="mobile-photos">
{% for image in site.static_files %}
	{% if image.path contains 'assets/clients/cat-mike/' %}
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