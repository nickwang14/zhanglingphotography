---
layout: gallery
custom_css:
   - customimagegrid
   - loadingscreen
page-title: PRODUCT
images:
   - 01product_pie01.jpg   
   - 02product_pie02.jpg
   - 08product_sapporo.jpg 
   - 13product_french02.jpg
   - 25product_coke01.jpg
   - 27product_coke03.jpg
   - 35product_mamiya03.jpg 
   - 09product_essie.jpg
   - 05product_perfume02.jpg
   - 06product_perfume03.jpg   
   - 14product_french03.jpg
   - 11product_mens02.jpg
   - 10product_mens01.jpg
   - 34product_mamiya01.jpg
   - 07product_suitcase.jpg
   - 37product_xmas03.jpg
   - 36product_xmas01.jpg
   - 12product_french01.jpg
   - 16product_vroom01.jpg
   - 32product_fuji02.jpg
   - 31product_fuji01.jpg
    

---

<section class="mobile-photos">
{% for image in site.static_files %}
	{% if image.path contains 'assets/product/' %}
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
				<img src="/assets/product/{{ page.permalink }}{{ link }}" id="{{image.path}}"/>
			</div><!-- /.modal-content -->
		  </div><!-- /.modal-dialog -->
		</div><!-- /.modal -->
	{% endfor %}
</section>
<section id="photos" class ="photos">
{% for link in page.images %}
    <a href="#index{{forloop.index}}" data-toggle="modal" data-target="#index{{forloop.index}}" class="mobile-noclick">
		<img src="/assets/product/{{ page.permalink }}{{ link }}" id="index{{forloop.index}}"/>
	</a>
	{% endfor %}
</section>