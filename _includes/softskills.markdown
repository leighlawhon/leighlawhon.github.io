<ul>
{% assign skills = site.data.skills.soft | sort: "title" %}
{% for skill in skills %}
<li class={{skill.level}}>{{skill.title}}</li>
{%endfor%}
</ul>