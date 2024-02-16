{%- assign features = (site.data.prioritize  | sort:"brice" | reverse) -%}
<table>
    <thead>
        <td>Priority</td>
        <td>Feature</td>
        <td>Discovery</td>
        <td>Design</td>
        <td>Development</td>
    </thead>
    <tbody>
        {% for feature in features%}
            <tr>
                <td> 
                    {{feature.brice}}
                </td>
                <td>
                    {{feature.feature}}
                </td>
                <td>
                    {{feature.discovery}}
                </td>
                <td>
                    {{feature.design}}
                </td>
                <td>
                    {{feature.development}}
                </td>
            </tr>
        {% endfor %}
    </tbody>
</table>

