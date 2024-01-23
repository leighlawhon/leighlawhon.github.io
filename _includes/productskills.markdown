<div>

### Product Management

| Skill | Level |
| ---- | ---- |
{% assign skills = site.data.skills.product | sort: "title" -%}
{% for skill in skills -%}
| {{skill.title}} | {{skill.level}} |
{%endfor%}

</div>