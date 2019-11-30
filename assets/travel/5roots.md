---
layout: gallery
custom_css:
   - customimagegrid
   - loadingscreen
permalink: /5roots/
title: "ROOTS"
images:
   - china01.jpg
   - china04.jpg
   - china07.jpg
   - china10.jpg
   - china13.jpg
   - china16.jpg
   - china19.jpg
   - china22.jpg
   - china02.jpg
   - china05.jpg
   - china08.jpg
   - china11.jpg
   - china14.jpg
   - china17.jpg
   - china20.jpg
   - china23.jpg
   - china03.jpg
   - china06.jpg
   - china09.jpg
   - china12.jpg
   - china15.jpg
   - china18.jpg
   - china21.jpg
   - china24.jpg

---

<section class="mobile-photos">
{% for image in site.static_files %}
	{% if image.path contains 'assets/travel/roots/' %}
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
				<img src="/assets/travel/roots/{{ link }}" id="{{image.path}}"/>
			</div><!-- /.modal-content -->
		  </div><!-- /.modal-dialog -->
		</div><!-- /.modal -->
	{% endfor %}
</section>
<section id="photos" class ="photos">
{% for link in page.images %}
    <a href="#index{{forloop.index}}" data-toggle="modal" data-target="#index{{forloop.index}}" class="mobile-noclick">
		<img src="/assets/travel/roots/{{ link }}" id="index{{forloop.index}}"/>
	</a>
	{% endfor %}
</section>