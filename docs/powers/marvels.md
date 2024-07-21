---
layout: default
title: Marvels
grand_parent: Characters
parent: Powers
permalink: /characters/powers/marvels/
---

---
layout: default
title: Rites
grand_parent: Characters
parent: Powers
permalink: /characters/powers/rites/
---


# Marvels


## Attunement


## Using Marvels
To use a Marvel, your current Attunement must be equal to or greater than the Marvel's Rank.

# Marvels Lists

<section>
{% assign eskills = "Aether,Bellor,Inferno,Lux,Mori,Nihil,Nox,Orbi,Phylla,Rime,Squall,Tellus,Tempest,Torrent,Vivus" | split: "," %}
{% for skill in eskills %}
    <div style="background-color: #1f1d2b50; margin: 6px; padding: 5px;">
        <p style='margin: 3px; font-weight:bold; font-size: 115%;'>{{skill}}</p>
        <details>
            <summary></summary>
            {% for r in site.data.powers.marvels %}
                {% if r.skill == skill %}
                    <div style="background-color: #37344f50; margin: 10px; padding: 5px;">
                        <h3 style="margin-top: 5px;">{{r.name}}</h3>
                        <h4 style="margin-top: 5px;">{{r.type}}</h4>
                        <h5 style="margin-top: 5px;">Rank &mdash; {{r.rank}}</h5>
                        <em>{{r.keywords | join: ", "}}</em>
                        <details>
                        <summary></summary>
                            {% if r.requires %}
                                <p><em>Requires: </em>{{r.requires}}</p>
                            {% endif %}
                            {% if r.effect %}
                                <p><strong>Effect</strong>
                                <br>{{r.effect}}</p>
                            {% endif %}
                            {% assign thresh = r.threshold %}
                            {% for t in thresh %}
                                <p><strong>Threshold &mdash; {{t.hits}}</strong>
                                <br>{{t.effect}}</p>
                            {% endfor %}
                        </details>
                    </div>
                    <div height=5px></div>
                {% endif %}
            {% endfor %}
        </details>
    </div>
    <div height=5px></div>
{% endfor %}
</section>

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