---
layout: default
custom_css:
   - loadingscreen
permalink: /clientworks/
---
<div class="list">
  {% for page in site.pages %}
    {% if page.page == "client" %}
    <a href="{{ page.url }}">
      {{ page.title }}
    </a>
    <br/>
    {% endif %}
  {% endfor %}
</div>