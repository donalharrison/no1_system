---
layout: page
name: Training
title: Training
permalink: /characters/training-2/
id: characters-training
parent: Characters
has_children: false
nav_order: 4
---


# Training
Training is the cornerstone of characters' capabilities & advancement.  Players invest Milestones into Training ranks, gaining access to [Talents](/characters/talents/) which provide new abilities or increase their [Skill](/no1_system/characters/skills/) ratings.  Each Milestone spent increases characters' rank in the respective Training & allows them to select one of the Talents on that Training's list of equal or lower rank that the character does not yet have.
Characters must meet all prerequisites before spending a Milestone on Training ranks.

Trainings are categorized in three different types -- Basics, Specializations, & Disciplines.  These categories reflect the advanced experience required to study, master, & leverage the Training's talents.  As such, each type has different 

## Talents
Talents acrquired through Training make up the core of character advancement & customization.  There are three distinct types of Talents:
- Ability: The 
- Static:
- Trigger: Triggers take effect when certain conditions are met when a character attempts an Action.  If an Action meets a Trigger's condition, the effects happens immediately following the resolution of the Action (unless noted otherwise in the Trigger's description).

<div class="mytabs">
<input type="radio" id="tabbasics" name="mytabs" checked="checked">
<label for="tabbasics">Basics</label>
<div class="tab">
<table style="text-align: center;">
    <tr>
        {% assign basics = site.data.training | where: "Type", "Basic" %}
        {% for t in basics %}

                <td style="width: 80; height: 80px">
                    <a href="{{ t.page_path }}">
                    <img src="{{ t.img_path }}" width="70" height="70">
                    <br>
                    {{ t.Name }}
                    </a>
                    </td>
                
                {% assign i = forloop.index | modulo: 4 %}
                {% if i == 0 %}
                    </tr>
                    <tr>
                {% endif %}
        {% endfor %}

    </tr>

</table>
</div>


<input type="radio" id="tabspecs" name="mytabs">
<label for="tabspecs">Specializations</label>
<div class="tab">
<table style="text-align: center;">
    <tr>
        {% assign specs = site.data.training | where: "Type", "Specialization" %}
        {% for t in specs %}

                <td style="width: 80; height: 80px">
                    <a href="{{ t.page_path }}">
                    <img src="{{ t.img_path }}" width="70" height="70">
                    <br>
                    {{ t.Name }}
                    </a>
                    </td>
                
                {% assign i = forloop.index | modulo: 4 %}
                {% if i == 0 %}
                    </tr>
                    <tr>
                {% endif %}
        {% endfor %}

    </tr>

</table>
</div>

<input type="radio" id="tabdiscs" name="mytabs">
<label for="tabdiscs">Disciplines</label>
<div class="tab">
<table style="text-align: center;">
    <tr>
        {% assign discs = site.data.training | where: "Type", "Discipline" %}
        {% for t in discs %}

                <td style="width: 80; height: 80px">
                    <a href="{{ t.page_path }}">
                    <img src="{{ t.img_path }}" width="70" height="70">
                    <br>
                    {{ t.Name }}
                    </a>
                    </td>
                
                {% assign i = forloop.index | modulo: 4 %}
                {% if i == 0 %}
                    </tr>
                    <tr>
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
    margin: 10px auto;
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
    padding: 20px;
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