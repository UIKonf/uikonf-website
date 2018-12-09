<div class="uk-grid">
    <div class="box uk-width-medium-1-3 uk-width-large-1-3 uk-width-small-1-1 ">
    {% if include.image %}
      <figure class="uk-overlay uk-overlay-hover">
        <img class="uk-overlay-spin" src="/static/images/{{ include.image }}" alt="{{ include.image-alt }}">
        <a class="uk-position-cover" href="{{ include.anchor }}" target="_blank"></a>
      </figure>
    {% endif %}
    </div>
    <div class="box uk-width-medium-2-3 uk-width-large-2-3 uk-width-small-1-1 ">
        <p>{{ include.content }}</p>
    </div>
</div>