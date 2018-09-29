---
layout: gallery
custom_css:
   - customimagegrid
   - loadingscreen
permalink: /sylva-aiemann/
title: "Sylva & Aiemann"
images: 
    - sylva-aiemann01.jpg
    - sylva-aiemann14.jpg
    - sylva-aiemann27.jpg
    - sylva-aiemann35.jpg
    - sylva-aiemann39.jpg
    - sylva-aiemann43.jpg
    - sylva-aiemann53.jpg
    - sylva-aiemann51.jpg
    - sylva-aiemann02.jpg
    - sylva-aiemann12.jpg
    - sylva-aiemann13.jpg
    - sylva-aiemann24.jpg
    - sylva-aiemann38.jpg
    - sylva-aiemann44.jpg
    - sylva-aiemann46.jpg
    - sylva-aiemann59.jpg
    - sylva-aiemann03.jpg
    - sylva-aiemann20.jpg
    - sylva-aiemann28.jpg
    - sylva-aiemann36.jpg
    - sylva-aiemann41.jpg
    - sylva-aiemann48.jpg
    - sylva-aiemann60.jpg
    - sylva-aiemann55.jpg
---
<div class="intro-text">
    <h1 style="color:grey;text-align:center;">Sylva & Aieman</h1>
    <div class="container">
        <div class="row">
            <div class="col-xs-2 col-sm-2 col-md-2 col-lg-2">
            </div>
            <div class="col-xs-8 col-sm-8 col-md-8 col-lg-8" >
            <i style="color:grey;">"Linda was super easy to work with, very easy going, taking in mind all of the ideas that my husband and I were interested in. The photos came out even better than the inspiration pictures we showed her! Would definitely recommend to friends and family!"</i>
            </div>
            <div class="col-xs-2 col-sm-2 col-md-2 col-lg-2">
            </div>
        </div>
    </div>
    <p style="color:grey;text-align:center;">- Sylva M. (Bride)</p>
</div>
<section class="mobile-photos">
{% for image in site.static_files %}
	{% if image.path contains 'assets/clients/sylva-aiemann/' %}
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