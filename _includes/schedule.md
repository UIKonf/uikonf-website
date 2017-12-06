<div class="uk-width-1-1">
  <ul class="uk-tab uk-tab-center uk-tab-grid uk-margin-large-bottom" data-uk-tab data-uk-switcher="{connect:'#Schedule'}">
		
  		{% if include.context == "schedule" %}
  	    	{% assign days = site.days | where:"isDetail", true %}
		{% elsif include.context == "home" %}
  	    	{% assign days = site.days | where:"isSummary", true %}		
  		{% endif %}
		
		{% assign columns = days.size %}
		{% for day in days %}	
  			{% if forloop.index == 0 %}
          <li class="uk-active uk-width-1-{{columns}}" aria-expanded="true"><a href="#"> {{ day.title }} </a></li>
  			{% else %}
          <li aria-expanded="false" class="uk-width-1-{{columns}}"><a href="#"> {{ day.title }}</a></li>
  			{% endif %}
  		{% endfor %}
  </ul>
		  
   <div id="Schedule" class="uk-switcher">
  	{% for day in days %}	
  			{% assign loopindex = forloop.index %}
  			{% if loopindex == 0 %}
          <div class="uk-active" aria-hidden="false">
  			{% else %}
          <div aria-hidden="true" class="">
  			{% endif %}
    		{% for item in day.items %}
  				{% if item.type == "break" %}
  					<div class="uk-grid">
      		  	<div class="uk-width-medium-1-6 uk-width-1-1">
          			<p class="light-text" ><i class="uk-icon-clock-o"></i> {{ item.time }}</p>
       		   	</div>
  	          <div class="uk-width-5-6">
                <p class="light-text"> {{ item.title }}</p>
  							{% if item.description %}
      				    <p><small>{{ item.description }}</small></p>
  							{% endif %}
  	          </div>
  			    </div>
  				{% else %}
         	 	<div class="uk-grid">
      		  	<div class="uk-width-medium-1-6 uk-width-1-1">
          			<p class="light-text"><i class="uk-icon-clock-o"></i> {{ item.time }}</p>
       		   	</div>
        		 	<div class="uk-width-medium-5-6 uk-width-1-1">
						{% if item.speaker %}<a href="/speakers/#{{ item.speaker }}">{% endif %}
							<h3 class="brand-color" style="font-size: 1.7rem;">{{ item.title }}{% if item.talk %} - {{ item.talk }}{% endif %}</h3>
						{% if item.speaker %} </a> {% endif %}
  							{% if item.description %}
      				     <p><small>{{ item.description }}</small></p>
  							{% endif %}
        			</div>
        		</div>
  				{% endif %}
  	    	{% endfor %}
        </div>
  	{% endfor %}
  </div>					  
</div>