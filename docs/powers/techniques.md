---
layout: default
title: Techniques
grand_parent: Characters
parent: Powers
permalink: /characters/powers/techniques/
---

# Techniques


## Current
Techniques allow your to channel raw energies into effects to harm or empower.  Calling upon these power creates a stream of evergy that flows through you, called ***Current***.  As this Current grows stronger, you can harness more powerful Techniques.

## Using Techniques
Each Technique includes a *Cost* & a *Current* value.  The Cost value is how much Current is required to use the Technique.  The Current value is how much Current the Technique generates for you to use other Techniques.  A Tehcniques Current value sets your available Current, it does not add to it.  Managing your Current can be challenging, requiring planning to build up to ever stronger Techniques.



# Technique Lists

{% assign techs = site.data.powers.techniques %}

<div class="mytabs">
    <input type="radio" id="tab_all" name="mytabs" checked="checked">
    <label for="tab_all" style="font-size:130%">All Skills</label>
    <div class="tab">
    {% for t in techs %}
        {% assign i = forloop.index | modulo: 2 %}
        {% if i == 0 %}
            <div style="background-color: #4b476650; margin: 10px; padding: 5px;">
        {% else %}
            <div style="background-color: #37344f50; margin: 10px; padding: 5px;">
        {% endif %}
        <h3 style="margin-top: 5px;">{{t.name}}</h3>
        <h4 style="margin-top: 5px;">{{t.type}}</h4>
        <em>{{t.keywords | join: ", "}}</em>
        <details>
            <summary></summary>
            {% if t.requires %}
                <p><em>Requires: </em>{{t.requires}}</p>
            {% endif %}
            {% if t.effect %}
                <p><strong>Effect</strong>
                <br>{{t.effect}}</p>
            {% endif %}
            {% assign thresh = t.threshold %}
            {% for t in thresh %}
                <p><strong>Threshold &mdash {{t.hits}}</strong>
                <br>{{t.effect}}</p>
            {% endfor %}
        </details>
    {% endfor %}
    </div>
    {% assign eskills = ["Inferno", "Lux", "Nox", "Plaga", "Rime", "Squall", "Tellus", "Tempest", "Torrent", "Vivus"] %}
    {% for eskill in eskills %}
        {% assign tabid = 'tab_' | append: eskill %}
        <input type="radio" id="{{ tabid }}" name="mytabs">
        <label for="{{ tabid }}" style="font-size:110%">{{ eskill }}</label>
        <div class="tab">
            {% for t in site.data.powers.techniques %}
                {% for tag in t.keywords %}
                    {% if tag == eskill %}
                        <div style="background-color: #37344f50; margin: 10px; padding: 5px;">
                        <h3 style="margin-top: 5px;">{{t.name}}</h3>
                        <h4 style="margin-top: 5px;">{{t.type}}</h4>
                        <em>{{t.keywords | join: ", "}}</em>
                        <details>
                            <summary></summary>
                            {% if t.requires %}
                                <p><em>Requires: </em>{{t.requires}}</p>
                            {% endif %}
                            {% if t.effect %}
                                <p><strong>Effect</strong>
                                <br>{{t.effect}}</p>
                            {% endif %}
                            {% assign thresh = t.threshold %}
                            {% for t in thresh %}
                                <p><strong>Threshold &mdash {{t.hits}}</strong>
                                <br>{{t.effect}}</p>
                            {% endfor %}
                        </div>
                        <div height=5px></div>
                    {% endif %}
                {% endfor %}
            {% endfor %}
        </div>
    {% endfor %}
</div>


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