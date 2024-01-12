---
title: 2D Character Controller Part Two
order: 3
---

## Objective
[Refactor](https://en.wikipedia.org/wiki/Code_refactoring) your character controller to an independent and publishable form with clean architecture. The script should “just worry about itself”. It just handles the movement, and it should be useful in more situations than moving the player’s character (like an ai logic script using it to move an enemy). It doesn’t handle input and provides a useful interface (through public functions) for other scripts to work with it. We could remove it and while that gameObject would stop working, nothing else in the project would break. 
You must meet the following requirements:
1.	Comment the code. Concisely yet clearly explain what each function does and how it’s used.
2.	Put the character controller into a unique namespace. 
3.	Separate user input from the system to a separate script. You will need to create this player input script.
4.	Every input into the system should be through a public function.
5.	The controller should handle (“sanitize”) inappropriate input without glitching, bugging out, or breaking (or it does break, but gives you a useful error message as to whats happening).
6.	Use only one-way dependencies (for this script: the input system depends on the character controller, but the character controller doesn’t care where input is from). We are avoiding “interdependencies”. The character controller doesn’t know or care about the input script at all.
7.	Comments that include your name and how the script(s) should be set up. (So I could set up a scene from your uploaded .cs files).
Above/Beyond/Out of scope:
1.	Handling output events/broadcasts/actions to inform other systems of things like special collisions or animation state changes. Basically, our output is just going to be movement.
2.	Handling player states like “isDead” or “canMove” if they weren’t needed for the core system to work.
3.	Use Attributes to add labels and organize how the component looks in the Inspector
4.	Include tests (with Debug.LogWarning or Debug.LogError) to inform the developer if the component is set up incorrectly, and force their hand with attributes like “RequireComponent”.
The only dependency this code should have is that the input system relies on the character controller. Which, yeah. Of course! Be sure to use a unique namespace. With that, I should be able to import every students code into one unity project and have 0 conflicts, even if they are all called “TheBestCharacterController”.

## Submission
Submit all required script files to Brightspace. (ie: the controller and input script, other scripts If they exist).

## Qualitative Judgement
The grade is quantitative, the various requirements will be met. During feedback, I may prove additional information as I consider the following questions. In other words, being able to complete these well is the spirit of the assignment, hitting all the requirements in the first section of the document is the grade of the assignment.
- How easy would it be to set up this script?
- How well named are all of the public functions and variables? Are they clear?
- How well does it work with other scripts?
- Is anything public that doesn’t need to be?
- Could I stick this in a different project and use it? How specific are the projects setup requirements? Does it unnecessarily rely on unity features like object names, tags, layers, rigidbodies, or the physics2D system?
- Could I use this character controllers to control non-player characters, replacing the input with an AI script to simulate input?
Despite the opportunity for going above/beyond with this assignment, there is no extra credit. 

## Purpose
We are focusing on writing code that is flexible, clean, and usable. With our movement problems solved last week, this is entirely focused just on the structure of the code. We are practicing avoiding bad habits like interdependencies. We hope to write code that is re-usable in future projects.

I should be able to write an AI script to control, for example, enemies, using the CharacterController to move them around. In the future, most or all our code should be written with these principles in mind, and how well one designs the architecture of a systems will be a graded element of future projects, even more so than the performance or efficiency of the scripts.

This is not often an element of programming that is brought to attention in many resources, particularly online guides or follow-along systems, where the architecture decisions have just sort of been made already. 

Smart system design is one of the most important elements in programming for game engines, and especially for immersive media where the user has such a high degree of agency. Learning how to write flexible code is learning how to make programming easier for ourselves. We will have fewer bugs, fewer headaches, less time spent refactoring, and if you choose to misinterpret these principles as life lessons, you may even become a better person.

## Getting Started
Your best resource is the example projects. Don't follow guides, but try to reverse-engineer what is happening in the sample projects, and apply similar concepts to your own code.

- GitHub Repo with example projects and code [https://github.com/hunterdyar/UnitySimpleCharacterControllers](https://github.com/hunterdyar/UnitySimpleCharacterControllers)
- Information on Namespaces in Unity: [https://docs.unity3d.com/Manual/Namespaces.html](https://docs.unity3d.com/Manual/Namespaces.html)
- Unofficial resource on Unity attributes: [https://unity3d.college/2017/05/22/unity-attributes/](https://unity3d.college/2017/05/22/unity-attributes/)
- Serialization and Attributes Video: [https://guidebook.hdyar.com/docs/programming/unity-and-programming/tips-and-tricks/serialization-and-attributes/](https://guidebook.hdyar.com/docs/programming/unity-and-programming/tips-and-tricks/serialization-and-attributes/)

*Good programming makes it easy to be lazy in the future.*