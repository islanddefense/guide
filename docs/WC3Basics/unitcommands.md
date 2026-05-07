### Unit Commands
Action/Command Hotkeys – There are 5 basic actions. All of them are useful, except patrol. Actions and spells can be shift queued to perform in an order. Understanding how unit commands and attack priorities will reduce frustration when units behave in ways you don't intend.

- <kbd>A</kbd> Attack 
    - Attacks targeted unit or if targeted on ground any enemy unit on its way to the targeted spot prioritizing targets as per attack priorities listed below.
- <kbd>P</kbd> Patrol
    - Patrols between the start position and target position, will attack targets on the way.
- <kbd>M</kbd> Move
    - Moves to the targeted spot, if targeted on a unit it will follow the unit until it's no longer possible i.e. unit enters fog of war or dies.
    - The move command has maphack, meaning if you order a move command across the map it will try to find the shortest path which is unblocked, if for example builders have blocked a path it will try to go around it, even if you had no knowledge this path was blocked.
- <kbd>S</kbd> Stop
    - Stops the current and any shift queued actions.
- <kbd>H</kbd> Hold Position.
    - Forces the unit to stand still but will attack any unit in melee range as per the priority listed below.


### Attack Priorities

A unit whose searching for a target to attack will prioritize in the following way:

1. Enemy hero that is attack
2. Enemy hero nearby but not attacking
3. Enemy units with attack command attacking
4. Enemy units with attack command not attacking
5. Enemy towers attacking
6. Enemy units without attack command
7. Enemy buildings not attacking

**Consequences for titan due to these priorities:**

- Attacking a lumber base with fruits and workers, attack clicking with the titan on ground will prioritize attacking fruits. This isn't preferred because workers can be detonated so we need to manually order the titan to attack workers individually before they are detonated.
- Sieging a base with titan it wants to prioritize attacking the towers which are out of range so we need to individually order attack commands for each wall.
- A minion or titan standing outside a base will try to attack the towers attacking it, this pathing will fail and it will go close to towers until it dies or you order it to go away. Instead we use hold position for our minions / titans outside bases.
- A builder coming down from a wotw cyclone and there are summons attacking you in range, the titan will prioritize attacking the summons instead of the builder so we need to manually issue an attack order on the builder.
- Sieging a base whose worker blocking you, blocking your entrance to the base. You can hold position and the titan will priotize attacking workers in melee range.

**Consequences for builders:**

- A titan sieging with minions goes invulnerable/invisible making the towers target the closest minion, basically spreading out your base damage over many units. We need to control group all our towers and issue attack commands to focus fire one unit.




