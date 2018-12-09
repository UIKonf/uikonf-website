<div class="headerimage-small uk-position-relative" style="background-image: url({{ site.baseurl }}/static/images/{{ include.image }});" data-uk-parallax="{bg: '-50'}">
  <img class="uk-invisible" src="{{ site.baseurl }}/static/images/{{ include.image }}" alt="home image"/>
  <div class="uk-position-cover uk-flex uk-flex-center uk-flex-middle uk-flex-column">
    <div class="teaser-register">
      <h1>{{ include.title }}</h1>
      {% if include.description %}
        <p>{{ include.description }}</p>
      {% else %}
        <div></div>
      {% endif %}
    </div>
  </div>
</div>
