---
layout: default
order: 1
title: Speakers
permalink: /speakers/
description: UIKonf 2017 - Speaker list
includeInNavigation: 0
redirect_from:
 - /speakers/boris_buegling.html
 - /speakers/peter_steinberger.html
 - /speakers/robbert-boehnke.html
---

<div class="headerimage uk-position-relative" style="background-image: url({{ site.baseurl }}/static/images/speakers-header-cropped.jpg);" data-uk-parallax="{bg: '-50'}">
  <img class="uk-invisible" src="{{ site.baseurl }}/static/images/speakers-header-cropped.jpg" alt="speaker image">
   <div class="uk-position-cover uk-flex uk-flex-center uk-flex-middle uk-flex-column">
      <div class="teaser-register">
	    <div class="uk-container uk-container-center">
			<div class="uk-grid">
        		<div class="uk-width-1-1">
        			<h1>Speakers at UIKonf 2017</h1>
				</div>
       	 		<div class="uk-width-medium-1-2 uk-text-left">
			 	   <p>UIKonf hosts a diverse selection of inspiring speakers. We select and invite about half of our speakers. The other half is selected by our community through our anonymous call for proposals system. Details coming soon.</p>
				</div>
    			<div class="uk-width-medium-1-2 uk-text-left">
					<p><a href="#newsletter">Sign up for our newsletter</a>, if you would like to receive an email when we announce the speakers and when the call for proposal starts.</p>
				</div>
			</div>
		</div>
     </div>
   </div>
</div>


{% for speaker in site.speakers %}
{% assign loopindex = forloop.index | modulo: 2 %}
  {% if loopindex == 1 %}
  <div class="backshape opposite light-grey">
  {% else %}
  <div class="backshape opposite">
  {% endif %}	
	<div class="wrapper">
		<div class="uk-container uk-container-center uk-margin-large-bottom">
			<div class="uk-grid">
	    	<div class="uk-width-medium-1-3 uk-width-small-1-1 uk-width-large-1-3">
	      		<a name="{{ speaker.anchor }}"></a>
      			<div class="box">
      				<figure class="uk-overlay uk-overlay-hover">
			    		<img class="uk-overlay-spin" src="{{ site.baseurl }}/static/images/speaker/{{ speaker.image }}" alt="{{ speaker.title }}">
							<a class="uk-position-cover" href="{{ speaker.twitter }}" target="_blank"></a>
					</figure>
		     		<div  class="info-box small">
		     			 <h4>{{ speaker.title }}</h4>
		    		</div>
		   	   </div>
	      	</div>
	      	<div class="uk-width-medium-2-3 uk-width-small-1-1 uk-width-large-2-3" style="padding-top:10px;">
				{{ speaker.content }}
	      	</div>
	  		</div>
		</div>
	</div>
</div>
{% endfor %}


<div class="straight light-grey">
	<div class="wrapper">
		<div class="uk-container uk-container-center uk-margin-large-top">
	    	<div class="uk-width-1-1">
	      		<p> <a href="#newsletter">Sign up for our newsletter</a> to be informed about upcoming speakers.</p>
	  		</div>
		</div>
	</div>
</div>
