---
layout: default
title: Hexes
grand_parent: Characters
parent: Powers
permalink: /characters/powers/hexes/
---

# Hexes


## Using Hexes
Most all Hexes have the Ongoing keyword.  These all have the Maintain Focus Trigger as detailed in the Keywords section.


# Hex List

<section>

<div style="background-color: ; margin: 5px;">

{% for s in site.data.powers.hexes %}
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
        <h4 style="margin-top: 5px;">Max Ranks</h4>
        {% for i in (1..j) %}
            <img style="width: 20px" src="/no1_system/assets/img/plain-circle.png">
        {% endfor %}
        {% if s.requires %}
            <p><em>Requires: </em>{{s.requires}}</p>
        {% endif %}
        {% if s.effect %}
            <p><strong>Effect</strong>
            <br>{{s.effect}}</p>
        {% endif %}
        {% assign thresh = s.threshold %}
            {% for t in thresh %}
                <p><strong>Threshold &mdash; {{t.hits}}</strong>
                <br>{{t.effect}}</p>
            {% endfor %}
    </details>
    </div>
{% endfor %}
</div>
</section>