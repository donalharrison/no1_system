---
layout: page
name: Training
title: Training
permalink: /characters/training/
id: characters-training
parent: Characters
has_children: true
nav_order: 2
---


# Training
Training is the cornerstone of characters' capabilities & advancement.  Players invest Milestones into Training ranks, gaining access to new [Talents](/characters/talents/) & increasing their [Skill](/characters/skills/) ratings.  Characters must meet all prerequisites before spending a Milestone on Training ranks, after which they may select one of the Talents on that Training's list that the character does not yet have.  Many Trainings provide more than one talent when characters buy the first rank.  All ranks in that training thereafter allow the character to select from the remaining Talents from the Training's list.
Trainings are categorized in three different type -- Basics, Specializations, & Disciplines.  These categories reflect the advance experience required to study, master, & leverage the Training's talents.  As such, each type has different 

## Basics

<table style="text-align: center;">
    <tr>
        {% assign basics = site.data.training | where: site.data.training.Type, "Basic" %}
        {% for t in basics %}
            {% if t.Type == "Basic" %}

                <td style="width: 80; height: 80px">

                    <img src="{{ t.img_path }}" width="70" height="70">
                    <br>
                    {{ t.Name }}
                    </td>
                
                {% assign i = forloop.index | modulo: 4 %}
                {% if i == 0 %}
                    </tr>
                    <tr>
                {% endif %}
            {% endif %}
        {% endfor %}

    </tr>

</table>

## Specializations

<table style="text-align: center;">
    <tr>
        {% for t in site.data.training %}
            {% if t.Type == "Specialization" %}

                <td style="width: 80; height: 80px">
                
                    <img src="{{ t.img_path }}" width="70" height="70">
                    <br>
                    {{ t.Name }}
                    </td>
                
                {% assign i = forloop.index | modulo: 4 %}
                {% if i == 0 %}
                    </tr>
                    <tr>
                {% endif %}
            {% endif %}
        {% endfor %}

    </tr>

</table>

## Disciplines

<table style="text-align: center;">
    <tr>
        {% for t in site.data.training %}
            {% if t.Type == "Discipline" %}

                <td style="width: 80; height: 80px">
                
                    <img src="{{ t.img_path }}" width="70" height="70">
                    <br>
                    {{ t.Name }}
                    </td>
                
                {% assign i = forloop.index | modulo: 4 %}
                {% if i == 0 %}
                    </tr>
                    <tr>
                {% endif %}
            {% endif %}
        {% endfor %}

    </tr>

</table>

## Training List

<table>
    <tr>
        <th>Name</th>
        <th>Type</th>
        <th>Prerequisites</th>
        <th>Description</th>
    </tr>
{% for t in site.data.training %}
    <tr>
        <td>
        {{ t.Name }}
        </td>
        <td>
        {{ t.Type }}
        </td>
        <td>
        {{ t.Prerequisites }}
        </td>
        <td>
        {{ t.Description }}
        </td>
    </tr>
{% endfor %}

</table>