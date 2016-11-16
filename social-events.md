---
layout: default
title: Social Events
permalink: /social-events/
description: UIKonf features a list of social events. You can set a donation for your ticket. Your contribution will be donated to a charity supporting refugees.
---

<div class="headerimage uk-position-relative" style="background-image: url({{ site.baseurl }}/static/images/speakers-header-cropped.jpg);" data-uk-parallax="{bg: '-50'}">
  <img class="uk-invisible" src="{{ site.baseurl }}/static/images/speakers-header-cropped.jpg" alt="speaker image">
   <div class="uk-position-cover uk-flex uk-flex-center uk-flex-middle uk-flex-column">
      <div class="teaser-register">
	    <div class="uk-container uk-container-center">
			<div class="uk-grid">
        		<div class="uk-width-1-1">
        			<h1>Social Events at UIKonf 2017</h1>
				</div>
       	 		<div class="uk-width-medium-1-2 uk-text-left">
			 	   <p>UIKonf features a list of social events on the day before the conference. These events are intended to help you break the ice with fellow conference attendees.</p> 
				</div>
       	 		<div class="uk-width-medium-1-2 uk-text-left">
				   <p>The events are free to attend, but we encourage you to submit a small donation. More details coming soon…</p>
				</div>
			</div>
		</div>
     </div>
   </div>
</div>


{% for event in site.events %}
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
      			<figure class="uk-overlay uk-overlay-hover"><img src="/static/images/{{ event.image }}" alt="{{ event.image-alt }}"> </figure>
		        <div  class="info-box small">
		          <h4>{{ event.title }}</h4>
		        </div>
		      </div>
	      	</div> 
			<div class="uk-width-medium-2-3 uk-width-small-1-1 uk-width-large-2-3" style="padding-top:10px;">
				{{ event.content }}
	       	 	<p>Start: {{ event.start }}</p>
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

