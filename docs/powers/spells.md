---
layout: default
title: Spells
grand_parent: Characters
parent: Powers
permalink: /characters/powers/spells/
---

# Spells

The mysteries of the Cosm leave traces across all of existence.  Hidden and forgotten lore may not be captured in the great voluems of history, but their effects are profound and resonana.
Some curious, and some say foolhardy, folk study these mysteries, known casually as Arcana.  Knowledge and comprehension of this mystical wisdom empowers these individuals to bend and shape reality to their will.

## Studying Spells
When you use an Ability that provides Spell Ranks, you invest those in specific Spells to increase their Rank reflecting your increased proficiency with them.

## Casting Spell
When casting a Spell, you make a roll for that specific Spell with a dice rating determined by your Ranks in that Spell.


# Spell List

<section>

<div class="column">

{% for s in site.data.powers.spells %}
{% assign i = forloop.index | modulo: 2 %}

<div class="row">
    <h3 style="margin:5px">{{s.name}}</h3>
    <h4 style="margin:5px">{{s.type}}</h4>
    <em>{{s.keywords}}</em>
    <details>
        <summary></summary>
        <p><strong>Requires: </strong>{{s.requires}}</p>
        <p><strong>Effect: </strong>{{s.effect}}</p>
        {% for t in s.threshold %}
        <h5 style="margin:5px">Threshold {{t.hits}} </h5>
        <p>{{t.effect}}</p>
        {% endfor %}
    </details>
</div>
{% endfor %}

</section>

<style>
  .row {
    display: flex;
    background-color: gray;

  }

  .column {
    flex: 95%;
    background-color: darkgray;
    margin: 5px;
  }
</style>