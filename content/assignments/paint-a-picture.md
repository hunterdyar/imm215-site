---
title: Paint a Picture
order: 2
draft: true
---

## Objective
Create a Script or a collection of scripts to paint a picture in Unity.

The code must use at least one for loop and at least one custom function.

Of course, using an image is not allowed to simply display a picture. Anything that generates the image from a script is allowed. You are allowed to use simple shapes (2D sprites, like squares and circles) that you ‘stamp’ down via Instantiation.

Color and size/scale must be changed via code.

Drawing using debug tools, which are visible in the Scene view but not the Game view, is allowed.

## Submission
Upload both the .cs script file (include a comment with your name) and a screenshot of the picture you “painted” to Brightspace.

## Purpose
This will require using functions and looking up how those functions work. It likely will also involve using variables. Advanced Code Flow elements are not strictly necessary but will make life easier.

This isn’t something Unity is really designed to do. But it certainly can. We just have to be creative and think outside of the box. You could, hypothetically, create a Texture and loop through every pixel and assign its color manually. That would be an inconvenient way to do things.

The main purpose of this assignment is to force us to write code and look up functions, without the code being very complicated.

## Assignment Details
The image must come from the code, the canvas should be blank before you enter play mode, save for the background color in the camera component properties.

Remember, you aren’t being graded on the quality of the painting. This is a programming assignment.

You are allowed to use LineRenderer if you update the positions from the script.

## Getting Started
One key method to use is the Instantiate function. One solid way to do the assignment is to start a new Unity 2D project, and create a gameObject with a spriteRenderer and a basic white shape for it’s sprite, and make that a prefab – our ‘stamp’. Next, in the actual code, we will call the Instantiate function to clone this prefab.

To change the color of the shape, we can change the value of the ‘Color’ property of the SpriteRenderer component of the object that we stamped.

When we Instantiate something, it returns a reference to the object that we cloned. We can find the SpriteRenderer component that is a part of that object with the GetComponent function.

```csharp
GameObject stamp = Instantiate(StampPrefab,position,orientation);
SpriteRenderer stampRenderer = stamp.GetComponent<SpriteRenderer>();
stampRenderer.color = new Color(0,0,0);
```

For a refresher, skim through a few of the [beginner scripting videos](https://learn.unity.com/project/beginner-gameplay-scripting) that Unity produced.

- [Loops in Unity](https://www.youtube.com/watch?v=Jefkb3Gm7vE)
- [Unity LineRenderer](https://docs.unity3d.com/ScriptReference/LineRenderer.html)
