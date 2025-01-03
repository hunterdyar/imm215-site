---
title: Novel Locomotion Implementation
order: 9
---
Implement a novel way to locomote in VR, for the Oculus Quest. Use Headset and standard controller inputs, no hand-tracking.

## Background
Locomotion is a difficult problem in VR. The simplest version of locomotion is to not: nothing other than the positional tracking of the devices. This is a great solution.
In this case, one moves around the real and virtual world 1-1.
This works so long as the virtual world is the same size or smaller than the users real-life play-space.
Unfortunately, our world is not usually smaller than our play space, so we need to devise some way to move in the virtual world without having to move the same amount in the real world.

The most common methods are full room-transitions, teleportation (with various forms of input and activation), and ‘sliding’ or joystick-movement.
All of them have their pros and cons, with some of the properties we care about being intuitiveness, ease of explanation, motion sickness, encouraging natural player movement, time to execute, accessibility, and ease of destination selection.

Redirected walking is another interesting approach, where we move the world invisibly, taking advantage of shortcomings in how humans perceive space.
We can walk in circles while, in the virtual world, we seem to be moving in a straight line. Programmatic systems can be automated to ‘redirect’ us to turn us in real-life, without us really noticing, and keep us in the playspace.
We can change how we move or rotate our view of the world by a small factor without it really bothering us. We can also make small adjustments to the world while our eyes flicker around (saccades), or simply rearrange the world behind our back.
All of these invisible tricks together account for ‘redirected walking’.

- More on [Redirected Walking](https://www.gdcvault.com/play/1024755/The-Science-and-Engineering-of)
- A survey of [VR Locomotion](https://locomotionvault.github.io/) methods 

For this assignment, the goal is not to create a “good” locomotion system. The goal is to create a ‘novel’ one – unique and interesting.\
Free yourself from whichever subjective constraints or qualifications and create what you wish to create.
Projects like my own ‘head thrasher movement’ (aggressively toss your head in the direction you want to move),
Michal Douglass’s “Getting Over it VR” (your are in a pot, and have a pickaxe, and will likely vomit),
or Ben Scott’s “Perfect and Excellent Elevator Transitions” (you push a button and elevator doors very slowly close in front of you, elevator muzak plays for an uncomfortably long time, and then they slowly open at your new location),
are all terrible in some ways, yet wonderful in others.

It’s a programming assignment, not a design assignment, so have fun with it, and don’t stress about your idea too much.

## Purpose
The purpose of this assignment is to implement a mechanic.
We have done that before – interaction systems, movement, and so on.
We will need to learn how movement works in VR, and how we can manipulate it. Yet, there are two additional challenges.

The first is that we must invent the mechanic ourselves, from an open-ended prompt.
We need to come up with something that is both interesting to us and “novel”, and one that we do not know how to implement, and then we need to figure that part out.
We also must not let our perceived technical production ability get in the way of having ideas.
We understand that what we end up creating might just be a hacky prototype of the “real” idea, and that our ability to judge what is and isn’t “easy” or “possible” is not very well trained.
It’s probably best to just come up with a few ideas and pitch them to Hunter, who can give us more informed insight on if they are within our ability to create, and how to get started.

The second is that we will do this in VR. This introduces lots of challenges – testing by jumping into and out of the headset is annoying, so we will want a workflow that minimizes the need to be in VR for testing various elements of the project.
We will need to familiarize ourselves with the toolkit we are using, and be able to capture input from the devices – which involves familiarizing ourselves with the heretofore untouched ‘new input system’.
A lot of the challenge here is not “programming” but figuring out the kinds of things we need to know in order to do the “actual programming”. 
This is still programming. Programmers spend a lot of time researching.

## Submission
Upload:
1. A working Quest build (the .apk file) that is named appropriately, and has the identifier set to something reasonable (not "DefaultCompany")
2. A zip file containing any of the script files you wrote (but not package files)

## Evaluation

Everyone will submit a working .apk build of their project, and I will put them on my device (ideally; before class starts).
All students will be invited to put the experiences on their own devices as well, and give feedback.
Limited class-time will be focused on my feedback while casting the quest to the TV.
Additionally, the student will describe how they went about writing the code that makes it work.
If the build is broken, they will showcase a video capture (you should have one ready, despite the lack of submission requirement, because documenting our work is a habit that we do ).
The project will be evaluated during this in-class presentation.

## Requirements
1. **A working demo of the system** -- A basic environment to move around in, with some visual indicators of position and scale and such (we need more than a flat plane or infinite void to understand how we are locomoting). It needs to be good enough to demonstrate the locomotion system well, and this is probably more involved than just a prototype-box of cubes.
2. **The System Must Be Novel** -- I reserve the right to veto any idea of I do not feel it will adequately fill the purpose of the assignment. A good idea might simply be too easy, or too hard to implement. No teleportation or joystick slide-movement.
2. **A Working APK**
3. **Scripts on Brightspace** -- Not directly evaluated, but required for accademic integrity purposes.
4. **Custom Implemented Mechanic** -- . No tutorial or borrowed code for the core functionality of the system. The idea does not need to be purely original, but the implementation needs to be yours. You can use borrowed or other code for non-core or miscellaneous features.
5. Must meet your **assigned scope** -- Because every project is unique, my expectations will be given individually to each student, in a public format (all expectations listed in a document visible to all students).

*Almost every project will involve research with a VR toolkit, reserach into the input system being used, Vector3 & vector math fundamentals, and interpolation.

## Getting Started
Read my notes on teleportation, thinking about pros and cons of a “real” locomotion system may inspire you in some way or another: [https://impr.hdyar.com/notes/teleportationNotes.html](https://impr.hdyar.com/notes/teleportationNotes.html)

-	Like a pickpocket bumping you while stealing your wallet –or my violent-head-thrashing system – large movements can disguise smaller discomforts.
-	Redirected walking is pretty amazing. While we likely won’t implement a featured redirected walking system, think through some of it’s principles. For example, instead of moving the player, what if we reorganized, rescaled, or twisted the world around them?
-	What about a system of scaling the world towards and away from you while you stay in place? Is this a locomotion system? Maybe!
-	What sorts of skeuomorphic elements can we introduce? A friend of mine created a phenomenally slow system where elevator doors would slide around you, and then you pushed a button, waited a bit with music, and then the doors slid open and disappeared. I’ve wanted to do the same with a bus or uber.
-	Why be at a human scale? Why move at a human speed?
-	Does the user need to be standing? Can standing up or sitting down signify a transition between user modes?
-	What should my hands be doing? Can I be holding a massive steering wheel?
-	What’s your worst idea? How can we make it not-actually-that-bad?
-	What would be the perfect locomotion system for [someone specific]. If I made a locomotion system for my father, an avid sailor, I imagine sitting on the floor and holding a tiller (the part that moves the rudder that steers the boat) would be quite an enjoyable and intuitive experience, although that is not a universal truth. 
-	What are interesting real-life movement systems that we could emulate? A bouncy castle? A ski-lift? Sled-dogs? Falling?
-	Can you design an environment I can explore while lying on my back?
-	Does the teleportation system have to be easy?
-	What about time scales? Can we “teleport” through time, instead of through space?
-	What if we are always moving, and the locomotion system stops us. Conveyor belt? Train stations? Invert the paradigms.
-	What signifies a “zone” to teleport to? Is it a “rug” or visual space? What if this was an object or item?
-	First Person Chess. (I don’t know what this means, it’s just in my notes on locomotion. Probably an accident and not an insightful consideration of movement limitations as defined by some “role” the user inhabits)
-	Just explore this and start remixing: https://locomotionvault.github.io/

Getting Over It, Wheelchair (intuitive and accessible), Mario Galaxy Slingshot-to-Stars, Pinball Plunger, Bowling and end-up-where-the-ball-stops (interesting for puzzles), Gun (you traveled the trajectory of a bullet with wind effects), go-to-where-you-appear-to-be-at-in-a-mirror, apple-toss, run with tom cruise hands, climbing and toss yourself, elevator emerges around you, scream to move, dance to move.