{%- assign features = site.data.prioritize -%}

{%- assign moscow = ["M","S","C","W"] -%}
{% for letter in moscow %}
    {{letter}}
    {% for feature in features%}
        {{feature.moscow}}
    {% endfor %}
{% endfor %}

TEST