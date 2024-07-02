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



# Technique List

{% assign techs = site.data.powers.techniques %}

{% for tag in techs.keywords | uniq %}
    <p>{{tag}}</p>
{% endfor %}