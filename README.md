# General Information
_**This chunk of information is taken straight from the assignment document, further information about each category can be found further below**_

## Deliverables
A single GDD placed as the readme for the repository for this project on GitHub. K-kruusi
invited to the repo as a contributor. Your name included in the readme, and a brief
description of your contribution submitted on blackboard.
Introduction
High up in the snowy mountains of Alterac Valley, there exists an eternal conflict between
the Dwarves of the Alliance and the Frost Wolf Orc Tribe of the Horde. Players must choose
a faction and a character representing one of the four arch-types: Tank, Healer, Mage, and
Assassin; and assist their faction leader in capturing dominion of all Alterac Valley.
## Background
Modeled after Alterac Valley from World of Warcraft, your game will have a much smaller
scope. No persistent characters, no inventory or gear. Just Orcs Vs Dwarves locked in epic
battle for now.
## Game Mechanics
1. Team - When joining players must choose a faction; Horde or Alliance
1. Unit - After picking a faction players must choose a role.
1. Graveyard - If your character dies, your ghost is transported back to the nearest
graveyard; and put into a queue of at most 30 seconds, before respawning at the
graveyard location. Graveyards are capturable, after holding the node for 5 minutes.
1. Each team starts off with 3 graveyards, an additional graveyard located in the center of
the map starts off unowned.
1. Towers - Near the fortress and each graveyard that the teams start off with is a tower;
towers have archers that will attack any opposing side forces that fight near them. They
have limited range and can be burnt down by the opposing team. The archers on the
tower can be killed but will respawn if the tower stands. Towers do not respawn.
1. Captains - Periodically captains of the faction will buff players belonging to that faction
with their own faction buff. Captains can be attacked by opposing side, after dying they
do not respawn.
1. Generals - Defeating the general of the opposing faction wins the game.The Generals
are guarded by 1 Advisor for each active tower that faction has. It’s almost impossible to
kill the general with multiple advisors up.
1. Spawn Location - Players start the match at an uncapturable graveyard just outside of
their main base. If their team controls no graveyards players will spawn at the entrance.
## Genre
40 vs 40 Cooperative competitive multiplayer game.
## Characters
1. Knight - High Passive Survivability, Low Damage, Disruption
1. Mage - High Damage, Cooldown-Based Survivability, Range
1. Assassin - High Damage, High Mobility, Disruption
1. Priest - Ability to Heal Self/Others, Range
## Abilities
Each class should at the minimum have 4 skills that fit their kit described above.
## Controls
1. Standard World of Warcraft like controls.
1. WASD movement.
1. Mouse based UI and scene target selection
1. Keys 1 through 0 for abilities
1. Menu for game settings
1. Menu for starting / joining a game
1. Escape for seeing the score + metagame information like HKs, killing blows etc.
## UI
1. Health of self
1. Resource (aka mana) of self
1. Ability buttons with mouse over descriptions
1. Current Target
1. Targets Health and resources
1. Buffs on allies and self
1. Group Members



# Gameplay

# Tools

# Graphics

## **Graphics Technologies**

The graphics technologies options available are:
1. OpenGL Custom Graphics Engine - Gives more flexibility of work and options in terms of what tools and features are needed for the game, however can take more time to build from scratch.
1. Unreal Engine 4 - Already holds a powerful engine with advanced graphics pipelines and tools. It has a powerful Lighting and Rendering system, which is a perfect option for a 3D game like ours. Some of the features included in the engine are: Sub-Surface Shading, PSO Caching (Pipeline State Object), Dynamic Resolution and Post Process Effects. A lot of those can be seen in games like Fortnite, Blade&Soul, Aion, Paragon, Gears of War4, Ark: Survival Evolved and A Way Out. 

## **Animations**
1. Models (Skeleton and Animations ready).
1. OBJ files with spread out keyFrames of the animations. (This will allow much smoother playback with less memory usage)
1. OBJ File Loader for OpenGL (To get vertex, texture, normal and face data).
1. UE4 can use the Skeletal Mesh Animation System which already holds several Animation Tools and Editors.

## **Design Patterns**
1. Flyweight Pattern (Model Handling and Loading)
1. State Pattern (Each character state: Combat, out of combat, Idle, Walking, Running, Jumping, etc..)

## **Performance**
Performance can see a hit depending on the amount of players (models) moving and being loaded on the same place. Using spells and other visual elements (particles) can further increase the requirements of the graphics.

## **System Requirements**
Minimum Requirements
1. OS: *Windows 7, 8, 10*
1. Processor: *Intel Core i5 2.8GHz or similar*
1. Memory: *4GB*
1. Graphics Card: *GTX 550 or similar*
1. Storage: *5GB*

Recommended Requirements
1. OS: *Windows 7, 8, 10*
1. Processor: *Intel Core i7 3.0GHz or similar*
1. Memory: *8GB*
1. Graphics Card: *GTX 750 or similar*
1. Storage: *5GB*

# **Networking**

## **TCP Server**
test
Used for when the player logs in or logs out of the game (need safe and reliable connection to server) and when they choose what game they will play in and also what their character / class will be before the game begins.

1. Player information (username, password, email).
1. Player statistics (wins, loses).
1. Character faction and class.
1. Core UI information 
1. Character deaths / kills for scoreboard

1. *Stretch goals: Sending messages to other players in the game. Needs to be TCP as the information must be accurate.*
1. *Stretch goals: Character creator information*

## **UDP Server**

For the gameplay (less error checking but it is much faster which is required for a game running online with 40-80 people ideally at 60 frames per second). 
Information to be sent in data packets:

1. Transform information (location and rotation).
1. Player actions (attacks, heals, captures of areas like graveyards).
1. Buffs and debuffs (let the player know if they get a buff and how long it will last. Client will handle how the buff changes their actions).
1. Character health (to be displayed on other players UI and to check for validity).

1. *Stretch Goals: TDB*

## **TCP or UDP**
1. Broadcasting tower / graveyard captures and captain / general deaths
1. NOTE: Logistics of sending information via TCP and UDP at the same time. Is it possible to connect players to 2 ports at the same time?

## **Database Information**
This section will list what we will need to store in the database
MySQL is the most likely candidate - We previously used it.

1. Player account information: username, email, password, etc.
1. Player gameplay statistics: wins / loses.
1. Character class statistics: health, actions, abilities.
1. Game version: What patch is the game running on, does the game need to be updated

1. *Stretch goals: Able to pull character creator information*




# Markup Text Testing

Here you can find references on how to use the markup language

It's very easy to make some words **bold** and other words *italic* with Markdown. 

You can even [link to Google!](http://google.com)

# This is an h1
## This is an h2 tag
###### This is an h6 tag

*This text will be italic*
_This will also be italic_

**This text will be bold**
__This will also be bold__

_You **can** combine them_

1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
   1. Item 3b
   
   
I think you should use an
`<addr>` element here instead.


```javascript
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```

First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column
