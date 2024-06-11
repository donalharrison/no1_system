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

    <h3>{{ t.name }}</h3>
    {% if t.type == "Multi" %}
        <p><strong>{{ t.type }}</strong></p>
    {% else %}
        <h4>{{ t.type }}</h4>
    {% endif %}
    {% for e in t.effect %}
        {{ e }}
        <br>
    {% endfor %}

{% endfor %}

</section>