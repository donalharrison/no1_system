---
layout: default
title: Gifts
grand_parent: Characters
parent: Powers
permalink: /characters/powers/gifts/
---


# Gifts


## Accessing Gifts
You have access to any Gift with a Rank equal to or less than your current Succor.  This means as you gain and lose Succor, the list of available Gifts you can call upon changes too.  Keep your patron(s) contented with your actions and they are bountiful in their tidings.  Fail to appease them and they will reduce you to the wretched ineptitude you so desperately try to escape.

### Static Gifts
Some Gifts have the Static Talent type.  These function just like any Static Talent, but only if your Succor is equal to or greater than their Rank.

Example:
> ## Mantle of Fire
> ### Rank 2
> #### Static
> **Requires:** Infero Affinity
> Reduce any Hits you suffer from fire and effects with the Inferno keyword by -2

As long as you have the Inferno Affinity and maintain a Succor of 2+, Mantle of Fire is active and you reduce Hits suffered from fire and Inferno effects by -2.

## Using Gifts
To use a Gift, roll a number of dice equal to the current Challenge.  The type of dice determined by your current Succor in the same manner as Skill ranks, with 0 Succor providing d4s and 4 or more Succor providing d12s.  Any Succor above 4 is available to soak up reductions to Succor resulting from using specific Gifts or Talents that require you to spend Succor, or in the unfortunate event that one of your Gifts contains a 1 in the result set.

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