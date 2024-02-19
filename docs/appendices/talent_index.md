---
layout: page
title: "Talent Index"
permalink: /apendices/talents/
id: talent-index
parent: Appendices
nav_order: 4
---

<table>
    <tr>
        <th>Name</th>
        <th>Training</th>
        <th>Type</th>
        <th>Description</th>
    </tr>
{% for t in site.data.talents %}
    <tr>
        <td>
        {{ t.Name }}
        </td>
        <td>
        {{ t.Training }}
        </td>
        <td>
        {{ t.Type }}
        </td>
        <td>
        {{ t.Effect }}
        </td>
    </tr>
{% endfor %}

</table>
