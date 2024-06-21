---
layout: page
title: "Traits"
permalink: /characters/traits/
id: characters-traits
parent: Characters
nav_order: 2
---

- Need to generate Arrays
- Gain 1 rating in a number of Skills equal to the associated Trait
- Max Skill rating 1 

# Traits

Traits describe the characters general qualities and characteristics, and categorize their Skills.

Traits determine the character’s starting Skills at character creation.  Players choose a number of Skills equal to their Trait and gain +1 Skill Rating in those skills.

Traits are also used to re-roll 1s during a Waypoint.  Each player rolls 1d6 to determine which Trait is focused at the beginning of a Waypoint.  For the duration of that Waypoint, the player may re-roll any dice result of 1 equal to their focused Trait.

## Dangerous

Represents a character's prowess in combat, physical power, and ability to handle weapons with deadly precision.

***Action Skills:*** *Exert, Grapple, Intimidate, Martial Arts, Strike, Shoot, Throw*

***Effect Skills:*** *Inferno, Tempest, Mori*

### Action Skills 
{% assign dang = site.data.skills | where: "trait", "Dangerous" %}
{% for s in dang %}
    {% if s.type == 1 %}
        {{ s.name }}
    {% endif %}
{% endfor %}


## Deft

Reflects physical and mental nimbleness, influencing a character's finesse in delicate tasks requiring precision.

***Action Skills:*** *Craft, Implements, Insight, Legerdemain, Operate, Pilot, Stealth, Tactics, Tumble*

***Effect Skills:*** *Squall, Nox*

## Savvy

Measures a character's knowledge, ingenuity, and social intelligence, affecting their ability to navigate intricate situations and interact with others effectively.

***Action Skills:*** *Computers, Current Events, Deceive, History, Linguistics, Navigate, Persuade, Research, Science, Streetwise, Survival*

***Effect Skills:*** *Rime, Mentis, Torrent*

## Steady

Represents a character's resilience, determination, and mental fortitude, influencing their ability to endure challenges, resist stress, and stay focused under pressure.

***Action Skills:*** *Composure, Endure, Focus, Investigate, Lead, Perceive*

***Effect Skills:*** *Lux, Tellus*

## Uncanny

Encompasses supernatural or extraordinary abilities, intuition, and a character's connection to the mysterious and unexplainable, granting them unique insights and powers.

***Action Skills:*** *--*

***Effect Skills:*** *Aether, Destroy, Intuit, Luck, Nihil, Resist, Vivus*

# Grit

Grit represents characters' capacity to take dramatic, and often heroic, action.  It is an abstraction of physical and mental health, of resolve and tenacity, of the determination that can only be mustered by individuals burdened with glorious purpose.  Grit is equal to the sum total of the character’s Traits.

# Defenses

Traits combine to construct characters’ Defenses.  

Defenses measure the number of Hits a character can take before they begin to lose their Grit.  All characters posses each of the 3 Defenses, but their Primary Defense is determined by their starting Profession.  The Primary Defense describes how the character generally avoids harm.

Some Abilities target specific Defenses.  Any Hits from these Abilities ignore the character’s Primary Defense (unless, of course, the Ability targets the Primary Defense).  Once a Defense is exhausted, all Hits are dealt directly to Grit until the character recovers their Defenses.

## Reflexes

Dangerous + Deft + Savvy

## Nerve

Savvy + Steady + Uncanny

## Vigor

Dangerous + Steady + Uncanny



# Starting Traits

Players choose from (or roll to determine if you're not a coward) the following arrays to apply to their characters' starting Trait scores. The scores can be applied to the Traits in any order the player wishes.

**1: 4 - 2 - 1 - 0 - 0**

**2: 3 - 3 - 1 - 0 - 0**

**3: 3 - 2 - 1 - 1 - 0**

**4: 3 - 1 - 1 - 1 - 1**

**5: 2 - 2 - 2 - 1 - 0**

**6: 2 - 2 - 1 - 1 - 1**