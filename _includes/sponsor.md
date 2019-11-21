<div class="uk-grid">
    <div class="uk-width-1-1@s">
    {% if include.image %}
      <figure class="uk-inline-clip uk-transition-toggle">
        <img class="uk-transition-scale-up" src="/static/images/{{ include.image }}" alt="{{ include.image-alt }}" style="opacity: 1">
        <a class="uk-position-cover" href="{{ include.anchor }}" target="_blank"></a>
      </figure>
    {% endif %}
    </div>

</div>