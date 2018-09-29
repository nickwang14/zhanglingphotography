---
layout: gallery
custom_css:
   - customimagegrid
   - loadingscreen
permalink: /serena-zao/
title: "Serena & Zao"
images: 
    - serena-zao02.jpg
    - serena-zao09.jpg
    - serena-zao10.jpg
    - serena-zao19.jpg
    - serena-zao05.jpg
    - serena-zao06.jpg
    - serena-zao08.jpg
    - serena-zao13.jpg
    - serena-zao03.jpg    
    - serena-zao04.jpg
    - serena-zao07.jpg
    - serena-zao20.jpg

---
<div class="intro-text">
    <h1 style="color:grey;text-align:center;">Serena & Zao</h1>
    <div class="container">
        <div class="row">
            <div class="col-xs-2 col-sm-2 col-md-2 col-lg-2">
            </div>
            <div class="col-xs-8 col-sm-8 col-md-8 col-lg-8" >
            <i style="color:grey;">"Linda is ver easy-going and fun to work with. We like how she has a wide assortment of props to help accent our photos! Linda has an eye for locating uncommon background scenes that aren't just "leaves" and "bushes". Pacing was also good, and she made us feel very comfortable in front of the lens."</i>
            </div>
            <div class="col-xs-2 col-sm-2 col-md-2 col-lg-2">
            </div>
        </div>
    </div>
    <p style="color:grey;text-align:center;">- Serena L. & Zao Z.</p>
</div>
<section class="mobile-photos">
{% for image in site.static_files %}
	{% if image.path contains 'assets/clients/serena-zao/' %}
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