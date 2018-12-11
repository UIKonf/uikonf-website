---
layout: default
order: 3
title: About
permalink: /about/
headerImage: about_image.jpg
description: UIKonf - Berlin's independent iOS conference is run by Engin Kurutepe, Maxim Zaks and Sabine Geithner.
includeInNavigation: 1
organizers:
 - name: Engin Kurutepe
   lastName: Kurutepe
   bio: General Manager at Keepsafe Europe. Still writes code for <a href="https://itunes.apple.com/de/app/solar-watch-24h-solar-clock/id1191365122?l=en&mt=8">Solar Watch</a>. Flies gliders at <a href="http://www.fcc-berlin.de">FCC Berlin</a>.
   link: https://twitter.com/ekurutepe
   image: engin-kurutepe.jpg
 - name: Sabine Geithner
   lastName: Geithner
   bio: iOS developer at Mercedes-Benz.io, former Online Marketer and Scientist.
   link: https://twitter.com/sabinegeithner
   image: sabine-geithner.jpg
 - name: Christine Braun
   lastName: Braun
   bio: Beratung und Kreation für Geschäfte mit guten Absichten <a href="mailto:post@chrissybrown.com">post@chrissybrown.com</a>.
   link: https://twitter.com/post4chrissy
   image: christine-braun.jpg
 - name: Bianca Walterspiel Stromlund
   lastName: Walterspiel
   bio: Managing Global Engineering Relations at Delivery Hero.
   link: https://twitter.com/biancawalty
   image: bianca-walterspiel.jpg
 - name: Julia von Kallenberg
   lastName: Kallenberg
   bio: iOS Developer at evenly.
   link: https://twitter.com/KallenbergJulia
   image: julia-kallenberg.jpg
alumni:
 - name: Diana Arce
   lastName: Arce
   link: https://twitter.com/visualosmosis
   image: diana_thumb.jpg
 - name: Chris Eidhof
   lastName: Eidhof
   link: https://twitter.com/chriseidhof
   image: chris_thumb.jpg
 - name: Matt Patterson
   lastName: Patterson
   link: https://twitter.com/fidothe
   image: matt_thumb.jpg
 - name: Peter Bihr
   lastName: Bihr
   link: https://twitter.com/peterbihr
   image: peter_thumb.jpg
 - name: Max Krüger
   lastName: Krüger
   link: https://twitter.com/KrgerMax
   image: max_thumb.jpg
 - name: Maxim Zaks
   lastName: Zaks
   bio: Software developer with a passion for Games, Testing and Agile.
   link: https://twitter.com/iceX33
   image: Maxim.jpg
---

{% include header-image.md image="about_image.jpg" title="About UIKonf" description="UIKonf is an independent conference for serious iOS developers" %}


{% capture organizers_content %}
	{% assign sortedOrganizers = page.organizers | sort: 'lastName' %}
	{% for person in sortedOrganizers %}
		<div class="uk-width-medium-1-3 uk-width-small-1-1 uk-width-large-1-5">
        {% include person.md title=person.name outbox-description=person.bio image=person.image link=person.link isSmall=1 %}
	  </div>
	{% endfor %}
{% endcapture %}
{% include content-block.md topShape="straight" title="Current Team" content=organizers_content %}


{% capture organizers_content %}
	{% assign sortedAlumni = page.alumni | sort: 'lastName' %}
	{% for person in sortedAlumni %}
		<div class="uk-width-large-1-5 uk-width-small-1-2 uk-width-medium-1-3">
        {% include person.md title=person.name image=person.image link=person.link isSmall=1 %}
	  </div>
	{% endfor %}
{% endcapture %}
{% include content-block.md topShape="straight" title="Alumni" content=organizers_content %}

