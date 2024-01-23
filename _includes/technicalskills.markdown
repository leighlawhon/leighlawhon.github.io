<table>
{% assign skills = site.data.skills.technical | sort: "title" %}
{% for skill in skills %}
<tr><td class={{skill.level}}>{{skill.title}}</td></tr>
{%endfor%}
</table>