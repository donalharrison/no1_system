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

<section>

<div style="margin: 5px;">

{% assign skill_trigs = site.data.skill_triggers.skill_triggers %}
{% for eskill in eskills %}
    {% assign i = forloop.index | modulo: 2 %}
    {% if i == 0 %}
        <div style="background-color: ##2e294d50; margin: 10px; padding: 5px;">
    {% else %}
        <div class="row" style="background-color: #37344f50; margin: 10px; padding: 5px;">
    {% endif %}
        <h2 style="margin:5px">{{ eskill }}</h2>
        <details>
            <summary></summary>
            {% for t in skill_trigs %}
                {% if t.skill == eskill %}
                    <div style="background-color: #4b476650; padding: 10px">
                        <h3 style="margin:5px">{{ t.name }}</h3>
                        <h4 style="margin:5px">{{ t.type }}</h4>
                        {% assign j = t.rank %}
                       <p>
                            <strong>Rank</strong><br>
                        {% for i in (1..j) %}
                            <img style="width: 15px" src="/no1_system/assets/img/plain-circle.png">
                        {% endfor %}
                        </p>
                        <p>
                            <strong>Effect &mdash;</strong>
                            <br>{{ t.effect }}
                        </p>
                    </div>
                    <div height=3px style="background-color: #37344f50; padding: 10px"></div>
                {% endif %}
            {% endfor %}
        </details>
    </div>
    <div height=5px></div>
{% endfor %}
</div>
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