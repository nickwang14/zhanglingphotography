---
layout: gallery
custom_css:
   - customimagegrid
   - loadingscreen
permalink: /art-of-war2/
title: "Art of War II"
page: "client"
images: 
    - artofwar01.jpg
    - artofwar04.jpg
    - artofwar07.jpg
    - artofwar10.jpg
    - artofwar13.jpg
    - artofwar16.jpg
    - artofwar19.jpg
    - artofwar22.jpg
    - artofwar25.jpg
    - artofwar28.jpg
    - artofwar31.jpg
    - artofwar34.jpg
    - artofwar38.jpg
    - artofwar42.jpg
    - artofwar43.jpg
    - artofwar02.jpg
    - artofwar05.jpg
    - artofwar08.jpg
    - artofwar11.jpg
    - artofwar14.jpg
    - artofwar17.jpg
    - artofwar20.jpg
    - artofwar23.jpg
    - artofwar26.jpg
    - artofwar29.jpg
    - artofwar32.jpg
    - artofwar35.jpg
    - artofwar39.jpg
    - artofwar41.jpg
    - artofwar44.jpg
    - artofwar03.jpg
    - artofwar06.jpg
    - artofwar09.jpg
    - artofwar12.jpg
    - artofwar15.jpg
    - artofwar18.jpg
    - artofwar21.jpg
    - artofwar24.jpg
    - artofwar27.jpg
    - artofwar30.jpg
    - artofwar33.jpg
    - artofwar36.jpg
    - artofwar37.jpg
    - artofwar40.jpg
    - artofwar45.jpg
---
<section class="mobile-photos">
{% for image in site.static_files %}
	{% if image.path contains 'assets/clientworks/sylva-aiemann/' %}
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
           <img src="/assets/clientworks{{ page.permalink }}{{ link }}" id="{{image.path}}"/>
        </div><!-- /.modal-content -->
        </div><!-- /.modal-dialog -->
    </div><!-- /.modal -->
	{% endfor %}
</section>
<section id="photos" class="photos">
{% for link in page.images %}
	 <a href="#index{{forloop.index}}" data-toggle="modal" data-target="#index{{forloop.index}}" class="mobile-noclick">
		<img src="/assets/clientworks{{ page.permalink }}{{ link }}" id="index{{forloop.index}}"/>
	</a>
{% endfor %}
</section>