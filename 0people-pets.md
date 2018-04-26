---
layout: gallery
custom_css:
   - customimagegrid
   - loadingscreen
page-title: PEOPLE & PETS
images:
   - 01dianafamily04.jpg
   - 04elaineollie02.jpg
   - 07elaineollie8.jpg
   - 10maycee01.jpg
   - 14bonniejimmy08.jpg 
   - 15bonniejimmy10.jpg
   - 21street05.jpg
   - 23street06.jpg
   - 21street11.jpg
   - 02dianafamily03.jpg
   - 05elaineollie03.jpg
   - 08elaineollie7.jpg
   - 11maycee04.jpg
   - 16bonniejimmy03.jpg
   - 20street09.jpg
   - 19street03.jpg
   - 26street04.jpg
   - 24street07.jpg
   - 03dianafamily07.jpg
   - 06elaineollie01.jpg
   - 09elaineollie10.jpg
   - 12maycee05.jpg
   - 13maycee02.jpg
   - 17street01.jpg
   - 22street08.jpg
   - 25fashion01.jpg
   - 27street10.jpg
   - 28street13.jpg

---
<section class="mobile-photos">
{% for image in site.static_files %}
	{% if image.path contains 'assets/people-pets/' %}
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
			        <button type="button" class="close" data-dismiss="modal" aria-label="Close"><span aria-hidden	="true">&times;</span></button>
			    </div>
				<img src="/assets/people-pets/{{ page.permalink }}{{ link }}" id="{{image.path}}"/>
			</div><!-- /.modal-content -->
		  </div><!-- /.modal-dialog -->
		</div><!-- /.modal -->
	{% endfor %}
</section>
<section id="photos" class ="photos">
{% for link in page.images %}
    <a href="#index{{forloop.index}}" data-toggle="modal" data-target="#index{{forloop.index}}" class="mobile-noclick">
		<img src="/assets/people-pets/{{ page.permalink }}{{ link }}" id="index{{forloop.index}}"/>
	</a>
	{% endfor %}
</section>