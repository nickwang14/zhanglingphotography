---
layout: gallery
custom_css:
   - customimagegrid
   - loadingscreen
permalink: /sylva-aiemann-full/
title: "Sylva & Aiemann"
page: "clientworks"
images: 
    - sylva-aiemann01.jpg
    - sylva-aiemann06.jpg
    - sylva-aiemann14.jpg
    - sylva-aiemann11.jpg
    - sylva-aiemann16.jpg
    - sylva-aiemann15.jpg
    - sylva-aiemann22.jpg
    - sylva-aiemann23.jpg
    - sylva-aiemann31.jpg
    - sylva-aiemann32.jpg
    - sylva-aiemann33.jpg
    - sylva-aiemann34.jpg
    - sylva-aiemann42.jpg
    - sylva-aiemann43.jpg
    - sylva-aiemann45.jpg
    - sylva-aiemann55.jpg
    - sylva-aiemann58.jpg
    - sylva-aiemann51.jpg
    - sylva-aiemann52.jpg
    - sylva-aiemann53.jpg
    - sylva-aiemann54.jpg
    - sylva-aiemann02.jpg
    - sylva-aiemann05.jpg
    - sylva-aiemann07.jpg
    - sylva-aiemann08.jpg
    - sylva-aiemann10.jpg
    - sylva-aiemann12.jpg
    - sylva-aiemann17.jpg
    - sylva-aiemann13.jpg
    - sylva-aiemann18.jpg
    - sylva-aiemann21.jpg
    - sylva-aiemann24.jpg
    - sylva-aiemann27.jpg
    - sylva-aiemann35.jpg
    - sylva-aiemann38.jpg
    - sylva-aiemann40.jpg
    - sylva-aiemann44.jpg
    - sylva-aiemann46.jpg
    - sylva-aiemann48.jpg
    - sylva-aiemann56.jpg
    - sylva-aiemann57.jpg
    - sylva-aiemann59.jpg
    - sylva-aiemann03.jpg
    - sylva-aiemann04.jpg
    - sylva-aiemann09.jpg
    - sylva-aiemann19.jpg
    - sylva-aiemann20.jpg
    - sylva-aiemann25.jpg
    - sylva-aiemann28.jpg
    - sylva-aiemann26.jpg
    - sylva-aiemann29.jpg
    - sylva-aiemann30.jpg
    - sylva-aiemann36.jpg
    - sylva-aiemann37.jpg
    - sylva-aiemann39.jpg
    - sylva-aiemann41.jpg
    - sylva-aiemann49.jpg
    - sylva-aiemann50.jpg
    - sylva-aiemann47.jpg
    - sylva-aiemann60.jpg
    - sylva-aiemann61.jpg
    - sylva-aiemann62.jpg
    - sylva-aiemann63.jpg
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
	{% if image.path contains 'assets/clientworks/sylva-aiemann-full/' %}
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