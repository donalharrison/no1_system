---
layout: page
name: Training Appendix
title: Training
permalink: /apendices/training/
id: training-appendix
parent: Apendices
has_children: false
nav_order: 4
---


# Training
Training is the cornerstone of characters' capabilities & advancement.  Players invest Milestones into Training ranks, gaining access to [Talents](/characters/talents/) which provide new abilities or increase their [Skill](/no1_system/characters/skills/) ratings.  Each Milestone spent increases characters' rank in the respective Training & allows them to select one of the Talents on that Training's list of equal or lower rank that the character does not yet have.
Characters must meet all prerequisites before spending a Milestone on Training ranks.

Trainings are categorized in three different types -- Basics, Specializations, & Disciplines.  These categories reflect the advanced experience required to study, master, & leverage the Training's talents.  As such, each type has different 

## Talents
Talents acrquired through Training make up the core of character advancement & customization.  There are three distinct types of Talents:
- Ability: The 
- Static:
- Trigger: Triggers take effect when certain conditions are met when a character attempts an Action.  If an Action meets a Trigger's condition, the effects happens immediately following the resolution of the Action (unless noted otherwise in the Trigger's description).

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
