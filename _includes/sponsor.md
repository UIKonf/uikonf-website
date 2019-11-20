<div class="uk-grid">
    <div class="box uk-width-1-3@m uk-width-1-1@s uk-width-1-3@l ">
    {% if include.image %}
      <figure class="uk-inline-clip uk-transition-toggle">
        <img class="uk-transition-scale-up" src="/static/images/{{ include.image }}" alt="{{ include.image-alt }}" style="opacity: 1">
        <a class="uk-position-cover" href="{{ include.anchor }}" target="_blank"></a>
      </figure>
    {% endif %}
    </div>
    <div class="box uk-width-2-3@m uk-width-1-1@s uk-width-2-3@l" style="padding-right:20px;">
        <p>{{ include.content }}</p>
    </div>
</div>