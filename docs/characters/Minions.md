---
layout: default
title: Minions
name: Minions
has_children: False
parent: Characters
permalink: /characters/minions/
nav_order: 5
---

# Minions
Minions are recruitable allied NPCs that take orders from the characters.  Different Training paths grant access to different type of minions.  The Overseer recruits Minions with the Henchmen keyword, the Necromancer recruits Minions with the Haunt keyword, and the Best Master recruits Minions with the Beast keyword.  Minions are not fully capable heroes, rather they are conscripts, assistants, aides, and soldiers of fortune.

### Using Minions
Minons all have a a Grit Trait, Melee and Ranged ratings, and most have 1 or more Triggers that work the same way as a character's Trigger Talents.  On each of their commander's turns, the Minion can use a Shift to Move.  The Minions' commander must use one of the Talents to lead them in order to apply the Minons' Melee or Ranged ratings to a result set, or to activate their Triggers.

## Retainers
Minions with the Retainer keyword are named NPCs that are more capable than other Minions, but not as capable as Characters (i.e., they're sidekicks and protégés).  Retainers are recruited by spending Renown.  When you  recruit a Retainer, you specify the Retainer Trait you are recruiting and the BAMF creates the Minion for you, introducing them at the next opportunity presented in the game fiction.

### Using Retainers
Retainers have the same ratings as all Minions.  In addition to Triggers, some Retainers may have Abilities that they can use.  Retainers each have a distinct list of Skills with which they have some expertise.  The Retainer's Minion Rating determines what type of dice they roll when using these skills.  Retainers can also be equipped with Gear with a total Gear Rating up to thier Grit Triat + their Minion Rating.  On each of the Commander's Turn, Retainers can use 1 of any of the Basic Shifts and can take one Action.

### Training Retainers
You can increase the Minion Rating to a maximum of 4 of any Retainer by spending additional Renown once they are recruited.  When you do, choose one (1):
- Increase the Retainer's Grit by +2
- Increase the Retainer's Melee and Ranged rating by +1
- Add a new Skill to the Retainer's Skills list

# Minons Table

<table>
    <thead>
        <tr style="font-weight: bold;">
            <td>Minion Name</td>
            <td>Keywords</td>
            <td>Rating</td>
            <td>Grit</td>
            <td>Melee</td>
            <td>Ranged</td>
            <td>Triggers</td>
        </tr>
    </thead>
    {% for m in site.data.minions.minons %}
    <tr>
        <td>{{ m.name }}</td>
        <td>{{ m.keywords }}</td>
        <td>{{ m.rating }}</td>
        <td>{{ m.grit }}</td>
        <td>{{ m.melee }}</td>
        <td>{{ m.ranged }}</td>
    </tr>
    {% endfor %}
</table>
    