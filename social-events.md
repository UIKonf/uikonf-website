---
layout: default
title: Social Events
permalink: /social-events/
description: UIKonf features a list of social events which are free for conference attendees
includeInNavigation: 0
---

<div class="headerimage uk-position-relative" style="background-image: url({{ site.baseurl }}/static/images/speakers-header-cropped.jpg);" data-uk-parallax="{bg: '-50'}">
  <img class="uk-invisible" src="{{ site.baseurl }}/static/images/speakers-header-cropped.jpg" alt="speaker image">
  <div class="uk-position-cover uk-flex uk-flex-center uk-flex-middle uk-flex-column">
    <div class="teaser">
	    <div class="uk-container uk-container-center">
				<div class="uk-grid">
        	<div class="uk-width-1-1">
        		<h1>Social Events at UIKonf 2018</h1>
			 	   	<p>UIKonf features a list of social events on the day before the conference. These events are intended to help you break the ice with fellow conference attendees.</p> 
					</div>
				</div>
			</div>
    </div>
  </div>
</div>

{% assign activeEvents = site.events | where:"active",1 %}

{% for event in activeEvents %}
{% assign loopindex = forloop.index | modulo: 2 %}
  {% if loopindex == 1 %}
  <div class="backshape opposite light-grey">
  {% else %}
  <div class="backshape opposite">
  {% endif %}	
		<div class="wrapper">
			<div class="uk-container uk-container-center uk-margin-large-top">
    		<div class="uk-grid">
	    		<div class="uk-width-medium-1-3 uk-width-small-1-1 uk-width-large-1-3">
      			<a name="{{ event.anchor }}"></a>
						<div class="box">
      				<figure class="uk-overlay uk-overlay-hover"><img src="/static/images/events/{{ event.image }}" alt="{{ event.image-alt }}"> </figure>
		        	<div  class="info-box small">
		          	<h4>{{ event.title }}</h4>
		        	</div>
		      	</div>
	      	</div> 
					<div class="uk-width-medium-2-3 uk-width-small-1-1 uk-width-large-2-3" style="padding-top:10px;">
						{{ event.content }}
	       		{% if event.start %}
	       			<p>Start: {{ event.start }}</p>
						{% endif %}	
	      	</div>
	  		</div>
			</div>
		</div>
	</div>
{% endfor %}

<!-- <div class="straight light-grey">
  <div class="wrapper">
    <div class="uk-container uk-container-center uk-margin-large-top">
        <div class="uk-width-1-1">
        <p>You can register your social event ticket through the confirmation email you received after registering your main conference ticket. </p>
            <p>If you already hold a UIKonf ticket, but haven't received an email to book an event ticket, <a href="mailto:questions@uikonf.com?subject=Social event tickets&body=Hi, I didn't receive the email to book a ticket for the social events. My UIKonf ticket reference is:" target="_blank">please contact us</a> with your booking reference.</p>
        <p>If you would like to guide one of the tours, <a href="mailto:questions@uikonf.com?subject=Social events guide">get in touch with us</a>.</p>
        </div>
    </div>
  </div>
</div> -->

