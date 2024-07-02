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
    <label for="tab_all" style="font-size:140%">All Skills</label>
    <div class="tab">

    {% for tech in techs %}
        <h3>{{ tech.name }}</h3>
        <details>
            <summary></summary>
                <p>{{ tech }}</p>
        </details>
    {% endfor %}
    </div>

    {% assign eskills = site.data.skills | where: "type", "2" | map: "name" | uniq | sort %}

    {% for eskill in eskills %}
        {% assign tabid = 'tab_' | append: eskill %}
        <input type="radio" id="{{ tabid }}" name="mytabs">
        <label for="{{ tabid }}" style="font-size:140%">{{ eskill }}</label>
        <div class="tab">
            {% for tech in site.data.powers.techniques %}
                {% for tag in tech.keywords %}
                    {% if tag == eskill %}
                        <p>{{ tech }}</p>
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