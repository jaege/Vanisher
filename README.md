# Vanisher
by Team Omega

* Yaohong Wu
* Jin Lin
* Luyao Huang
* Quan Yuan
* Yu Qu

## Introduction
Vanisher is a stealth game. The player controls a thief. To win, the thief must go to the destination without being caught by the guards. The thief can simply hide behind obstacles and crouch towards the destination. The thief can collect some special abilities to help him escape. Possible abilities include throwing a stone to distract a guard, exploding a smoke bomb to obscure a guard's vision and running faster. The thief may also need to solve simple puzzles to find a way towards the destination.

## Installation Requirements
Unity 2017.3.0 (or higher) is required.

## Gameplay Instruction
### Movements
Press 'w/s/a/d' to move the thief.

Move the mouse to change orientation of camera.

Hold left 'shift' to walk slowly (reduced footstep sound).

Press 'c' to crouch (no footstep sound).

### Abilities
To throw a stone (if the thief has this ability), press '1' to preview the trajectory and click the mouse to throw.

To explode a smoke bomb (if the thief has this ability), press '2'.

To run faster (if the thief has this ability), press '3'.

### Interaction with Environment
Press 'f' to interact with a controller/energy block.

### States of a Guard
A guard has 4 states, indicated by the color of the sphere above him.

White: the guard is patrolling along some trajectory.

Green: the guard is suspecting, i.e. looking at a direction for a while.

Purple: the guard goes to a place and search, i.e. look around, this place.

Red: the guard finds the thief and chases him.


## How to Observe Technology Requirements
### Character Animation
The thief is animated using a fairly complex animation bleed tree. Transitions between different animations are smooth. Please play with character movement using w/s/a/d/c/left shift.

### AI
A powerful AI system (finite state machine) is installed in every guard in our game. The spherical indicator above each guard indicates the currect state (patrol/suspect/chase/search) that the guard is in. Different colors of this indicator correspond to different states. The default state is 'patrol'. If the thief shows up in front of a guard, the guard will transition into 'suspect' state. If a guard hears the footstep of the thief, the guard will transition into 'search' state. If a guard finds the thief, he will chase the thief.

### Physics Simulation and Interaction
The stone throwing skill of the thief is an example of using physics simulation. The smoke bomb and visual effect of accelerating are implemented using particle systems. Some collision-based examples include collectable energy blocks, touchable controllers, etc. A few more examples include openable doors, electricity on the ground, etc.

### UI
Game start and pause menus are implemented. Game-over and you-win canvases are shown on appropriate losing/winning conditions.

The cooldown effect and number of each ability is shown on the lefthand side of the screen. The health of the thief is represented using two heart sprites on the top-left corner of the screen.

A small map (the projection of the scene on the x-z plane) is shown on the top-right corner to help the thief.

Some text of hint may be shown if the thief is on a certain place, e.g. the start room.


## Deficiencies or Known Bugs
The thief's jump animation may start when the thief is running over an uneven part of the ground, e.g. the sill of a doorway. This behavior may look awkward sometimes, especially when the thief is running pretty fast.


## External Resources Used
Our main camera and basic animator are based on 'Cameras' and 'Characters' in Standard Assets. 

The basic models/animations of the thief and police are downloaded from https://www.mixamo.com. 

"Sci-Fi Styled Modular Pack", "WarZone", "Scifi Asset Pack" are download from Unity Asset Store.

Background music and sound effects are all from https://freesound.org.


## Who did What
Yaohong Wu:
focus on game management, event management and audio management; help fix bugs on/improve different modules (e.g. player abilities, UI); aggregate each member's work; organize team meeting, etc.

Jin Lin:
focus on animation and modelling module; camera and mini map setting; demo videos editting; help fix bugs and integrate files; participate in group meeting, etc.

Luyao Huang:
focus on player module (e.g. player abilities) and level design (e.g. puzzles, interaction with controllers, chests, etc.); participate in group meeting, etc.

Quan Yuan:
focus on enemy AI module (e.g. FSM); help fix bugs on camera, animation, game logic, etc.; help polish game (e.g. wave effect for stone collision); participate in group meeting, etc.

Yu Qu:
focus on UI module (UI sprites and menus design, menu functionalities, cooldown effects, etc.); participate in group meeting, etc.
