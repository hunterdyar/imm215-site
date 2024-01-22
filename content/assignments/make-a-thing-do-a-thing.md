---
title: Make A Thing Do A Thing
layout: Assignment
order: 4
---

Create a new project or use the character controller. Or use someone else's character controller.

Your assignment is to implement a behaviour into a 2D game (prototype). You also must write a 'problem breakdown'.

You will come up with an idea, and then email the professor for apporoval - your idea must be approved as being complex enough to 'count'.

### Minimum Requirements
- 2 Scripts with some dependency (ie: a public function on one being called by the other)
- Clean code, appropriate names/comments, etc
- The behaviour is described and effective
- I can make a reasonable guess as to what the code does from reading it
- Approved Complexity.

### Breakdown
An informal piece of writing with the following parts:

1. Name of behaviour
1. A brief description of what should happen. This makes no reference to the implementation (solution), it is only a description of the desired effect.
1. List all of the unique components of the behaviour. As many as you can think of. "Shooting" might become "Spawning bullets, bullet motion, destroying bullets on impact, particles on impact, health of enemy, destroying enemy when below 0 health, etc"
1. Once you think you are done, go back to the previous step break it down further. It probably isn't specific enough.
1. Finally, describe your proposed implementation, see below.

#### Describing an Implementation

List your scripts, and for each script:
 - List it's inputs (public functions, unity events hooked into, things it needs to know about).
 - outputs (the ... behaviour).
 - The part(s) of the behaviour that it is responsible for.
 - The Connections it has to other scripts. "Input.cs script calls the fire function, and it spawns the bullet which is assumed to have a bullet.cs script"

> It will not be complex. It should be so simple it feels kind of silly to write. If it doesn't feel silly, then keep breaking it down into smaller pieces.

### Submission
Upload your breakdown (text file?) and all script files. Project will be reviewed during class.

### Purpose
The real goal is to go through the problem-solving exercise of "How can I make this thing I want to happen happen". Describe the behavious, break apart the pieces of functionality needed to make it happen, and break the problem down into pieces.

### Possible Behaviours
- Shooting things
- Collecting things
- Weird advanced movement, like teleportation? Dash?
- Game Manager
- Something with a timer
