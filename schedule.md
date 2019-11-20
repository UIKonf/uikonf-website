---
layout: default
order: 1
title: Schedule
permalink: /schedule/
description: UIKonf 2018 - Schedule for May 14th & 15th
includeInNavigation: 1
---

<div class="headerimage uk-position-relative" style="background-image: url({{ site.baseurl }}/static/images/about_image.jpg);" uk-parallax="by: -50">
  <img class="uk-invisible" src="{{ site.baseurl }}/static/images/about_image.jpg" alt="home image">
   <div class="uk-position-cover uk-flex uk-flex-center uk-flex-middle uk-flex-column">
      <div class="teaser">
      	<h1>UIKonf 2019 Schedule</h1>
        <p>UIKonf is an independent conference for serious iOS developers</p>
     </div>
   </div>
</div>

<div class="opposite relative">
  <div class="wrapper">
        <div class="uk-width-6-10@m">
          <div class="uk-grid" style="padding: 0 15px;">
            <div class="uk-width-1-1 uk-text-center">
              <h2 class="brand-color">Schedule</h2>
            </div>
		            {% include schedule.md context="schedule" %}
           </div>
       </div>
    </div>
</div>
