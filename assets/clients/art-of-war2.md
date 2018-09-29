---
layout: gallery
custom_css:
   - customimagegrid
   - loadingscreen
permalink: /art-of-war2/
title: "Art of War II"
images: 
    - artofwar07.jpg
    - artofwar25.jpg
    - artofwar30.jpg
    - artofwar32.jpg
    - artofwar43.jpg
    - artofwar06.jpg
    - artofwar16.jpg
    - artofwar17.jpg
    - artofwar36.jpg
    - artofwar41.jpg
    - artofwar23.jpg
    - artofwar22.jpg
    - artofwar39.jpg
    - artofwar40.jpg
    - artofwar45.jpg
---
<div class="intro-text">
    <h1 style="color:grey;text-align:center;">Art of War II</h1>
</div>
<section class="mobile-photos">
{% for image in site.static_files %}
	{% if image.path contains 'assets/clients/art-of-war2/' %}
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