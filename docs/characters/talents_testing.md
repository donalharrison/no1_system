---
layout: page
name: Training
title: Talents
permalink: /characters/talents-test/
id: characters-talents-test
parent: Characters
has_children: false
nav_order: 8
---

# Talents

<section>
{% for t in site.data.talents_tmp.talents %}
    {% assign i = forloop.index | modulo: 2 %}
        {% if i == 0 %}
            <div style="background-color: #37344f50; padding: 10px">
        {% else %}
            <div style="background-color: #23213050; padding: 10px">
        {% endif %}
    <h3 style="padding-bottom:5px">{{ t.name }}</h3>
    {% if t.type == "Multi" %}
        <strong><em>{{ t.type }}</em></strong>
    {% else %}
        <h4>{{ t.type }}</h4>
    {% endif %}
    {% for e in t.effect %}
        <p>
        {{ e }}
        </p>
    {% endfor %}
    </div>
{% endfor %}

</section>