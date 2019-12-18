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
 - name: Sabine Geithner
   lastName: Geithner
   bio: iOS developer at Mercedes-Benz.io, former Online Marketer and Scientist.
   link: https://twitter.com/sabinegeithner
   image: authors/sabine-geithner.jpg
 - name: Christine Braun
   lastName: Braun
   bio: Consulting and creation for businesses with good intentions <a href="mailto:post@chrissybrown.com">post@chrissybrown.com</a>.
   link: https://twitter.com/post4chrissy
   image: authors/christine-braun.jpg
 - name: Bianca Walterspiel Stromlund
   lastName: Walterspiel
   bio: Managing Global Engineering Relations at Delivery Hero.
   link: https://twitter.com/biancawalty
   image: authors/bianca-walterspiel.jpg
 - name: Julia Kallenberg
   lastName: Kallenberg
   bio: iOS Developer at <a target="_blank" href="http://www.nebenan.de">nebenan.de</a>. Traveler and former project manager for renewable energies.
   link: https://twitter.com/KallenbergJulia
   image: authors/julia-kallenberg.jpg
alumni:
 - name: Engin Kurutepe
   lastName: Kurutepe
   link: https://kurutepe.com
   image: authors/engin-kurutepe.jpg
 - name: Diana Arce
   lastName: Arce
   link: https://twitter.com/visualosmosis
   image: alumni/diana_thumb.jpg
 - name: Chris Eidhof
   lastName: Eidhof
   link: https://twitter.com/chriseidhof
   image: alumni/chris_thumb.jpg
 - name: Matt Patterson
   lastName: Patterson
   link: https://twitter.com/mattpatterson
   image: alumni/matt_thumb.jpg
 - name: Peter Bihr
   lastName: Bihr
   link: https://twitter.com/peterbihr
   image: alumni/peter_thumb.jpg
 - name: Max Krüger
   lastName: Krüger
   link: https://twitter.com/KrgerMax
   image: alumni/max_thumb.jpg
 - name: Maxim Zaks
   lastName: Zaks
   bio: Software developer with a passion for Games, Testing and Agile.
   link: https://twitter.com/iceX33
   image: alumni/Maxim.jpg
---

{% capture organizers_content %}
	{% assign sortedOrganizers = page.organizers | sort: 'lastName' %}
	{% for person in sortedOrganizers %}
		<div class="uk-width-1-1@s uk-width-1-4@m uk-text-center uk-margin-medium-bottom">
        {% include person.html title=person.name description=person.bio image=person.image link=person.link isSmall=1 %}
	  </div>
	{% endfor %}
{% endcapture %}
{% include content-block.html title="Current Team" content=organizers_content %}


{% capture organizers_content %}
	{% assign sortedAlumni = page.alumni | sort: 'lastName' %}
	{% for person in sortedAlumni %}
		<div class="uk-width-1-1@s uk-width-1-6@m uk-text-center uk-margin-medium-bottom">
        {% include person.html title=person.name image=person.image link=person.link isSmall=1 %}
	  </div>
	{% endfor %}
{% endcapture %}
{% include content-block.html title="Alumni" content=organizers_content %}

