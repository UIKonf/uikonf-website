
<div class="wrapper">
    <div class="uk-container">
        <div class="uk-grid uk-grid-small">
            {% if include.title %}
            <div class="uk-width-1-1 uk-text-center">
                <h2 class="brand-color">{{ include.title }}</h2>
            </div>
            {% endif %}
            {{ include.content }}
        </div>
    </div>
</div>