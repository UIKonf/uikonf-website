---
layout: default
order: 4
title: Videos
includeInNavigation: 1
permalink: /videos/
description: Watch the videos of UIKonf 2016, 2015, 2014 and 2013 or learn more about Berlin's independent iOS developer conference.
redirect_from:
 - /videos/apps-are-just-the-tip-of-the-iceberg/
 - /videos/beyond-voiceover/
 - /videos/build-for-familiarity-or-no-one-will-use-your-app/
 - /videos/building-better-transitions/
 - /videos/cocoapods/
 - /videos/core-data-for-fun-and-profit/
 - /videos/demystifying-security-best-practices/
 - /videos/designing-custom-interfaces/
 - /videos/high-performance-core-data/
 - /videos/how-i-learned-to-stop-worrying-about-state-and-love-reactivecocoa/
 - /videos/how-to-bend-uikit-to-your-will/
 - /videos/image-performance/
 - /videos/inheriting-code-from-other-people/
 - /videos/modular-ios-apps/
 - /videos/objective-c-funtime-know-your-runtime/
 - /videos/opengl-es-demystified/
 - /videos/reverse-engineering-ios-apps/
 - /videos/software-interactions-with-the-real-world/
 - /videos/techniques-for-writing-dsls-in-objective-c/
 - /videos/textkit-for-the-rest-of-us/
 - /videos/unit-testing-on-ios-no-voodoo-necessary/
 - /videos/use-your-tools-app-optimization-with-instruments/
 - /videos/were-not-doing-a-startup/
videos:
  - title: UIKonf 2019
    url: https://www.youtube.com/embed/videoseries?list=PLdr22uU_wISr-FYeKblv3LMe_kHFzRFBw
    isMain: 1
 - title: UIKonf 2018
   url: https://www.youtube.com/embed/videoseries?list=PLdr22uU_wISohI7PIhzq0gotGfKZl1lGo
   isMain: 0
 - title: UIKonf 2017
   url: https://www.youtube.com/embed/videoseries?list=PLdr22uU_wISqntV4tQmx9H6sj9gMtj7nG
   isMain: 0
 - title: UIKonf 2016
   url: https://www.youtube.com/embed/videoseries?list=PLdr22uU_wISqm9QbnczWxXs9qyuWpSU4k
   isMain: 0
 - title: UIKonf 2015
   url: https://www.youtube.com/embed/SDZkKvC8r40?list=PLdr22uU_wISpW6XI1J0S7Lp-X8Km-HaQW
   isMain: 0
 - title: UIKonf 2014
   url: https://www.youtube.com/embed/TDAKOYQ7B-4?list=PLdr22uU_wISq-xmSdu1QQ4OJxr68qnJ54
   isMain: 0
 - title: UIKonf 2013
   url: https://www.youtube.com/embed/-fb4bIkniq8?list=PLdr22uU_wISruLvW5HhcbwbtkZ5w6hguY
   isMain: 0
---

{% include header-image.md image="videos_image.jpg" title="Videos" %}

{% capture video_content %}
	<div class="uk-width-medium-8-10 uk-container-center">
					<div class="videos-section uk-grid uk-margin-large-top">
						{% assign mainVideos = page.videos | where:"isMain",1 %}
						{% for video in mainVideos %}
  	      				<div class="uk-width-1-1 uk-text-center">
							<h3 class="brand-color">{{ video.title }}</h3>
  	      					<div class="uk-responsive-height">
                				<iframe width="100%" height="500" src="{{ video.url }}" frameborder="0" allowfullscreen></iframe>
  	      					</div>
			      		</div>
						{% endfor %}

			      		<div class="uk-width-1-1 uk-margin-large-top">
		        			<h1 class="brand-color">Other Videos</h1>
		      			</div>
						{% assign otherVideos = page.videos | where:"isMain",0 %}
						{% for video in otherVideos %}
						<div class="uk-width-medium-1-2">
  	      					<h3 class="brand-color">{{ video.title }}</h3>
  	      					<div class="uk-responsive-height">
  	      						<iframe width="100%" height="300" src="{{ video.url }}" frameborder="0" allowfullscreen></iframe>
  	      					</div>
			      		</div>
						{% endfor %}
			      	</div>
			    </div>
{% endcapture %}
{% include content-block.md topShape="straight" content=video_content %}
