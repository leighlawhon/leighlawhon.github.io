{%- assign features = site.data.prioritize -%}
{%- assign sum = 0 -%}
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
                <td> {%- assign sum = sum | plus: feature.b -%}
                     {%- assign sum = sum | plus: feature.r -%}
                     {%- assign sum = sum | plus: feature.i -%}
                     {%- assign sum = sum | plus: feature.c -%}
                     {%- assign sum = sum | divided_by: feature.e %}
                     {{sum}}
                    <br/><small>{{feature.brice}} <br/>{{feature.b}} + {{feature.r}} + {{feature.i}} + {{feature.c}} / {{fetaure.e}}</small></td>
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

