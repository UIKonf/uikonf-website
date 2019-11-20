
<div class="wrapper">
	<div class="uk-container uk-margin-large-bottom">
		<div class="uk-grid">
			<div class="uk-width-medium-1-3 uk-width-small-1-1 uk-width-1-3@l">
				<a name="{{ include.anchor }}"></a>
				<div class="box">
					<figure class="uk-inline-clip uk-transition-toggle">
						{%if include.link %}
							{% assign overlay-class="uk-transition-scale-up" %} 
						{% else %}
							{% assign overlay-class="uk-overlay" %} 
						{% endif %}
						<img class="{{ overlay-class }}" src="{{ site.baseurl }}/static/images/{{ include.image }}" alt="{{ include.imageAlt }}" style="opacity: 1">
						{% if include.link %}<a class="uk-position-cover" href="{{ include.link }}" target="_blank"></a>{% endif %}
					</figure>
					<div  class="info-box small">
						<h4>{{ include.imageTitle }}</h4>
					</div>
				</div>
			</div>
			<div class="uk-width-medium-2-3 uk-width-small-1-1 uk-width-large-2-3" style="padding-top:10px;">
				{{ include.content }}
			</div>
		</div>
	</div>
</div>
