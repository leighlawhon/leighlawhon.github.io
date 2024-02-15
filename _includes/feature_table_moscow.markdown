{%- assign features = site.data.prioritize -%}
{%- assign moscow = site.data.moscow -%}
<table>
    <thead>
        <td>Priority</td>
        <td>Org Team</td>
        <td>Feature</td>
        <td>Goal</td>
        <td>Deadline</td>
    </thead>
    <tbody>
        {% for priority in moscow %}
            {% for feature in features%}
                {{feature.moscow}}
                {%if priority.letter = feature.moscow%}
                <tr>
                    <td>{{priority.name}}</td>
                    <td>
                        {{feature.org}}
                    </td>
                    <td>
                        {{feature.feature}}
                    </td>
                    <td>
                        {{feature.goal}}
                    </td>
                    <td>
                        {{feature.deadline}}
                    </td>
                </tr>
                {% endif %}
            {% endfor %}
        {% endfor %}
    </tbody>
</table>

