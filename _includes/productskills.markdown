<ul>
{% assign skills = site.data.skills.product | sort: "title" %}
{% for skill in skills %}
<li class={{skill.level}}>{{skill.title}}</li>
{%endfor%}
</ul>