---
layout: gallery
custom_css:
   - customimagegrid
   - loadingscreen
permalink: /capital-punishment/
title: "Capital Punishment"
images: 
    - cp01.jpg
    - cp04.jpg
    - cp07.jpg
    - cp10.jpg
    - cp13.jpg
    - cp16.jpg
    - cp19.jpg
    - cp23.jpg
    - cp02.jpg
    - cp05.jpg
    - cp08.jpg
    - cp11.jpg
    - cp14.jpg
    - cp17.jpg
    - cp20.jpg
    - cp22.jpg
    - cp03.jpg
    - cp06.jpg
    - cp09.jpg
    - cp12.jpg
    - cp15.jpg
    - cp18.jpg
    - cp21.jpg
    - cp24.jpg
    
---
<div class="intro-text">
    <h1 style="color:grey;text-align:center;">Capital Punishment</h1>
</div>
<section class="mobile-photos">
{% for image in site.static_files %}
	{% if image.path contains 'assets/clients/capital-punishment/' %}
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