---
layout: default
custom_css:
   - loadingscreen
page-title: COLLECTIONS

directories:
- events01_almostkennedy
- events02_reminiscence
- events03_engagement
- events04_exhibition
- travel01_china2015
---
<section class="collection-banners">
{% for directory in page.directories %}
	<a href= "./assets/collections/{{ directory }}.html">
		<img src="./assets/collections/{{ directory }}.jpg">
	</a>
{% endfor %}
<section>