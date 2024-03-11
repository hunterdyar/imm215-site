---
title: Interaction System
order: 8
---

Build a system in C# using object oriented patterns.

## Objective
Create a system that uses a parent/child class inheritance or C# interfaces, and a working example project that uses it.
You do not have to create, literally, an interactable-item system.
It can be something else with a similar structure and use case – run your idea past me if you are not sure.
First, I recommend building off of one of your character controllers, or use a character controller from the [sample code](https://github.com/hunterdyar/UnitySimpleCharacterControllers) as a starting example place.

- A parent/child class setup for something in your project. (Items)
- A system that allows other elements in your project to use these (Player picking up items, or an inventory, etc.) 
- This system utilizes the hierarchical class relationships to function. (i.e.: Children objects override a virtual parent function, or objects use functions defined on interfaces). In other words, at some point code is being called “on” the parent class or “on” the interface, even though the code that is executing is a child.
- Appropriate elements (like public functions) should exist to let other parts of your project hook into and out of the system. In an interaction system, this might be things like interacting with the item, picking it up, checking if a reference to an item exists in an inventory, or getting a list of all of the objects you have (the UI might draw icons for them all). 
- It makes sense. One has selected a reasonable use of an interaction system. 

*The prototypical (and titular) example is an interaction system. See below for details.*

## Submission
We have been talking about architecture and re-usable code. This project is about extendable code.

Where I can easily add new features – new objects that get picked up. The interaction system doesn’t need to be perfectly separated from the rest of the project, or purely compartmentalized and pluggable into any new project. 

Make a copy of your assets folder, and upload a .zip of it. **Include a readme.md file in the root directory.**
It should include your name and a description of the project, how the different parts work.
**Each script should include a few lines of comments clarifying what it does.**
Put your code into a namespace so I can use one Unity project to open and examine your submissions without conflicts.

## Purpose
Writing flexible code that has these kinds of useful parent/children classes is fundamental to creating immersive experiences.
In VR systems, we will often create a parent class for something exactly like “Interactable” that contains code that lets us pick up and put down an item and calls a virtual function or event if we press a button while holding it.

Buttons, Guns, coffee mugs, whatever, might all be “Interactables”. 
We are staying with the 2D project world to minimize the time spent working on the example project, and maximize the time spent structuring the system underneath it.
Yet these exact flexible structures are pivotal to creating and iterating in the immersive space. 

It will eventually be useful to start spending time with Unity’s UI system.
While not really part of this class, and not required as a graded element of the project; one will to need familiarizee themselves with it eventually.
This project is a good opportunity to also integrete HUD/UI elements without those elements being 'core' (read: graded).

## Rubric
Rubric Breakdown
- 40% Inheritance – You have a system with parent classes (with virtual functions) and child classes (that override those functions), and you call functions on the base class and have unique functionality happen because of child classes overriding those functions.
- 25% System other. The code. *How well it works and how efficient it is. Makes sense. Code meets requirements, in namespace, is commented and use the inheritance system, etc.*
- 25% Example project. *Should function and use the system.*
- 10% Submission other. *Readme files, any used sources credited, etc.*
