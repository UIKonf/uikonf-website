---
layout: page
order: 2
title: Workshops
permalink: /workshops/
headerTitle: Workshops at UIKonf 2019
includeInNavigation: 1
description: UIKonf 2019 - Workshops
---

{% assign sorted = site.workshops | where_exp: "item", "item.includedIn contains 'workshops'" | sort: 'order' %}
{% for workshop in sorted %}
	{% include workshop.html workshop=workshop %}
{% endfor %}

In addition to these workshops, the last day of UIKonf will host an unconference-like get-together where everyone can share their knowledge in self-organized labs. If you want to offer a workshop as well, <a href="mailto:questions@uikonf.com" target="_blank">get in touch with us</a>.
