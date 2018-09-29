---
layout: gallery
custom_css:
   - customimagegrid
   - loadingscreen
page-title: EVENTS
images:
  - 04events_artofwar01.jpg
  - 05events_artofwar02.jpg
  - 02events_lightsfest1.jpg
  - 01events_lightsfest2.jpg
  - 13events_accords1.jpg
  - 16events-ossiano2.jpg
  - 06events_artofwar03.jpg
  - 07events_remniscence01.jpg
  - 10events_lights01.jpg
  - 03events_lightsfest3.jpg
  - 14events_accords2.jpg
  - 17events_ossiano1.jpg
  - 08events_remniscence02.jpg
  - 09events_remniscence03.jpg
  - 11events_lights02.jpg
  - 12events_lights03.jpg
  - 15events_accords3.jpg
  - 18events_ossiano3.jpg
---
<section class="mobile-photos">
{% for image in site.static_files %}
	{% if image.path contains 'assets/events' %}
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
				<img src="/assets/events/{{ page.permalink }}{{ link }}" id="{{image.path}}"/>
			</div><!-- /.modal-content -->
		  </div><!-- /.modal-dialog -->
		</div><!-- /.modal -->
	{% endfor %}
</section>
<section id="photos" class ="photos">
{% for link in page.images %}
    <a href="#index{{forloop.index}}" data-toggle="modal" data-target="#index{{forloop.index}}" class="mobile-noclick">
		<img src="/assets/events/{{ page.permalink }}{{ link }}" id="index{{forloop.index}}"/>
	</a>
	{% endfor %}
</section>