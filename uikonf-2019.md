---
layout: page
order: 1
title: Speakers 2019
collection: uikonf-2019
permalink: /uikonf-2019
headerImage: uikonf_2020_hero_image.jpg
headerTitle: Speakers at UIKonf 2019
headerDescription: For UIKonf 2019 we decided to present you a special edition with an amazing all female speaker line up. We therefore decided to pause the CfP for this year and invite all speakers personally. These were our amazing speakers...
includeInNavigation: 0
---

<div class="uk-section">
  {% for speaker in site.uikonf-2019 %}
  <div class="uk-grid" id="{{ speaker.anchor }}">
    <div class="uk-width-1-4@m uk-text-center uk-margin-bottom">
      {% assign imagePath = 'speaker/2019/' | append: speaker.image %}
      {% include thumbnail.html link=speaker.twitter image=imagePath alt=speaker.title %}
    </div>
    <div class="uk-width-3-4@m uk-text-center uk-text-left@m">
      <h4>{{ speaker.title }}</h4>
      {{ speaker.content | markdownify }}
    </div>
  </div>
  {% endfor %}
</div>

Sign up for our newsletter to be informed about upcoming speakers.
