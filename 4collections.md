---
layout: default
custom_css:
   - loadingscreen
   - custom_accordian
page-title: COLLECTIONS

directories:
- events01_almostkennedy
- events02_reminiscence
- events03_engagement
- events04_exhibition
- projects01_elaineollie
- travel01_china2015
---
<section class="collection-banners">
  <div class="panel-group" id="accordion" role="tablist" aria-multiselectable="true">
  <!-- Events -->
    <div class="panel panel-default">
      <div class="panel-heading" role="tab" id="headingOne">
        <h4 class="panel-title">
          <a role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
          Events
          </a>
        </h4>
      </div>
      <div id="collapseOne" class="panel-collapse collapse in" role="tabpanel" aria-labelledby="headingOne">
        <div class="panel-body">
          {% for directory in page.directories %}
      			{% if directory contains 'events' %}
      			<a href= "/{{ directory }}">
      				<img src="./assets/collections/{{ directory }}.jpg">
      			</a>
      			{% endif %}
      		{% endfor %}
        </div>
      </div>
    </div>
  <!-- Projects -->
     <div class="panel panel-default">
      <div class="panel-heading" role="tab" id="headingTwo">
        <h4 class="panel-title">
          <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseTwo" aria-expanded="true" aria-controls="collapseTwo">
            Projects
          </a>
        </h4>
      </div>
      <div id="collapseTwo" class="panel-collapse collapse in" role="tabpanel" aria-labelledby="headingTwo">
        <div class="panel-body">
          {% for directory in page.directories %}
            {% if directory contains 'projects' %}
            <a href= "/{{ directory }}">
              <img src="./assets/collections/{{ directory }}.jpg">
            </a>
            {% endif %}
          {% endfor %}
        </div>
      </div>
    </div>
  <!-- Travel -->
    <div class="panel panel-default">
      <div class="panel-heading" role="tab" id="headingThree">
        <h4 class="panel-title">
          <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseThree" aria-expanded="true" aria-controls="collapseThree">
            Travel
          </a>
        </h4>
      </div>
      <div id="collapseThree" class="panel-collapse collapse in" role="tabpanel" aria-labelledby="headingThree">
        <div class="panel-body">
           {% for directory in page.directories %}
      			{% if directory contains 'travel' %}
      			<a href= "/{{ directory }}">
      				<img src="./assets/collections/{{ directory }}.jpg">
      			</a>
      			{% endif %}
      		{% endfor %}
        </div>
      </div>
    </div>
   </div>
</section>
