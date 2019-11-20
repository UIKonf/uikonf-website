---
layout: default
title: UIKonf 2017
permalink: /uikonf-2017/
description: UIKonf 2017 - Speaker list
includeInNavigation: 0
---

<div class="headerimage-small uk-position-relative" style="background-image: url({{ site.baseurl }}/static/images/speakers-header-cropped.jpg);" uk-parallax="by: -50">
  <img class="uk-invisible" src="{{ site.baseurl }}/static/images/speakers-header-cropped.jpg" alt="speaker image">
   <div class="uk-position-cover uk-flex uk-flex-center uk-flex-middle uk-flex-column">
      <div class="teaser">
	    <div class="uk-container">
			<div class="uk-grid">
        		<div class="uk-width-1-1">
        			<h1>Speakers at UIKonf 2017</h1>
				</div>
			</div>
		</div>
     </div>
   </div>
</div>

<div class="backshape opposite"><div class="wrapper"></div></div>



<div class="backshape opposite">
	  <div class="wrapper">
		{% for speaker in site.uikonf-2017 %}
		<div class="uk-container uk-margin-large-bottom">
			<div class="uk-grid">
	    	<div class="uk-width-medium-1-3 uk-width-small-1-1 uk-width-1-3@l">
	      		<a name="{{ speaker.anchor }}"></a>
      			<div class="box">
      				<figure class="uk-inline-clip uk-transition-toggle">
			    		<img class="uk-transition-scale-up" src="{{ site.baseurl }}/static/images/{{ speaker.image }}" alt="{{ speaker.title }}">
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
		{% endfor %}
	</div>
</div>

