---
layout: page
title: Gameplay
permalink: /core/core_loop/
parent: Core System
nav_order: 2
has_children: true
---

# Core Gameplay Loop

At the beginning of each Encounter, the BAMF will set the Timer to determine how many rounds the Encounter will encompass.

Once a Timer is set, the players and the BAMF make an [Initiative](/no1_system/core/initiative/) test to determine which team takes action first.

Play proceeds in rounds during which each player takes a turn.

On each turn, the player can take one [Shift](/no1_system/core/shifts/) and one [Action](/no1_system/core/actions/).

If the final result set of an Action contains a 1, the Initiative shifts to the opposing team and the [Entropy](/no1_system/core/core_mechanisms/#entropy) increases by 1.

If there are ***No 1s*** in the final result set, the active player chooses which player takes the next turn and the [Momentum](/no1_system/core/core_mechanisms/#momentum) increases by 1.

Play proceeds in this manner until the active Timer expires.

When the active Timer expires, the BAMF compares the current Momentum and Entropy to determine how the Scene advances.
* If the Momentum is greater than the Entropy, the heroes gain an advantage in the next Encounter. 
* If the Entropy is greater than the Momentum, the situation grows more dangerous for the heroes.



## Example