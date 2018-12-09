<div class="{{ include.topShape }}">
    <div class="wrapper">
        <div class="uk-container uk-container-center">
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
</div>