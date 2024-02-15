{%- assign features = site.data.prioritize -%}

<table>
    <thead>
        <td>Priority</td>
        <td>Org Team</td>
        <td>Feature</td>
        <td>Goal</td>
        <td>Deadline</td>
    </thead>
    <tbody>
        {%- assign moscow = ["M","S","C","W"] -%}
        {% for letter in moscow %}
            {% for feature in features%}
                {%if letter = feature.moscow%}
                <tr>
                    <td>{{letter}}</td>
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