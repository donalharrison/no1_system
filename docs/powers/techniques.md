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

{% assign eskills = site.data.skills.name | where: "type", "2" | uniq %}
<p>{{eskills}}</p>

{% assign techs = site.data.powers.techniques %}

<p>{{techs}}</p>

{% for tag in techs.keywords | uniq %}
    <p>{{tag}}</p>
{% endfor %}