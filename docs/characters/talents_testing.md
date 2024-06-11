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

    ### {{ t.Name}}
    * {{ t.Type }} *

    ** {{ t.Effect }}

___

{% endfor %}