---
layout: gallery
custom_css:
   - customimagegrid
   - loadingscreen
permalink: /whalesbone-2019/
title: "Event @ Whalesbone"
images: 
    - whalesbone01.jpg
    - whalesbone04.jpg
    - whalesbone03.jpg
    - whalesbone09.jpg
    - whalesbone05.jpg
    - whalesbone07.jpg
    - whalesbone02.jpg
    - whalesbone08.jpg
    - whalesbone06.jpg
    
---
<div class="intro-text">
    <h1 style="color:grey;text-align:center;">Event @ Whalesbone</h1>
</div>
<section class="mobile-photos">
{% for image in site.static_files %}
	{% if image.path contains 'assets/clients/whalesbone/' %}
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