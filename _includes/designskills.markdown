<ul>
{% assign skills = site.data.skills.design | sort: "title" %}
{% for skill in skills %}
<li class={{skill.level}}>{{skill.title}}</li>
{%endfor%}
</ul>