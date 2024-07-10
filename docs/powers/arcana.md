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
    <div style="background-color: #37344f50; padding: 10px">
    <h3 style="margin:5px">{{ a.name }}</h3>
    <h4 style="margin:5px">Max Ranks</h4>
    {% assign j = a.max_ranks %}
    {% for i in (1..j) %}
        <img style="width: 20px" src="/no1_system/assets/img/plain-circle.png">
    {% endfor %}
    <details>
        <summary>
        </summary>
    {% if a.requires %}
        <p style="margin:5px, font-size: 8">
            <strong>Requires: </strong><em>{{ a.requires }}</em>
        </p>
    {% endif %}
        <p><strong>Threshold &mdash; {{a.threshold}}</strong>
    {% for asp in a.aspects %}
        <div style="background-color: #4b476650; padding: 8px;">
        {{ asp.skill }}
        <h4 style="margin:5px">{{ asp.type }}</h4>
        <strong>Strain:</strong> {{ asp.strain }}<br>
        <table>
            <tr>
                <th style="width: 20%;">Rank</th>
                <th>Effect</th>
            </tr>
            {% assign eff = asp.effects %}
            {% for dtl in asp.effects %}
                <tr>
                <td style="width: 20%;">
                {% assign k = dtl.rank %}
                {% for i in (1..k) %}
                    <img style="width: 20px" src="/no1_system/assets/img/plain-circle.png">
                {% endfor %}
                </td>
                <td>{{ dtl.effect }}</td>
                </tr>
            {% endfor %}
        </table>
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