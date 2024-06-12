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

## Skills Lists

<div class="mytabs">

{% assign skill_traits = site.data.skills | map: "trait" | uniq | sort %} 

{% for strait in skill_traits %}
    {% assign tabid = 'tab_' | append: strait %}

    {% if strait == 'Dangerous' %}
        <input type="radio" id="{{ tabid }}" name="mytabs" checked="checked">
    {% else %}
        <input type="radio" id="{{ tabid }}" name="mytabs">
    {% endif %}

    <label for="{{ tabid }}" style="font-size:140%">{{ strait }}</label>

    <div class="tab">
    <h3>Action Skills</h3>
    <table style="text-align: left;">
        <tr>
            {% assign skills = site.data.skills | where: "trait", strait | where: "type", "1" %}
            {% for s in skills %}
                <td style="width: 33%; height: 80px; padding: 5px">
                <p style="font-size:125%; margin:3px;">
                    <strong>
                    {{ s.name }}
                    </strong>
                </p>
                <hr style="margin: 3px;">
                <p style="margin: 3px;">
                    {{ s.description }}
                </p>
                </td>
                {% assign i = forloop.index | modulo: 3 %}
                {% if i == 0 %}
                    </tr>
                    <tr>
                {% endif %}
            {% endfor %}

        </tr>
    </table>
    <h3>Effect Skills</h3>
    <table style="text-align: left;">
        <tr>
            {% assign skills = site.data.skills | where: "trait", strait | where: "type", "2" %}
            {% for s in skills %}
                <td style="width: 33%; height: 80px; padding: 5px">
                <p style="font-size:125%; margin:3px;">
                    <strong>
                    {{ s.name }}
                    </strong>
                </p>
                <hr style="margin: 3px;">
                <p style="margin: 3px;">
                    {{ s.description }}
                </p>
                </td>
                {% assign i = forloop.index | modulo: 3 %}
                {% if i == 0 %}
                    </tr>
                    <tr>
                {% endif %}
            {% endfor %}

        </tr>
    </table>
    </div>

{% endfor %}

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