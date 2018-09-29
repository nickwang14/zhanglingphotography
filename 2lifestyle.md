---
layout: gallery
custom_css:
   - customimagegrid
   - loadingscreen
page-title: LIFESTYLE
images:
   - 02lifestyle_pie02.jpg
   - 01lifestyle_pie01.jpg   
   - 10lifestyle_mamiya03.jpg 
   - 25lifestyle_coke01.jpg
   - 26lifestyle_coke02.jpg
   - 27lifestyle_coke03.jpg
   - 05lifestyle_perfume02.jpg
   - 06lifestyle_perfume03.jpg  
   - 08lifestyle_mamiya01.jpg
   - 28lifestyle_tea01.jpg
   - 29lifestyle_tea03.jpg
   - 33lifestyle_fuji03.jpg 
   - 17lifestyle_vroom02.jpg
   - 16lifestyle_vroom01.jpg 
   - 12lifestyle_xmas01.jpg
   - 14lifestyle_xmas03.jpg
   - 31lifestyle_fuji01.jpg
   - 32lifestyle_fuji02.jpg

---

<section class="mobile-photos">
{% for image in site.static_files %}
	{% if image.path contains 'assets/lifestyle/' %}
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
				<img src="/assets/lifestyle/{{ page.permalink }}{{ link }}" id="{{image.path}}"/>
			</div><!-- /.modal-content -->
		  </div><!-- /.modal-dialog -->
		</div><!-- /.modal -->
	{% endfor %}
</section>
<section id="photos" class ="photos">
{% for link in page.images %}
    <a href="#index{{forloop.index}}" data-toggle="modal" data-target="#index{{forloop.index}}" class="mobile-noclick">
		<img src="/assets/lifestyle/{{ page.permalink }}{{ link }}" id="index{{forloop.index}}"/>
	</a>
	{% endfor %}
</section>