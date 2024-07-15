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

{{eskills}},

<hr>
<section>
{% assign tskills = site.data.skill_triggers.skill_triggers | map: "skill" | uniq | sort %}
{% for e in eskills %}
    {% for t in tskills %}
        {% if t == e %}
            <p>{{t}} &mdash; {{e}}</p>
        {% endif %}
    {% endfor %}
{% endfor %}
</section>

<section>

{% for eskill in eskills %}
    <div style="background-color: #37344f50; padding: 10px">
        <h3>{{ eskill }}</h3>
        {% assign talents = site.data.skill_triggers.skill_triggers %}
        {% for t in talents %}
                <div style="background-color: #4b476650; padding: 10px">
                    {{ t.skill }}
                </div>
                <div height=3px></div>
        {% endfor %}
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