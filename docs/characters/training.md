---
layout: page
name: Training
title: Training
permalink: /characters/training/
id: characters-training
parent: Characters
has_children: false
nav_order: 3
---

# Training
Training is the cornerstone of characters' capabilities & advancement.  Players invest Milestones into Training ranks, gaining access to [Talents](/characters/talents/) which provide new abilities or increase their [Skill](/no1_system/characters/skills/) ratings.  Each Milestone spent increases characters' rank in the respective Training & allows them to select one of the Talents on that Training's list of equal or lower rank that the character does not yet have.
Characters must meet all prerequisites before spending a Milestone on Training ranks.

## Talents
Talents acrquired through Training make up the core of character advancement & customization.  There are three distinct types of Talents -- **Abilities, Static, & Triggers**.

### Abilities
Ability Talents require an Action to use.  Abilities include a Skill name in their description, which indicates the Skill you roll when using the Ability.

### Shift
Shift Talents require a Shift to use.  Some Shift talens contains a Skill name in their description, in which case you you roll this Skill.

### Static
Static Talents are always in effect.

### Trigger
Triggers take effect when certain conditions are met when in the game fiction.  If Trigger's condition is met, the effects happens immediately following the resolution of the the triggering effect.

## Training Lists
Trainings are classified as Basics, Specializations, or Disciplines.  These categories reflect the advanced experience required to study, master, & leverage the Training's talents.

Basics are the earliest Trainings availabe to characters, generally requiring only certain Trait ratings.  Specializations are more advanced Trainings that also require specific Skill Ranks.  Disciplines are the pinnacle of Training, representing expertise and mastery of esoteric Talents, with requirements that can only be accomplished in the game fiction.


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