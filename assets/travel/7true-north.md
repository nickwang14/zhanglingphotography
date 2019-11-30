---
layout: gallery
custom_css:
   - customimagegrid
   - loadingscreen
permalink: /7true-north/
title: "TRUE NORTH"
images:
   - gaspe02.jpg
   - montreal01.jpg
   - montreal09.jpg
   - montreal13.jpg
   - ottawa13.jpg
   - ottawa12.jpg
   - qcity01.jpg
   - qcity04.jpg
   - qcity06.jpg
   - qcity14.jpg
   - tobermory01.jpg
   - toronto02.jpg
   - gaspe03.jpg
   - montreal02.jpg
   - montreal11.jpg
   - ottawa01.jpg
   - ottawa04.jpg
   - ottawa05.jpg
   - qcity02.jpg
   - qcity05.jpg
   - qcity10.jpg
   - toronto07.jpg
   - tobermory02.jpg
   - toronto01.jpg
   - gaspe04.jpg
   - montreal12.jpg   
   - montreal07.jpg
   - ottawa03.jpg
   - ottawa09.jpg
   - ottawa15.jpg
   - qcity03.jpg
   - qcity07.jpg
   - toronto03.jpg
   - toronto04.jpg
   - tobermory03.jpg
   - vancouver03.jpg

---

<section class="mobile-photos">
{% for image in site.static_files %}
	{% if image.path contains 'assets/travel/true-north/' %}
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
				<img src="/assets/travel/true-north
		/{{ link }}" id="{{image.path}}"/>
			</div><!-- /.modal-content -->
		  </div><!-- /.modal-dialog -->
		</div><!-- /.modal -->
	{% endfor %}
</section>
<section id="photos" class ="photos">
{% for link in page.images %}
    <a href="#index{{forloop.index}}" data-toggle="modal" data-target="#index{{forloop.index}}" class="mobile-noclick">
		<img src="/assets/travel/true-north
/{{ link }}" id="index{{forloop.index}}"/>
	</a>
	{% endfor %}
</section>