---
layout: default
custom_css:
   - loadingscreen
page-title: COLLECTIONS

directories:
- events01
- events02
- events03
- travel01
---
<section class="collection-banners">
{% for directory in page.directories %}
	<a href= "./assets/collections/{{ directory }}.html">
		<img src="./assets/collections/banners/{{ directory }}.jpg">
	</a>
{% endfor %}
<section>