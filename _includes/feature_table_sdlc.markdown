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
            {% if feature.sdlc %}
            <tr>
                <td> 
                    {{feature.brice}}
                </td>
                <td>
                    {{feature.feature}}
                </td>
                <td>
                    {{feature.sdlc.discovery}} weeks
                </td>
                <td>
                    {{feature.sdlc.design}} weeks
                </td>
                <td>
                    {{feature.sdlc.development}} weeks
                </td>
            </tr>
            {% endif %}
        {% endfor %}
    </tbody>
</table>

