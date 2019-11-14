<div class="uk-width-1-1">
  <ul class="uk-tab uk-flex-center uk-tab-grid uk-margin-large-bottom" uk-tab uk-switcher="{connect:'#Schedule', active:2 }">
		
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
      		  			<div class="uk-width-1-6@m uk-width-1-1">
          					<p class="light-text" ><i class="uk-icon-clock-o"></i> {{ item.time }}</p>
       		   			</div>
  	          		   <div class="uk-width-5-6">
                		   <p class="light-text"> {{ item.title }}</p>
  							
							{% if item.description %}
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
	      		  	<div class="uk-width-1-6@m uk-width-1-1">
	          			<p class="light-text"><i class="uk-icon-clock-o"></i> {{ item.time }}</p>
	       		   	</div>
	        		 	<div class="uk-width-5-6@m uk-width-1-1">
							{% if item.anchor %}<a href="/workshops/#{{ item.anchor }}">{% endif %}
								<h3 class="brand-color" style="font-size: 1.7rem;">{{ item.title }}{% if item.talk %} - {{ item.talk }}{% endif %}</h3>
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
      		  	<div class="uk-width-1-6@m uk-width-1-1">
					{% if item.time %}
          				<p class="light-text"><i class="uk-icon-clock-o"></i> {{ item.time }}</p>
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
						    <h3 style="font-size: 1.7rem;"><span class="mytaxi-color">MyTaxi Stage: </span>{{ item.talk }}</h3>
						{% else %}
							<h3 class="brand-color" style="font-size: 1.7rem;">{{ item.title }}{% if item.talk %} - {{ item.talk }}{% endif %}</h3>
						{% endif %}
						{% if item.anchor %} </a> {% endif %}
						{% if item.description %} <p><small>{{ item.description }}</small></p>  {% endif %}
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