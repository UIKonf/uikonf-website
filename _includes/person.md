<div class="box">
    <figure class="uk-inline-clip uk-transition-toggle">
        <img class="uk-transition-scale-up" src="/static/images/{{ include.image }}" alt="{{ include.title }}"  style="opacity: 1" />
        <a class="uk-position-cover" href="{{ include.link }}"></a>
    </figure>
    {% if include.isSmall == 1 %}
    <div class="info-box small">
    {% else %}
    <div class="info-box">
    {% endif %}
        <h4>{{ include.title }}</h4>
        {% if include.inbox-description %}
            <p><small>{{ include.inbox-description }}</small></p>
        {% endif %}
    </div>
</div>
{% if include.outbox-description %}
	<p><small>{{ include.outbox-description }}</small></p>
{% endif %}
