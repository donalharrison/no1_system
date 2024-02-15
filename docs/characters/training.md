---
layout: page
name: Training
title: Training
permalink: /characters/training/
id: characters-training
parent: Characters
has_children: true
nav_order: 3
---


# Training
Training is the cornerstone of characters' capabilities & advancement.  Players invest Milestones into Training ranks, gaining access to new [Talents](/characters/talents/) & increasing their [Skill](/no1_system/characters/skills/) ratings.  Characters must meet all prerequisites before spending a Milestone on Training ranks, after which they may select one of the Talents on that Training's list that the character does not yet have.  Many Trainings provide more than one talent when characters buy the first rank.  All ranks in that training thereafter allow the character to select from the remaining Talents from the Training's list.
Trainings are categorized in three different type -- Basics, Specializations, & Disciplines.  These categories reflect the advance experience required to study, master, & leverage the Training's talents.  As such, each type has different 

## Basics

<table style="text-align: center;">
    <tr>
        {% assign basics = site.data.training | where: "Type", "Basic" %}
        {% for t in basics %}

                <td style="width: 80; height: 80px">
                    <a href="{{ t.page_path }}">
                    <img src="{{ t.img_path }}" width="70" height="70">
                    <br>
                    {{ t.Name }}
                    </a>
                    </td>
                
                {% assign i = forloop.index | modulo: 4 %}
                {% if i == 0 %}
                    </tr>
                    <tr>
                {% endif %}
        {% endfor %}

    </tr>

</table>

## Specializations

<table style="text-align: center;">
    <tr>
        {% assign specs = site.data.training | where: "Type", "Specialization" %}
        {% for t in specs %}

                <td style="width: 80; height: 80px">
                    <a href="{{ t.page_path }}">
                    <img src="{{ t.img_path }}" width="70" height="70">
                    <br>
                    {{ t.Name }}
                    </a>
                    </td>
                
                {% assign i = forloop.index | modulo: 4 %}
                {% if i == 0 %}
                    </tr>
                    <tr>
                {% endif %}
        {% endfor %}

    </tr>

</table>

## Disciplines

<table style="text-align: center;">
    <tr>
        {% assign discs = site.data.training | where: "Type", "Discipline" %}
        {% for t in discs %}

                <td style="width: 80; height: 80px">
                    <a href="{{ t.page_path }}">
                    <img src="{{ t.img_path }}" width="70" height="70">
                    <br>
                    {{ t.Name }}
                    </a>
                    </td>
                
                {% assign i = forloop.index | modulo: 4 %}
                {% if i == 0 %}
                    </tr>
                    <tr>
                {% endif %}
        {% endfor %}

    </tr>

</table>
