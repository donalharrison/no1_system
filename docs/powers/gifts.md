---
layout: default
title: Gifts
grand_parent: Characters
parent: Powers
permalink: /characters/powers/gifts/
---


# Gifts


## Accessing Gifts


## Using Gifts


# Gift List

<section>

<div style="background-color: ; margin: 5px;">

{% assign eskills = "Aether,Bellor,Destroy,Inferno,Intuit,Mori,Nihil,Ordi,Rime,Vivus" | split: "," %}
{% for skill in eskills %}
    <div style="background-color: #1f1d2b50; margin: 6px; padding: 5px;">
        <p style='margin: 3px; font-weight:bold; font-size: 115%;'>{{skill}}</p>
        <details>
            <summary></summary>
        {% assign gifts = site.data.powers.gifts | where: 'skill', skill | sort: 'rank' %}
        {% for s in gifts %}
            {% assign i = forloop.index | modulo: 2 %}
            {% if i == 0 %}
                <div style="background-color: #4b476650; margin: 10px; padding: 5px;">
            {% else %}
                <div class="row" style="background-color: #37344f50; margin: 10px; padding: 5px;">
            {% endif %}
                <h3 style="margin-top: 5px;">{{s.name}}</h3>
                <h4 style="margin-top: 5px;">{{s.type}}</h4>
                <strong>Rank {{s.rank}}</strong>
                <em>{{s.keywords | join: ", "}}</em>
                <details>
                    <summary></summary>
                    {% if s.requires %}
                        <p><em>Requires: </em>{{s.requires}}</p>
                    {% endif %}
                    {% if s.effect %}
                        <p><strong>Effect</strong>
                        <br>{{s.effect}}</p>
                    {% endif %}
                    {% if threshold %}
                        {% assign thresh = s.threshold %}
                            {% for t in thresh %}
                                <p><strong>Threshold &mdash; {{t.hits}}</strong>
                                <br>{{t.effect}}</p>
                            {% endfor %}
                    {% endif %}
                </details>
            </div>
        {% endfor %}
        </details>
    </div>
{% endfor %}
</div>
</section>