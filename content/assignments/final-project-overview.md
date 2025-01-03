---
title: Final Project Pitch
order: 10
---

## Objective
Create an experience using the Unity Engine and an external API or piece of Hardware. Ideally, that API is in the world of immersive technology. VR, AR, Holographic Display, or a 3D experience. You can pitch an idea for any platform, any API, any hardware, that is supported by Unity3D. I reserve the right to veto any idea.

You can work individually or in groups of 2. Group projects scope will be scaled up appropriately. This lets us have multiple students work with the same API without simply doing the same thing.

The projects should not be very large in scope – about 1 week of work. We are going to spend a disproportionate amount of time researching, designing, architecting, and polishing the code for the projects. So “simple” ideas are strong ones.

I will be working with each student (or group) to help set fair and educational project and outcome objectives on a per-project basis. Per-project objectives will be discussed publicly, and all students can see how all others will be graded.

In a big-picture sense, our objective is to work with and learn how to use other developer’s code. Not just my example projects or the built in Unity tools, but to research [often baffling, arbitrary, or opaque] decisions that hardware and software developers have used and figure out how to integrate it. This process of research and implementation will be common for us as interaction developers. Many who work in this field consider themselves more “hackers” than “developers”, and this project is about learning how to work with that mentality.

## Pitches Submission
Come to class with your top 3 ideas. We will vote on projects, veto projects, remove and re-vote, perhaps form groups, and decide what we will do during class. You can change your idea of something somebody else pitched if that sounds interesting.

First, we will go through and veto projects that I believe are technically infeasible, out of scope, don’t hit our learning objectives, or are otherwise inappropriate.

We will go through and discuss projects until we have a short list of possibilities. This first culling step is independent of “what project do you want to work on” and more about the ideas in general. You should leave class ready to get working.


## Grading
This, the pitch, is graded in class.

- 3 Earnest Project ideas: 30% x 3 = 90.
- 10% for the pitch and knowing your ideas well and communicating them effectively during class. 

## Purpose
An API stands for “Application Programming Interface”. We’ve talked about interfaces as a concept in programming architecture. API’s are bigger picture, often encompassing entire services, hardware, applications and so on.

You will also see the term “SDK”. SDK stands for Software Development Kit, and it is all of the things that you need to create software for a particular platform. The SDK might be a unity package full of scripts we put in our project in order to use an API.

Other related terms include “Library” or “Framework” which, broadly, all involve pre-existing code that is made to be used in other projects (library) or used as a starting point or system for other projects (framework). There’s a lot of overlap.

The purpose of the final project is to get experience working with external code libraries and projects, such as the API’s created by hardware manufacturers like Microsoft, Oculus, Magic Leap, Leap Motion, and so on.

A lot of the work we will do in the immersive media space is less about programming systems from scratch, and more about research, hacking, mushing, and smashing various API’s together to make-a-thing-do-a-thing. We need experience working with API’s and we need practice working with unknowns.  

There some broad categories to API’s. Some allow interfacing with hardware, others simply provide data. Obviously, I am more interested in working with unique or immersive hardware – in other words “programming for immersive experiences”. That said, with a good pitch, I am open minded to the tools we use.


## Getting Started
*Note: This section has not been updated in a few years. API's and Hardware have changed. I'll discuss new tools during class.*

Previous Projects: A Relaxing VR environment that streamed live radio into Unity, A relaxing VR environment that updated the surroundings to match local weather data, and a multiplayer meme museum.
See other documents, dig into your notes, and start writing down ideas.
This might be a good time to try a “49 bad ideas” exercise, where you write down 50 ideas without hitting the backspace key on your keyboard once.
Some immersive technology supported by Unity3D
-	…Virtual Reality
-	WebVR (https://github.com/mozilla/unity-webvr-export )
-	Spatialized Audio
-	Google Cardboard
-	Google Daydream
-	Magic Leap AR Headset
-	Volumetric Filmmaking (depthKit)
-	Live Video Feed, chroma keying
-	Bose AR [audio] headphones
-	DepthKit
-	Azure Kinect (real time 3D Scanning, real time skeleton data)
-	Oculus pass-through AR
-	Hand tracking
Some Non-Immerisve API’s/platforms
-	Basically any HTTP, REST, or web API used for website programming (see: https://www.programmableweb.com/) can be fenagled into unity.
-	Interfacing with Arduino input (gyroscope sensors, arcade sticks, flex sensors attached to clothes, create custom controllers, etc). 
-	Open Weather API
-	Webcam data
-	Microphone data
Keijiro Takahashi, in particular, has created a number of repositories/tools/API’s that allow for interfacing with various hardware: https://github.com/keijiro
The libraries for MIDI and OSC (two ways that hardware sends/receives signals) open up infinite possibilities with other devices that use MIDI or OSC.
-	Volumetric Video
-	Real time audio input and output
-	MIDI input - https://github.com/keijiro/Minis - https://github.com/keijiro/MidiJack
-	OSC - https://github.com/keijiro/OscJack
-	Various creative coding tools - https://github.com/keijiro/Klak
-	React to audio: https://github.com/keijiro/Reaktion
Some project ideas I have had:
-	Stereogram viewer (webVR/Cardboard)
-	AR Weather applet (Magic Leap)
-	Flying controls (Arduino + probably, ICAROS)
-	Normcore Multiplayer VR project - https://normcore.io/?utm_source=normalvr.com
-	Bose AR glasses comedically narrating my movements using various phone data (gps? Notifications?) like from that Will Farrell Movie, Stranger than Fiction
-	A single gigantic scroll wheel for when reading web pages. Made out of a spinning hardware wheel.
-	Using my racing wheel and petals to drive my mouse around the screen.
-	A game about making silly faces during zoom calls using OpenCV face tracking software
-	A game built into a snapchat filter
-	AR word-vomit
-	VR e-sports replay viewer/spectator camera
-	2023:
-	Something with the ‘GameBoard’ virtual tabletop thing I bought
-	Visualize git project history
-	Visualize file systems
-	I bought a lastgameboard thing, probably could do something fun with that
-	Meta quest pro pass-through setup.
-	Unity Netcode for Gameobjects Multiplayer!

Previous student projects:
-	Current weather in VR
-	Got Hololens running, made a recipe viewer
-	Sound-reactive flappy bird yelling game
-	Looking glass City visualizer
-	Vive tracking puck room controls
-	multiplayer prop hunt with a baseball bat
-	hand tracking basketball
-	

