---
layout: default
order: 0
permalink: /schedule/
description: UIKonf 2017 - Schedule for May 15th & 16th
---

<div class="headerimage uk-position-relative" style="background-image: url({{ site.baseurl }}/static/images/about_image.jpg);" data-uk-parallax="{bg: '-50'}">
  <img class="uk-invisible" src="{{ site.baseurl }}/static/images/about_image.jpg" alt="home image">
   <div class="uk-position-cover uk-flex uk-flex-center uk-flex-middle uk-flex-column">
      <div class="teaser-register">
      	<h1>UIKonf 2017 Schedule</h1>
        <p>UIKonf is an independent conference for serious iOS developers</p>
     </div>
   </div>
</div>

<div class="backshape opposite relative">
  <div class="wrapper">
        <div class="uk-width-medium-6-10 uk-container-center">
          <div class="uk-grid">
            <div class="uk-width-1-1 uk-text-center">
              <h2 class="brand-color">Schedule</h2>
            </div>
		     {% include schedule.md context="schedule" %}
           </div>
       </div>
    </div>
</div>
