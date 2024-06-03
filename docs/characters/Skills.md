---
layout: page
title: "Skills"
permalink: /characters/skills/
id: characters-skills
parent: Characters
nav_order: 3
---

# Skills

Skills represent the character’s capabilities across a variety of domains.

Skills have ratings from 0 to 4.  A characters Skill rating determines which die is rolled when taking an action involving the Skill as detailed in the Skill Rating table.

```
Rating |  Die
0      |  d4
1      |  d6
2      |  d8
3      |  d10
4      |  d12
```

## Action Skills
Action Skills are a crucial subset of Skills in the game that allow players to perform various tasks and actions without needing a specific Ability to utilize the Skill. These Skills represent the character's aptitude, proficiencies, and expertise that enable them to handle a wide range of situations.

## Effect Skills 
Effect Skills are a distinct set of Skills that require the use of a separate Action to be activated. These Skills represent specialized abilities or techniques that characters can use to produce specific effects or outcomes within the game.

Effect Skills come with the added benefit of Skill Talents which alter the results of any Actions for which the Skill is applied.  Characters acquire one Skill Talent for every rank they have in the Effect Skill.
Skill Talents come in two varieties: *Static* and *Trigger*.
*Static Skill Talents* take effect any time the Skill is used, while *Trigger Skill Talents* only occur when the result of the Skill attempt meet the Trigger's condition(s).

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


<div class="mytabs">
<input type="radio" id="tabbasics" name="mytabs" checked="checked">
<label for="tabdangerous">Dangerous</label>

<div class="tab">
<h2>Action Skills</h2>
<table style="text-align: center;">
    <tr>
        {% assign skills = site.data.skills | where: "trait", "Dangerous" %}
        {% for s in skills %}
            {% if s.type == 1 %}
                <td style="width: 110; height: 80px">
                    {{ s.name }}
                <br>
                <hr>
                <p>
                    {{ s.description }}
                </p>
                </td>
                {% assign i = forloop.index | modulo: 3 %}
                {% if i == 0 %}
                    </tr>
                    <tr>
                {% endif %}
            {% endif %}
        {% endfor %}

    </tr>
</table>
<br>
<h2>Effect Skills</h2>
<table style="text-align: center;">
    <tr>
        {% assign skills = site.data.skills | where: "trait", "Dangerous" %}
        {% for s in skills %}
            {% if s.type == "2" %}
                <td style="width: 110; height: 80px">
                    {{ s.name }}
                <br>
                <hr>
                <p>
                    {{ s.description }}
                </p>
                </td>
                {% assign i = forloop.index | modulo: 3 %}
                {% if i == 0 %}
                    </tr>
                    <tr>
                {% endif %}
            {% endif %}
        {% endfor %}

    </tr>
</table>
</div>


</div>


<style>
 
.mytabs {
    display: flex;
    flex-wrap: wrap;
    margin: 0px auto;
    padding: 25px;
}
.mytabs input[type="radio"] {
    display: none;
}

.mytabs label {
    padding: 25px;
    font-weight: bold;
}

.mytabs .tab {
    width: 100%;
    padding: 0px;
    order: 1;
    display: none;
}
.mytabs .tab h2 {
    font-size: 3em;
}

.mytabs input[type='radio']:checked + label + .tab {
    display: block;
}

.mytabs input[type="radio"]:checked + label {
    background: #444985;
}
</style>