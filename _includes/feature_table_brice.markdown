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
        {% for feature in features | sort "brice" %}
            <tr>
                <td> 
                     {{feature.brice | round: 2}}
                    <br/><small>{{feature.b}} + {{feature.r}} + {{feature.i}} + {{feature.c}} / {{feature.e}}</small></td>
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
        {% endfor %}
    </tbody>
</table>

