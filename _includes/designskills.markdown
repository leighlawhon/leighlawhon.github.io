### Design 

| Skill | Level |
| ---- | ---- |
{% assign skills = site.data.skills.design | sort: "title" -%}
{% for skill in skills -%}
| {{skill.title}} | {{skill.level}} |
{%endfor%}
