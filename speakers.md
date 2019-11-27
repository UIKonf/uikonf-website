---
layout: page
order: 1
title: Speakers
permalink: /speakers/
headerImage: uikonf_2020_hero_image.jpg
headerTitle: Speakers at UIKonf
description: UIKonf hosts a diverse selection of inspiring speakers. We select and invite about half of our speakers. The other half is selected by our community through our anonymous call for proposals system. Details coming soon.
includeInNavigation: 0
redirect_from:
 - /speakers/boris_buegling.html
 - /speakers/peter_steinberger.html
 - /speakers/robbert-boehnke.html
---

{% for speaker in site.speakers %}
  	{% assign imagePath = 'speaker/' | append: speaker.image %}
  	{% include 1-2-image-content-block.html anchor=speaker.anchor image=imagePath imageAlt=speaker.title imageTitle=speaker.title link=speaker.twitter content=speaker.content %}	
{% endfor %}

Sign up for our newsletter to be informed about upcoming speakers.

