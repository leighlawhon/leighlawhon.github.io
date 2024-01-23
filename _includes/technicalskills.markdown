{% assign skills = site.data.skills.technical | sort: "title" -%}
{% for skill in skills -%}
<div class={{skill.level}}>{{skill.title}}</div>
{%endfor%}