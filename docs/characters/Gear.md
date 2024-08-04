---
layout: default
title: Gear
name: Gear
has_children: False
parent: Characters
permalink: /characters/gear
nav_order: 5
---

# Gear
Gear is every item, weapon, tool, wand, potion, etc., your character carries.

## Gear Ratings
Pieces of Gear have Gear Ratings that determine how much space they take in yoru Inventory.  Certain Types of Gear have Keywords that allow you to spend their Gear Ratings in certain ways.  If a piece of Gear has a Rating of 0, it is considered broken and any result set produce by using the Gear is reduced by -2 Hits.

## Reparing Gear
Gear can be repaired by professionals and artisans for a fee, or by certain Talents & Powers that restore Gear Rating or allow the use of the Craft skill to repair.

# Loadout
The Loadout determines to total amount of Gear Rating your character can have Equipped at one time.
Loadout is equal to the sum of your character's maximum Dangerous Trait + maximum Steady Trait + Endure Skill Rank + Exert Skill Rank + Implements Skill Rank + 3.

# Inventory
Your Inventory rating determines the total Gear Rating your character can carry at one time (including their Loadout).
Inventory is Equal to your character's maximum Grit + Endure Skill Rank + Exert Skill Rank + Implements Skill Rank + 8.

# Acquiring Gear

## Using Gear Points
If you have unspent Gear points, you may use them to acquire Gear at a rate of 1:1 to the Gear's Rating.  You have to spend a number of Gear points equal to the item's total gear Rating in order to acquire it, otherwise you must make a Wealth roll to acquire Gear.

## Using Wealth
Characters can attempt to purchase Gear using their Wealth score.  To do so, the player makes a Wealth roll using their Wealth score to determine the type of dice to roll and the Gear's Cost to determine the Challenge (i.e., the number of dice to roll).
- If the Hits in the result set of the Wealth roll equals or exceeds the Gear's Pruchase Threshold, the character acquire the Gear.
- If the Hits in the result set of the Wealth roll is less than the Gear's Pruchase Threshold, the character can reduce their Wealth score by -1 and acquire the Gear.
- The the result set of the Wealth roll contains a 1, the character's Wealth score is reduced by -1.


# Gear Keywords

## Skill Keywords
The Skill associated with the use of the Gear.

## Armor
You gain an Armor Defense equal to this Gear's Rating.  When you suffer Hits from an attack, you may have this Gear absorb some of the Hits by reducing its Current Rating.

## Weapon
You may reduce this Gear's Rating to reroll a 1 in the result set of an Action using this Gear's Skill.

## Two-Handed
The Gear requires the use of both hands.

## Layer
The Gear can be Equipped underneath other Gear with the Armor keyword.  You can only have one Layer Equipped at a time.

# Gear Table



<table>
    <thead>
        <tr>
            <td>Gear Name</td>
            <td>Gear Rating</td>
            <td>Skills</td>
            <td>Keywords</td>
            <td>Cost</td>
            <td>Purchase Threshold</td>
        </tr>
    </thead>
    {% for g in site.data.gear.gear %}
    <tr>
        <td>{{ g.name }}</td>
        <td>{{ g.rating }}</td>
        <td>{{ g.skill }}</td>
        <td>{{ g.keywords }}</td>
        <td>{{ g.cost }}</td>
        <td>{{ g.threshold }}</td>
    </tr>
    {% endfor %}
</table>
    
