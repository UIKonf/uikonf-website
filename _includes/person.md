 <figure class="uk-transition-toggle">
    <div class="uk-border-circle uk-inline-clip">
        <a href="{{ include.link }}"><div class="uk-transition-scale-up person-photo" style="background-image: url('/static/images/{{ include.image }}')"></div></a>
    </div>
 </figure>
<p><b>{{ include.title }}</b></p>
{% if include.description %}
    <p><small>{{ include.description }}</small></p>
{% endif %}