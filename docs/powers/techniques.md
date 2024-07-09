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
<div>
{% assign eskills = "Aether,Inferno,Lux,Mori,Nihil,Nox,Plaga,Rime,Squall,Tellus,Tempest,Torrent,Vivus" | split: "," %}
<h2 style='margin: 5px'>Aether</h2>
<details>
    <summary></summary>
    <div>
    {% for t in site.data.powers.techniques %}
        {% if t.skill == "Aether" %}
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
                        <p><strong>Threshold &mdash; {{t.hits}}</strong>
                        <br>{{t.effect}}</p>
                    {% endfor %}
                </details>
            </div>
            <div height=5px></div>
        {% endif %}
    {% endfor %}
    </div>
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