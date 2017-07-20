---
layout: gallery
custom_css:
   - customimagegrid
   - loadingscreen
title: LANDSCAPE
---

<section id= "photos">
	{% for image in site.static_files %}
	    {% if image.path contains 'assets/landscape' %}
	    <div class="modal fade" tabindex="-1" role="dialog" id="index{{forloop.index}}">
		  <div class="modal-dialog modal-lg">
		    <div class="modal-content ">
		      <div class="modal-header">
		        <button type="button" class="close" data-dismiss="modal" aria-label="Close"><span aria-hidden="true">&times;</span></button>
		      </div>
				<img src="{{image.path}}" alt="{{image.name}}" id="{{image.path}}"/>
		    </div><!-- /.modal-content -->
		  </div><!-- /.modal-dialog -->
		</div><!-- /.modal -->
	    <a href="#index{{forloop.index}}" data-toggle="modal" data-target="#index{{forloop.index}}">
			<img src="{{image.path}}" alt="{{image.name}}" id="index{{forloop.index}}"/>
		</a>
	    {% endif %}
	{% endfor %}
</section>