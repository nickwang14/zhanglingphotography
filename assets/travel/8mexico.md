---
layout: gallery
custom_css:
   - customimagegrid
   - loadingscreen
permalink: /8mexico/
title: "MEXICO"
images:
   - mexico01.jpg
   - mexico04.jpg
   - mexico07.jpg
   - mexico10.jpg
   - mexico13.jpg
   - mexico16.jpg
   - mexico19.jpg
   - mexico22.jpg
   - mexico02.jpg
   - mexico05.jpg
   - mexico08.jpg
   - mexico11.jpg
   - mexico14.jpg
   - mexico17.jpg
   - mexico20.jpg
   - mexico23.jpg
   - mexico03.jpg
   - mexico06.jpg
   - mexico09.jpg
   - mexico12.jpg
   - mexico15.jpg
   - mexico18.jpg
   - mexico21.jpg
   - mexico24.jpg

---

<section class="mobile-photos">
{% for image in site.static_files %}
	{% if image.path contains 'assets/travel/mexico/' %}
		<img src="{{image.path}}" alt="{{image.name}}" id="index{{forloop.index}}" class="mobile-photos mobile-noclick"/>
	{% endif %}
{% endfor %}
</section>
<section id="modal">
	<h1> {{ page.title }} </h1>
	{% for link in page.images %}
	    <div class="modal fade" tabindex="-1" role="dialog" id="index{{forloop.index}}">
		  <div class="modal-dialog modal-lg">
		    <div class="modal-content">
			    <div class="modal-header">
			        <button type="button" class="close" data-dismiss="modal" aria-label="Close"><span aria-hidden="true">&times;</span></button>
			    </div>
				<img src="/assets/travel/mexico/{{ link }}" id="{{image.path}}"/>
			</div><!-- /.modal-content -->
		  </div><!-- /.modal-dialog -->
		</div><!-- /.modal -->
	{% endfor %}
</section>
<section id="photos" class ="photos">
{% for link in page.images %}
    <a href="#index{{forloop.index}}" data-toggle="modal" data-target="#index{{forloop.index}}" class="mobile-noclick">
		<img src="/assets/travel/mexico/{{ link }}" id="index{{forloop.index}}"/>
	</a>
	{% endfor %}
</section>