---
layout: default
title: Concoctions
grand_parent: Characters
parent: Powers
permalink: /characters/powers/concoctions/
---

# Concoctions

There are 4 types of Concoction:
- Elixirs -- heal and restore their users.
- Oils -- make Gear more efefctive.
- Poision -- hinder and harm their users.
- Potions -- imbue their users with powers.


## Preparing Concoctions
Each Concoction Rank comes with a number of Doses yielded.


## Using Concoctions
Concoctions all hacve the Consummable keyword, allowing their effects to be accessed using a Shift.

# Concoction List


{% assign c_uni = site.data.powers.concoctions | map: "type" | uniq | sort %}

<section>
{% for c_type in c_uni %}
    <h2 style="margin:8px">{{ c_type }}s</h2>
    {% assign concs = site.data.powers.concoctions | where: "type", c_type %}
    {% assign c_nms = site.data.powers.concoctions | where: "type", c_type | map: "name" | uniq | sort %}
    {% for c_nm in c_nms %}
        <div style="background-color: #37344f50; padding: 10px">
            <h3 style="margin:5px">{{ c_nm }}</h3>
            <h4 style="margin:5px">{{ c_type }}</h4>
            <details>
                <summary>
                </summary>
                {% for c in concs %}
                    {% if c.name == c_nm %}
                        <div style="background-color: #4b476650; padding: 10px">
                            {% assign j = c.ranks %}
                            <strong>Ranks</strong><br>
                            {% for i in (1..j) %}
                                <img style="width: 20px" src="/no1_system/assets/img/plain-circle.png">
                            {% endfor %}
                            <p><strong>Doses &mdash;</strong>  {{ c.doses }}</p>
                            <p><strong>Effect &mdash;</strong>
                            <br>{{ c.effect }}</p>
                        </div>
                        <div style="height:8px;"></div>
                    {% endif %}
                {% endfor %}
            </details>
            </div>
            <div style="height:12px;"></div>
    {% endfor %}
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