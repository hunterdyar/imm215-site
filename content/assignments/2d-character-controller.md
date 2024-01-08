---
title: 2D Character Controller
---

## Objective
Create a Script - a Unity component - that can be used to move a player game object around a 2D environment. Create a test scene for this to happen in. The player object should be able to respond to player input and move around the scene. It should handle preventing movement into invalid locations.
Above/beyond/you don’t have to worry about:
1.	Fine-tuning a decent example scene
2.	Making character images
3.	Handling interactions with non-solid things like collectable items
4.	Detecting when the player hits something that kills them

## Submission
This submission will be graded pass/fail. Maybe it’s all broken, that’s fine. The next assignment is an expansion of this one, and that will be formally graded. If it’s all broken, you have more work to fix it before that graded submission.  

Upload all relevant .cs files to Brightspace. The real “grading” will be during class as we go around and look at all of the projects. Late submissions or absent students will be graded during a 1-1 make up meeting the student needs to schedule.

It is imperative that this assignment is completed on time. Next week’s assignment builds on top of this one.

## Purpose
This will require writing functions, using variables, and testing in a scene. It will help us get back up-to-speed on our fundamentals: Variables, Syntax, Functions, and code flow. Practice!

Neither 2D games nor character-movement scripts are particularly applicable to immersive experiences. 

They do introduce the concept of isolating user input from systems.

We are using this as an entry point. We will be working outside of immersive media for convenience, fast iteration, ease of documentation, all while learning programming concepts that are still extremely applicable and important in programming immersive experiences.

A small 2D game provides a simple way to start digging into programming concepts that do apply to immersive experiences, with minimal “unnecessary overhead” – we don’t need to learn too much about sprite renderers (they display an image) and physics (add a “2D” suffix). For example, a 2D game will require data managers and systems, input handling, working with collisions, keeping track of a global state, and other structural similarities to immersive experiences. 

## Assignment Details
This project will consist of one or two scripts – components -- that move a player through a scene. You have control what style of game the project is. Top down shooter? Side scrolling game? Platformer? Grid-based puzzler? Snake clone? Etc. Don’t try to pick something “easy”. Among other reasons, it’s likely we don’t have a clear ideas of what “easy” means yet! Instead, choose something that interests you from a design perspective. What game would you want to make and/or play?

## Scope
Some character controllers are simpler than others. I want you challenging yourself to try and do things well, to come up with a plan and execute on it. I think simpler projects, like “roll-a-ball” but 2D, would be basically unacceptable without further complexity added. I won’t quantize any “word count”, but the controllers should have a few functions and variables, and player input should be separated.

## Degrees of Movement
Acceleration -> Velocity -> Position
If you remember from physics, the derivative of position is velocity and the derivative of velocity is acceleration (Remember derivatives? Doesn’t matter)*. We can edit an object’s position directly, like chess. We could edit an objects velocity directly, like top down/side scrolling shooters (Galaga); or we can edit an objects acceleration directly, like a racing game or asteroids.
Each strategy has its strengths and weaknesses. I wouldn’t want to play checkers by driving a racecar to a location.
Platformers are usually a mix of velocity and acceleration. Basically, velocity, (especially for jumps) but with a little bit of friction with the ground, quickly getting up to speed and sliding to a stop.

#### Bonus Trivia for Fun and Profit
*The names of the derivatives of position, in order: position, velocity, acceleration, jerk/jolt, jounce/snap, crackle, pop, lock, drop, shot, put. Fun! Going the other way (integrals), it’s position, absement, absity, abseleration, abserk, absounce. Neat! While we’re at it, Momentum (mass times acceleration) has the following derivatives: Momentum, Force, Yank, Tug, Snatch, Shake.*

## Types of 2D Movement
•	Asteroids (Accelerate and Rotate)
•	Pac-Man/Snake (Always move forward, turn to cardinal directions)
•	Platformer (Mario!)
•	Grid-Based with snapping (like Sokabon, https://www.sokobanonline.com/)
•	Grid-Based, slides through grid positions (Pokemon)
•	Beat Em Up (ie: https://www.youtube.com/watch?v=MDrc5Jzm2wc, https://www.youtube.com/watch?v=g7xeGpoCScs)
•	2D Fighting (ie: Street Fighter II, Mortal Combat)
•	Twin Stick Shooter (Move, Aim) https://www.youtube.com/watch?v=YSpo2VvN0SM 
•	Twin Stick Shooter with aiming constraints (https://www.youtube.com/watch?v=Zu9QyThTpXo)
•	Side-scrolling Infinite Runner (http://canabalt.com/)
•	Side-Scrolling racing with jumps, gravity (ExciteBike, https://www.youtube.com/watch?v=fRgMCtaWoSU)

Some games (Pokémon) have movement as a byproduct, while others (Mario, Galaga) have movement as fundamental to gameplay. Other games, like infinite-runners or Snake, take a movement mechanic and add an interesting gimmick to the mechanic in order to create the core conceit of the game.

Other games have basic movement, like Street Fighter, My Friend Pedro, or Katana Zero, but add complexity and situations that make the “simple” mechanics far more interesting as they interact with enemies and the environment.

We are not designing a game, don’t feel pressured to make an extremely interesting mechanic with a good “hook” (gimmick). Just pick something that’s interesting to you and do it. 

## Getting Started
Complete examples for this (that also will help for next week’s assignment) are available as a Unity project you can download and investigate: https://github.com/hunterdyar/UnitySimpleCharacterControllers
Click the green “Code” button and then “Download Zip”. Unzip it, then add the folder in Unity Hub as a unity project. Change the version of Unity to one you have installed and open it\
Obviously you can’t just copy that code, but it should certainly help you figure out some functions/tools are available to you.  
To move a player, you will modify it’s transform.position property. You can do this directly, or with support functions like transform.Rotate and transform.Translate. More information on transform at the scripting api: https://docs.unity3d.com/ScriptReference/Transform.html
Alternatively, you can use a Rigidbody2D component, and edit it’s velocity property. You can do that directly for a velocity based system, or use the AddForce and AddTorque for an acceleration based system.
Instead of thinking about “position, velocity, or acceleration” just think of a kind of game – asteroids, side scrolling shooter, sokabon/grid puzzler, infinite runner, platformer, etc etc – and try and make a controller for that kind of movement.
I do not recommend platformer. A simple one is easy enough, but they get quite time consuming to fine-tune. Coyote time, and mild input-buffering. Trust me, I’ve spent weeks on one once.

## 2D Physics
Unity has two physics systems built into it, “Physics” and “Physics2D”. They are completely independent of each other. So we have a Rigidbody2D and Collider2D instead of Rigidbody and Collider’s, and OnCollisionEnter2D instead of OnCollisionEnter. The Physics2D system won’t use the regular systems components (like colliders) and won’t call the regular event functions. 
So just remember the 2D suffix. Most functions are similar between 2D and regular physics, with only minor differences in syntax.

## Handling Input
Generally, we want to handle input with the Input class. I am writing this assignment in 2019. Will we be using the new or old Input system? Probably the old one? 

## Sprites
When you drag a jpg or something into Unity, it may not work off-the-bat. Click on the image in the Project window, which should open it’s import settings in the Inspector. Is the type set to “Sprite”? 
When you select a “2D” template instead of “3D”, this sprite (vs. texture) default type for imported images is one of the differences between the templates.
