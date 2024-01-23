{% assign skills = site.data.skills.design | sort: "title" -%}
{% for skill in skills -%}
<div class={{skill.level}}>{{skill.title}}</div>
{%endfor%}