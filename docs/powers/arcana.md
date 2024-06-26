---
layout: default
title: Arcana
grand_parent: Characters
parent: Powers
permalink: /characters/powers/arcana/
---

# Arcana

The mysteries of the Cosm leave traces across all of existence.  Hidden and forgotten lore may not be captured in the great voluems of history, but their effects are profound and resonana.
Some curious, and some say foolhardy, folk study these mysteries, known casually as Arcana.  Knowledge and comprehension of this mystical wisdom empowers these individuals to bend and shape reality to their will.

## Studying Arcana
When you use an Ability that provides Arcana Ranks, you invest those in specific Arcana to increase their Rank and augmenting the Arcanum's effects.

## Using Arcana
Arcana have Aspects, each of which has an Effect Skill associated with ia.  When you invoke an Arcana, select which Aspect you wish to use and roll the associated Effect Skill.
The Arcana's effects depend on how many rank you have invested.


# Arcana List

{% assign arcs = site.data.powers.arcana %}

<section>
{% for a in arcs %}
    {% assign i = forloop.index | modulo: 2 %}
    {% if i == 0 %}
        <div style="background-color: #37344f50; padding: 10px">
    {% else %}
        <div style="background-color: #23213050; padding: 10px">
    {% endif %}
    <h3 style="margin:5px">{{ a.name }}</h3>
    <h4 style="margin:5px">Max Ranks</h4>
    {% assign j = a.max_ranks %}
    {% for i in (1..j) %}
        <img style="width: 30px" src="/no1_system/assets/img/plain-circle.png">
    {% endfor %}
    {% if a.requires %}
        <p style="margin:5px, font-size: 8">
            <strong>Requires: </strong><em>{{ a.requires }}</em>
        </p>
    {% endif %}
    {% for asp in a.aspects %}
        <div style="background-color: #4b4766; padding: 8px">
        {{ asp.skill }}
        <h4 style="margin:2px">{{ asp.type }}</h4>
        <strong>Strain:</strong> {{ asp.strain }}<br>
        {% for eff in asp.effect %}
            <p>{{ eff.rank }}</p>
            <p>{{ eff.effect }}</p>
        {% endfor %}
        </div>
        <div></div>
    {% endfor %}
    </div>
    <div></div>
{% endfor %}
</section>