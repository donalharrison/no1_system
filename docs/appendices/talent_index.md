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
        <th>Rank</th>
        <th>Type</th>
        <th>Description</th>
    </tr>
{% for t in site.data.talents_tmp.talents %}
    <tr>
        <td>
        {{ t.name }}
        </td>
        <td>
        {{ t.tree }}
        </td>
        <td>
        {{ t.rank }}
        </td>
        <td>
        {{ t.type }}
        </td>
        <td>
        {{ t.effect }}
        </td>
    </tr>
{% endfor %}

</table>
<p>
{% for i in site.data.talents_tmp.talents %}
    {{ i.tree }}
{% endfor %}
</p>

<p>
    {{ site.data.talents_tmp.talents | inspect }}
</p>