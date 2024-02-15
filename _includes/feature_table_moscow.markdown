{%- assign features = site.data.prioritize -%}

<table>
    <thead>
        <td>Org Team</td>
        <td>Feature</td>
        <td>Goal</td>
        <td>Deadline</td>
    </thead>
    <tbody>

        {% for feature in features%}
        <tr>
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
        {%endfor%}
    </tbody>
</table>