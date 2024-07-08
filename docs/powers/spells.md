---
layout: default
title: Spells
grand_parent: Characters
parent: Powers
permalink: /characters/powers/spells/
---

# Spells
Spells are cool.

## Studying Spells
When you use an Ability that provides Spell Ranks, you invest those in specific Spells to increase their Rank reflecting your increased proficiency with them.

## Casting Spell
When casting a Spell, you make a roll for that specific Spell with a dice rating determined by your Ranks in that Spell.


# Spell List

<section>

<div style="background-color: ; margin: 5px;">

{% for s in site.data.powers.spells %}
    {% assign i = forloop.index | modulo: 2 %}
    {% if i == 0 %}
        <div style="background-color: #4b476650; margin: 10px; padding: 5px;">
    {% else %}
        <div class="row" style="background-color: #37344f50; margin: 10px; padding: 5px;">
    {% endif %}
    <h3 style="margin-top: 5px;">{{s.name}}</h3>
    <h4 style="margin-top: 5px;">{{s.type}}</h4>
    <em>{{s.keywords | join: ", "}}</em>
    <details>
        <summary></summary>
        {% assign j = s.max_ranks %}
        {% for i in (1..j) %}
            <img style="width: 20px" src="/no1_system/assets/img/plain-circle.png">
        {% endfor %}
        {% if s.requires %}
            <p><em>Requires: </em>{{s.requires}}</p>
        {% endif %}
        <p><strong>Effect</strong>
        <br>{{s.effect}}</p>
        {% assign thresh = s.threshold %}
            {% for t in thresh %}
                <h5>Threshold {{t.hits}} </h5>
                <p>{{t.effect}}</p>
            {% endfor %}
        <p>{{thresh}}</p>
    </details>
    </div>
{% endfor %}
</div>
</section>