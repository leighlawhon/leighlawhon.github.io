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
        {% for feature in features%}
            <tr>
                <td>test<br/>{{ feature.b }} + {{ feature.r }} + {{ feature.i }} + {{ fetaure.c )}}/ {{ fetaure.e }}</td>
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
    </tbody>
</table>

