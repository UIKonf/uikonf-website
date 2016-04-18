<div class="uk-width-1-1">
    <ul class="uk-tab uk-tab-center uk-tab-grid uk-margin-large-bottom" data-uk-tab data-uk-switcher="{connect:'#Schedule'}">
  		{% for day in site.days %}
			{% assign columns = 3 %}
			{% if include.context == "schedule" %}
			    {% assign columns = 4 %}
			{% endif %}
			
			{% assign shouldShow = false %}
			{% if include.context == "home" and day.isSummary %}
				{% assign shouldShow = true %}
			{% elsif include.context == "schedule" and day.isDetail %}
				{% assign shouldShow = true %}
			{% endif %}
			
			{% if shouldShow %}
				{% if forloop.index == 0 %}
                  <li class="uk-active uk-width-1-{{columns}}" aria-expanded="true"><a href="#"> {{ day.title }} </a></li>
				{% else %}
                  <li aria-expanded="false" class="uk-width-1-{{columns}}"><a href="#"> {{ day.title }}</a></li>
				{% endif %}
			{% endif %}
		{% endfor %}
     </ul>
			  
     <div id="Schedule" class="uk-switcher">
    	{% for day in site.days %}	
			{% assign shouldShow = false %}
			{% if include.context == "home" and day.isSummary %}
				{% assign shouldShow = true %}
			{% elsif include.context == "schedule" and day.isDetail %}
				{% assign shouldShow = true %}
			{% endif %}
				
			{% if shouldShow %}
				{% assign loopindex = forloop.index %}
				{% if loopindex == 0 %}
                      <div class="uk-active" aria-hidden="false">
				{% else %}
                      <div aria-hidden="true" class="">
				{% endif %}
	    		{% for item in day.items %}
                   	 	<div class="uk-grid">
                      		  	<div class="uk-width-medium-2-6 uk-width-1-1">
                        			<p class="light-text"><i class="uk-icon-clock-o"></i> {{ item.time }}</p>
                     		   	</div>
                      		 	<div class="uk-width-medium-4-6 uk-width-1-1">
                        				<h3 class="brand-color">{{ item.title }}</h3>
                        				<p><small>{{ item.description }}</small></p>
                      			</div>
                    		</div>
  			    {% endfor %}
				      </div>
			{% endif %}
  		{% endfor %}
	</div>					  
</div>