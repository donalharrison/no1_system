---
layout: page
name: Talents Appendix
title: TTalents Appendix
permalink: /apendices/talents_appendix/
id: talents-appendix
parent: Apendices
has_children: false
nav_order: 4
---


# Talents

<section>
{% for t in site.data.talents.talents %}
    {% assign i = forloop.index | modulo: 2 %}
        {% if i == 0 %}
            <div style="background-color: #37344f50; padding: 10px">
        {% else %}
            <div style="background-color: #23213050; padding: 10px">
        {% endif %}
    <h3 style="margin:5px">{{ t.name }}</h3>
    {% if t.type == "Multi" %}
        <strong><em>{{ t.type }}</em></strong>
    {% else %}
        <h4 style="margin:5px; padding-bottom:15px; padding-top:2px">{{ t.type }}</h4>
    {% endif %}
    {% for e in t.effect %}
        <p>
        {{ e }}
        </p>
    {% endfor %}
    </div>
{% endfor %}

</section>