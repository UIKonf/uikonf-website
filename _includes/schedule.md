<div class="uk-width-1-1 brand-color-text uk-margin-large-bottom">
  <ul class="uk-tab uk-flex-center uk-margin-large-bottom " uk-tab uk-switcher="{connect:'#Schedule', active:2 }">
		
  		{% if include.context == "schedule" %}
  	    	{% assign days = site.days | where:"isDetail", true %}
		{% elsif include.context == "home" %}
  	    	{% assign days = site.days | where:"isSummary", true %}		
  		{% endif %}
		
		{% assign columns = days.size %}
		{% for day in days %}	
  			{% if forloop.index == 0 %}
          <li class="uk-active uk-width-1-{{columns}}" aria-expanded="true">
		  	<a href="#"> {{ day.title }} </a>
		  </li>
  			{% else %}
          <li aria-expanded="false" class="uk-width-1-{{columns}}">
		  	<a href="#" class="uk-text-capitalize"> {{ day.title }}</a>
		  </li>
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
				{% if include.context == "schedule" %}
					{% assign description_text = item.description %}
				{% endif %}

  				{% if item.type == "break" %}
  					<div class="uk-grid">
      		  			<div class="">
          					<p class="" ><i></i> {{ item.time }}</p>
       		   			</div>
  	          		   <div class="uk-width-5-6">
                		   <p class=""> {{ item.title }}</p>
  							
							{% if description_text %}
      				    	<p><small>{{ item.description }}</small></p>
  							{% endif %}
							
	  						{% if item.location %}
	      				    <p><small><strong>Location: </strong>
								{% if item.location_link %}
									<a href="{{ item.location_link }}" target="_blank">{{ item.location }}</a>
								{% else %}
									{{ item.location }}
								{% endif %}
							</small></p>
	  						{% endif %}
  	          		  </div>
  			    	</div>
  				{% elsif item.type == "workshop" %}
	         	 	<div class="uk-grid">
						<div class="">
							<p class="">{{ item.time }}</p>
						</div>
	        		 	<div class="uk-width-5-6@m uk-width-1-1">
							{% if item.anchor %}<a href="/workshops/#{{ item.anchor }}">{% endif %}
								<h5>{{ item.title }}{% if item.talk %} - {{ item.talk }}{% endif %}</h5>
							{% if item.anchor %} </a> {% endif %}
	      				     <p><small>
	       				    	 	<strong>Duration:</strong> {{ item.duration }} <br/>
								 	<strong>Costs:</strong> {{ item.costs }} - 
	 								<a href="{{ item.registration }}" target="_blank">Book a ticket</a> | 
									<a href="/workshops/#{{ item.anchor }}">Learn More</a>
							 </small></p>						
	        			</div>
	        		</div>
  				{% else %}
         	 	<div class="uk-grid">
      		  	<div class="">
					{% if item.time %}
          				<p class="">{{ item.time }}</p>
					{% endif %}
       		   	</div>
        		 	<div class="uk-width-5-6@m uk-width-1-1">
						{% if item.anchor %}
							{% if item.type == "mytaxi-stage" %}
								<a href="/mytaxi-stage/#{{ item.anchor }}">
							{% else %}
								<a href="/speakers/#{{ item.anchor }}">
							{% endif %}
						{% endif %}
						{% if item.type == "mytaxi-stage" %}
						    <h5><span class="mytaxi-color">MyTaxi Stage: </span>{{ item.talk }}</h5>
						{% else %}
							<h5>{{ item.title }}{% if item.talk %} - {{ item.talk }}{% endif %}</h5>
						{% endif %}
						{% if item.anchor %} </a> {% endif %}
						{% if description_text %} <p><small>{{ description_text }}</small></p>  {% endif %}
  						{% if item.location %}
      				    <p><small><strong>Location: </strong>
							{% if item.location_link %}
								<a href="{{ item.location_link }}" target="_blank">{{ item.location }}</a>
							{% else %}
								{{ item.location }}
							{% endif %}
						</small></p>
  						{% endif %}
        			</div>
        		</div>
  				{% endif %}
  	    	{% endfor %}
        </div>
  	{% endfor %}
  </div>					  
</div>