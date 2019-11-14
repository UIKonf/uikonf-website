<div class="box uk-width-1-2@m uk-width-1-3@l">
    <figure class="uk-overlay uk-overlay-hover">
        {% if include.active == 1 %}
            <img class="uk-overlay-spin" src="/static/images/events/{{ include.image }}" alt="{{ include.image-alt }}">
            <a class="uk-position-cover" href="/social-events#{{ include.anchor }}"></a>
        {% else %}
            <img src="/static/images/events/{{ include.image }}" alt="{{ include.image-alt }}"> 
        {% endif %}
    </figure>
    <div class="grey info-box">
        <h4>{{ include.title }}</h4>
        <p>
            <small>{{ include.description }}</small>
        </p>
    </div>
</div>