---
layout: default
title: Spirits
grand_parent: Characters
parent: Powers
permalink: /characters/powers/spirits/
---

# Spirits



## Binding Spirits


## Using Spirits


# Spirits List

{% assign spirits = site.data.powers.spirits %}

<section>
{% for s in spirits %}
    <div style="background-color: #37344f50; padding: 10px">
    <h3 style="margin:5px">{{ s.name }}</h3>
    <h4 style="margin:5px">Spirit Ranks</h4>
    {% assign j = s.cost %}
    {% for i in (1..j) %}
        <img style="width: 15px" src="/no1_system/assets/img/plain-circle.png">
    {% endfor %}
    <details>
        <summary>
        </summary>
    {% if s.requires %}
        <p style="margin:5px, font-size: 8">
            <strong>Requires: </strong><em>{{ s.requires }}</em>
        </p>
    {% endif %}
    {% for eff in s.effects %}
        <div style="background-color: #4b476650; padding: 8px;">
            {{ eff.skill }}
            <h4 style="margin:5px">{{ asp.type }}</h4>
            <p><strong>Effect</strong></p>
            <p>{{ eff.effect }}</p>
        </div>
        <div style="height:8px;"></div>
    {% endfor %}
    </details>
    </div>
    <div style="height:12px;"></div>
{% endfor %}
</section>

<style>
    tr:nth-child(even) {
        background-color: #34324050;
    }
    
    tr {
        border-bottom: 1px solid #ddd;
        }
</style>