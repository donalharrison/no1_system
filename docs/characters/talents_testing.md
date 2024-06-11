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

{% for t in site.data.talents_tmp.talents %}

    <h3>{{ t.Name}}</h3>
    <h4>{{ t.Type }}</h4>

    {{ t.Effect }}

{% endfor %}