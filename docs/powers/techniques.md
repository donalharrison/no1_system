---
layout: default
title: Techniques
grand_parent: Characters
parent: Powers
permalink: /characters/powers/techniques/
---

# Techniques


## Current


## Using Techniques



# Technique Lists

{% assign techs = site.data.powers.techniques %}

<p>{{techs}}</p>

{% for tag in techs.keywords | uniq %}
    <p>{{tag}}</p>
{% endfor %}