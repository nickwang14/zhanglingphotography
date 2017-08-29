---
layout: gallery
custom_css:
   - loadingscreen
   - custom_accordian
permalink: /projects01_elaineollie/
---

<section id="photos">
{% for image in site.static_files %}
	    {% if image.path contains 'assets/collections/projects01_elaineollie/' %}
    <a href="#index{{forloop.index}}" data-toggle="modal" data-target="#index{{forloop.index}}" class="mobile-noclick">
		<img src="{{image.path}}" alt="{{image.name}}" id="index{{forloop.index}}"
		style="padding-bottom: 10px; padding-top: 10px;"/>
	</a>
	 {% endif %}
	{% endfor %}
</section>
