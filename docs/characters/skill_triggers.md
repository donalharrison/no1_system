---
layout: page
title: "Skill Triggers"
permalink: /characters/skills/skill_triggers
id: characters-skills-triggers
grand_parent: Characters
parent: Skills
nav_order: 1
---

{: .note}
Original design by Keithen "Barph" Petty.

# Skill Triggers
Skill triggers are special Triggered Talents that alter the results of any Actions or Shifts with which the Effect Skill is applied.  Characters acquire one Skill Trigger for every rank they have in the Effect Skill.  When the condition(s) of the Skill Trigger is met, the effects happens immediately following the resolution of the the triggering effect.


{% assign eskills = site.data.skill_triggers.skill_triggers | map: "skill" | uniq | sort %}

{{eskills}}

<section>
{% for skill in eskills %}
    <div style="background-color: #4b476650; margin: 6px; padding: 5px;">
        <p style='margin: 3px; font-weight:bold; font-size: 115%;'>{{skill}}</p>
        <details>
            <summary></summary>
            {% assign triggers = site.data.skill_triggers | where: "skill", skill }
            {% for t in triggers %}
                {% if t.skill == {{skill}} %}
                    <div style="background-color: #37344f50; margin: 10px; padding: 5px;">
                        <h3 style="margin-top: 5px;">{{t.name}}</h3>
                        <h4 style="margin-top: 5px;">{{t.type}}</h4>
                        {% if t.ranks %}
                            {% assign j = t.ranks %}
                            <h4 style="margin-top: 5px;">Ranks</h4>
                            {% for i in (1..j) %}
                                <img style="width: 10px" src="/no1_system/assets/img/plain-circle.png">
                            {% endfor %}
                        {% endif %}
                        {% if t.effect %}
                            <p><strong>Effect</strong>
                            <br>{{t.effect}}</p>
                        {% endif %}
                    </div>
                    <div height=5px></div>
                {% endif %}
            {% endfor %}
        </details>
    </div>
    <div height=5px></div>
{% endfor %}
</section>

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