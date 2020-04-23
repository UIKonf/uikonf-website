---
layout: page
order: 6
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
 - name: Christine Braun
   lastName: Braun
   bio: Consulting and creation for businesses with good intentions <a href="mailto:post@chrissybrown.com">post@chrissybrown.com</a>.
   link: https://twitter.com/post4chrissy
   image: authors/christine-braun.jpg
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

{% assign sortedOrganizers = page.organizers | sort: 'lastName' %}

<div class="uk-section">
    <div class="uk-container">
        <h2 class="uk-text-center">Current Team</h2>
        <div class="uk-container uk-width-2-3@m">
            <div class="uk-grid uk-flex-center uk-child-width-1-3@m uk-child-width-1-1@s uk-margin-medium-top uk-margin-medium-bottom">
                	{% for person in sortedOrganizers %}
		                <div class="uk-margin-bottom uk-text-center">
                      {% include person.html title=person.name description=person.bio image=person.image link=person.link isSmall=1 %}
	                  </div>
	                {% endfor %}
            </div>
        </div>
    </div>
</div>


{% assign sortedAlumni = page.alumni | sort: 'lastName' %}

<div class="uk-section">
    <div class="uk-container">
        <h2 class="uk-text-center">Alumni</h2>
        <div class="uk-container uk-width-1-1@m">
            <div class="uk-grid uk-flex-center uk-child-width-1-6@m uk-child-width-1-1@s uk-margin-medium-top uk-margin-medium-bottom">
                	{% for person in sortedAlumni %}
		                <div class="uk-margin-bottom uk-text-center">
                      {% include person.html title=person.name image=person.image link=person.link isSmall=1 %}
	                  </div>
	                {% endfor %}
            </div>
        </div>
    </div>
</div>