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
            <div style="background-color: #37344f">
        {% else %}
            <div style="background-color: #232130">
        {% endif %}
    <strong>{{ t.name }}</strong>
    {% if t.type == "Multi" %}
        <strong><em>{{ t.type }}</em></strong>
    {% else %}
        <h4>{{ t.type }}</h4>
    {% endif %}
    {% for e in t.effect %}
        {{ e }}
        <br>
    {% endfor %}
    </div>
{% endfor %}

</section>