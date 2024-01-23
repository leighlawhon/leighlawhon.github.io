<ul>
{% assign skills = site.data.skills.technical | sort: "title" %}
{% for skill in skills %}
<li class={{skill.level}}>{{skill.title}}</li>
{%endfor%}
</ul>