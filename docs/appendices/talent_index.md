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
{% for t in site.data.talents_tmp.talents %}
    <tr>
        <td>
        {{ t.Name }}
        </td>
        <td>
        {{ t.tree }}
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
<p>
{% for i in site.data.talents %}
    {{ i.tree }}
{% endfor %}
</p>

<p>
    {{ site.data.talents | inspect }}
</p>