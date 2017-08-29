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
		<img src="{{image.path}}" alt="{{image.name}}" id="index{{forloop.index}}"
		style="padding-bottom: 10px; padding-top: 10px;"/>

	 {% endif %}
	{% endfor %}
</section>
