---
layout: page
title: "Traits"
permalink: /characters/traits/
id: characters-traits
parent: Characters
nav_order: 1
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

<section>
<strong>Action Skills: </strong><em>
{% assign skls = site.data.skills | where: "trait", "Dangerous" | where: "type", "1" %}
{% for s in skls %}
    {{ s.name }},
{% endfor %}
</em>
</section>

<section>
<strong>Effect Skills: </strong><em>
{% assign skls = site.data.skills | where: "trait", "Dangerous" | where: "type", "2" %}
{% for s in skls %}
    {{ s.name }},
{% endfor %}
</em>
</section>

## Deft

Reflects physical and mental nimbleness, influencing a character's finesse in delicate tasks requiring precision.

<section>
<strong>Action Skills: </strong><em>
{% assign skls = site.data.skills | where: "trait", "Deft" | where: "type", "1" %}
{% for s in skls %}
    {{ s.name }},
{% endfor %}
</em>
</section>

<section>
<strong>Effect Skills: </strong><em>
{% assign skls = site.data.skills | where: "trait", "Deft" | where: "type", "2" %}
{% for s in skls %}
    {{ s.name }},
{% endfor %}
</em>
</section>

## Savvy

Measures a character's knowledge, ingenuity, and social intelligence, affecting their ability to navigate intricate situations and interact with others effectively.

<section>
<strong>Action Skills: </strong><em>
{% assign skls = site.data.skills | where: "trait", "Savvy" | where: "type", "1" %}
{% for s in skls %}
    {{ s.name }},
{% endfor %}
</em>
</section>

<section>
<strong>Action Skills: </strong><em>
{% assign skls = site.data.skills | where: "trait", "Savvy" | where: "type", "2" %}
{% for s in skls %}
    {{ s.name }},
{% endfor %}
</em>
</section>

## Steady

Represents a character's resilience, determination, and mental fortitude, influencing their ability to endure challenges, resist stress, and stay focused under pressure.

<section>
<strong>Action Skills: </strong><em>
{% assign skls = site.data.skills | where: "trait", "Steady" | where: "type", "1" %}
{% for s in skls %}
    {{ s.name }},
{% endfor %}
</em>
</section>

<section>
<strong>Action Skills: </strong><em>
{% assign skls = site.data.skills | where: "trait", "Steady" | where: "type", "2" %}
{% for s in skls %}
    {{ s.name }},
{% endfor %}
</em>
</section>

## Uncanny

Encompasses supernatural or extraordinary abilities, intuition, and a character's connection to the mysterious and unexplainable, granting them unique insights and powers.

<section>
<strong>Action Skills: </strong><em>
{% assign skls = site.data.skills | where: "trait", "Uncanny" | where: "type", "1" %}
{% for s in skls %}
    {{ s.name }},
{% endfor %}
</em>
</section>

<section>
<strong>Action Skills: </strong><em>
{% assign skls = site.data.skills | where: "trait", "Uncanny" | where: "type", "2" %}
{% for s in skls %}
    {{ s.name }},
{% endfor %}
</em>
</section>

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
