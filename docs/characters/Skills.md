---
layout: page
title: "Skills"
permalink: /characters/skills/
id: characters-skills
---

# Skills

Skills represent the character’s training across a variety of domains.

Skills have ratings from 0 to 4.  A characters Skill rating determines which die is rolled when taking an action involving the Skill as detailed in the Skill Rating table.

```
Rating |  Die
0      |  d4
1      |  d6
2      |  d8
3      |  d10
4      |  d12
```
 
## Skill List
Below is a list the base system Skills & a brief description of their uses.  The list is ordered by the Skill's associated Traits.
[!Note] Some Skills require Training to be used (*marked X; below*).  Characters can acquire access to these skills by spending Milestones on Trainings that confer expertise with the Skill.

<table>
    <tr>
        <th>Name</th>
        <th>Trait</th>
        <th>Requires Training</th>
        <th>Description</th>
    </tr>
{% for t in site.data.skills %}
    <tr>
        <td>
        {{ t.name }}
        </td>
        <td>
        {{ t.trait }}
        </td>
        <td>
        {{ t.requires_training }}
        </td>
        <td>
        {{ t.description }}
        </td>
    </tr>
{% endfor %}

</table>
