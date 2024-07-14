---
layout: default
title: Epics
grand_parent: Characters
parent: Powers
permalink: /characters/powers/epics/
---

# Epics
Great tales, poems, and songs that capture stories of myth and legend.  Their utterance empowers you an your allies, and reubkes those who oppose you.

## Performing Epics
Epics have multiple verses, each of which produce different effects.  Each verse has a different (usually escalating) Threshold to perform them perfectly.  You must perform the verses in order in order to gain the benefits of their effect (unless you have the In Media Res talent).  Epics all have an Ongoing rating, so be carful to not let your perfromance get interrupted.  If an Epic you are performing gets interrupted, you must start performing over at its first verse if you want to attempt the performance again.

# Epics List

{% assign epics = site.data.powers.arcana %}

<section>
{% for a in epics %}
    <div style="background-color: #37344f50; padding: 10px">
        <h3 style="margin:5px">{{ a.name }}</h3>
        <h4 style="margin:5px">Max Ranks</h4>
        {% assign j = a.max_ranks %}
        {% for i in (1..j) %}
            <img style="width: 20px" src="/no1_system/assets/img/plain-circle.png">
        {% endfor %}
        <p><strong>Threshold &mdash; {{a.threshold}}</strong></p>
        <details>
            <summary>
            </summary>
            {% if a.requires %}
                <p style="margin:5px, font-size: 8">
                    <strong>Requires: </strong><em>{{ a.requires }}</em>
                </p>
            {% endif %}
            {% for v in a.verses %}
                {% if v.threshold %}
                    <div style="background-color: #4b476650; padding: 8px;">
                        <strong>{{ v.verse }}</strong>
                        <h4 style="margin:5px">{{ v.type }}</h4>
                        {% assign thresh = v.threshold %}
                        {% for t in thresh %}
                            <p><strong>Threshold &mdash; {{t.hits}}</strong>
                            <br>{{t.effect}}</p>
                        {% endfor %}
                    </div>
                    <div style="height:8px;"></div>
                {% endif %}
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