---
layout: gallery
custom_css:
   - customimagegrid
   - loadingscreen
permalink: /almost-kennedy/
title: "Almost Kennedy"
page: "client"

---
<section id="modal">
	{% for image in site.static_files %}
	    {% if image.path contains 'assets/clientworks/almost-kennedy/' %}
	    <div class="modal fade" tabindex="-1" role="dialog" id="index{{forloop.index}}">
		  <div class="modal-dialog modal-lg">
		    <div class="modal-content">
			    <div class="modal-header">
			        <button type="button" class="close" data-dismiss="modal" aria-label="Close"><span aria-hidden="true">&times;</span></button>
			    </div>
				<img src="{{image.path}}" alt="{{image.name}}" id="{{image.path}}"/>
			</div><!-- /.modal-content -->
		  </div><!-- /.modal-dialog -->
		</div><!-- /.modal -->
	    {% endif %}
	{% endfor %}
</section>
<section id="photos">
{% for image in site.static_files %}
	    {% if image.path contains 'assets/clientworks/almost-kennedy/' %}
    <a href="#index{{forloop.index}}" data-toggle="modal" data-target="#index{{forloop.index}}" class="mobile-noclick">
		<img src="{{image.path}}" alt="{{image.name}}" id="index{{forloop.index}}"/>
	</a>
	 {% endif %}
	{% endfor %}
</section>
