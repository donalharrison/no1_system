---
layout: page
title: "No1 - Skills"
permalink: /characters/trainings/
---


# Training
Training is the cornerstone of characters' capabilities & advancement.  Players invest Milestones into Training, gaining access to new [Talents](/characters/talents/) & increasing their [Skill](/characters/skills/) ratings.

## Training List

<table>
    <tr>
        <th>Name</th>
        <th>Type</th>
        <th>Prerequisites</th>
        <th>Description</th>
    </tr>
{% for t in site.data.training %}
    <tr>
        <td>
        {{ t.Name }}
        </td>
        <td>
        {{ t.Type }}
        </td>
        <td>
        {{ t.Prerequisites }}
        </td>
        <td>
        {{ t.Description }}
        </td>
    </tr>
{% endfor %}

</table>