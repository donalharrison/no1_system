
## Skill List
Below is a list the base system Skills & a brief description of their uses.  The list is ordered by the Skill's associated Traits.

{: .note}
Some Skills require Training to be used (*marked X; below*).  Characters can acquire access to these skills by spending Milestones on Trainings that confer expertise with the Skill.

<table class="searchable sortable">
    <thead>
        <th>Name</th>
        <th>Trait</th>
        <th>Requires Training</th>
        <th>Description</th>
    </thead>
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