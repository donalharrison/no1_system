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
<strong>Effect Skills: </strong><em>
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
<strong>Effect Skills: </strong><em>
{% assign skls = site.data.skills | where: "trait", "Steady" | where: "type", "2" %}
{% for s in skls %}
    {{ s.name }},
{% endfor %}
</em>
</section>

## Uncanny

Encompasses supernatural or extraordinary abilities, intuition, and a character's connection to the mysterious and unexplainable, granting them unique insights and powers.

<section>
<strong>Effect Skills: </strong><em>
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

Defenses measure the number of Hits a character can take before they begin to lose their Grit.  All characters posses each of the 3 Defenses, with their Primary Defense selected during character creation Profession.  The Primary Defense describes how the character generally avoids harm.

Some Abilities target specific Defenses.  Any Hits from these Abilities ignore the character’s Primary Defense (unless, of course, the Ability targets the Primary Defense).  Once any Defense is exhausted (i.e., equals 0), all Hits are dealt directly to Grit until the character uses the Recover Action to recover their Defenses.

## Reflexes

Dangerous + Deft + Savvy

## Nerve

Savvy + Steady + Uncanny

## Vigor

Dangerous + Steady + Uncanny

# Qualities

## Enemies
Enemies are those NPCs that you've crossed in some way during your adventures.  Generally, Enemies represent foes who want to see your deeds undone or made difficult.  Higher Enemies scores can be across multiple enemy factions, reflecting that you've crossed paths with many foes, or they can be consolidated into a single entity or group (e.g., the +4 Enemies score gained from the Nemesis Experience option).

## Favors
Favors reflect some small debt owed to your cahracter by a known NPC.  Favor points can be spent to gain some small advantage in the game fiction.  Examples include (but are not limited to) having a Noble pull strings to get you invited to a ball, having a sailor grant you passage on their vessel, or having a guard captain allow you to enter a restricted area.

## Gear
Gear points are spent to acquire Gear without using Wealth.  Gear points are exchanged 1:1 for Gear Rating of equipment (e.g., a Longsword can be acquired by using 2 Gear points)

## Renown
Renown is used to recruit minions with the Retainer keyword.  Retainers are named minions that are more capable than other minions, but not as capable as Characters (i.e., they're sidekicks and protégés).  Renown points can also be spent train Retainers, increasing their ratings, Grit, etc.

## Secrets
Secrets are small truths about the game fiction that your character has somehow acquired.  For each Secret point you have, the BAMF will provide you one truth about a fictional situation.  These truths are short statements about a situation that is not otherwise common knowledge.  Secrets do not give you comprehensive outlay of information, instead giving you a piece of information that helps you to assemble the larger puzzle.

Not all Secrets will be provided at the onset of the game allowing you to keep some truths reserved to recall at a later point.  The first and every other Secret point you acquire are revelead at the game's beginning.  Every second secret point you have is reserved to be revelaed later.  For any Secrets you have reserved, you may ask the BAMF if you know anything about a situation, allowing the BAMF to reveal a truth at that point if there is an appropriate context in the game fiction.  Alternatively, the BAMF can reveal a reserved Secret to you at an appropriate point in the fiction without your prompt.

## Wealth
Wealth is used to pruchasing Gear, clearing debts, or payign bribes.  Your Wealth score acts like a Skill Rank, determining the type of dice rolled in a Wealth roll.  The Cost of the desired purchase determines the Challenge of the Wealth roll, and the success of the roll is determined by the purchase's Thershold.  More details on using Wealth can be found in the Gear section.