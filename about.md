---
layout: page
order: 3
title: About
permalink: /about/
headerImage: uikonf_2020_hero_image.jpg
headerTitle: About UIKonf
description: UIKonf - UIKonf is an independent conference for serious iOS developers
includeInNavigation: 1
organizers:
 - name: Engin Kurutepe
   lastName: Kurutepe
   bio: Indie Developer at <a href="https://fifteenjugglers.com">Fifteen Jugglers</a> making <a href="https://solarwat.ch">SolarWatch</a> and <a href="https://calltap.app">CallTap</a>. Glider pilot.
   link: https://kurutepe.com
   image: engin-kurutepe.jpg
 - name: Sabine Geithner
   lastName: Geithner
   bio: iOS developer at Mercedes-Benz.io, former Online Marketer and Scientist.
   link: https://twitter.com/sabinegeithner
   image: sabine-geithner.jpg
 - name: Christine Braun
   lastName: Braun
   bio: Consulting and creation for businesses with good intentions <a href="mailto:post@chrissybrown.com">post@chrissybrown.com</a>.
   link: https://twitter.com/post4chrissy
   image: christine-braun.jpg
 - name: Bianca Walterspiel Stromlund
   lastName: Walterspiel
   bio: Managing Global Engineering Relations at Delivery Hero.
   link: https://twitter.com/biancawalty
   image: bianca-walterspiel.jpg
 - name: Julia Kallenberg
   lastName: Kallenberg
   bio: iOS Developer at <a target="_blank" href="http://www.nebenan.de">nebenan.de</a>. Traveler and former project manager for renewable energies.
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

{% capture organizers_content %}
	{% assign sortedOrganizers = page.organizers | sort: 'lastName' %}
	{% for person in sortedOrganizers %}
		<div class="uk-width-1-1@s uk-width-1-5@m uk-text-center uk-margin-medium-bottom">
        {% include person.md title=person.name description=person.bio image=person.image link=person.link isSmall=1 %}
	  </div>
	{% endfor %}
{% endcapture %}
{% include content-block.md title="Current Team" content=organizers_content %}


{% capture organizers_content %}
	{% assign sortedAlumni = page.alumni | sort: 'lastName' %}
	{% for person in sortedAlumni %}
		<div class="uk-width-1-1@s uk-width-1-5@m uk-text-center uk-margin-medium-bottom">
        {% include person.md title=person.name image=person.image link=person.link isSmall=1 %}
	  </div>
	{% endfor %}
{% endcapture %}
{% include content-block.md title="Alumni" content=organizers_content %}

